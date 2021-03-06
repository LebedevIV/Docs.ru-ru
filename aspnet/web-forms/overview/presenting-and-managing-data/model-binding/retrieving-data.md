---
uid: web-forms/overview/presenting-and-managing-data/model-binding/retrieving-data
title: Извлечение и отображение данных с помощью модели привязки и веб-форм | Документация Майкрософт
author: Rick-Anderson
description: В этой серии руководств показано основными аспектами с помощью привязки модели с проектом веб-форм ASP.NET. Привязка модели позволяет взаимодействие с данными более прямой-...
ms.author: riande
ms.date: 02/27/2014
ms.assetid: 9f24fb82-c7ac-48da-b8e2-51b3da17e365
msc.legacyurl: /web-forms/overview/presenting-and-managing-data/model-binding/retrieving-data
msc.type: authoredcontent
ms.openlocfilehash: c53c27f4852eab9813bd917315111e7cd3b04953
ms.sourcegitcommit: 184ba5b44d1c393076015510ac842b77bc9d4d93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "54396289"
---
<a name="retrieving-and-displaying-data-with-model-binding-and-web-forms"></a>Извлечение и отображение данных с помощью привязки модели и веб-форм
====================

> В этой серии руководств показано основными аспектами с помощью привязки модели с проектом веб-форм ASP.NET. Привязка модели упрощает взаимодействие с данными более эффективную чем работа с данными объектов источника (например, элемент управления ObjectDataSource и SqlDataSource). Эта серия начинается с вводный материал и перемещает до более продвинутых в последующих руководствах.
> 
>  Шаблон привязки модели работает с любой технологии доступа к данным. В этом руководстве используется платформа Entity Framework, но можно использовать технологии доступа к данным, который наиболее вам знакомы. Из элемента управления с привязкой к данным сервера, например в элементе управления GridView, ListView, DetailsView и FormView укажите имена методов для выбора, обновления, удаления и создания данных. В этом руководстве вы укажете значение для SelectMethod. 
> 
> В этом методе обеспечивают логику для получения данных. В следующем учебном курсе UpdateMethod и InsertMethod и DeleteMethod установит значения.
>
> Вы можете [загрузить](https://go.microsoft.com/fwlink/?LinkId=286116) весь проект в C# или Visual Basic. Загружаемый код работает с Visual Studio 2012 и более поздних версий. Он использует шаблон Visual Studio 2012, который немного отличается от шаблона Visual Studio 2017, в этом учебнике.
> 
> В этом руководстве вы запустите приложение в Visual Studio. Можно также развернуть приложение поставщика услуг размещения и сделать его доступным через Интернет. Корпорация Майкрософт предлагает бесплатные услуг хостинга до 10 веб-сайтов в  
>  [бесплатную пробную учетную запись Azure](https://azure.microsoft.com/free/?WT.mc_id=A443DD604). Сведения о развертывании веб-проекта Visual Studio веб-приложениях службы приложений Azure, см. в разделе [веб-развертывание ASP.NET с помощью Visual Studio](../../deployment/visual-studio-web-deployment/introduction.md) рядов. Этот учебник также показано, как использовать Entity Framework Code First Migrations для развертывания базы данных SQL Server в базу данных SQL Azure.
> 
> ## <a name="software-versions-used-in-the-tutorial"></a>Версии программного обеспечения, используемые в этом руководстве
> 
> - Microsoft Visual Studio 2017 или Microsoft Visual Studio Community 2017
>   
> Этот учебник также работает с Visual Studio 2012 и Visual Studio 2013, но существуют некоторые различия в пользовательский интерфейс и проекта шаблон.


## <a name="what-youll-build"></a>Вы создадите

В этом руководстве вам потребуется:

* Создание объектов данных, которые отражают университет с студентов, зачисленных на курсы
* Построение таблиц базы данных из объектов
* Заполнение базы данных тестовыми данными
* Отображение данных в веб-формы

## <a name="create-the-project"></a>Создание проекта

1. В Visual Studio 2017 создайте **веб-приложение ASP.NET (.NET Framework)** проект с именем **ContosoUniversityModelBinding**.

   ![Создание проекта](retrieving-data/_static/image19.png)

2. Нажмите кнопку **ОК**. Появляется диалоговое окно, чтобы выбрать шаблон.

   ![Выберите веб-форм](retrieving-data/_static/image3.png)

3. Выберите **веб-форм** шаблона. 

4. При необходимости задайте для аутентификации **учетные записи отдельных пользователей**. 

5. Нажмите кнопку **ОК**, чтобы создать проект.

## <a name="modify-site-appearance"></a>Изменение внешнего вида узла

   Внести некоторые изменения для настройки внешнего вида узла. 
   
   1. Откройте файл Site.Master.
   
   2. Изменить заголовок, отображаемый **университета Contoso** и не **Мое приложение ASP.NET**.

      [!code-aspx-csharp[Main](retrieving-data/samples/sample1.aspx?highlight=1)]

   3. Измените текст заголовка из **имя_приложения** для **университета Contoso**.

      [!code-aspx-csharp[Main](retrieving-data/samples/sample2.aspx?highlight=7)]

   4. Изменение заголовка ссылок навигации для сайта соответствующие. 
   
      Удаление ссылок для **о** и **контакт** и вместо этого ссылка на **учащихся** страницы, который будет создан.

      [!code-aspx-csharp[Main](retrieving-data/samples/sample3.aspx)]

   5. Сохраните Site.Master.

## <a name="add-a-web-form-to-display-student-data"></a>Добавьте веб-форму для отображения данных об учащихся

   1. В **обозревателе решений**, щелкните правой кнопкой мыши проект, выберите **добавить** и затем **новый элемент**. 
   
   2. В **Добавление нового элемента** выберите **веб-форма с главной страницы** шаблона и назовите его **Students.aspx**.

      ![Создание страницы](retrieving-data/_static/image5.png)

   3. Нажмите **Добавить**.
   
   4. Главная страница веб-формы, выберите **Site.Master**.
   
   5. Нажмите кнопку **ОК**.
   

## <a name="add-the-data-model"></a>Добавление модели данных

В **моделей** папки, добавьте класс с именем **UniversityModels.cs**.

   1. Щелкните правой кнопкой мыши **моделей**выберите **добавить**, а затем **новый элемент**. Откроется диалоговое окно **Добавление нового элемента**.

   2. В меню навигации слева выберите **кода**, затем **класс**.

      ![Создание класса модели](retrieving-data/_static/image20.png)

   3. Назовите класс **UniversityModels.cs** и выберите **добавить**.

      В этом файле определения `SchoolContext`, `Student`, `Enrollment`, и `Course` классов следующим образом:

      [!code-csharp[Main](retrieving-data/samples/sample4.cs)]

      `SchoolContext` Класс является производным от `DbContext`, который управляет подключения к базе данных и изменения в данных.

      В `Student` класса, обратите внимание, что атрибуты, примененные к `FirstName`, `LastName`, и `Year` свойства. В этом учебнике используется эти атрибуты для проверки данных. Чтобы упростить код, только эти свойства помечаются атрибутами проверки данных. В реальном проекте можно применить ко всем свойствам, требуя проверки атрибутов проверки.

   4. Сохраните UniversityModels.cs.

## <a name="set-up-the-database-based-on-classes"></a>Настройка базы данных, основанные на классах

В этом руководстве используется [Code First Migrations](https://docs.microsoft.com/en-us/ef/ef6/modeling/code-first/migrations/) для создания объектов и таблиц баз данных. Эти таблицы хранят сведения об учащихся и их курсы.

   1. Выберите **средства** > **диспетчер пакетов NuGet** > **консоль диспетчера пакетов**.

   2. В **консоль диспетчера пакетов**, выполните следующую команду:  
      `enable-migrations -ContextTypeName ContosoUniversityModelBinding.Models.SchoolContext`

      Если команда выполнена успешно, появится сообщение о том, что были включены миграций.

      ![выполняет миграцию](retrieving-data/_static/image8.png)

      Обратите внимание, что файл с именем *Configuration.cs* будет создана. `Configuration` Класс имеет `Seed` метод, который можно предварительно заполнить таблицы базы данных тестовыми данными.

## <a name="pre-populate-the-database"></a>Заполнение базы данных

   1. Откройте Configuration.cs.
   
   2. Добавьте следующий код в метод `Seed` . Кроме того, добавьте `using` инструкции для `ContosoUniversityModelBinding. Models` пространства имен.

      [!code-csharp[Main](retrieving-data/samples/sample5.cs)]

   3. Сохраните Configuration.cs.

   4. В консоли диспетчера пакетов выполните команду **добавьте миграции исходного**.

   5. Выполните команду **обновления базы данных**.

      Если получено исключение при выполнении этой команды `StudentID` и `CourseID` значения могут отличаться от `Seed` значения метода. Откройте эти таблицы базы данных и найти существующие значения для `StudentID` и `CourseID`. Добавьте эти значения в код для заполнения `Enrollments` таблицы.

## <a name="add-a-gridview-control"></a>Добавление элемента управления GridView

С заполненной базы данных вы теперь все готово для получения этих данных и отображения его. 

1. Open Students.aspx.

2. Найдите `MainContent` заполнителя. В рамку, добавьте **GridView** элемент управления, который включает в себя этот код.

   [!code-aspx-csharp[Main](retrieving-data/samples/sample6.aspx)]

   Сведения:
   * Обратите внимание, что значение, заданное для `SelectMethod` свойства в элементе GridView. Это значение указывает метод, используемый для извлечения данных GridView, который создается в следующем шаге. 
   
   * `ItemType` Свойству `Student` класса, созданного ранее. Этот параметр позволяет ссылаться на свойства класса в разметке. Например `Student` класс имеет коллекцию с именем `Enrollments`. Можно использовать `Item.Enrollments` для извлечения этой коллекции и затем использовать [синтаксиса LINQ](https://docs.microsoft.com/dotnet/csharp/programming-guide/concepts/linq/query-syntax-and-method-syntax-in-linq) для получения каждого учащегося зарегистрированы кредиты sum.
   
3. Сохраните Students.aspx.

## <a name="add-code-to-retrieve-data"></a>Добавьте код для получения данных

   Добавьте в файл кода Students.aspx, метод, указанный для `SelectMethod` значение. 
   
   1. Откройте Students.aspx.cs.
   
   2. Добавить `using` инструкций для `ContosoUniversityModelBinding. Models` и `System.Data.Entity` пространства имен.

      [!code-csharp[Main](retrieving-data/samples/sample7.cs)]

   3. Добавьте метод, указанный для `SelectMethod`:

      [!code-csharp[Main](retrieving-data/samples/sample8.cs)]

      `Include` Предложение повышает производительность запросов, но не требуется. Без `Include` предложения, данные извлекаются с помощью [ *отложенная загрузка*](https://en.wikipedia.org/wiki/Lazy_loading), который используется для отправки отдельный запрос к базе данных каждый раз связанные данные извлекаются. С помощью `Include` предложения, данные извлекаются с помощью *Безотложная загрузка*, означающее запроса к одной базе данных получает все связанные данные. Если связанные данные не используются, Безотложная загрузка является менее эффективным, так как получить дополнительные данные. Тем не менее в этом случае Безотложная загрузка дает максимальную производительность поскольку взаимосвязанные данные отображаются для каждой записи.

      Дополнительные сведения о вопросах производительности при загрузке связанных данных, см. в разделе **Lazy Eager и явная загрузка связанных данных** статьи [чтение связанных данных с помощью Entity Framework в ASP.NET Приложение MVC](../../../../mvc/overview/getting-started/getting-started-with-ef-using-mvc/reading-related-data-with-the-entity-framework-in-an-asp-net-mvc-application.md) статьи.

      По умолчанию данные сортируются по значениям свойства, помеченного как ключ. Вы можете добавить `OrderBy` предложение, чтобы указать значение сортировки. В этом примере значение по умолчанию `StudentID` свойство используется для сортировки. В [сортировка, разбиение по страницам и фильтрация данных](sorting-paging-and-filtering-data.md) статьи, пользователь включено для выбора столбца для сортировки.
 
   4. Сохраните Students.aspx.cs.

## <a name="run-your-application"></a>Запустите приложение 

Запустите веб-приложения (**F5**) и перейдите к **учащихся** страницы, где отображается следующее:

   ![Отображение данных](retrieving-data/_static/image16.png)

## <a name="automatic-generation-of-model-binding-methods"></a>Автоматическое создание методы привязки модели

При работе с этой серии руководств, можно просто скопировать код из учебника в проект. Однако Недостаток такого подхода является, вам может не по нескольким признакам функции, предоставляемые Visual Studio для автоматического создания кода для методы привязки модели. При работе на ваших собственных проектов, автоматическое создание кода может сэкономить время и получить представление о том, как реализовать операцию. В этом разделе описывается функция создания кода. В этом разделе носит чисто информационный характер и не содержит любой код, который необходимо реализовать в своем проекте. 

При установке значения для `SelectMethod`, `UpdateMethod`, `InsertMethod`, или `DeleteMethod` свойства в коде разметки, можно выбрать **создайте новый метод** параметр.

![Создание метода](retrieving-data/_static/image18.png)

Visual Studio не только создает метод в коде программной части с правильной сигнатурой, но также создает код реализации для выполнения операции. Если сначала установить `ItemType` возможности, свойство перед использованием автоматического создания кода, в созданном коде используется, введите для операций. Например, при задании `UpdateMethod` автоматически создается свойство, следующий код:

[!code-csharp[Main](retrieving-data/samples/sample9.cs)]

Опять же этот код не должны быть добавлены в проект. В следующем руководстве вы реализуете методы для обновления, удаления и добавления новых данных.

## <a name="summary"></a>Сводка

В этом руководстве вы создана классы модели данных и создать базу данных из этих классов. Заполнение таблиц базы данных тестовыми данными. Используемые привязки модели для получения данных из базы данных и затем отображаются данные в элементе управления GridView.

В следующем [руководстве](updating-deleting-and-creating-data.md) в этой серии, если включить обновление, удаление и создание данных.

> [!div class="step-by-step"]
> [Вперед](updating-deleting-and-creating-data.md)
