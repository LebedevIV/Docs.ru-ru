---
uid: mvc/overview/getting-started/database-first-development/generating-views
title: Учебник. Создать представления для EF Database First с помощью приложения ASP.NET MVC
description: Это руководство посвящено Создание контроллеров и представлений с помощью формирования шаблонов ASP.NET.
author: Rick-Anderson
ms.author: riande
ms.date: 01/28/2019
ms.topic: tutorial
ms.assetid: 669367cf-8e30-4eb6-821d-10a7d9bb906c
msc.legacyurl: /mvc/overview/getting-started/database-first-development/generating-views
msc.type: authoredcontent
ms.openlocfilehash: 7a56c0f9197a99427bcde6103ebc69d245e8ce63
ms.sourcegitcommit: c47d7c131eebbcd8811e31edda210d64cf4b9d6b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2019
ms.locfileid: "55236423"
---
# <a name="tutorial-generate-views-for-ef-database-first-with-aspnet-mvc-app"></a>Учебник. Создать представления для EF Database First с помощью приложения ASP.NET MVC

С помощью MVC, Entity Framework и формирование шаблонов ASP.NET, можно создать веб-приложение, которое предоставляет интерфейс для существующей базы данных. В этой серии руководств показано, как автоматически создавать код, позволяющий пользователям для отображения, изменения и создавать и удалять данные, находящиеся в таблице базы данных. Созданный код соответствует столбцам в таблице базы данных.

Это руководство посвящено Создание контроллеров и представлений с помощью формирования шаблонов ASP.NET.

В этом учебнике рассмотрены следующие задачи.

> [!div class="checklist"]
> * Добавление элемента формирования шаблонов
> * Добавление ссылок на новые представления
> * Отображение представлений учащегося
> * Отображение представлений регистрации

## <a name="prerequisite"></a>Предварительные требования

* [Создание веб-приложение и модели данных](creating-the-web-application.md)

## <a name="add-scaffold"></a>Добавление элемента формирования шаблонов

Все готово для создания кода, который предоставит операций стандартные данные о классах модели. Добавьте код, добавив элемент формирования шаблонов. Существует много параметров для типа параметра формирования шаблонов, которые можно добавить; в этом руководстве каркаса будет включать контроллера и представлений, которые соответствуют Student и регистрации модели, для которых вы создали в предыдущем разделе.

Для поддержания согласованности в проекте, вы добавите новый контроллер для существующего **контроллеров** папки. Щелкните правой кнопкой мыши **контроллеров** и выберите **добавить** > **создать шаблонный элемент**.

Выберите **контроллер MVC 5 с представлениями, использующий Entity Framework** параметр. Этот параметр будет создавать контроллера и представлений для обновления, удаления, создания и отображения данных в модели.

![Добавьте контроллер mvc](generating-views/_static/image2.png)

Выберите **учащегося (ContosoSite.Models)** класс модели и выберите команду **ContosoUniversityDataEntities (ContosoSite.Models)** для класса контекста. Оставьте имя контроллера как **StudentsController**.

Нажмите кнопку **Добавить**.

Если произошла ошибка, возможно, так как вы не создавали проекта в предыдущем разделе. Если это так, попробуйте выполнить сборку проекта и затем снова добавьте элемента формирования шаблонов.

После завершения процесса создания кода вы увидите новый контроллер и представления в вашем проекте **контроллеров** и **представления** > **учащихся** папки .


Снова выполните те же действия, но добавить элемент формирования шаблонов для **регистрации** класса. По завершении у вас есть **EnrollmentsController.cs** файл и папку в узле **представления** с именем **регистрациями** с представлениями Create, Delete, сведений, редактирования и индекс.

## <a name="add-links-to-new-views"></a>Добавление ссылок на новые представления

Для упрощения перехода на новые представления, можно добавить несколько гиперссылок в индексе представления для учащихся и регистрации. Откройте файл в **представления** > **домашней** > *Index.cshtml*, который является домашней страницей для вашего сайта. Добавьте следующий код ниже jumbotron.

[!code-cshtml[Main](generating-views/samples/sample1.cshtml)]

Для метода ActionLink первый параметр является текст, отображаемый в ссылке. Второй параметр — действие, а третий параметр — имя контроллера. Например первая ссылка указывает на действие индекса в StudentsController. Фактический hyperlink создается на основе этих значений. Первую ссылку в конечном счете пользователи открывают **Index.cshtml** файл включен в **представления/учащихся** папки.

## <a name="display-student-views"></a>Отображение представлений учащегося

Вы проверите, что код, добавленный в проект правильно отображает список учащихся и позволяет пользователям изменение, создание или удаление записей учащихся в базе данных.

Щелкните правой кнопкой мыши **представления** > **Главная** > *Index.cshtml* файла и выберите **просмотреть в браузере**. На домашней странице приложения выберите **список учащихся**.

![](generating-views/_static/image6.png)

На **индекс** странице, обратите внимание на список учащихся и ссылки, чтобы изменить эти данные. Выберите **Create New** ссылку и ввести некоторые значения для нового учащегося. Нажмите кнопку **создать**и обратите внимание, что нового учащегося добавляется в список.

Вернитесь на **индекс** выберите **изменить** связать и изменить некоторые значения для учащегося. Нажмите кнопку **Сохранить**и обратите внимание, что запись учащегося была изменена.

Наконец, выберите **удалить** ссылку и убедитесь, что Вы действительно хотите удалить запись, щелкнув **удалить** кнопки.

Без написания кода, вы добавили представления, которые выполняют общие операции с данными в таблице учащихся.

Вы заметите, что текстовую метку для поля на основе базы данных свойства (такие как **LastName**) который не обязательно нужно отобразить на веб-странице. Например, вы можете предпочесть метку, которая будет **Фамилия**. Отображение проблема будет решена позже в этом руководстве.

## <a name="display-enrollment-views"></a>Отображение представлений регистрации

Базы данных включает в себя отношение "один ко многим" между таблицами Student и регистрации и отношение "один ко многим" между таблицами Course и Enrollment. Представления для регистрации правильно обрабатывать эти связи. Перейдите на домашнюю страницу сайта и нажмите кнопку **список регистраций** ссылку и затем **Create New** ссылку.

Представление отображает форму для создания новой записи регистрации. В частности, обратите внимание, что форма содержит **CourseID** стрелку раскрывающегося списка и **StudentID** стрелку раскрывающегося списка. Как заполняются значениями из связанных таблиц.

Кроме того предоставленных значений автоматически применяется проверка зависимости от типа данных поля. **Оценка** требуется номер, поэтому сообщение об ошибке отображается при попытке предоставить несовместимое значение: *Поле корпоративного класса должно быть числом.*

Вы убедились, что автоматически создается представления позволяют пользователям работать с данными в базе данных. В следующем руководстве этой серии будет обновлять базу данных и внесите соответствующие изменения в веб-приложения.

## <a name="next-steps"></a>Следующие шаги

В этом учебнике рассмотрены следующие задачи.

> [!div class="checklist"]
> * Добавлена каркаса
> * Добавлены ссылки на новые представления
> * Представления отображается учащегося
> * Представления отображается регистрации

Перейдите к следующему руководству, чтобы узнать, как изменение базы данных.
> [!div class="nextstepaction"]
> [Изменение базы данных](changing-the-database.md)