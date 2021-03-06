---
uid: signalr/overview/getting-started/tutorial-server-broadcast-with-signalr
title: Учебник. Передача сообщений с сервера с помощью SignalR 2 | Документация Майкрософт
author: tdykstra
description: Этом руководстве показано, как создать веб-приложения, использующего ASP.NET SignalR 2 для предоставления широковещательных функциональные возможности сервера.
ms.author: bradyg
ms.date: 01/02/2019
ms.topic: tutorial
ms.assetid: 1568247f-60b5-4eca-96e0-e661fbb2b273
msc.legacyurl: /signalr/overview/getting-started/tutorial-server-broadcast-with-signalr
msc.type: authoredcontent
ms.openlocfilehash: a243c78c7d552f1c82a88c6083871fcd16538618
ms.sourcegitcommit: ebf4e5a7ca301af8494edf64f85d4a8deb61d641
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "54837433"
---
# <a name="tutorial-server-broadcast-with-signalr-2"></a>Учебник. Передача сообщений с помощью SignalR 2 сервера

[!INCLUDE [Consider ASP.NET Core SignalR](~/includes/signalr/signalr-version-disambiguation.md)]

Этом руководстве показано, как создать веб-приложения, использующего ASP.NET SignalR 2 для предоставления широковещательных функциональные возможности сервера. Рассылка сервера означает, что сервер запускается связям клиентам.

Приложение, которое вы создадите в этом руководстве имитирует биржевые сводки, типичный сценарий для широковещательных функциональные возможности сервера. Периодически сервер случайным образом обновляет акций и рассылка обновлений для всех подключенных клиентов. В браузере, цифры и символы в **изменить** и **%** динамически изменять столбцы в ответ на уведомления от сервера. Если открыть дополнительные браузеров на том же URL-адрес, все они Показывать те же данные и те же изменения в данные одновременно.

![Создание веб-](tutorial-server-broadcast-with-signalr/_static/image1.png)

В этом учебнике рассмотрены следующие задачи.

> [!div class="checklist"]
> * Создание проекта
> * Настройте серверный код
> * Проверьте серверный код
> * Настройка кода клиента
> * Изучите код клиента
> * Тестирование приложения
> * Включение ведения журнала

> [!IMPORTANT]
> Если вы не хотите работать шаги по созданию приложения, можно установить пакет SignalR.Sample в новом проекте пустое веб-приложение ASP.NET. Если вы установите пакет NuGet без выполнения действия в этом руководстве, необходимо выполнить инструкции в *readme.txt* файл. Для запуска пакета, необходимо добавить OWIN startup класса какие вызовы `ConfigureSignalR` метод в установленном пакете. Вы получите ошибку, если вы не добавили класс запуска OWIN. См. в разделе [установить образец StockTicker](#install-the-stockticker-sample) этой статьи.


## <a name="prerequisites"></a>Предварительные требования

 * [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/) с **ASP.NET и веб-разработка** рабочей нагрузки.

## <a name="create-the-project"></a>Создание проекта

В этом разделе показано, как использовать Visual Studio 2017 для создания пустой веб-приложения ASP.NET.

1. В Visual Studio создайте веб-приложения ASP.NET.

    ![Создание веб-](tutorial-server-broadcast-with-signalr/_static/image2.png)

1. В **новый веб-приложение ASP.NET - SignalR.StockTicker** окне оставьте **пустой** затем выберите **ОК**.

## <a name="set-up-the-server-code"></a>Настройте серверный код

В этом разделе настраивается код, который выполняется на сервере.

### <a name="create-the-stock-class"></a>Создайте класс акции

Начните с создания *Stock* класс, который используется для хранения и передачи информации о акций модели.

1. В **обозревателе решений**, щелкните правой кнопкой мыши проект и выберите **добавить** > **класс**.

1. Назовите класс *Stock* и добавьте его в проект.

1. Замените код в *Stock.cs* файла следующим кодом:

    [!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample1.cs)]

    Два свойства, которые вы укажете при создании акций, `Symbol` (например, MSFT корпорации Майкрософт) и `Price`. Другие свойства зависят от того, как и когда будет установлено `Price`. В первый раз, можно задать `Price`, значение возвращает распространяется `DayOpen`. После этого при задании `Price`, приложение вычисляет `Change` и `PercentChange` значения свойств, основанное на различии между `Price` и `DayOpen`.

