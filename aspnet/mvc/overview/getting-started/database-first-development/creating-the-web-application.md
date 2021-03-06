---
uid: mvc/overview/getting-started/database-first-development/creating-the-web-application
title: Учебник. Создание веб-приложения и моделей данных для EF Database First с ASP.NET MVC
description: Это руководство посвящено созданию веб-приложения и создание моделей данных, основанных на таблицах базы данных.
author: Rick-Anderson
ms.author: riande
ms.date: 01/28/2019
ms.topic: tutorial
ms.assetid: bc8f2bd5-ff57-4dcd-8418-a5bd517d8953
msc.legacyurl: /mvc/overview/getting-started/database-first-development/creating-the-web-application
msc.type: authoredcontent
ms.openlocfilehash: dced55386c3f810e406c5c2b3f0071b45e3b2dbd
ms.sourcegitcommit: c47d7c131eebbcd8811e31edda210d64cf4b9d6b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2019
ms.locfileid: "55236371"
---
# <a name="tutorial-create-the-the-web-application-and-data-models-for-ef-database-first-with-aspnet-mvc"></a>Учебник. Создание веб-приложения и моделей данных для EF Database First с ASP.NET MVC

 С помощью MVC, Entity Framework и формирование шаблонов ASP.NET, можно создать веб-приложение, которое предоставляет интерфейс для существующей базы данных. В этой серии руководств показано, как автоматически создавать код, позволяющий пользователям для отображения, изменения и создавать и удалять данные, находящиеся в таблице базы данных. Созданный код соответствует столбцам в таблице базы данных.

Это руководство посвящено созданию веб-приложения и создание моделей данных, основанных на таблицах базы данных.

В этом учебнике рассмотрены следующие задачи.

> [!div class="checklist"]
> * Создание веб-приложения ASP.NET
> * Создание моделей

## <a name="prerequisites"></a>Предварительные требования

* [Начало работы с Entity Framework 6 Database First с помощью MVC 5](setting-up-database.md)

## <a name="create-an-aspnet-web-app"></a>Создание веб-приложения ASP.NET

В новое решение или в том же решении, что проект базы данных, создайте новый проект в Visual Studio и выберите **веб-приложение ASP.NET** шаблона. Назовите проект **ContosoSite**.

![Создание проекта](creating-the-web-application/_static/image1.png)

Нажмите кнопку **ОК**.

В окне "новый проект ASP.NET", выберите **MVC** шаблона. Можно снять **разместить в облаке** параметр сейчас, так как вы развернете приложение в облако позднее. Нажмите кнопку **ОК** для создания приложения.

Создается проект с по умолчанию файлы и папки.

В этом руководстве используется Entity Framework 6. Можно еще раз проверьте версии Entity Framework в проекте в окне «Управление пакетами NuGet». При необходимости обновите версию Entity Framework.

![Показать версию](creating-the-web-application/_static/image3.png)

## <a name="generate-the-models"></a>Создание моделей

Теперь вы создадите модели Entity Framework из таблиц базы данных. Эти модели представляют собой классы, которые будут использоваться для работы с данными. Каждая модель отражает таблицы в базе данных и содержит свойства, которые соответствуют столбцам в таблице.

Щелкните правой кнопкой мыши **моделей** и выберите **добавить** и **новый элемент**.

В окне «Добавление нового элемента» выберите **данных** в левой области и **ADO.NET Entity Data Model** из параметров в центральной области. Назовите новый файл модели **ContosoModel**.

Нажмите кнопку **Добавить**.

В мастере модели EDM выберите **конструктор EF из базы данных**.

Нажмите кнопку **Далее**.

При наличии подключения базы данных, определенные в вашей среде разработки, может появиться одно из этих подключений предварительно выбраны. Тем не менее вы хотите создать новое подключение к базе данных, созданной в первой части этого руководства. Нажмите кнопку **новое подключение** кнопки.

В окне «Свойства подключения» введите имя локального сервера, где она была создана (в данном случае **\Projects13 (localdb)**). После ввода имени сервера, выберите ContosoUniversityData из доступных баз данных.

![Задание свойств соединения](creating-the-web-application/_static/image8.png)

Нажмите кнопку **ОК**.

Теперь будут показаны свойства подключения. Можно использовать имя по умолчанию для подключения в файле Web.Config.

Нажмите кнопку **Далее**.

Выберите последнюю версию Entity Framework.

Нажмите кнопку **Далее**.

Выберите **таблиц** для создания моделей для всех трех таблиц.

Нажмите кнопку **Готово**.

Если появляется предупреждение системы безопасности, выберите **ОК** для продолжения выполнения шаблона.

Модели создаются на основе таблиц базы данных и отображения диаграммы, показывающий свойства и связи между таблицами.

![Схема модели](creating-the-web-application/_static/image11.png)

Папку Models теперь включает много новых файлов, связанные с моделями, которые были созданы из базы данных.

**ContosoModel.Context.cs** файл содержит класс, производный от **DbContext** класса, а также предоставляет свойство для каждого класса модели, который соответствует таблице базы данных. **Course.cs**, **Enrollment.cs**, и **Student.cs** файлы содержат классы моделей, которые представляют таблицы базы данных. Класс контекста и классы моделей будет использовать при работе с помощью формирования шаблонов.

Прежде чем продолжить с этим руководством, выполните сборку проекта. В следующем разделе вы создадите код на основе моделей данных, но этот раздел не будет работать, если проект не построен.

## <a name="next-steps"></a>Следующие шаги

В этом учебнике рассмотрены следующие задачи.

> [!div class="checklist"]
> * Создали веб-приложение ASP.NET
> * Созданные модели

Перейдите к следующему руководству, чтобы научиться создавать создания кода, на основе моделей данных.
> [!div class="nextstepaction"]
> [Создание представлений](generating-views.md)