### <a name="create-the-stocktickerhub-and-stockticker-classes"></a>Создание классов StockTickerHub и StockTicker

Вы используете API концентратора SignalR для обработки взаимодействия клиентом и сервером. Объект `StockTickerHub` класс, производный от `SignalRHub` класс, обрабатывающий получение подключений и вызовы методов из клиентов. Также необходимо поддерживать биржевых данных и запустите `Timer` объекта. `Timer` Объект периодически будет активировать обновление цены, независимо от клиентских подключений. Эти функции нельзя поместить в `Hub` класса, так как концентраторы являются временными. Приложение создает `Hub` экземпляр класса для каждой задачи на концентраторе, такие как подключения и вызовы от клиента к серверу. Поэтому механизм, который отслеживает биржевых данных, затем обновляет цены и передает изменения цены должен выполняться в отдельном классе. Этот класс будет назван `StockTicker`.

![Широковещательная рассылка из StockTicker](tutorial-server-broadcast-with-signalr/_static/image3.png)

Требуется только один экземпляр `StockTicker` класса для запуска на сервере, поэтому вам потребуется настроить ссылку из каждого `StockTickerHub` экземпляр одноэлементного `StockTicker` экземпляра. `StockTicker` Класс имеет для широковещательной передачи клиентов, так как он имеет биржевых данных и триггеров обновлений, но `StockTicker` не `Hub` класса. `StockTicker` Класс должен получить ссылку на объект контекста подключения концентратора SignalR. Он этого можно использовать объект контекста подключения SignalR для рассылки клиентам.

#### <a name="create-stocktickerhubcs"></a>Create StockTickerHub.cs

1. В **обозревателе решений**, щелкните правой кнопкой мыши проект и выберите **добавить** > **новый элемент**.

1. В **Добавление нового элемента — SignalR.StockTicker**выберите **установленные** > **Visual C#**   >  **Web**  >  **SignalR** , а затем выберите **класс концентратора SignalR (v2)**.

1. Назовите класс *StockTickerHub* и добавьте его в проект.

    На этом шаге создается *StockTickerHub.cs* файл класса. Одновременно он добавляет набор файлов сценариев и ссылки на сборки, поддерживающий SignalR в проект.

1. Замените код в *StockTickerHub.cs* файла следующим кодом:

    [!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample2.cs)]

1. Сохраните файл.

Приложение использует [концентратора](https://msdn.microsoft.com/library/microsoft.aspnet.signalr.hub(v=vs.111).aspx) класс определяет методы, которые клиенты могут вызывать на сервере. При определении одного метода: `GetAllStocks()`. Когда клиент сначала производит подключение к серверу, он вызывает этот метод, чтобы получить список всех акций с их текущие цены. Метод может выполняться синхронно и возвращать `IEnumerable<Stock>` так, как он возвращает данные из памяти.

Если метод должен получить данные, выполнив то, что будет включать в себя оповещения, такие как поиск в базе данных или вызов веб-службы, следует указать `Task<IEnumerable<Stock>>` как возвращаемое значение асинхронной обработки. Дополнительные сведения см. в разделе [ASP.NET руководство по API концентраторов SignalR - Server - когда следует выполнить асинхронно](../guide-to-the-api/hubs-api-guide-server.md#asyncmethods).

`HubName` Атрибут указывает, как приложение будет ссылаться в концентратор в код JavaScript на стороне клиента. Имя по умолчанию на стороне клиента, если вы не используете этот атрибут является версией camelCase имя класса, который в данном случае было бы `stockTickerHub`.

Как можно будет увидеть позже при создании `StockTicker` класс, приложение создает одноэлементный экземпляр этого класса в его статическое `Instance` свойство. Этот одноэлементный экземпляр `StockTicker` находится в памяти независимо от того, сколько клиентов подключить или отключить. Этот экземпляр является то, что `GetAllStocks()` метод используется для возврата текущего биржевых данных.

#### <a name="create-stocktickercs"></a>Создание StockTicker.cs

1. В **обозревателе решений**, щелкните правой кнопкой мыши проект и выберите **добавить** > **класс**.

1. Назовите класс *StockTicker* и добавьте его в проект.

1. Замените код в *StockTicker.cs* файла следующим кодом:

    [!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample3.cs)]

Так как все потоки будут выполняться один и тот же экземпляр кода StockTicker, StockTicker класс должен быть поточно ориентированными.

### <a name="examine-the-server-code"></a>Проверьте серверный код

Если посмотреть на код на сервере, он поможет вам понять, как работает приложение.

#### <a name="storing-the-singleton-instance-in-a-static-field"></a>Хранение одноэлементного экземпляра в статическом поле

Этот код инициализирует статические `_instance` поля, поддерживающего `Instance` свойство с помощью экземпляра класса. Поскольку конструктор является закрытым, он является единственным экземпляром класса, который можно создать приложение. Приложение использует [отложенной инициализации](/dotnet/framework/performance/lazy-initialization) для `_instance` поля. Они не используются для повышения производительности. Это, чтобы убедиться в том, что создание экземпляра является поточно ориентированной.

[!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample4.cs)]

Каждый раз, клиент подключается к серверу, новый экземпляр класса StockTickerHub, работающих в отдельном потоке Получает одноэлементный экземпляр StockTicker из `StockTicker.Instance` статическое свойство, как показано ранее в `StockTickerHub` класса.

#### <a name="storing-stock-data-in-a-concurrentdictionary"></a>Хранение данных акций в руководство.

Конструктор инициализирует `_stocks` коллекции с демонстрационными данными акций, и `GetAllStocks` возвращает акций. Как было показано ранее, эта коллекция акций возвращается по `StockTickerHub.GetAllStocks`, являющийся серверного метода в `Hub` класс, который клиенты могут вызывать.

[!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample5.cs)]

[!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample6.cs)]

Представляет собой коллекцию акции [ConcurrentDictionary](https://msdn.microsoft.com/library/dd287191.aspx) тип потокобезопасности. В качестве альтернативы можно использовать [словарь](https://msdn.microsoft.com/library/xfhwa508.aspx) объекта и явным образом блокировка словаря, при внесении изменений в него.

Для этого примера приложения, достаточно для хранения данных приложений в памяти и потери данных, когда приложение освобождает `StockTicker` экземпляра. В реальном приложении необходимо изменить с помощью хранилища данных серверной части, например базу данных.

#### <a name="periodically-updating-stock-prices"></a>Периодическое обновление акций

Запускается конструктор `Timer` объект, который периодически вызывает методы, которые обновляют акций на основе случайной выборки.

[!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample7.cs)]

 `Timer` вызовы `UpdateStockPrices`, который передает значения NULL в параметре state. Перед обновлением цены, приложение принимает блокировку на `_updateStockPricesLock` объекта. Код проверяет, если другой поток уже обновляется цены, и затем вызывает `TryUpdateStockPrice` на каждой из них в списке. `TryUpdateStockPrice` Метод решает, следует ли изменить цену акций и какой объем, чтобы изменить его. Если изменяется акций, приложение вызывает `BroadcastStockPrice` рассылать изменения цены акций для всех подключенных клиентов.

`_updatingStockPrices` Флаг назначенному [volatile](https://msdn.microsoft.com/library/x13ttww7.aspx) чтобы убедиться, что он является потокобезопасным.

[!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample8.cs)]

В реальном приложении `TryUpdateStockPrice` метод будет вызывать веб-службы для поиска цены. В этом коде приложение использует генератор случайных чисел для внесения изменений случайным образом.

#### <a name="getting-the-signalr-context-so-that-the-stockticker-class-can-broadcast-to-clients"></a>Получение контекста SignalR, таким образом, чтобы класс StockTicker могут производить широковещательную рассылку для клиентов

Поскольку изменения цен здесь приходят в `StockTicker` объекта, это объект, которому требуется вызывать `updateStockPrice` метод на все подключенные клиенты. В `Hub` класс, у вас есть API для вызова методов клиента, но `StockTicker` не является производным от `Hub` класса и не имеет ссылки на любое `Hub` объекта. Чтобы вещать на подключенных клиентов `StockTicker` класс должен получить экземпляр контекста SignalR для `StockTickerHub` класса и использовать его для вызова методов на клиентах.

Код получает ссылку на контекст SignalR, когда он создает одноэлементный экземпляр класса, которые ссылаются на передается конструктору, и конструктор поместит его в `Clients` свойство.

Есть две причины, почему вы хотите получить контекст только один раз: получение контекста является ресурсоемкие задачи и его после гарантирует приложение сохраняет последовательности сообщений, отправляемых клиентам.

[!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample9.cs)]

Начало `Clients` свойство контекста и поместив его `StockTickerClient` свойство позволяет написать код для вызова методов клиента, который выглядит так же, как это происходит в `Hub` класса. Например, чтобы вещать на все клиенты можно написать `Clients.All.updateStockPrice(stock)`.

`updateStockPrice` Метод, который вы вызываете в `BroadcastStockPrice` еще не существует. Она будет добавлена позже при написании кода, который выполняется на стороне клиента. Можно ссылаться на `updateStockPrice` здесь потому что `Clients.All` является динамической, что означает, что приложение будет вычислено выражение во время выполнения. При выполнении этого вызова метода, SignalR будет отправлять имя метода и значение параметра на клиенте, и если клиент имеет метод с именем `updateStockPrice`, приложение вызывает этот метод и передать значение параметра.

`Clients.All` означает, что отправки всем клиентам. SignalR предоставляет другие параметры, чтобы указать, какие клиенты или группы клиентов для отправки. Дополнительные сведения см. в разделе [HubConnectionContext](https://msdn.microsoft.com/library/microsoft.aspnet.signalr.hubs.hubconnectioncontext(v=vs.111).aspx).

### <a name="register-the-signalr-route"></a>Регистрация маршрутов SignalR

Сервер должен знать, какой URL-адрес для перехвата и направить SignalR. Чтобы сделать это, добавьте класс запуска OWIN:

1. В **обозревателе решений**, щелкните правой кнопкой мыши проект и выберите **добавить** > **новый элемент**.

1. В **Добавление нового элемента — SignalR.StockTicker** выберите **установленные** > **Visual C#**   >  **Web** и затем выберите **класс запуска OWIN**.

1. Назовите класс *запуска* и выберите **ОК**.

1. Замените код по умолчанию в *Startup.cs* файла следующим кодом:

    [!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample10.cs)]

Теперь вы завершили настройку серверный код. В следующем разделе настроим клиента.

## <a name="set-up-the-client-code"></a>Настройка кода клиента

В этом разделе настраивается код, который выполняется на стороне клиента.

### <a name="create-the-html-page-and-javascript-file"></a>Создание HTML-страницы и файл JavaScript

HTML-страницу, отобразятся данные и данные будут организованы в файл JavaScript.

#### <a name="create-stocktickerhtml"></a>Создание StockTicker.html

Во-первых мы добавим HTML-клиента.

1. В **обозревателе решений**, щелкните правой кнопкой мыши проект и выберите **добавить** > **HTML-страницу**.

1. Назовите файл *StockTicker* и выберите **ОК**.

1. Замените код по умолчанию в *StockTicker.html* файла следующим кодом:

    [!code-html[Main](tutorial-server-broadcast-with-signalr/samples/sample11.html?highlight=40-43)]

    HTML-код создается таблица с пятью столбцами, строку заголовка и строку данных, имеющего одну ячейку, которая охватывает все пять столбцов. Строки данных показывает «идет загрузка...» мгновенно при запуске приложения. Код JavaScript будет удалить эту строку и добавьте в строках месте биржевых данных, получаемых с сервера.

    Укажите теги сценария:

    * Файл скрипта jQuery.

    * Файл скрипта SignalR core.

    * Файл скрипта учетные записи-посредники SignalR.

    * Файл сценария StockTicker, будет создано позже.

    Приложение динамически создает файл скрипта учетные записи-посредники SignalR. Он указывает URL-адрес «/ signalr/концентраторы» и определяет методы прокси-сервера для методов применительно к классу Hub в данном случае для `StockTickerHub.GetAllStocks`. При желании можно создать этот файл JavaScript вручную с помощью [служебные программы SignalR](http://nuget.org/packages/Microsoft.AspNet.SignalR.Utils/). Не забудьте отключить создание динамического файла в `MapHubs` вызов метода.

1. В **обозревателе решений**, разверните **сценариев**.

    Библиотеки скрипта для jQuery и SignalR, отображаются в проект.

    > [!IMPORTANT]
    > Диспетчер пакетов будет установить более позднюю версию сценариев SignalR.

1. Обновите ссылки на скрипты в блоке кода в соответствии с версии файлов скриптов в проекте.

1. В **обозревателе решений**, щелкните правой кнопкой мыши *StockTicker.html*, а затем выберите **задать в качестве начальной страницы**.

#### <a name="create-stocktickerjs"></a>Создание StockTicker.js

Теперь создайте файл JavaScript.

1. В **обозревателе решений**, щелкните правой кнопкой мыши проект и выберите **добавить** > **файл JavaScript**.

1. Назовите файл *StockTicker* и выберите **ОК**.

1. Добавьте следующий код в *StockTicker.js* файла:

    [!code-javascript[Main](tutorial-server-broadcast-with-signalr/samples/sample12.js)]

### <a name="examine-the-client-code"></a>Изучите код клиента

Если вы изучите код клиента, поможет вам узнать, как клиентский код взаимодействует с серверный код, чтобы сделать работу приложения.

#### <a name="starting-the-connection"></a>При подключении

`$.connection` ссылается на прокси-серверы SignalR. Код получает ссылку на прокси-сервер для `StockTickerHub` класса и помещает его `ticker` переменной. Имя прокси-сервера — это имя, установленное с `HubName` атрибут:

[!code-javascript[Main](tutorial-server-broadcast-with-signalr/samples/sample13.js)]

[!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample14.cs)]

После определения всех переменных и функций, в последней строке кода в файле инициализирует подключения SignalR путем вызова SignalR `start` функции. `start` Функция выполняется асинхронно и возвращает [объект jQuery отложенный](http://api.jquery.com/category/deferred-object/). Можно вызвать функцию Готово для указания функции, вызываемой по завершении асинхронного действия приложения.

[!code-javascript[Main](tutorial-server-broadcast-with-signalr/samples/sample15.js)]

#### <a name="getting-all-the-stocks"></a>Получение всех акции

`init` Вызовы функций `getAllStocks` функции на сервере и на основании данных, возвращаемый сервером для обновления таблицы акций. Обратите внимание, что, по умолчанию, необходимо использовать camelCasing на клиенте, несмотря на то, что имя метода в стиле Pascal на сервере. CamelCasing правило применяется только к методам, не объекты. Например, ссылке на `stock.Symbol` и `stock.Price`, а не `stock.symbol` или `stock.price`.

[!code-javascript[Main](tutorial-server-broadcast-with-signalr/samples/sample16.js)]

[!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample17.cs)]

В `init` метод, приложение создает HTML для строки таблицы для каждого объекта акций, полученный от сервера путем вызова `formatStock` для свойства форматирования `stock` объекта, а затем путем вызова `supplant` для замещения местозаполнителей в `rowTemplate` переменной с `stock` значений свойств объектов. Затем полученный HTML добавляется к таблице акций.

> [!NOTE]
> Вы вызываете `init` , передав его в виде `callback` функцию, которая выполняется после асинхронного `start` функции завершения. Если вызван `init` как отдельный оператор JavaScript после вызова метода `start`, функция будет ошибкой, так как оно будет выполняться немедленно, не дожидаясь функции запуска для завершения подключения к. В этом случае `init` функция попытается вызвать `getAllStocks` функцию, прежде чем приложение устанавливает соединение с сервером.

#### <a name="getting-updated-stock-prices"></a>Получение обновленной акций.

Когда сервер изменяет цены акции, он вызывает `updateStockPrice` на подключенных клиентов. Приложение добавляет функцию свойству клиентского объекта `stockTicker` прокси-сервера, чтобы сделать его доступным для вызовов с сервера.

[!code-javascript[Main](tutorial-server-broadcast-with-signalr/samples/sample18.js)]

`updateStockPrice` Форматы функция stock-объектом получил от сервера в таблицу строк так же, как в `init` функции. Вместо того чтобы добавить строку в таблицу, он находит акции текущей строки в таблице и заменяет эту строку на новую.

## <a name="test-the-application"></a>Тестирование приложения

Можно протестировать приложение, чтобы убедиться, что он работает. Вы увидите все окна браузера отображения динамической таблицы акций акций постоянно меняется.

1. На панели инструментов, включите **отладки скриптов** и затем нажмите кнопку воспроизведения, чтобы запустить приложение в режиме отладки.

    ![Снимок экрана: Включение режим отладки и выбрав play пользователя.](tutorial-server-broadcast-with-signalr/_static/image4.png)

    Откроется окно браузера на отображение **Live Stock таблицы**. Таблицы акций изначально отображает строки «загрузка...», затем, через некоторое время, приложение показывает начальные данные акций и запустите акций для изменения.

1. Скопируйте URL-адрес из браузера, откройте два других браузеров и вставьте URL-адреса в панели адрес.

    Исходное отображение биржевых совпадает с первым браузером, и изменения происходят одновременно.

1. Закройте все браузеры, открыть обозреватель и перейдите к тем же URL-адрес.

    Одноэлементный объект StockTicker продолжали работать на сервере. **Live Stock таблицы** показывает, продолжают акций для изменения. Вы не видите первоначальной таблицы с нуля изменить данные.

1. Закройте браузер.

## <a name="enable-logging"></a>Включение ведения журнала

SignalR имеет встроенные функции, которую можно включить на стороне клиента для устранения неисправностей. В этом разделе включите ведение журнала и примеры, показывающие, как журналы скажет, какой из следующих методов транспорта использует SignalR см. в разделе:

* [WebSockets](http://en.wikipedia.org/wiki/WebSocket), поддерживается IIS 8 и современных обозревателей.

* [Сервер отправил события](http://en.wikipedia.org/wiki/Server-sent_events), поддерживаемых браузеров, отличных от Internet Explorer.

* [Forever frame](http://en.wikipedia.org/wiki/Comet_(programming)#Hidden_iframe), поддерживаемых обозревателем Internet Explorer.

* [AJAX, длинный опрос](http://en.wikipedia.org/wiki/Comet_(programming)#Ajax_with_long_polling), поддерживаемый всеми браузерами.

Для любого соединения SignalR выбирает лучший метод транспорта, сервер и клиент поддерживают.

1. Откройте *StockTicker.js*.

1. Добавление выделенной строкой кода, чтобы включить ведение журнала непосредственно перед код, который инициализирует подключение в конце файла:

    [!code-javascript[Main](tutorial-server-broadcast-with-signalr/samples/sample19.js?highlight=2)]

1. Нажмите клавишу **F5**, чтобы запустить проект.

1. Откройте окно инструментов разработчика в браузере и выберите консоль, чтобы просмотреть журналы. Может потребоваться обновить страницу, чтобы просмотреть журналы SignalR согласования метода транспорта для нового соединения.

    * Если вы используете Internet Explorer 10 в Windows 8 (IIS 8), метод транспорта является **WebSockets**.

    * Если вы используете Internet Explorer 10 в Windows 7 (IIS 7.5), метод транспорта является **iframe**.

    * Если вы используете Firefox 19 в Windows 8 (IIS 8), метод транспорта является **WebSockets**.

        > [!TIP]
        > В обозревателе Firefox установите надстройка Firebug, чтобы получать окно консоли.

    * Если вы используете Firefox 19 в Windows 7 (IIS 7.5), метод транспорта является **сервер отправил** события.

## <a name="install-the-stockticker-sample"></a>Установка образца StockTicker

[Microsoft.AspNet.SignalR.Sample](http://nuget.org/packages/microsoft.aspnet.signalr.sample) устанавливает приложение StockTicker. Пакет NuGet включает больше возможностей, чем упрощенная версия, которая создана с нуля. В этом разделе руководства вы установите пакет NuGet и просмотрите новые функции и код, который реализует их.

> [!IMPORTANT]
> Если установить пакет без выполнения на предыдущих шагах этого учебника, необходимо добавить класс запуска OWIN в проект. Этот файл readme.txt для пакета NuGet описывает этот шаг.

### <a name="install-the-signalrsample-nuget-package"></a>Установите пакет SignalR.Sample NuGet

1. В **обозревателе решений** щелкните проект правой кнопкой мыши и выберите **Управление пакетами NuGet**.

1. В **диспетчер пакетов NuGet: SignalR.StockTicker**выберите **Обзор**.

1. Из **источник пакета**выберите **nuget.org**.

1. Введите *SignalR.Sample* в поле поиска и выберите **Microsoft.AspNet.SignalR.Sample** > **установить**.

1. В **обозревателе решений**, разверните *SignalR.Sample* папки.

    Установка пакета SignalR.Sample создана папка и ее содержимое.

1. В *SignalR.Sample* папку, щелкните правой кнопкой мыши *StockTicker.html*, а затем выберите **задать в качестве начальной страницы**.

    > [!NOTE]
    > Установка SignalR.Sample NuGet пакета может изменить версию jQuery, у вас есть в вашей *сценариев* папки. Новый *StockTicker.html* файл пакета установки в *SignalR.Sample* папки будут синхронизированы с версии jQuery, которая устанавливает пакет, но если вы хотите запустить исходную *StockTicker.html* файл еще раз, необходимо сначала обновить ссылку на jQuery в тег сценария.

### <a name="run-the-application"></a>Запуск приложения

 В таблице, который вы видели в первом приложении было полезных функций. Приложение полной биржевые сводки показывает новые функции: горизонтальной прокруткой окно, отображающее биржевых данных и акции, если изменить цвет, как растет и делятся.

1. Нажмите клавишу **F5** для запуска приложения.

     При первом запуске приложения, «Марка» «закрыто», и вы увидите создается статическая таблица и окно биржевых котировок, которое не прокрутки.

1. Выберите **Open Market**.

    ![Снимок экрана: live биржевых котировок.](tutorial-server-broadcast-with-signalr/_static/image5.png)

    * **Live биржевых котировок акций** поле начинает прокручиваться по горизонтали, и сервер запускается периодически рассылать изменения цены акций на основе случайной выборки.

    * Каждый раз изменяет цены акций, приложение обновляет оба **Live Stock таблицы** и **Live биржевых котировок акций**.

    * При изменении цены акции является положительным, в приложении отображается акции с зеленым фоном.

    * Если изменение является отрицательным, в приложении отображается акции с красным фоном.

1. Выберите **закрыть рынка**.

    * Таблицы обновляет stop.

    * Биржевых котировок останавливает прокрутки.

1. Выберите **сбросить**.

    * Выполняется сброс всех биржевых данных.

    * Приложение восстанавливает начальное состояние до изменения цен к работе.

1. Скопируйте URL-адрес из браузера, откройте два других браузеров и вставьте URL-адреса в панели адрес.

1. Вы видите те же данные, динамически обновляются в то же время, в каждом браузере.

1. При выборе любого из элементов управления, все браузеры одинаково реагировать на в то же время.

### <a name="live-stock-ticker-display"></a>Динамическое отображение биржевых котировок акций

**Live биржевых котировок акций** отображается неупорядоченный список в `<div>` элемент в формате в одну строку от стилей CSS. Инициализирует приложение и обновляет биржевых котировок так же, как таблицы:, заменив заполнители в `<li>` строка шаблона и динамическое добавление `<li>` элементы `<ul>` элемент. Приложение включает прокрутку с помощью jQuery `animate` функции для изменения margin-left неупорядоченного списка в пределах `<div>`.

#### <a name="signalrsample-stocktickerhtml"></a>SignalR.Sample StockTicker.html

Биржевые сводки HTML-код:

[!code-html[Main](tutorial-server-broadcast-with-signalr/samples/sample20.html)]

#### <a name="signalrsample-stocktickercss"></a>SignalR.Sample StockTicker.css

Биржевые сводки код CSS:

[!code-html[Main](tutorial-server-broadcast-with-signalr/samples/sample21.html)]

#### <a name="signalrsample-signalrstocktickerjs"></a>SignalR.Sample SignalR.StockTicker.js

Прокрутите кода jQuery, что позволяет:

[!code-javascript[Main](tutorial-server-broadcast-with-signalr/samples/sample22.js)]

### <a name="additional-methods-on-the-server-that-the-client-can-call"></a>Дополнительные методы на сервере, который клиент может вызывать

Чтобы добавить гибкости в приложение, существуют дополнительные методы, которые приложение может вызывать.

#### <a name="signalrsample-stocktickerhubcs"></a>SignalR.Sample StockTickerHub.cs

`StockTickerHub` Класс определяет четыре дополнительные методы, которые клиент может вызывать:

[!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample23.cs)]

Приложение вызывает `OpenMarket`, `CloseMarket`, и `Reset` в ответ на кнопки в верхней части страницы. Они показывают шаблон из одного клиента, активируя изменение в состоянии, немедленно распространяются на все клиенты. Каждый из этих методов вызывает метод в `StockTicker` класс, который вызывает изменение состояния рынка и затем осуществляет широковещательную передачу новое состояние.

#### <a name="signalrsample-stocktickercs"></a>SignalR.Sample StockTicker.cs

В `StockTicker` класс, приложение сохраняет сведения о состоянии рынка с `MarketState` свойство, которое возвращает `MarketState` значение перечисления:

[!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample24.cs)]

Каждый из методов, изменяющих состояние рынка делать это внутри блок lock поскольку `StockTicker` класс должен быть поточно ориентированные:

[!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample25.cs)]

Чтобы убедиться, что этот код является поточно ориентированной, `_marketState` поля, поддерживающего `MarketState` свойстве, назначенном `volatile`:

[!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample26.cs)]

`BroadcastMarketStateChange` И `BroadcastMarketReset` методы похожи на BroadcastStockPrice метод, который вы уже видели, за исключением того, они вызывают различные методы, определенные на стороне клиента:

[!code-csharp[Main](tutorial-server-broadcast-with-signalr/samples/sample27.cs)]

### <a name="additional-functions-on-the-client-that-the-server-can-call"></a>Дополнительные функции на клиенте, который сервер может обратиться

`updateStockPrice` Функция теперь обрабатывает в таблице и отображение биржевых котировок и использует `jQuery.Color` начинает мигать, красного и зеленого цвета.

Новые функции в *SignalR.StockTicker.js* Включение и отключение кнопок, исходя из состояния рынка. Они также остановить или запустить **Live биржевых котировок акций** горизонтальная прокрутка. Так как многие функции добавляются к `ticker.client`, приложение использует [jQuery расширить функции](http://api.jquery.com/jQuery.extend/) их добавления.

[!code-javascript[Main](tutorial-server-broadcast-with-signalr/samples/sample28.js)]

### <a name="additional-client-setup-after-establishing-the-connection"></a>Программа установки дополнительного клиента после подключения к

После того как клиент устанавливает соединение, он имеет некоторые проделать дополнительную работу:

* Проверить, является ли рынке открытым или закрытым для вызова соответствующего `marketOpened` или `marketClosed` функции.

* Подключите вызовы методов сервера кнопок.

[!code-javascript[Main](tutorial-server-broadcast-with-signalr/samples/sample29.js)]

Методы сервера не отправлены кнопки до, после того как приложение устанавливает соединение. Это так, что код не может вызывать методы сервера, прежде чем они доступны.

## <a name="additional-resources"></a>Дополнительные ресурсы

В этом руководстве вы узнали, как запрограммировать приложение SignalR, которое передает сообщения с сервера все подключенные клиенты. Теперь можно выполнить рассылку сообщения на периодической основе и в ответ на уведомления из любого клиента. Концепция многопоточных одноэлементный экземпляр можно использовать для поддержания состояния сервера в многопользовательских online game сценариях. Например, см. в разделе [ShootR игры на основании SignalR](https://github.com/NTaylorMullen/ShootR).

Учебники, которые показывают связи peer-to-peer сценариев, см. в разделе [начало работы с SignalR](introduction-to-signalr.md) и [обновления в реальном времени с SignalR](tutorial-high-frequency-realtime-with-signalr.md).

Дополнительные сведения о SignalR см. следующие ресурсы:

* [ASP.NET SignalR](../../index.md)
* [Проект SignalR](http://signalr.net/)
* [SignalR GitHub и примерами](https://github.com/SignalR/SignalR)
* [Вики-сайте SignalR](https://github.com/SignalR/SignalR/wiki)

## <a name="next-steps"></a>Следующие шаги

В этом учебнике рассмотрены следующие задачи.

> [!div class="checklist"]
> * Проект создан
> * Настройте серверный код
> * Проверить код на сервере
> * Настройка кода клиента
> * Проверить код клиента
> * Тестирование приложения
> * Ведение журнала включено

Перейдите к следующей статье, чтобы научиться создавать в режиме реального времени веб-приложения, использующего ASP.NET SignalR 2.
> [!div class="nextstepaction"]
> [Создание в режиме реального времени веб-приложения с помощью SignalR](real-time-web-applications-with-signalr.md)