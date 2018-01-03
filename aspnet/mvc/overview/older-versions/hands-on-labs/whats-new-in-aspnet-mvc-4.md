---
uid: mvc/overview/older-versions/hands-on-labs/whats-new-in-aspnet-mvc-4
title: "Новые возможности в ASP.NET MVC 4 | Документы Microsoft"
author: rick-anderson
description: "ASP.NET MVC 4 — это платформа для создания масштабируемых, основанную на стандартах веб-приложений с помощью надежных конструктивных шаблонов и эффективных возможностей ASP.NET и..."
ms.author: aspnetcontent
manager: wpickett
ms.date: 02/18/2013
ms.topic: article
ms.assetid: 48f7feb3-872f-485d-b96f-e30011ff8c4a
ms.technology: dotnet-mvc
ms.prod: .net-framework
msc.legacyurl: /mvc/overview/older-versions/hands-on-labs/whats-new-in-aspnet-mvc-4
msc.type: authoredcontent
ms.openlocfilehash: 3de952224e23eed29f90ed0e8c662e4ee3f531ce
ms.sourcegitcommit: 9a9483aceb34591c97451997036a9120c3fe2baf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2017
---
<a name="whats-new-in-aspnet-mvc-4"></a><span data-ttu-id="90c93-103">Новые возможности в ASP.NET MVC 4</span><span class="sxs-lookup"><span data-stu-id="90c93-103">What's New in ASP.NET MVC 4</span></span>
====================
<span data-ttu-id="90c93-104">по [Web лагеря команды](https://twitter.com/webcamps)</span><span class="sxs-lookup"><span data-stu-id="90c93-104">by [Web Camps Team](https://twitter.com/webcamps)</span></span>

[<span data-ttu-id="90c93-105">Загрузите комплект учебных материалов лагеря Web</span><span class="sxs-lookup"><span data-stu-id="90c93-105">Download Web Camps Training Kit</span></span>](http://www.microsoft.com/en-us/download/29843)

> <span data-ttu-id="90c93-106">ASP.NET MVC 4 — это платформа для создания масштабируемых, основанную на стандартах веб-приложений с помощью надежных конструктивных шаблонов и эффективных возможностей ASP.NET и .NET framework.</span><span class="sxs-lookup"><span data-stu-id="90c93-106">ASP.NET MVC 4 is a framework for building scalable, standards-based web applications using well-established design patterns and the power of the ASP.NET and the .NET framework.</span></span> <span data-ttu-id="90c93-107">Этот новый, четвертая версия платформы основное внимание уделяется упрощение разработки мобильных веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="90c93-107">This new, fourth version of the framework focuses on making mobile web application development easier.</span></span>
> 
> <span data-ttu-id="90c93-108">Вначале при создании нового проекта ASP.NET MVC 4 теперь имеется шаблон проекта приложений для мобильных устройств, которые можно использовать для построения отдельное приложение, специально для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="90c93-108">To begin with, when you create a new ASP.NET MVC 4 project there is now a mobile application project template you can use to build a standalone app specifically for mobile devices.</span></span> <span data-ttu-id="90c93-109">Кроме того ASP.NET MVC 4 интегрируется с jQuery Mobile через jQuery.Mobile.MVC пакет NuGet.</span><span class="sxs-lookup"><span data-stu-id="90c93-109">Additionally, ASP.NET MVC 4 integrates with jQuery Mobile through a jQuery.Mobile.MVC NuGet package.</span></span> <span data-ttu-id="90c93-110">jQuery Mobile — это платформа на основе HTML5, для разработки веб-приложений, совместимых с всех платформ популярных мобильных устройствах, включая Windows Phone, iPhone, Android и т. д.</span><span class="sxs-lookup"><span data-stu-id="90c93-110">jQuery Mobile is an HTML5-based framework for developing web apps that are compatible with all popular mobile device platforms, including Windows Phone, iPhone, Android and so on.</span></span> <span data-ttu-id="90c93-111">Тем не менее если вам требуется специализации, ASP.NET MVC 4 также позволяет обслуживать различные представления для различных устройств и обеспечивают оптимизацию для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="90c93-111">However, if you need specialization, ASP.NET MVC 4 also enables you to serve different views for different devices and provide device-specific optimizations.</span></span>
> 
> <span data-ttu-id="90c93-112">В этой практической будет начинаться с ASP.NET MVC 4 &quot;веб-приложение&quot; шаблон проекта для создания приложения фотоальбома.</span><span class="sxs-lookup"><span data-stu-id="90c93-112">In this hands-on lab, you will start with the ASP.NET MVC 4 &quot;Internet Application&quot; project template to create a Photo Gallery application.</span></span> <span data-ttu-id="90c93-113">Постепенно, поможет повысить эффективность приложения с помощью jQuery Mobile, а также новые функции ASP.NET MVC 4, чтобы сделать его совместимым с различных мобильных устройств и настольных компьютеров веб-браузеры.</span><span class="sxs-lookup"><span data-stu-id="90c93-113">You will progressively enhance the app using jQuery Mobile and ASP.NET MVC 4's new features to make it compatible with different mobile devices and desktop web browsers.</span></span> <span data-ttu-id="90c93-114">Также вы узнаете о новых рецепты кода для создания кода, а также как ASP.NET MVC 4 проще написать асинхронные методы действия с помощью поддержки задачи&lt;ActionResult&gt; типы возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="90c93-114">You will also learn about new code recipes for code generation and how ASP.NET MVC 4 makes it easier for you to write asynchronous action methods by supporting Task&lt;ActionResult&gt; return types.</span></span>
> 
> <span data-ttu-id="90c93-115">Все образцы кода и фрагменты кода включаются в Web лагеря комплект учебных материалов, доступных в [https://www.microsoft.com/en-us/download/29843](https://www.microsoft.com/en-us/download/29843).</span><span class="sxs-lookup"><span data-stu-id="90c93-115">All sample code and snippets are included in the Web Camps Training Kit, available at [https://www.microsoft.com/en-us/download/29843](https://www.microsoft.com/en-us/download/29843).</span></span>


<a id="Objectives"></a>

<a id="Objectives"></a>
### <a name="objectives"></a><span data-ttu-id="90c93-116">Цели</span><span class="sxs-lookup"><span data-stu-id="90c93-116">Objectives</span></span>

<span data-ttu-id="90c93-117">В этой практической вы узнаете, как:</span><span class="sxs-lookup"><span data-stu-id="90c93-117">In this hands-on lab, you will learn how to:</span></span>

- <span data-ttu-id="90c93-118">Воспользоваться преимуществами расширений для ASP.NET MVC проект шаблоны, в том числе нового шаблона проекта приложений для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="90c93-118">Take advantage of the enhancements to the ASP.NET MVC project templates-including the new mobile application project template</span></span>
- <span data-ttu-id="90c93-119">Использовать атрибут просмотра HTML5 и медиа-запросами CSS для улучшения отображения на мобильных устройствах</span><span class="sxs-lookup"><span data-stu-id="90c93-119">Use the HTML5 viewport attribute and CSS media queries to improve the display on mobile devices</span></span>
- <span data-ttu-id="90c93-120">Используйте jQuery Mobile для прогрессивного улучшения и для создания оптимизированных для сенсорных экранов веб-интерфейса</span><span class="sxs-lookup"><span data-stu-id="90c93-120">Use jQuery Mobile for progressive enhancements and for building touch-optimized web UI</span></span>
- <span data-ttu-id="90c93-121">Создавать мобильные особых представлений</span><span class="sxs-lookup"><span data-stu-id="90c93-121">Create mobile-specific views</span></span>
- <span data-ttu-id="90c93-122">Использовать компонент представления переключателя для переключения между представлениями мобильные и Классические приложения</span><span class="sxs-lookup"><span data-stu-id="90c93-122">Use the view-switcher component to toggle between mobile and desktop views in the application</span></span>
- <span data-ttu-id="90c93-123">Создание асинхронных контроллеров с помощью поддержки задач</span><span class="sxs-lookup"><span data-stu-id="90c93-123">Create asynchronous controllers using task support</span></span>

<a id="Prerequisites"></a>

<a id="Prerequisites"></a>
### <a name="prerequisites"></a><span data-ttu-id="90c93-124">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="90c93-124">Prerequisites</span></span>

<span data-ttu-id="90c93-125">Необходимо иметь следующие элементы для этой лаборатории.</span><span class="sxs-lookup"><span data-stu-id="90c93-125">You must have the following items to complete this lab:</span></span>

- <span data-ttu-id="90c93-126">[Microsoft Visual Studio Express 2012 для Web](https://www.microsoft.com/visualstudio/eng/products/visual-studio-express-for-web) или выше (чтение [приложении Б](#AppendixB) инструкции по его установке).</span><span class="sxs-lookup"><span data-stu-id="90c93-126">[Microsoft Visual Studio Express 2012 for Web](https://www.microsoft.com/visualstudio/eng/products/visual-studio-express-for-web) or superior (read [Appendix B](#AppendixB) for instructions on how to install it).</span></span>
- <span data-ttu-id="90c93-127">[ASP.NET MVC 4](../../../mvc4.md) (включен в установку Microsoft Visual Studio 2012)</span><span class="sxs-lookup"><span data-stu-id="90c93-127">[ASP.NET MVC 4](../../../mvc4.md) (included in the Microsoft Visual Studio 2012 installation)</span></span>
- <span data-ttu-id="90c93-128">Эмулятор Windows Phone (включен в [Windows Phone 7.1.1 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=29233))</span><span class="sxs-lookup"><span data-stu-id="90c93-128">Windows Phone Emulator (included in the [Windows Phone 7.1.1 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=29233))</span></span>
- <span data-ttu-id="90c93-129">Необязательно — [WebMatrix 2](https://www.microsoft.com/web/webmatrix/) с **Electric Plum iPhone симулятор** расширения (только для Упражнение 3 используется для просмотра веб-приложения с эмулятор iPhone)</span><span class="sxs-lookup"><span data-stu-id="90c93-129">Optional - [WebMatrix 2](https://www.microsoft.com/web/webmatrix/) with **Electric Plum iPhone Simulator** extension (only for Exercise 3 used to browse the web application with an iPhone simulator)</span></span>

<a id="Setup"></a>

<a id="Setup"></a>
### <a name="setup"></a><span data-ttu-id="90c93-130">Установка</span><span class="sxs-lookup"><span data-stu-id="90c93-130">Setup</span></span>

<span data-ttu-id="90c93-131">В документе лаборатории будет предложено вставлять блоки кода.</span><span class="sxs-lookup"><span data-stu-id="90c93-131">Throughout the lab document, you will be instructed to insert code blocks.</span></span> <span data-ttu-id="90c93-132">Для удобства большинство этого кода предоставляется как Visual Studio к фрагментам кода, который можно использовать из среды Visual Studio, чтобы избежать необходимости вручную добавить.</span><span class="sxs-lookup"><span data-stu-id="90c93-132">For your convenience, most of that code is provided as Visual Studio Code Snippets, which you can use from within Visual Studio to avoid having to add it manually.</span></span>

<span data-ttu-id="90c93-133">Чтобы установить фрагменты кода:</span><span class="sxs-lookup"><span data-stu-id="90c93-133">To install the code snippets:</span></span>

1. <span data-ttu-id="90c93-134">Откройте окно проводника Windows и перейдите в лаборатории **Source\Setup** папки.</span><span class="sxs-lookup"><span data-stu-id="90c93-134">Open a Windows Explorer window and browse to the lab's **Source\Setup** folder.</span></span>
2. <span data-ttu-id="90c93-135">Дважды щелкните **Setup.cmd** файл в этой папке, чтобы установить фрагменты кода Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="90c93-135">Double-click the **Setup.cmd** file in this folder to install the Visual Studio code snippets.</span></span>

<span data-ttu-id="90c93-136">Если вы не знакомы с фрагментов кода Visual Studio и хотите узнать о способах их использования, можно ссылаться в приложение из этого документа &quot; [с помощью фрагментов кода в приложении A:](#AppendixA)&quot;.</span><span class="sxs-lookup"><span data-stu-id="90c93-136">If you are not familiar with the Visual Studio Code Snippets, and want to learn how to use them, you can refer to the appendix from this document &quot;[Appendix A: Using Code Snippets](#AppendixA)&quot;.</span></span>

<a id="Exercises"></a>

<a id="Exercises"></a>
## <a name="exercises"></a><span data-ttu-id="90c93-137">Упражнения</span><span class="sxs-lookup"><span data-stu-id="90c93-137">Exercises</span></span>

<span data-ttu-id="90c93-138">Данная практическая работа включает следующие упражнения:</span><span class="sxs-lookup"><span data-stu-id="90c93-138">This hands-on lab includes the following exercises:</span></span>

1. [<span data-ttu-id="90c93-139">Новые шаблоны проектов ASP.NET MVC 4</span><span class="sxs-lookup"><span data-stu-id="90c93-139">New ASP.NET MVC 4 Project Templates</span></span>](#Exercise1)
2. [<span data-ttu-id="90c93-140">Создание веб-приложения фотоальбом</span><span class="sxs-lookup"><span data-stu-id="90c93-140">Creating the Photo Gallery Web Application</span></span>](#Exercise2)
3. [<span data-ttu-id="90c93-141">Добавление поддержки для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="90c93-141">Adding Support for Mobile Devices</span></span>](#Exercise3)
4. [<span data-ttu-id="90c93-142">Использование асинхронных контроллеров</span><span class="sxs-lookup"><span data-stu-id="90c93-142">Using Asynchronous Controllers</span></span>](#Exercise4)

> [!NOTE]
> <span data-ttu-id="90c93-143">Каждого упражнения сопровождается **окончания** папку, содержащую полученное в результате решение, должен быть получен после завершения выполнения упражнений.</span><span class="sxs-lookup"><span data-stu-id="90c93-143">Each exercise is accompanied by an **End** folder containing the resulting solution you should obtain after completing the exercises.</span></span> <span data-ttu-id="90c93-144">Это решение можно использовать как руководство, если вам нужна дополнительная помощь при выполнении упражнений.</span><span class="sxs-lookup"><span data-stu-id="90c93-144">You can use this solution as a guide if you need additional help working through the exercises.</span></span>


<span data-ttu-id="90c93-145">Предполагаемое время для выполнения этого занятия: **60 минут**.</span><span class="sxs-lookup"><span data-stu-id="90c93-145">Estimated time to complete this lab: **60 minutes**.</span></span>

<a id="Exercise1"></a>

<a id="Exercise_1_New_ASPNET_MVC_4_Project_Templates"></a>
### <a name="exercise-1-new-aspnet-mvc-4-project-templates"></a><span data-ttu-id="90c93-146">Упражнение 1: Новые шаблоны проектов ASP.NET MVC 4</span><span class="sxs-lookup"><span data-stu-id="90c93-146">Exercise 1: New ASP.NET MVC 4 Project Templates</span></span>

<span data-ttu-id="90c93-147">В этом упражнении вы исследуете улучшения, внесенные в шаблоны проекта ASP.NET MVC 4.</span><span class="sxs-lookup"><span data-stu-id="90c93-147">In this exercise, you will explore the enhancements in the ASP.NET MVC 4 Project templates.</span></span> <span data-ttu-id="90c93-148">Дополнение к шаблону веб-приложение, уже присутствует в MVC 3, эта версия теперь включает отдельный шаблон для мобильных приложений.</span><span class="sxs-lookup"><span data-stu-id="90c93-148">In addition to the Internet Application template, already present in MVC 3, this version now includes a separate template for Mobile applications.</span></span> <span data-ttu-id="90c93-149">Во-первых будут рассмотрены некоторые возможности соответствующие каждый из этих шаблонов.</span><span class="sxs-lookup"><span data-stu-id="90c93-149">First, you will look at some relevant features of each of the templates.</span></span> <span data-ttu-id="90c93-150">После этого будет работать в визуализации страницы правильно на различных платформах с использованием правильного подхода.</span><span class="sxs-lookup"><span data-stu-id="90c93-150">Then, you will work on rendering your page properly on the different platforms by using the right approach.</span></span>

<a id="Task_1_-_Exploring_the_Internet_Application_Template"></a>
#### <a name="task-1---exploring-the-internet-application-template"></a><span data-ttu-id="90c93-151">Задача 1. изучение шаблона приложения Интернета</span><span class="sxs-lookup"><span data-stu-id="90c93-151">Task 1 - Exploring the Internet Application Template</span></span>

1. <span data-ttu-id="90c93-152">Откройте **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="90c93-152">Open **Visual Studio**.</span></span>
2. <span data-ttu-id="90c93-153">Выберите **файл | Новые | Проект** команду меню.</span><span class="sxs-lookup"><span data-stu-id="90c93-153">Select the **File | New | Project** menu command.</span></span> <span data-ttu-id="90c93-154">В **новый проект** диалогового окна выберите **Visual C# | Web** шаблона на левой панели дерева, а затем выберите **веб-приложение ASP.NET MVC 4.**</span><span class="sxs-lookup"><span data-stu-id="90c93-154">In the **New Project** dialog, select the **Visual C# | Web** template on the left pane tree, and choose **ASP.NET MVC 4 Web Application.**</span></span> <span data-ttu-id="90c93-155">Назовите проект **PhotoGallery**, выберите расположение (или оставьте значение по умолчанию) и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="90c93-155">Name the project **PhotoGallery**, select a location (or leave the default) and click **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="90c93-156">После этого следует настроить сейчас вы создаете решение Коллекция фотографий ASP.NET MVC 4.</span><span class="sxs-lookup"><span data-stu-id="90c93-156">You will later customize the PhotoGallery ASP.NET MVC 4 solution you are now creating.</span></span>

    <span data-ttu-id="90c93-157">![Создание нового проекта](whats-new-in-aspnet-mvc-4/_static/image1.png "Создание нового проекта")</span><span class="sxs-lookup"><span data-stu-id="90c93-157">![Creating a new project](whats-new-in-aspnet-mvc-4/_static/image1.png "Creating a new project")</span></span>

    <span data-ttu-id="90c93-158">*Создание нового проекта*</span><span class="sxs-lookup"><span data-stu-id="90c93-158">*Creating a new project*</span></span>
3. <span data-ttu-id="90c93-159">В **нового проекта ASP.NET MVC 4** диалогового окна выберите **веб-приложение** шаблон проекта и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="90c93-159">In the **New ASP.NET MVC 4 Project** dialog, select the **Internet Application** project template and click **OK**.</span></span> <span data-ttu-id="90c93-160">Убедитесь, что были выбраны в качестве обработчика представлений Razor.</span><span class="sxs-lookup"><span data-stu-id="90c93-160">Make sure you have selected Razor as the view engine.</span></span>

    <span data-ttu-id="90c93-161">![Создание нового приложения ASP.NET MVC 4 Интернет](whats-new-in-aspnet-mvc-4/_static/image2.png "Создание нового приложения ASP.NET MVC 4 Интернета")</span><span class="sxs-lookup"><span data-stu-id="90c93-161">![Creating a new ASP.NET MVC 4 Internet Application](whats-new-in-aspnet-mvc-4/_static/image2.png "Creating a new ASP.NET MVC 4 Internet Application")</span></span>

    <span data-ttu-id="90c93-162">*Создание нового приложения ASP.NET MVC 4 Интернета*</span><span class="sxs-lookup"><span data-stu-id="90c93-162">*Creating a new ASP.NET MVC 4 Internet Application*</span></span>

    > [!NOTE]
    > <span data-ttu-id="90c93-163">Синтаксис Razor была введена в ASP.NET MVC 3.</span><span class="sxs-lookup"><span data-stu-id="90c93-163">Razor syntax has been introduced in ASP.NET MVC 3.</span></span> <span data-ttu-id="90c93-164">Его задача — чтобы свести к минимуму число знаков и нажатий клавиш в файл, включение fast и жидкости кодирования рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="90c93-164">Its goal is to minimize the number of characters and keystrokes required in a file, enabling a fast and fluid coding workflow.</span></span> <span data-ttu-id="90c93-165">Razor использует существующие C# и VB (или других) языковые навыки и доставляет синтаксиса разметки шаблона, который включает это здорово рабочий процесс построения HTML.</span><span class="sxs-lookup"><span data-stu-id="90c93-165">Razor leverages existing C# / VB (or other) language skills and delivers a template markup syntax that enables an awesome HTML construction workflow.</span></span>
4. <span data-ttu-id="90c93-166">Нажмите клавишу **F5** для запуска решения и просмотреть обновленные шаблоны.</span><span class="sxs-lookup"><span data-stu-id="90c93-166">Press **F5** to run the solution and see the renewed templates.</span></span> <span data-ttu-id="90c93-167">Проверьте работу следующих функций:</span><span class="sxs-lookup"><span data-stu-id="90c93-167">You can check out the following features:</span></span>

    <span data-ttu-id="90c93-168">**Шаблоны в современном стиле**</span><span class="sxs-lookup"><span data-stu-id="90c93-168">**Modern-style templates**</span></span>

    <span data-ttu-id="90c93-169">Шаблоны были обновлены, предоставляя дополнительные стили, современный вид.</span><span class="sxs-lookup"><span data-stu-id="90c93-169">The templates have been renewed, providing more modern-looking styles.</span></span>

    <span data-ttu-id="90c93-170">![Шаблоны ASP.NET MVC 4 приведен](whats-new-in-aspnet-mvc-4/_static/image3.png "приведен шаблоны MVC 4")</span><span class="sxs-lookup"><span data-stu-id="90c93-170">![ASP.NET MVC 4 restyled templates](whats-new-in-aspnet-mvc-4/_static/image3.png "MVC 4 restyled templates")</span></span>

    <span data-ttu-id="90c93-171">*Шаблоны ASP.NET MVC 4 приведен*</span><span class="sxs-lookup"><span data-stu-id="90c93-171">*ASP.NET MVC 4 restyled templates*</span></span>

    <span data-ttu-id="90c93-172">![Новая страница контакт](whats-new-in-aspnet-mvc-4/_static/image4.png "страницы нового контакта")</span><span class="sxs-lookup"><span data-stu-id="90c93-172">![New Contact page](whats-new-in-aspnet-mvc-4/_static/image4.png "New Contact page")</span></span>

    <span data-ttu-id="90c93-173">*Новая страница контакта*</span><span class="sxs-lookup"><span data-stu-id="90c93-173">*New Contact page*</span></span>

    <span data-ttu-id="90c93-174">**Адаптивной отрисовки**</span><span class="sxs-lookup"><span data-stu-id="90c93-174">**Adaptive Rendering**</span></span>

    <span data-ttu-id="90c93-175">Извлеките изменения размера окна браузера и обратите внимание на то, как динамически адаптируется макет страницы и новый размер окна.</span><span class="sxs-lookup"><span data-stu-id="90c93-175">Check out resizing the browser window and notice how the page layout dynamically adapts to the new window size.</span></span> <span data-ttu-id="90c93-176">Эти шаблоны использовать методика адаптивной отрисовки к просмотру правильно в настольных и мобильных платформ без настройки.</span><span class="sxs-lookup"><span data-stu-id="90c93-176">These templates use the adaptive rendering technique to render properly in both desktop and mobile platforms without any customization.</span></span>

    <span data-ttu-id="90c93-177">![Шаблон проекта ASP.NET MVC 4 в другом браузере размеры](whats-new-in-aspnet-mvc-4/_static/image5.png "шаблон проекта ASP.NET MVC 4 в другом браузере размеры")</span><span class="sxs-lookup"><span data-stu-id="90c93-177">![ASP.NET MVC 4 project template in different browser sizes](whats-new-in-aspnet-mvc-4/_static/image5.png "ASP.NET MVC 4 project template in different browser sizes")</span></span>

    <span data-ttu-id="90c93-178">*Шаблон проекта ASP.NET MVC 4 в другом браузере размеры*</span><span class="sxs-lookup"><span data-stu-id="90c93-178">*ASP.NET MVC 4 project template in different browser sizes*</span></span>

    <span data-ttu-id="90c93-179">**Обширные возможности пользовательского интерфейса с помощью JavaScript**</span><span class="sxs-lookup"><span data-stu-id="90c93-179">**Richer UI with JavaScript**</span></span>

    <span data-ttu-id="90c93-180">Другое усовершенствование шаблоны проектов по умолчанию является использование JavaScript для обеспечения более интерактивны JavaScript.</span><span class="sxs-lookup"><span data-stu-id="90c93-180">Another enhancement to default project templates is the use of JavaScript to provide a more interactive JavaScript.</span></span> <span data-ttu-id="90c93-181">Ссылки входа и регистрации, используемые в шаблоне проиллюстрировать, как использовать jQuery проверки для проверки ввода поля со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="90c93-181">The Login and Register links used in the template exemplify how to use the jQuery Validations to validate the input fields from client-side.</span></span>

    ![jQuery проверки](whats-new-in-aspnet-mvc-4/_static/image6.png)

    <span data-ttu-id="90c93-183">*jQuery проверки*</span><span class="sxs-lookup"><span data-stu-id="90c93-183">*jQuery Validation*</span></span>

    > [!NOTE]
    > <span data-ttu-id="90c93-184">Обратите внимание, что два журнала в разделах, в первом разделе можно в систему под учетной записью зарегистрированный на узле и во втором разделе, вы можете altenativelly в систему с помощью другой службы проверки подлинности, например google (отключено по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="90c93-184">Notice the two log in sections, in the first section you can log in using a registerd account from the site and in the second section you can altenativelly log in using another authentication service like google (disabled by default).</span></span>
5. <span data-ttu-id="90c93-185">Закройте браузер, чтобы остановить отладчик и вернуться в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="90c93-185">Close the browser to stop the debugger and return to Visual Studio.</span></span>
6. <span data-ttu-id="90c93-186">Откройте файл **AuthConfig.cs** в компоненте **приложения\_запустить** папки.</span><span class="sxs-lookup"><span data-stu-id="90c93-186">Open the file **AuthConfig.cs** located under the **App\_Start** folder.</span></span>
7. <span data-ttu-id="90c93-187">Удаление комментария из последней строки для регистрации клиента Google для *OAuth* проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="90c93-187">Remove the comment from the last line to register Google client for *OAuth* authentication.</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample1.cs)]

    > [!NOTE]
    > <span data-ttu-id="90c93-188">Обратите внимание, что можно легко включить проверку подлинности с использованием любой OpenID или OAuth службы как Facebook, Twitter, Майкрософт, и т. д.</span><span class="sxs-lookup"><span data-stu-id="90c93-188">Notice you can easily enable authentication using any OpenID or OAuth service like Facebook, Twitter, Microsoft, etc.</span></span>
8. <span data-ttu-id="90c93-189">Нажмите клавишу **F5** для запуска решения, а затем перейдите на страницу входа.</span><span class="sxs-lookup"><span data-stu-id="90c93-189">Press **F5** to run the solution and navigate to the login page.</span></span>
9. <span data-ttu-id="90c93-190">Выберите **Google** службу для входа.</span><span class="sxs-lookup"><span data-stu-id="90c93-190">Select **Google** service to log in.</span></span>

    ![При выборе журнала в службе](whats-new-in-aspnet-mvc-4/_static/image7.png)

    <span data-ttu-id="90c93-192">*При выборе журнала в службе*</span><span class="sxs-lookup"><span data-stu-id="90c93-192">*Selecting the log in service*</span></span>
10. <span data-ttu-id="90c93-193">Вход с помощью учетной записи Google.</span><span class="sxs-lookup"><span data-stu-id="90c93-193">Log in using your Google account.</span></span>
11. <span data-ttu-id="90c93-194">Разрешить узла (localhost) для извлечения сведений из учетной записи Google.</span><span class="sxs-lookup"><span data-stu-id="90c93-194">Allow the site (localhost) to retrieve information from Google account.</span></span>
12. <span data-ttu-id="90c93-195">Наконец необходимо зарегистрировать на сайте, чтобы связать учетную запись Google.</span><span class="sxs-lookup"><span data-stu-id="90c93-195">Finally, you will have to register in the site to associate the Google account.</span></span>

    ![Связать учетную запись Google](whats-new-in-aspnet-mvc-4/_static/image8.png)

    <span data-ttu-id="90c93-197">*Связывание учетной записи Google*</span><span class="sxs-lookup"><span data-stu-id="90c93-197">*Associating your Google account*</span></span>
13. <span data-ttu-id="90c93-198">Закройте браузер, чтобы остановить отладчик и вернуться в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="90c93-198">Close the browser to stop the debugger and return to Visual Studio.</span></span>
14. <span data-ttu-id="90c93-199">Теперь изучите решение, чтобы извлечь некоторые новые возможности, появившиеся в ASP.NET MVC 4 в шаблоне проекта.</span><span class="sxs-lookup"><span data-stu-id="90c93-199">Now explore the solution to check out some other new features introduced by ASP.NET MVC 4 in the project template.</span></span>

    <span data-ttu-id="90c93-200">![Шаблон проекта ASP.NET MVC 4 Интернет приложений](whats-new-in-aspnet-mvc-4/_static/image9.png "шаблон проекта ASP.NET MVC 4 Интернет приложений")</span><span class="sxs-lookup"><span data-stu-id="90c93-200">![The ASP.NET MVC 4 Internet Application Project Template](whats-new-in-aspnet-mvc-4/_static/image9.png "The ASP.NET MVC 4 Internet Application Project Template")</span></span>

    <span data-ttu-id="90c93-201">*Шаблон проекта приложения Internet ASP.NET MVC 4*</span><span class="sxs-lookup"><span data-stu-id="90c93-201">*The ASP.NET MVC 4 Internet Application Project Template*</span></span>

    - <span data-ttu-id="90c93-202">**HTML 5 разметки**</span><span class="sxs-lookup"><span data-stu-id="90c93-202">**HTML 5 Markup**</span></span>

        <span data-ttu-id="90c93-203">Обзор представлений шаблона, чтобы узнать, разметку новой темы.</span><span class="sxs-lookup"><span data-stu-id="90c93-203">Browse template views to find out the new theme markup.</span></span>

        <span data-ttu-id="90c93-204">![Новый шаблон с помощью Razor и HTML5 About.cshtml разметки. ] (whats-new-in-aspnet-mvc-4/_static/image10.png "Новый шаблон, с помощью Razor и HTML5 About.cshtml разметки.")</span><span class="sxs-lookup"><span data-stu-id="90c93-204">![New template, using Razor and HTML5 markup About.cshtml.](whats-new-in-aspnet-mvc-4/_static/image10.png "New template, using Razor and HTML5 markup About.cshtml.")</span></span>

        <span data-ttu-id="90c93-205">*Новый шаблон с помощью Razor и HTML5 разметки (About.cshtml).*</span><span class="sxs-lookup"><span data-stu-id="90c93-205">*New template, using Razor and HTML5 markup (About.cshtml).*</span></span>
    - <span data-ttu-id="90c93-206">**Обновленные библиотек JavaScript**</span><span class="sxs-lookup"><span data-stu-id="90c93-206">**Updated JavaScript libraries**</span></span>

        <span data-ttu-id="90c93-207">Шаблон по умолчанию ASP.NET MVC 4 теперь включает использованием KnockoutJS, платформа JavaScript MVVM, которая позволяет создавать разнообразные и с высокой скоростью отклика веб-приложений, с помощью JavaScript и HTML.</span><span class="sxs-lookup"><span data-stu-id="90c93-207">The ASP.NET MVC 4 default template now includes KnockoutJS, a JavaScript MVVM framework that lets you create rich and highly responsive web applications using JavaScript and HTML.</span></span> <span data-ttu-id="90c93-208">Как и в MVC3, jQuery и jQuery библиотеки пользовательского интерфейса также включаются в ASP.NET MVC 4.</span><span class="sxs-lookup"><span data-stu-id="90c93-208">Like in MVC3, jQuery and jQuery UI libraries are also included in ASP.NET MVC 4.</span></span>

        > [!NOTE]
        > <span data-ttu-id="90c93-209">Можно получить дополнительные сведения о библиотеке с использованием KnockOutJS в этой связи: [ [http://learn.knockoutjs.com/](http://learn.knockoutjs.com/)](http://learn.knockoutjs.com/).</span><span class="sxs-lookup"><span data-stu-id="90c93-209">You can get more information about KnockOutJS library in this link: [[http://learn.knockoutjs.com/](http://learn.knockoutjs.com/)](http://learn.knockoutjs.com/).</span></span> <span data-ttu-id="90c93-210">Кроме того, вы можете узнать о jQuery и jQuery UI в [ [http://docs.jquery.com/](http://docs.jquery.com/)](http://docs.jquery.com/).</span><span class="sxs-lookup"><span data-stu-id="90c93-210">Additionally, you can learn about jQuery and jQuery UI in [[http://docs.jquery.com/](http://docs.jquery.com/)](http://docs.jquery.com/).</span></span>

<a id="Task_2_-_Exploring_the_Mobile_Application_Template"></a>
#### <a name="task-2---exploring-the-mobile-application-template"></a><span data-ttu-id="90c93-211">Задача 2 - изучение шаблон мобильных приложений</span><span class="sxs-lookup"><span data-stu-id="90c93-211">Task 2 - Exploring the Mobile Application Template</span></span>

<span data-ttu-id="90c93-212">ASP.NET MVC 4 облегчает разработку веб-сайты для мобильных устройств и браузеров планшета.</span><span class="sxs-lookup"><span data-stu-id="90c93-212">ASP.NET MVC 4 facilitates the development of websites for mobile and tablet browsers.</span></span> <span data-ttu-id="90c93-213">Этот шаблон имеет такую же структуру приложения как веб-приложение, шаблон (Обратите внимание, что код контроллера практически идентичен), но его стиль был изменен для отображаться должным образом в мобильных устройств на базе сенсорный ввод.</span><span class="sxs-lookup"><span data-stu-id="90c93-213">This template has the same application structure as the Internet Application template (notice that the controller code is practically identical), but its style was modified to render properly in touch-based mobile devices.</span></span>

1. <span data-ttu-id="90c93-214">Выберите **файл | Новые | Проект** команду меню.</span><span class="sxs-lookup"><span data-stu-id="90c93-214">Select the **File | New | Project** menu command.</span></span> <span data-ttu-id="90c93-215">В **новый проект** диалогового окна выберите **Visual C# | Web** шаблона на левой панели дерева, а затем выберите **веб-приложение ASP.NET MVC 4.**</span><span class="sxs-lookup"><span data-stu-id="90c93-215">In the **New Project** dialog, select the **Visual C# | Web** template on the left pane tree, and choose the **ASP.NET MVC 4 Web Application.**</span></span> <span data-ttu-id="90c93-216">Назовите проект **PhotoGallery.Mobile**, выберите расположение (или оставьте значение по умолчанию), выберите &quot;добавить решение&quot; и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="90c93-216">Name the project **PhotoGallery.Mobile**, select a location (or leave the default), select &quot;Add to solution&quot; and click **OK**.</span></span>
2. <span data-ttu-id="90c93-217">В **нового проекта ASP.NET MVC 4** диалогового окна выберите **мобильного приложения** шаблон проекта и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="90c93-217">In the **New ASP.NET MVC 4 Project** dialog, select the **Mobile Application** project template and click **OK**.</span></span> <span data-ttu-id="90c93-218">Убедитесь, что были выбраны в качестве обработчика представлений Razor.</span><span class="sxs-lookup"><span data-stu-id="90c93-218">Make sure you have selected Razor as the view engine.</span></span>

    <span data-ttu-id="90c93-219">![Создание нового приложения ASP.NET MVC 4 Mobile](whats-new-in-aspnet-mvc-4/_static/image11.png "Создание нового приложения ASP.NET MVC 4 мобильных устройств")</span><span class="sxs-lookup"><span data-stu-id="90c93-219">![Creating a new ASP.NET MVC 4 Mobile Application](whats-new-in-aspnet-mvc-4/_static/image11.png "Creating a new ASP.NET MVC 4 Mobile Application")</span></span>

    <span data-ttu-id="90c93-220">*Создание нового приложения ASP.NET MVC 4 мобильных устройств*</span><span class="sxs-lookup"><span data-stu-id="90c93-220">*Creating a new ASP.NET MVC 4 Mobile Application*</span></span>
3. <span data-ttu-id="90c93-221">Теперь имеется возможность просматривать решения и посмотрите, какие новые функции, представленные в шаблоне решения ASP.NET MVC 4 для мобильных устройств:</span><span class="sxs-lookup"><span data-stu-id="90c93-221">Now you are able to explore the solution and check out some of the new features introduced by the ASP.NET MVC 4 solution template for mobile:</span></span>

    - <span data-ttu-id="90c93-222">**jQuery Mobile библиотеки**</span><span class="sxs-lookup"><span data-stu-id="90c93-222">**jQuery Mobile Library**</span></span>

        <span data-ttu-id="90c93-223">Шаблон проекта приложения для мобильных устройств включает мобильных библиотеки jQuery, который является библиотекой открытым исходным кодом для мобильных устройств с браузерами.</span><span class="sxs-lookup"><span data-stu-id="90c93-223">The Mobile Application project template includes the jQuery Mobile library, which is an open source library for mobile browser compatibility.</span></span> <span data-ttu-id="90c93-224">jQuery Mobile применяет прогрессивном расширении браузеры для мобильных устройств, поддерживающих CSS и JavaScript.</span><span class="sxs-lookup"><span data-stu-id="90c93-224">jQuery Mobile applies progressive enhancement to mobile browsers that support CSS and JavaScript.</span></span> <span data-ttu-id="90c93-225">Прогрессивном расширении включает все браузеры для отображения базовое содержимое веб-страницы, хотя позволяет самых мощных браузеры отображение сложных элементов.</span><span class="sxs-lookup"><span data-stu-id="90c93-225">Progressive enhancement enables all browsers to display the basic content of a web page, while it only enables the most powerful browsers to display the rich content.</span></span> <span data-ttu-id="90c93-226">JavaScript и CSS, включенные в файлы jQuery мобильных стиль помочь браузеры для мобильных устройств в соответствии с содержимым на экране, без внесения изменений в разметке страницы.</span><span class="sxs-lookup"><span data-stu-id="90c93-226">The JavaScript and CSS files, included in the jQuery Mobile style, help mobile browsers to fit the content in the screen without making any change in the page markup.</span></span>

        ![jQuery-mobile-library-included-in-the-template](whats-new-in-aspnet-mvc-4/_static/image12.png)

        <span data-ttu-id="90c93-228">*библиотеки jQuery мобильных устройств, включенных в шаблон*</span><span class="sxs-lookup"><span data-stu-id="90c93-228">*jQuery mobile library included in the template*</span></span>
    - <span data-ttu-id="90c93-229">**Разметки на основе HTML5**</span><span class="sxs-lookup"><span data-stu-id="90c93-229">**HTML5 based markup**</span></span>

        ![Mobile-application-template-using-HTML5-markup](whats-new-in-aspnet-mvc-4/_static/image13.png)

        <span data-ttu-id="90c93-231">*Шаблон мобильного приложения, используя разметку HTML5, (Login.cshtml и index.cshtml)*</span><span class="sxs-lookup"><span data-stu-id="90c93-231">*Mobile application template using HTML5 markup, (Login.cshtml and index.cshtml)*</span></span>
4. <span data-ttu-id="90c93-232">Нажмите клавишу **F5** для запуска решения.</span><span class="sxs-lookup"><span data-stu-id="90c93-232">Press **F5** to run the solution.</span></span>
5. <span data-ttu-id="90c93-233">Откройте **Windows Phone 7 эмулятор**.</span><span class="sxs-lookup"><span data-stu-id="90c93-233">Open the **Windows Phone 7 Emulator**.</span></span>
6. <span data-ttu-id="90c93-234">На начальном экране телефона откройте Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="90c93-234">In the phone start screen, open Internet Explorer.</span></span> <span data-ttu-id="90c93-235">Извлечь URL-адрес, где запущен приложения рабочего стола и перейдите в этот URL-адрес, по телефону (например `http://localhost:[PortNumber]/`).</span><span class="sxs-lookup"><span data-stu-id="90c93-235">Check out the URL where the desktop application started and browse to that URL from the phone (e.g. `http://localhost:[PortNumber]/`).</span></span>
7. <span data-ttu-id="90c93-236">Теперь можно ввести страницы входа или извлечь о странице.</span><span class="sxs-lookup"><span data-stu-id="90c93-236">Now you are able to enter the login page or check out the about page.</span></span> <span data-ttu-id="90c93-237">Обратите внимание, что стиль веб-сайта основана на новое приложение магазина Windows для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="90c93-237">Notice that the style of the website is based on the new Metro app for mobile.</span></span> <span data-ttu-id="90c93-238">Шаблон проекта ASP.NET MVC 4 правильно отображается на мобильных устройствах, убедившись, что все элементы страницы были видимы и включены.</span><span class="sxs-lookup"><span data-stu-id="90c93-238">The ASP.NET MVC 4 project template is correctly displayed on mobile devices, making sure all the elements of the page are visible and enabled.</span></span> <span data-ttu-id="90c93-239">Обратите внимание, что ссылки в заголовке достаточно большой, касании или щелчке.</span><span class="sxs-lookup"><span data-stu-id="90c93-239">Notice that the links on the header are big enough to be clicked or tapped.</span></span>

    <span data-ttu-id="90c93-240">![Проект шаблона страниц в мобильном устройстве](whats-new-in-aspnet-mvc-4/_static/image14.png "проект шаблона страниц в мобильных устройств")</span><span class="sxs-lookup"><span data-stu-id="90c93-240">![Project template pages in a mobile device](whats-new-in-aspnet-mvc-4/_static/image14.png "Project template pages in a mobile device")</span></span>

    <span data-ttu-id="90c93-241">*Страницы шаблона проекта в мобильных устройств*</span><span class="sxs-lookup"><span data-stu-id="90c93-241">*Project template pages in a mobile device*</span></span>
8. <span data-ttu-id="90c93-242">Новый шаблон также использует **просмотра метатег**.</span><span class="sxs-lookup"><span data-stu-id="90c93-242">The new template also uses the **Viewport meta tag**.</span></span> <span data-ttu-id="90c93-243">Большинство мобильных браузеров определяют ширину окна браузера виртуальный или &quot;просмотра&quot;, которого больше, чем фактическую ширину мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="90c93-243">Most mobile browsers define a width for a virtual browser window or &quot;viewport&quot;, which is larger than the actual width of the mobile device.</span></span> <span data-ttu-id="90c93-244">Это позволяет браузеры для мобильных устройств для отображения всей веб-страницы внутри виртуального экрана.</span><span class="sxs-lookup"><span data-stu-id="90c93-244">This enables mobile browsers to display the entire web page inside the virtual display.</span></span> <span data-ttu-id="90c93-245">**Просмотра метатег** позволяет веб-разработчикам задать ширину, высоту и масштабирования области обозревателя на мобильных устройствах **.**</span><span class="sxs-lookup"><span data-stu-id="90c93-245">The **Viewport meta tag** allows web developers to set the width, height and scale of the browser area on mobile devices **.**</span></span> <span data-ttu-id="90c93-246">Шаблон для мобильных приложений ASP.NET MVC 4 задает окно просмотра по ширине устройства (&quot;ширина = устройство ширина&quot;) в шаблон макета (*одну\_Layout.cshtml*), после чего все страницы будут иметь их просмотра значение ширины экрана устройства.</span><span class="sxs-lookup"><span data-stu-id="90c93-246">The ASP.NET MVC 4 template for Mobile Applications sets the viewport to the device width (&quot;width=device-width&quot;) in the layout template (*Views\Shared\_Layout.cshtml*), so that all the pages will have their viewport set to the device screen width.</span></span> <span data-ttu-id="90c93-247">Обратите внимание, просмотра метатег не изменится в представление браузера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="90c93-247">Notice that the Viewport meta tag will not change the default browser view.</span></span>
9. <span data-ttu-id="90c93-248">Откройте  **\_Layout.cshtml**, расположенного в **представления | Общие** папки и комментарий метатег окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="90c93-248">Open **\_Layout.cshtml**, located in the **Views | Shared** folder, and comment the Viewport meta tag.</span></span> <span data-ttu-id="90c93-249">Запустите приложение, если нет уже открыт и извлечь различия.</span><span class="sxs-lookup"><span data-stu-id="90c93-249">Run the application, if not already opened, and check out the differences.</span></span>


    [!code-cshtml[Main](whats-new-in-aspnet-mvc-4/samples/sample2.cshtml)]

    <span data-ttu-id="90c93-250">![Сайт, преобразовав метатег окно просмотра](whats-new-in-aspnet-mvc-4/_static/image15.png "сайта преобразовав метатег окна просмотра")</span><span class="sxs-lookup"><span data-stu-id="90c93-250">![The site after commenting the viewport meta tag](whats-new-in-aspnet-mvc-4/_static/image15.png "The site after commenting the viewport meta tag")</span></span>

    <span data-ttu-id="90c93-251">*Узел, преобразовав метатег окна просмотра*</span><span class="sxs-lookup"><span data-stu-id="90c93-251">*The site after commenting the viewport meta tag*</span></span>
10. <span data-ttu-id="90c93-252">В Visual Studio нажмите клавишу **SHIFT** + **F5** остановить отладку приложения.</span><span class="sxs-lookup"><span data-stu-id="90c93-252">In Visual Studio, press **SHIFT** + **F5** to stop debugging the application.</span></span>
11. <span data-ttu-id="90c93-253">Раскомментируйте метатег окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="90c93-253">Uncomment the viewport meta tag.</span></span>


    [!code-cshtml[Main](whats-new-in-aspnet-mvc-4/samples/sample3.cshtml)]

<a id="Task_3_-_Using_Adaptive_Rendering"></a>
#### <a name="task-3---using-adaptive-rendering"></a><span data-ttu-id="90c93-254">Задача 3 - с помощью адаптивной отрисовки</span><span class="sxs-lookup"><span data-stu-id="90c93-254">Task 3 - Using Adaptive Rendering</span></span>

<span data-ttu-id="90c93-255">В этой задаче вы узнаете, как другой метод для отображения веб-страницы правильно на мобильных устройствах и веб-браузеров в то же время без настройки.</span><span class="sxs-lookup"><span data-stu-id="90c93-255">In this task, you will learn another method to render a Web page correctly on mobile devices and Web browsers at the same time without any customization.</span></span> <span data-ttu-id="90c93-256">Вы уже использовали просмотра метатег с одинаковой цели.</span><span class="sxs-lookup"><span data-stu-id="90c93-256">You have already used Viewport meta tag with a similar purpose.</span></span> <span data-ttu-id="90c93-257">Теперь будет соответствовать другой мощный метод: *адаптивной отрисовки*.</span><span class="sxs-lookup"><span data-stu-id="90c93-257">Now you will meet another powerful method: *adaptive rendering*.</span></span>

<span data-ttu-id="90c93-258">Методика адаптивной отрисовки использует **медиа-запросами CSS3** настроить стиль, применяемый к странице.</span><span class="sxs-lookup"><span data-stu-id="90c93-258">Adaptive rendering is a technique that uses **CSS3 media queries** to customize the style applied to a page.</span></span> <span data-ttu-id="90c93-259">Медиа-запросами определить условия внутри таблицы стилей, группирование стилей CSS при определенном условии.</span><span class="sxs-lookup"><span data-stu-id="90c93-259">Media queries define conditions inside a style sheet, grouping CSS styles under a certain condition.</span></span> <span data-ttu-id="90c93-260">Только в том случае, если условие равно true, стиль применяется к объявленным объектов.</span><span class="sxs-lookup"><span data-stu-id="90c93-260">Only when the condition is true, the style is applied to the declared objects.</span></span>

<span data-ttu-id="90c93-261">Гибкие возможности, предоставляемые методика адаптивной отрисовки включает любые настройки для отображения сайта на разных устройствах.</span><span class="sxs-lookup"><span data-stu-id="90c93-261">The flexibility provided by the adaptive rendering technique enables any customization for displaying the site on different devices.</span></span> <span data-ttu-id="90c93-262">Можно определить столько стили, которые нужно на отдельную таблицу стилей без написания кода логики Выбор стиля.</span><span class="sxs-lookup"><span data-stu-id="90c93-262">You can define as many styles as you want on a single style sheet without writing logic code to choose the style.</span></span> <span data-ttu-id="90c93-263">Таким образом это очень аккуратно способ адаптации стили страницы, как он позволяет сократить дублирование кода и логику для подготовки к просмотру целей.</span><span class="sxs-lookup"><span data-stu-id="90c93-263">Therefore, it is a very neat way of adapting page styles, as it reduces the amount of duplicated code and logic for rendering purposes.</span></span> <span data-ttu-id="90c93-264">С другой стороны использование полосы пропускания возрастет, как ненамного удается увеличить размер файлов CSS.</span><span class="sxs-lookup"><span data-stu-id="90c93-264">On the other hand, bandwidth consumption would increase, as the size of your CSS files could grow marginally.</span></span>

<span data-ttu-id="90c93-265">С помощью технологии адаптивной отрисовки, ваш сайт будет **отображаются правильно, независимо от браузера.**</span><span class="sxs-lookup"><span data-stu-id="90c93-265">By using the adaptive rendering technique, your site will be **displayed properly, regardless of the browser.**</span></span> <span data-ttu-id="90c93-266">Однако следует учитывать, если загрузка дополнительных пропускной способности является серьезной проблемой.</span><span class="sxs-lookup"><span data-stu-id="90c93-266">However, you should consider if the bandwidth extra load is a concern.</span></span>

> [!NOTE]
> <span data-ttu-id="90c93-267">Стандартный формат носителя запроса имеет: @media \[область: все | портативные | печати | проекции | экрана\] ([значение: свойство] и... [свойство: значение])</span><span class="sxs-lookup"><span data-stu-id="90c93-267">The basic format of a media query is: @media \[Scope: all | handheld | print | projection | screen\] ([property:value] and ... [property:value])</span></span>


<span data-ttu-id="90c93-268">Примеры запросов носителя: &gt;  **@media все и (максимальная ширина: 1000px) и (минимальной ширины: 700px) {}:** для всех разрешений между 700px и 1000px.</span><span class="sxs-lookup"><span data-stu-id="90c93-268">Examples of media queries: &gt;**@media all and (max-width: 1000px) and (min-width: 700px) {}:** For all the resolutions between 700px and 1000px.</span></span>

> <span data-ttu-id="90c93-269">**@mediaэкран и (минимальной ширины: 400 пикс) и (максимальная ширина: 700px) {...}:** только для экранов.</span><span class="sxs-lookup"><span data-stu-id="90c93-269">**@media screen and (min-width: 400px) and (max-width: 700px) { ... }:** Only for screens.</span></span> <span data-ttu-id="90c93-270">Разрешение должно быть в диапазоне от 400 до 700px.</span><span class="sxs-lookup"><span data-stu-id="90c93-270">The resolution must be between 400 and 700px.</span></span>
> 
> <span data-ttu-id="90c93-271">**@mediaпортативные и (минимальной ширины: 20em), экран и (минимальной ширины: 20em) {...}:** для карманных ПК (устройств и мобильных устройств) и экраны.</span><span class="sxs-lookup"><span data-stu-id="90c93-271">**@media handheld and (min-width: 20em), screen and (min-width: 20em) { ... }:** For handhelds(mobile and devices) and screens.</span></span> <span data-ttu-id="90c93-272">Минимальная ширина должна быть больше 20em.</span><span class="sxs-lookup"><span data-stu-id="90c93-272">The minimum width must be greater than 20em.</span></span>
> 
> <span data-ttu-id="90c93-273">Дополнительные сведения об этом можно найти на [сайт консорциума W3C](http://www.w3.org/TR/css3-mediaqueries/).</span><span class="sxs-lookup"><span data-stu-id="90c93-273">You can find more information about this on the [W3C site](http://www.w3.org/TR/css3-mediaqueries/).</span></span>


<span data-ttu-id="90c93-274">Теперь будет изучено, как работает адаптивной отрисовки, повышения удобочитаемости ASP.NET MVC 4 по умолчанию шаблона веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="90c93-274">You will now explore how the adaptive rendering works, improving the readability of the ASP.NET MVC 4 default website template.</span></span>

1. <span data-ttu-id="90c93-275">Откройте **PhotoGallery.sln** решений, созданных в задаче 1 и выберите **PhotoGallery** проекта.</span><span class="sxs-lookup"><span data-stu-id="90c93-275">Open the **PhotoGallery.sln** solution you have created at Task 1 and select the **PhotoGallery** project.</span></span> <span data-ttu-id="90c93-276">Нажмите клавишу **F5** для запуска решения.</span><span class="sxs-lookup"><span data-stu-id="90c93-276">Press **F5** to run the solution.</span></span>
2. <span data-ttu-id="90c93-277">Изменение ширины браузера, установка windows вдвое или меньше, чем четверти его исходный размер.</span><span class="sxs-lookup"><span data-stu-id="90c93-277">Resize the browser's width, setting the windows to half or to less than a quarter of its original size.</span></span> <span data-ttu-id="90c93-278">Обратите внимание, что происходит с элементами в заголовке: некоторые элементы не будут отображаться в видимой области заголовка.</span><span class="sxs-lookup"><span data-stu-id="90c93-278">Notice what happens with the items in the header: Some elements will not appear in the visible area of the header.</span></span>
3. <span data-ttu-id="90c93-279">Откройте **Site.css** файл из обозревателя решений Visual Studio, расположенный в **содержимого** папки проекта.</span><span class="sxs-lookup"><span data-stu-id="90c93-279">Open **Site.css** file from the Visual Studio Solution explorer, located in **Content** project folder.</span></span> <span data-ttu-id="90c93-280">Нажмите клавишу **сочетание клавиш CTRL + F** откройте Visual Studio интегрированный поиск и запись  **@media**  искомый **запрос носителя CSS**.</span><span class="sxs-lookup"><span data-stu-id="90c93-280">Press **CTRL + F** to open Visual Studio integrated search, and write **@media** to locate the **CSS media query**.</span></span>

    <span data-ttu-id="90c93-281">Условия запроса мультимедиа, определенные в этом шаблоне работает таким образом: если меньше размера окна браузера **850 px**, применены правила CSS, являются определены внутри этого блока носителя.</span><span class="sxs-lookup"><span data-stu-id="90c93-281">The media query condition defined in this template works in this way: When the browser's window size is below **850 px**, the CSS rules applied are the ones defined inside this media block.</span></span>

    <span data-ttu-id="90c93-282">![Выбрать запрос носителя](whats-new-in-aspnet-mvc-4/_static/image16.png "поиск запрос носителя")</span><span class="sxs-lookup"><span data-stu-id="90c93-282">![Locating the media query](whats-new-in-aspnet-mvc-4/_static/image16.png "Locating the media query")</span></span>

    <span data-ttu-id="90c93-283">*Поиск запросов мультимедиа*</span><span class="sxs-lookup"><span data-stu-id="90c93-283">*Locating the media query*</span></span>
4. <span data-ttu-id="90c93-284">Замените значение атрибута Максимальная ширина 850 px с **10px**, чтобы отключить адаптивной отрисовки и нажмите клавишу **сочетание клавиш CTRL + S** для сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="90c93-284">Replace the max-width attribute value set in 850 px with **10px**, in order to disable the adaptive rendering, and press **CTRL + S** to save the changes.</span></span> <span data-ttu-id="90c93-285">Вернуться к браузера и нажмите клавишу **сочетание клавиш CTRL + F5** обновления страницы с внесенные изменения.</span><span class="sxs-lookup"><span data-stu-id="90c93-285">Return to the browser and press **CTRL + F5** to refresh the page with the changes you have made.</span></span> <span data-ttu-id="90c93-286">Имеются различия в обе страницы при изменении ширины окна.</span><span class="sxs-lookup"><span data-stu-id="90c93-286">Notice the differences in both pages when adjusting the width of the window.</span></span>

    <span data-ttu-id="90c93-287">![В левой части страницы применяет @media задан стиль в правом стиль](whats-new-in-aspnet-mvc-4/_static/image17.png "применяет в левой части страницы @media задан стиль в правом стиль")</span><span class="sxs-lookup"><span data-stu-id="90c93-287">![In the left, the page is applying the @media style, in the right, the style is omitted](whats-new-in-aspnet-mvc-4/_static/image17.png "In the left, the page is applying the @media style, in the right, the style is omitted")</span></span>

    <span data-ttu-id="90c93-288">*В левой части страницы применяет @media стиля в правом стиль пропущен*</span><span class="sxs-lookup"><span data-stu-id="90c93-288">*In the left, the page is applying the @media style, in the right, the style is omitted*</span></span>

    <span data-ttu-id="90c93-289">Теперь проверим, что происходит на мобильных устройствах:</span><span class="sxs-lookup"><span data-stu-id="90c93-289">Now, let's check out what happens on mobile devices:</span></span>

    <span data-ttu-id="90c93-290">![В левой части страницы применяет @media задан стиль в правом стиль](whats-new-in-aspnet-mvc-4/_static/image18.png "применяет в левой части страницы @media задан стиль в правом стиль")</span><span class="sxs-lookup"><span data-stu-id="90c93-290">![In the left, the page is applying the @media style, in the right, the style is omitted](whats-new-in-aspnet-mvc-4/_static/image18.png "In the left, the page is applying the @media style, in the right, the style is omitted")</span></span>

    <span data-ttu-id="90c93-291">*В левой части страницы применяет @media стиля в правом стиль пропущен*</span><span class="sxs-lookup"><span data-stu-id="90c93-291">*In the left, the page is applying the @media style, in the right, the style is omitted*</span></span>

    <span data-ttu-id="90c93-292">Несмотря на то, что вы заметите, что изменения при отображении страницы в браузере не очень важно при использовании мобильного устройства различия становятся более очевидным.</span><span class="sxs-lookup"><span data-stu-id="90c93-292">Although you will notice that the changes when the page is rendered in a Web browser are not very significant, when using a mobile device the differences become more obvious.</span></span> <span data-ttu-id="90c93-293">В левой части изображения мы видим, что пользовательский стиль повысить читаемость.</span><span class="sxs-lookup"><span data-stu-id="90c93-293">On the left side of the image, we can see that the custom style improved the readability.</span></span>

    <span data-ttu-id="90c93-294">Во многих сценариях дополнительные, что упрощает применение условного стиля на веб-сайт и решить общие проблемы со стилями аккуратно подход можно использовать адаптивной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="90c93-294">Adaptive rendering can be used in many more scenarios, making it easier to apply conditional styling to a Web site and solving common style issues with a neat approach.</span></span>

    <span data-ttu-id="90c93-295">Метатег окна просмотра и медиа-запросами CSS не являются специфичными для ASP.NET MVC 4, можно воспользоваться преимуществами этих функций в любой веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="90c93-295">The Viewport meta tag and CSS media queries are not specific to ASP.NET MVC 4, so you can take advantage of these features in any web application.</span></span>
5. <span data-ttu-id="90c93-296">В Visual Studio нажмите клавишу **SHIFT** + **F5** остановить отладку приложения.</span><span class="sxs-lookup"><span data-stu-id="90c93-296">In Visual Studio, press **SHIFT** + **F5** to stop debugging the application.</span></span>

<a id="Exercise2"></a>

<a id="Exercise_2_Creating_the_Photo_Gallery_Web_Application"></a>
### <a name="exercise-2-creating-the-photo-gallery-web-application"></a><span data-ttu-id="90c93-297">Упражнение 2: Создание веб-приложения фотоальбом</span><span class="sxs-lookup"><span data-stu-id="90c93-297">Exercise 2: Creating the Photo Gallery Web Application</span></span>

<span data-ttu-id="90c93-298">В этом упражнении будет работать в приложении фотоальбома для отображения фотографий.</span><span class="sxs-lookup"><span data-stu-id="90c93-298">In this exercise, you will work on a Photo Gallery application to display photos.</span></span> <span data-ttu-id="90c93-299">Начните с шаблона проекта ASP.NET MVC 4, и затем нужно добавить компонент для получения фотографий из службы и отображать их на домашней странице.</span><span class="sxs-lookup"><span data-stu-id="90c93-299">You will start with the ASP.NET MVC 4 project template, and then you will add a feature to retrieve photos from a service and display them in the home page.</span></span>

<span data-ttu-id="90c93-300">В следующем упражнении обновит это решение для улучшения способ отображения на мобильных устройствах.</span><span class="sxs-lookup"><span data-stu-id="90c93-300">In the following exercise, you will update this solution to enhance the way it is displayed on mobile devices.</span></span>

<a id="Task_1_-_Creating_a_Mock_Photo_Service"></a>
#### <a name="task-1---creating-a-mock-photo-service"></a><span data-ttu-id="90c93-301">Задача 1. Создание службы макетов фото</span><span class="sxs-lookup"><span data-stu-id="90c93-301">Task 1 - Creating a Mock Photo Service</span></span>

<span data-ttu-id="90c93-302">В этой задаче вы создадите макетов фото службы для получения содержимого, которое будет отображаться в коллекции.</span><span class="sxs-lookup"><span data-stu-id="90c93-302">In this task, you will create a mock of the photo service to retrieve the content that will be displayed in the gallery.</span></span> <span data-ttu-id="90c93-303">Чтобы сделать это, будет добавлен новый контроллер, просто возвращает JSON-файла с данными каждой фотографии.</span><span class="sxs-lookup"><span data-stu-id="90c93-303">To do this, you will add a new controller that will simply return a JSON file with the data of each photo.</span></span>

1. <span data-ttu-id="90c93-304">Откройте **Visual Studio** Если еще не открыт.</span><span class="sxs-lookup"><span data-stu-id="90c93-304">Open **Visual Studio** if not already opened.</span></span>
2. <span data-ttu-id="90c93-305">Выберите **файл | Новые | Проект** команду меню.</span><span class="sxs-lookup"><span data-stu-id="90c93-305">Select the **File | New | Project** menu command.</span></span> <span data-ttu-id="90c93-306">В **новый проект** диалогового окна выберите **Visual C# | Web** шаблона на левой панели дерева, а затем выберите **веб-приложение ASP.NET MVC 4.**</span><span class="sxs-lookup"><span data-stu-id="90c93-306">In the **New Project** dialog, select the **Visual C# | Web** template on the left pane tree, and choose **ASP.NET MVC 4 Web Application.**</span></span> <span data-ttu-id="90c93-307">Назовите проект **PhotoGallery**, выберите расположение (или оставьте значение по умолчанию) и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="90c93-307">Name the project **PhotoGallery**, select a location (or leave the default) and click **OK**.</span></span> <span data-ttu-id="90c93-308">Кроме того, вы можете продолжать работать с вашей существующей ASP.NET MVC 4 **веб-приложение** решения от **упражнении 1** и пропустить следующий шаг.</span><span class="sxs-lookup"><span data-stu-id="90c93-308">Alternatively, you can continue working from your existing ASP.NET MVC 4 **Internet Application** solution from **Exercise 1** and skip the next step.</span></span>
3. <span data-ttu-id="90c93-309">В **нового проекта ASP.NET MVC 4** выберите **веб-приложение** шаблон проекта и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="90c93-309">In the **New ASP.NET MVC 4 Project** dialog box, select the **Internet Application** project template and click **OK**.</span></span> <span data-ttu-id="90c93-310">Убедитесь, что у вас выбран в качестве обработчика представлений Razor.</span><span class="sxs-lookup"><span data-stu-id="90c93-310">Make sure you have Razor selected as the View Engine.</span></span>
4. <span data-ttu-id="90c93-311">В **обозревателе решений**, щелкните правой кнопкой мыши **приложения\_данные** папку проекта и выберите **добавить | Существующий элемент**.</span><span class="sxs-lookup"><span data-stu-id="90c93-311">In the **Solution Explorer**, right-click the **App\_Data** folder of your project, and select **Add | Existing Item**.</span></span> <span data-ttu-id="90c93-312">Перейдите к **Source\Assets\App\_данные** папку части этой лаборатории и добавьте **Photos.json** файла.</span><span class="sxs-lookup"><span data-stu-id="90c93-312">Browse to the **Source\Assets\App\_Data** folder of this lab and add the **Photos.json** file.</span></span>
5. <span data-ttu-id="90c93-313">Создание нового контроллера с именем **PhotoController**.</span><span class="sxs-lookup"><span data-stu-id="90c93-313">Create a new controller with the name **PhotoController**.</span></span> <span data-ttu-id="90c93-314">Для этого щелкните правой кнопкой мыши **контроллеров** папки, перейдите на **добавить** и выберите **контроллера.**</span><span class="sxs-lookup"><span data-stu-id="90c93-314">To do this, right-click on the **Controllers** folder, go to **Add** and select **Controller.**</span></span> <span data-ttu-id="90c93-315">Полное имя контроллера, оставьте **контроллер MVC пустой** шаблона и нажмите кнопку **добавить**.</span><span class="sxs-lookup"><span data-stu-id="90c93-315">Complete the controller name, leave the **Empty MVC controller** template and click **Add**.</span></span>

    <span data-ttu-id="90c93-316">![Добавление PhotoController](whats-new-in-aspnet-mvc-4/_static/image19.png "Добавление PhotoController")</span><span class="sxs-lookup"><span data-stu-id="90c93-316">![Adding the PhotoController](whats-new-in-aspnet-mvc-4/_static/image19.png "Adding the PhotoController")</span></span>

    <span data-ttu-id="90c93-317">*Добавление PhotoController*</span><span class="sxs-lookup"><span data-stu-id="90c93-317">*Adding the PhotoController*</span></span>
6. <span data-ttu-id="90c93-318">Замените **индекс** метод со следующими **коллекции** действие и возвращают содержимое из файла JSON, вы недавно добавили в проект.</span><span class="sxs-lookup"><span data-stu-id="90c93-318">Replace the **Index** method with the following **Gallery** action, and return the content from the JSON file you have recently added to the project.</span></span>

    <span data-ttu-id="90c93-319">(Фрагмент - кода *действия коллекции ASP.NET MVC 4 лаборатории - Ex02 -*)</span><span class="sxs-lookup"><span data-stu-id="90c93-319">(Code Snippet - *ASP.NET MVC 4 Lab - Ex02 - Gallery Action*)</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample4.cs)]
7. <span data-ttu-id="90c93-320">Нажмите клавишу **F5** для запуска решения и перейдите в следующий URL-адрес для тестирования службы макеты фото: `http://localhost:[port]/photo/gallery` (значение [порт] зависит от текущего порта, где было запущено приложение).</span><span class="sxs-lookup"><span data-stu-id="90c93-320">Press **F5** to run the solution, and then browse to the following URL in order to test the mocked photo service: `http://localhost:[port]/photo/gallery` (the [port] value depends on the current port where the application was launched).</span></span> <span data-ttu-id="90c93-321">Этот URL-адрес запроса, должны извлекать содержимое **Photos.json** файла.</span><span class="sxs-lookup"><span data-stu-id="90c93-321">The request to this URL should retrieve the content of the **Photos.json** file.</span></span>

    <span data-ttu-id="90c93-322">![Тестирование службы макеты фото](whats-new-in-aspnet-mvc-4/_static/image20.png "тестирование службы макеты фото")</span><span class="sxs-lookup"><span data-stu-id="90c93-322">![Testing the mocked photo service](whats-new-in-aspnet-mvc-4/_static/image20.png "Testing the mocked photo service")</span></span>

    <span data-ttu-id="90c93-323">*Тестирование службы макеты фото*</span><span class="sxs-lookup"><span data-stu-id="90c93-323">*Testing the mocked photo service*</span></span>

<span data-ttu-id="90c93-324">В фактической реализации можно было использовать [веб-API ASP.NET](../../../../web-api/index.md) для реализации службы фотоальбома.</span><span class="sxs-lookup"><span data-stu-id="90c93-324">In a real implementation you could use [ASP.NET Web API](../../../../web-api/index.md) to implement the Photo Gallery service.</span></span> <span data-ttu-id="90c93-325">Веб-API ASP.NET — это платформа, которая позволяет легко создавать службы HTTP широкого диапазона клиентов, включая браузеры и мобильные устройства.</span><span class="sxs-lookup"><span data-stu-id="90c93-325">ASP.NET Web API is a framework that makes it easy to build HTTP services that reach a broad range of clients, including browsers and mobile devices.</span></span> <span data-ttu-id="90c93-326">ASP.NET Web API - это идеальная платформа для сборки REST-приложений на базе .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="90c93-326">ASP.NET Web API is an ideal platform for building RESTful applications on the .NET Framework.</span></span>

<a id="Task_2_-_Displaying_the_Photo_Gallery"></a>
#### <a name="task-2---displaying-the-photo-gallery"></a><span data-ttu-id="90c93-327">Задача 2 - отображение коллекции фотографий</span><span class="sxs-lookup"><span data-stu-id="90c93-327">Task 2 - Displaying the Photo Gallery</span></span>

<span data-ttu-id="90c93-328">В этой задаче будет обновлять домашнюю страницу, чтобы показать коллекции фотографий с помощью службы макеты, созданный в первой задаче этого упражнения.</span><span class="sxs-lookup"><span data-stu-id="90c93-328">In this task, you will update the Home page to show the photo gallery by using the mocked service you created in the first task of this exercise.</span></span> <span data-ttu-id="90c93-329">Добавим файлы модели и обновить представления коллекции.</span><span class="sxs-lookup"><span data-stu-id="90c93-329">You will add model files and update the gallery views.</span></span>

1. <span data-ttu-id="90c93-330">В Visual Studio нажмите клавишу **SHIFT** + **F5** остановить отладку приложения.</span><span class="sxs-lookup"><span data-stu-id="90c93-330">In Visual Studio, press **SHIFT** + **F5** to stop debugging the application.</span></span>
2. <span data-ttu-id="90c93-331">Создание **фото** класса в **моделей** папки.</span><span class="sxs-lookup"><span data-stu-id="90c93-331">Create the **Photo** class in the **Models** folder.</span></span> <span data-ttu-id="90c93-332">Для этого щелкните правой кнопкой мыши **моделей** выберите **добавить** и нажмите кнопку **класса**.</span><span class="sxs-lookup"><span data-stu-id="90c93-332">To do this, right-click on the **Models** folder, select **Add** and click **Class**.</span></span> <span data-ttu-id="90c93-333">Задайте имя **Photo.cs** и нажмите кнопку **добавить**.</span><span class="sxs-lookup"><span data-stu-id="90c93-333">Then, set the name to **Photo.cs** and click **Add**.</span></span>
3. <span data-ttu-id="90c93-334">Добавьте следующие члены для **фото** класса.</span><span class="sxs-lookup"><span data-stu-id="90c93-334">Add the following members to the **Photo** class.</span></span>

    <span data-ttu-id="90c93-335">(Фрагмент - кода *модели ASP.NET MVC 4 лаборатории - Ex02 - фотография*)</span><span class="sxs-lookup"><span data-stu-id="90c93-335">(Code Snippet - *ASP.NET MVC 4 Lab - Ex02 - Photo model*)</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample5.cs)]
4. <span data-ttu-id="90c93-336">Откройте **HomeController.cs** файл из **контроллеров** папки.</span><span class="sxs-lookup"><span data-stu-id="90c93-336">Open the **HomeController.cs** file from the **Controllers** folder.</span></span>
5. <span data-ttu-id="90c93-337">Добавьте следующие инструкции using.</span><span class="sxs-lookup"><span data-stu-id="90c93-337">Add the following using statements.</span></span>

    <span data-ttu-id="90c93-338">(Фрагмент - кода *HomeController директивы ASP.NET MVC 4 лаборатории - Ex02 -*)</span><span class="sxs-lookup"><span data-stu-id="90c93-338">(Code Snippet - *ASP.NET MVC 4 Lab - Ex02 - HomeController Usings*)</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample6.cs)]
6. <span data-ttu-id="90c93-339">Обновление **индекс** действие, чтобы использовать **HttpClient** для получения коллекции данных, а затем используйте **JavaScriptSerializer** десериализуемые модели представления.</span><span class="sxs-lookup"><span data-stu-id="90c93-339">Update the **Index** action to use **HttpClient** to retrieve the gallery data, and then use the **JavaScriptSerializer** to deserialize it to the view model.</span></span>

    <span data-ttu-id="90c93-340">(Фрагмент - кода *действие индекса ASP.NET MVC 4 лаборатории - Ex02 -*)</span><span class="sxs-lookup"><span data-stu-id="90c93-340">(Code Snippet - *ASP.NET MVC 4 Lab - Ex02 - Index Action*)</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample7.cs)]
7. <span data-ttu-id="90c93-341">Откройте **Index.cshtml** файла, расположенного в **Views\Home** папки и замените все содержимое следующим кодом.</span><span class="sxs-lookup"><span data-stu-id="90c93-341">Open the **Index.cshtml** file located under the **Views\Home** folder and replace all the content with the following code.</span></span>

    <span data-ttu-id="90c93-342">Этот код просматривает все фотографии, полученный из службы и отображает их в неупорядоченный список.</span><span class="sxs-lookup"><span data-stu-id="90c93-342">This code loops through all the photos retrieved from the service and displays them into an unordered list.</span></span>

    <span data-ttu-id="90c93-343">(Фрагмент - кода *список фото ASP.NET MVC 4 лаборатории - Ex02 -*)</span><span class="sxs-lookup"><span data-stu-id="90c93-343">(Code Snippet - *ASP.NET MVC 4 Lab - Ex02 - Photo List*)</span></span>


    [!code-cshtml[Main](whats-new-in-aspnet-mvc-4/samples/sample8.cshtml)]
8. <span data-ttu-id="90c93-344">В **обозревателе решений**, щелкните правой кнопкой мыши **содержимого** папку проекта и выберите **добавить | Существующий элемент**.</span><span class="sxs-lookup"><span data-stu-id="90c93-344">In the **Solution Explorer**, right-click the **Content** folder of your project, and select **Add | Existing Item**.</span></span> <span data-ttu-id="90c93-345">Перейдите к **Source\Assets\Content** папку части этой лаборатории и добавьте **Site.css** файла.</span><span class="sxs-lookup"><span data-stu-id="90c93-345">Browse to the **Source\Assets\Content** folder of this lab and add the **Site.css** file.</span></span> <span data-ttu-id="90c93-346">Необходимо будет подтвердить его замену.</span><span class="sxs-lookup"><span data-stu-id="90c93-346">You will have to confirm its replacement.</span></span> <span data-ttu-id="90c93-347">Если у вас есть **Site.css** файл открыт, необходимо будет подтвердить также перезагрузить файл.</span><span class="sxs-lookup"><span data-stu-id="90c93-347">If you have the **Site.css** file open, you will have to confirm to reload the file also.</span></span>
9. <span data-ttu-id="90c93-348">Откройте проводник и скопировать всю **фотографии** папка размещена в **Source\Assets** папку части этой лаборатории в корневую папку проекта в обозревателе решений.</span><span class="sxs-lookup"><span data-stu-id="90c93-348">Open File Explorer and copy the entire **Photos** folder located under the **Source\Assets** folder of this lab to the root folder of your project in Solution Explorer.</span></span>
10. <span data-ttu-id="90c93-349">Запустите приложение.</span><span class="sxs-lookup"><span data-stu-id="90c93-349">Run the application.</span></span> <span data-ttu-id="90c93-350">Теперь вы увидите домашнюю страницу отображения фотографий в коллекции.</span><span class="sxs-lookup"><span data-stu-id="90c93-350">You should now see the home page displaying the photos in the gallery.</span></span>

    <span data-ttu-id="90c93-351">![Фотоальбом](whats-new-in-aspnet-mvc-4/_static/image21.png "фотоальбом")</span><span class="sxs-lookup"><span data-stu-id="90c93-351">![Photo Gallery](whats-new-in-aspnet-mvc-4/_static/image21.png "Photo Gallery")</span></span>

    <span data-ttu-id="90c93-352">*Фотоальбом*</span><span class="sxs-lookup"><span data-stu-id="90c93-352">*Photo Gallery*</span></span>
11. <span data-ttu-id="90c93-353">В Visual Studio нажмите клавишу **SHIFT** + **F5** остановить отладку приложения.</span><span class="sxs-lookup"><span data-stu-id="90c93-353">In Visual Studio, press **SHIFT** + **F5** to stop debugging the application.</span></span>

<a id="Exercise3"></a>

<a id="Exercise_3_Adding_support_for_mobile_devices"></a>
### <a name="exercise-3-adding-support-for-mobile-devices"></a><span data-ttu-id="90c93-354">Упражнение 3: Добавление поддержки для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="90c93-354">Exercise 3: Adding support for mobile devices</span></span>

<span data-ttu-id="90c93-355">Одно из ключевых обновлений в ASP.NET MVC 4 — поддержка разработки мобильных приложений.</span><span class="sxs-lookup"><span data-stu-id="90c93-355">One of the key updates in ASP.NET MVC 4 is the support for mobile development.</span></span> <span data-ttu-id="90c93-356">В этом упражнении вы исследуете новые возможности мобильных приложений ASP.NET MVC 4, расширяя Коллекция фотографий решения, созданный в предыдущем упражнении.</span><span class="sxs-lookup"><span data-stu-id="90c93-356">In this exercise, you will explore ASP.NET MVC 4 new features for mobile applications by extending the PhotoGallery solution you have created in the previous exercise.</span></span>

<a id="Task_1_-_Installing_jQuery_Mobile_in_an_ASPNET_MVC_4_Application"></a>
#### <a name="task-1---installing-jquery-mobile-in-an-aspnet-mvc-4-application"></a><span data-ttu-id="90c93-357">Задача 1. Установка jQuery Mobile, в приложении ASP.NET MVC 4</span><span class="sxs-lookup"><span data-stu-id="90c93-357">Task 1 - Installing jQuery Mobile in an ASP.NET MVC 4 Application</span></span>

1. <span data-ttu-id="90c93-358">Откройте **начать** решений, расположенный **источника/Ex3-MobileSupport/начало/** папки.</span><span class="sxs-lookup"><span data-stu-id="90c93-358">Open the **Begin** solution located at **Source/Ex3-MobileSupport/Begin/** folder.</span></span> <span data-ttu-id="90c93-359">В противном случае можно продолжить использование **окончания** решения получен путем выполнения в предыдущем упражнении.</span><span class="sxs-lookup"><span data-stu-id="90c93-359">Otherwise, you might continue using the **End** solution obtained by completing the previous exercise.</span></span>

    1. <span data-ttu-id="90c93-360">Если вы открыли указанных **начать** решение, необходимо будет загрузить несколько отсутствующих пакетов NuGet прежде чем продолжить.</span><span class="sxs-lookup"><span data-stu-id="90c93-360">If you opened the provided **Begin** solution, you will need to download some missing NuGet packages before continue.</span></span> <span data-ttu-id="90c93-361">Чтобы сделать это, нажмите кнопку **проекта** и выбрать пункт **управление пакетами NuGet**.</span><span class="sxs-lookup"><span data-stu-id="90c93-361">To do this, click the **Project** menu and select **Manage NuGet Packages**.</span></span>
    2. <span data-ttu-id="90c93-362">В **управление пакетами NuGet** диалоговое окно, нажмите кнопку **восстановить** чтобы скачивать отсутствующие пакеты.</span><span class="sxs-lookup"><span data-stu-id="90c93-362">In the **Manage NuGet Packages** dialog, click **Restore** in order to download missing packages.</span></span>
    3. <span data-ttu-id="90c93-363">Наконец, постройте решение, нажав кнопку **построения** | **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="90c93-363">Finally, build the solution by clicking **Build** | **Build Solution**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="90c93-364">Одним из преимуществ использования NuGet является у вас не указан для отправки всех библиотек в вашем проекте, уменьшив размер проекта.</span><span class="sxs-lookup"><span data-stu-id="90c93-364">One of the advantages of using NuGet is that you don't have to ship all the libraries in your project, reducing the project size.</span></span> <span data-ttu-id="90c93-365">С помощью NuGet Power Tools указав версий пакета в файле Packages.config можно для загрузки всех необходимых библиотек первый раз, при запуске проекта.</span><span class="sxs-lookup"><span data-stu-id="90c93-365">With NuGet Power Tools, by specifying the package versions in the Packages.config file, you will be able to download all the required libraries the first time you run the project.</span></span> <span data-ttu-id="90c93-366">Вот почему необходимо будет выполнить эти шаги после открытия существующего решения в этой лаборатории.</span><span class="sxs-lookup"><span data-stu-id="90c93-366">This is why you will have to run these steps after you open an existing solution from this lab.</span></span>
2. <span data-ttu-id="90c93-367">Откройте **консоль диспетчера пакетов** , щелкнув **средства** &gt; **диспетчер пакетов библиотеки** &gt; **диспетчера пакетов Консоль** пункт меню.</span><span class="sxs-lookup"><span data-stu-id="90c93-367">Open the **Package Manager Console** by clicking the **Tools** &gt; **Library Package Manager** &gt; **Package Manager Console** menu option.</span></span>

    <span data-ttu-id="90c93-368">![Открытие консоли диспетчера пакетов NuGet](whats-new-in-aspnet-mvc-4/_static/image22.png "Открытие консоли диспетчера пакетов NuGet")</span><span class="sxs-lookup"><span data-stu-id="90c93-368">![Opening the NuGet Package Manager Console](whats-new-in-aspnet-mvc-4/_static/image22.png "Opening the NuGet Package Manager Console")</span></span>

    <span data-ttu-id="90c93-369">*Открытие консоли диспетчера пакетов NuGet*</span><span class="sxs-lookup"><span data-stu-id="90c93-369">*Opening the NuGet Package Manager Console*</span></span>
3. <span data-ttu-id="90c93-370">В консоли диспетчера пакетов выполните следующую команду, чтобы установить **jQuery.Mobile.MVC** пакета.</span><span class="sxs-lookup"><span data-stu-id="90c93-370">In the Package Manager Console run the following command to install the **jQuery.Mobile.MVC** package.</span></span>

    <span data-ttu-id="90c93-371">jQuery Mobile — это библиотека открытым исходным кодом, для создания оптимизированных для сенсорных экранов веб-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="90c93-371">jQuery Mobile is an open source library for building touch-optimized web UI.</span></span> <span data-ttu-id="90c93-372">Пакет NuGet jQuery.Mobile.MVC включает вспомогательные методы для использования с приложением ASP.NET MVC 4 jQuery Mobile.</span><span class="sxs-lookup"><span data-stu-id="90c93-372">The jQuery.Mobile.MVC NuGet package includes helpers to use jQuery Mobile with an ASP.NET MVC 4 application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="90c93-373">Выполнив следующую команду, будут загружать библиотеки jQuery.Mobile.MVC из Nuget.</span><span class="sxs-lookup"><span data-stu-id="90c93-373">By running the following command, you will be downloading the jQuery.Mobile.MVC library from Nuget.</span></span>

    <span data-ttu-id="90c93-374">по полудню</span><span class="sxs-lookup"><span data-stu-id="90c93-374">PM</span></span>

    [!code-powershell[Main](whats-new-in-aspnet-mvc-4/samples/sample9.ps1)]

    <span data-ttu-id="90c93-375">Эта команда устанавливает jQuery Mobile и некоторые вспомогательные файлы, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="90c93-375">This command installs jQuery Mobile and some helper files, including the following:</span></span>

    - <span data-ttu-id="90c93-376">**Представления/Общие/\_Layout.Mobile.cshtml**: макет мобильное jQuery, оптимизированный для меньшего размера экрана.</span><span class="sxs-lookup"><span data-stu-id="90c93-376">**Views/Shared/\_Layout.Mobile.cshtml**: is a jQuery Mobile-based layout optimized for a smaller screen.</span></span> <span data-ttu-id="90c93-377">Если веб-сайт получает запрос от мобильных браузеров, он заменяет исходного макета (\_Layout.cshtml) на следующее.</span><span class="sxs-lookup"><span data-stu-id="90c93-377">When the website receives a request from a mobile browser, it will replace the original layout (\_Layout.cshtml) with this one.</span></span>
    - <span data-ttu-id="90c93-378">Переключатель вида компонента: состоит из **представления/Общие/\_ViewSwitcher.cshtml** частичного представления и **ViewSwitcherController.cs** контроллера.</span><span class="sxs-lookup"><span data-stu-id="90c93-378">A view-switcher component: consists of the **Views/Shared/\_ViewSwitcher.cshtml** partial view and the **ViewSwitcherController.cs** controller.</span></span> <span data-ttu-id="90c93-379">Этот компонент будет отображать ссылку на браузеры мобильных устройств, чтобы пользователь мог перейти к рабочему столу версии страницы.</span><span class="sxs-lookup"><span data-stu-id="90c93-379">This component will show a link on mobile browsers to enable users to switch to the desktop version of the page.</span></span>  
        <span data-ttu-id="90c93-380">![Проект фотоальбома с поддержка мобильных устройств](whats-new-in-aspnet-mvc-4/_static/image23.png "проект фотоальбома с поддержка мобильных устройств")</span><span class="sxs-lookup"><span data-stu-id="90c93-380">![Photo Gallery project with mobile support](whats-new-in-aspnet-mvc-4/_static/image23.png "Photo Gallery project with mobile support")</span></span>

        <span data-ttu-id="90c93-381">*Проект фотоальбома с поддержка мобильных устройств*</span><span class="sxs-lookup"><span data-stu-id="90c93-381">*Photo Gallery project with mobile support*</span></span>
4. <span data-ttu-id="90c93-382">Регистрация мобильных устройств пакеты.</span><span class="sxs-lookup"><span data-stu-id="90c93-382">Register the Mobile bundles.</span></span> <span data-ttu-id="90c93-383">Чтобы сделать это, откройте **Global.asax.cs** файл и добавьте следующую строку.</span><span class="sxs-lookup"><span data-stu-id="90c93-383">To do this, open the **Global.asax.cs** file and add the following line.</span></span>

    <span data-ttu-id="90c93-384">(Фрагмент - кода *ASP.NET MVC 4 лаборатории - Ex03 - регистрация мобильных устройств пакеты*)</span><span class="sxs-lookup"><span data-stu-id="90c93-384">(Code Snippet - *ASP.NET MVC 4 Lab - Ex03 - Register Mobile Bundles*)</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample10.cs)]
5. <span data-ttu-id="90c93-385">Запустите приложение с помощью рабочего стола веб-браузер.</span><span class="sxs-lookup"><span data-stu-id="90c93-385">Run the application using a desktop web browser.</span></span>
6. <span data-ttu-id="90c93-386">Откройте **эмуляторе Windows Phone 7** в **меню «Пуск» | Все программы | Windows Phone SDK 7.1 | Эмулятор Windows Phone.**</span><span class="sxs-lookup"><span data-stu-id="90c93-386">Open the **Windows Phone 7 Emulator,** located in **Start Menu | All Programs | Windows Phone SDK 7.1 | Windows Phone Emulator.**</span></span>
7. <span data-ttu-id="90c93-387">На начальном экране телефона откройте Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="90c93-387">In the phone start screen, open Internet Explorer.</span></span> <span data-ttu-id="90c93-388">Извлечь URL-адрес, где запуска приложения и перейдите к URL-адреса с помощью браузера телефона (например `http://localhost:[PortNumber]/`).</span><span class="sxs-lookup"><span data-stu-id="90c93-388">Check out the URL where the application started and browse to that URL with the phone browser (e.g. `http://localhost:[PortNumber]/`).</span></span>

    <span data-ttu-id="90c93-389">Обратите внимание, что приложение будет выглядеть в эмуляторе Windows Phone, как jQuery.Mobile.MVC создал новые ресурсы в проекте, которые показывают представления, оптимизированный для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="90c93-389">You will notice that your application will look different in the Windows Phone emulator, as the jQuery.Mobile.MVC has created new assets in your project that show views optimized for mobile devices.</span></span>

    <span data-ttu-id="90c93-390">Сообщение в верхней части телефона, обозначающие связи, переключается в представление рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="90c93-390">Notice the message at the top of the phone, showing the link that switches to the Desktop view.</span></span> <span data-ttu-id="90c93-391">Кроме того  **\_Layout.Mobile.cshtml** макет, который был создан пакет установки — включая структуру, в приложении.</span><span class="sxs-lookup"><span data-stu-id="90c93-391">Additionally, the **\_Layout.Mobile.cshtml** layout that was created by the package you have installed is including a different layout in the application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="90c93-392">На данный момент нет ссылки вернуться назад в представление для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="90c93-392">So far, there is no link to get back to mobile view.</span></span> <span data-ttu-id="90c93-393">Он включается в более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="90c93-393">It will be included in later versions.</span></span>

    <span data-ttu-id="90c93-394">![Представление коллекции фотографий на домашней странице для мобильных устройств](whats-new-in-aspnet-mvc-4/_static/image24.png "представление коллекции фотографий на домашней странице для мобильных устройств")</span><span class="sxs-lookup"><span data-stu-id="90c93-394">![Mobile view of the Photo Gallery Home page](whats-new-in-aspnet-mvc-4/_static/image24.png "Mobile view of the Photo Gallery Home page")</span></span>

    <span data-ttu-id="90c93-395">*Представление коллекции фотографий на домашней странице для мобильных устройств*</span><span class="sxs-lookup"><span data-stu-id="90c93-395">*Mobile view of the Photo Gallery Home page*</span></span>
8. <span data-ttu-id="90c93-396">В Visual Studio нажмите клавишу **SHIFT** + **F5** остановить отладку приложения.</span><span class="sxs-lookup"><span data-stu-id="90c93-396">In Visual Studio, press **SHIFT** + **F5** to stop debugging the application.</span></span>

<a id="Task_2_-_Creating_Mobile_Views"></a>
#### <a name="task-2---creating-mobile-views"></a><span data-ttu-id="90c93-397">Задача 2 - Создание мобильных представлений</span><span class="sxs-lookup"><span data-stu-id="90c93-397">Task 2 - Creating Mobile Views</span></span>

<span data-ttu-id="90c93-398">В этой задаче вы создадите мобильной версии индекс представления с содержимым, адаптированная для повышения appareance на мобильных устройствах.</span><span class="sxs-lookup"><span data-stu-id="90c93-398">In this task, you will create a mobile version of the index view with content adapted for better appareance in mobile devices.</span></span>

1. <span data-ttu-id="90c93-399">Копировать **Views\Home\Index.cshtml** просмотра и вставьте его для создания копии, переименовать новый файл в **Index.Mobile.cshtml**.</span><span class="sxs-lookup"><span data-stu-id="90c93-399">Copy the **Views\Home\Index.cshtml** view and paste it to create a copy, rename the new file to **Index.Mobile.cshtml**.</span></span>
2. <span data-ttu-id="90c93-400">Открытие нового созданного **Index.Mobile.cshtml** просмотра и замените существующий &lt;ul&gt; тег с этим кодом.</span><span class="sxs-lookup"><span data-stu-id="90c93-400">Open the new created **Index.Mobile.cshtml** view and replace the existing &lt;ul&gt; tag with this code.</span></span> <span data-ttu-id="90c93-401">Таким образом происходит обновление &lt;ul&gt; тег с заметками jQuery мобильных данных использование мобильных тем из jQuery.</span><span class="sxs-lookup"><span data-stu-id="90c93-401">By doing this, you will be updating the &lt;ul&gt; tag with jQuery Mobile data annotations to use the mobile themes from jQuery.</span></span>


    [!code-html[Main](whats-new-in-aspnet-mvc-4/samples/sample11.html)]

    > [!NOTE] 
    > 
    > <span data-ttu-id="90c93-402">Обратите внимание на указанные ниже моменты.</span><span class="sxs-lookup"><span data-stu-id="90c93-402">Notice that:</span></span>
    > 
    > - <span data-ttu-id="90c93-403">**Роли данных** атрибута **listview** будет отображаться в список с помощью стилей listview.</span><span class="sxs-lookup"><span data-stu-id="90c93-403">The **data-role** attribute set to **listview** will render the list using the listview styles.</span></span>
    > 
    > - <span data-ttu-id="90c93-404">**Вставки данных** атрибута равным true будет отображать список со скругленными углами и поля.</span><span class="sxs-lookup"><span data-stu-id="90c93-404">The **data-inset** attribute set to true will show the list with rounded border and margin.</span></span>
    > 
    > - <span data-ttu-id="90c93-405">**Фильтр данных** атрибута **true** создаст поле поиска.</span><span class="sxs-lookup"><span data-stu-id="90c93-405">The **data-filter** attribute set to **true** will generate a search box.</span></span>
    > 
    > <span data-ttu-id="90c93-406">Дополнительные сведения о соглашениях мобильных jQuery в документации для проекта: [ [http://jquerymobile.com/demos/1.1.1/](http://jquerymobile.com/demos/1.1.1/)](http://jquerymobile.com/demos/1.1.1/)</span><span class="sxs-lookup"><span data-stu-id="90c93-406">You can learn more about jQuery Mobile conventions in the project documentation: [[http://jquerymobile.com/demos/1.1.1/](http://jquerymobile.com/demos/1.1.1/)](http://jquerymobile.com/demos/1.1.1/)</span></span>
3. <span data-ttu-id="90c93-407">Нажмите клавишу **сочетание клавиш CTRL + S** для сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="90c93-407">Press **CTRL + S** to save the changes.</span></span>
4. <span data-ttu-id="90c93-408">Переключитесь в **эмулятор Windows Phone** и обновите узел.</span><span class="sxs-lookup"><span data-stu-id="90c93-408">Switch to the **Windows Phone Emulator** and refresh the site.</span></span> <span data-ttu-id="90c93-409">Обратите внимание, новый внешний вид списка коллекции, а также новое поле поиска, расположенных в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="90c93-409">Notice the new look and feel of the gallery list, as well as the new search box located on the top.</span></span> <span data-ttu-id="90c93-410">Введите слово в поле поиска (например, **Tulips**) для начала поиска в коллекции фотографий.</span><span class="sxs-lookup"><span data-stu-id="90c93-410">Then, type a word in the search box (for instance, **Tulips**) to start a search in the photo gallery.</span></span>

    <span data-ttu-id="90c93-411">![Коллекции, используя стиль listview с фильтрацией](whats-new-in-aspnet-mvc-4/_static/image25.png "коллекции, используя стиль listview с фильтрацией")</span><span class="sxs-lookup"><span data-stu-id="90c93-411">![Gallery using listview style with filtering](whats-new-in-aspnet-mvc-4/_static/image25.png "Gallery using listview style with filtering")</span></span>

    <span data-ttu-id="90c93-412">*Коллекции, используя стиль listview с фильтрацией*</span><span class="sxs-lookup"><span data-stu-id="90c93-412">*Gallery using listview style with filtering*</span></span>

    <span data-ttu-id="90c93-413">Итак, вы использовали рецепт Mobilizer представление для создания копии индекс представления с &quot;мобильных&quot; суффикс.</span><span class="sxs-lookup"><span data-stu-id="90c93-413">To summarize, you have used the View Mobilizer recipe to create a copy of the Index view with the &quot;mobile&quot; suffix.</span></span> <span data-ttu-id="90c93-414">Этот суффикс указывает ASP.NET MVC 4, что каждый запрос, созданный на мобильном устройстве будет использовать эту копию индекса.</span><span class="sxs-lookup"><span data-stu-id="90c93-414">This suffix indicates to ASP.NET MVC 4 that every request generated from a mobile device will use this copy of the index.</span></span> <span data-ttu-id="90c93-415">Кроме того были обновлены мобильной версии индекс представления, чтобы использовать jQuery Mobile для повышения сайта интерфейса на мобильных устройствах.</span><span class="sxs-lookup"><span data-stu-id="90c93-415">Additionally, you have updated the mobile version of the Index view to use jQuery Mobile for enhancing the site look and feel in mobile devices.</span></span>
5. <span data-ttu-id="90c93-416">Вернитесь в Visual Studio и откройте **Site.Mobile.css** в компоненте **содержимого** папки.</span><span class="sxs-lookup"><span data-stu-id="90c93-416">Go back to Visual Studio and open **Site.Mobile.css** located under the **Content** folder.</span></span>
6. <span data-ttu-id="90c93-417">Исправьте позиционирования Название фотографии, чтобы отобразить в правой части изображения.</span><span class="sxs-lookup"><span data-stu-id="90c93-417">Fix the positioning of the photo title to make it show at the right side of the image.</span></span> <span data-ttu-id="90c93-418">Чтобы сделать это, добавьте следующий код в **Site.Mobile.css** файла.</span><span class="sxs-lookup"><span data-stu-id="90c93-418">To do this, add the following code to the **Site.Mobile.css** file.</span></span>

    <span data-ttu-id="90c93-419">CSS</span><span class="sxs-lookup"><span data-stu-id="90c93-419">CSS</span></span>

    [!code-css[Main](whats-new-in-aspnet-mvc-4/samples/sample12.css)]
7. <span data-ttu-id="90c93-420">Нажмите клавишу **сочетание клавиш CTRL + S** для сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="90c93-420">Press **CTRL + S** to save the changes.</span></span>
8. <span data-ttu-id="90c93-421">Вернитесь в **эмулятор Windows Phone** и обновите узел.</span><span class="sxs-lookup"><span data-stu-id="90c93-421">Switch back to the **Windows Phone Emulator** and refresh the site.</span></span> <span data-ttu-id="90c93-422">Обратите внимание, что название фотографии теперь позиционируется.</span><span class="sxs-lookup"><span data-stu-id="90c93-422">Notice the photo title is properly positioned now.</span></span>

    <span data-ttu-id="90c93-423">![Заголовок располагается справа от изображения](whats-new-in-aspnet-mvc-4/_static/image26.png "заголовок располагается справа от изображения")</span><span class="sxs-lookup"><span data-stu-id="90c93-423">![Title positioned on the right side of the image](whats-new-in-aspnet-mvc-4/_static/image26.png "Title positioned on the right side of the image")</span></span>

    <span data-ttu-id="90c93-424">*Заголовок располагается справа от изображения*</span><span class="sxs-lookup"><span data-stu-id="90c93-424">*Title positioned on the right side of the image*</span></span>

<a id="Task_3_-_jQuery_Mobile_Themes"></a>
#### <a name="task-3---jquery-mobile-themes"></a><span data-ttu-id="90c93-425">Задача 3 - jQuery Mobile темы</span><span class="sxs-lookup"><span data-stu-id="90c93-425">Task 3 - jQuery Mobile Themes</span></span>

<span data-ttu-id="90c93-426">Каждый макет и мини-приложение в jQuery Mobile построена новую объектно ориентированного CSS платформу, делает возможным применение темы полные унифицированную визуального проектирования сайтов и приложений.</span><span class="sxs-lookup"><span data-stu-id="90c93-426">Every layout and widget in jQuery Mobile is designed around a new object-oriented CSS framework that makes it possible to apply a complete unified visual design theme to sites and applications.</span></span>

<span data-ttu-id="90c93-427">по умолчанию jQuery Mobile темы включает 5 образцов, которые получают буквы (a, b, c, d, e) краткий справочник.</span><span class="sxs-lookup"><span data-stu-id="90c93-427">jQuery Mobile's default Theme includes 5 swatches that are given letters (a, b, c, d, e) for quick reference.</span></span>

<span data-ttu-id="90c93-428">В этой задаче будет обновлена мобильных макет для использования другой темы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="90c93-428">In this task, you will update the mobile layout to use a different theme than the default.</span></span>

1. <span data-ttu-id="90c93-429">Переключитесь в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="90c93-429">Switch back to Visual Studio.</span></span>
2. <span data-ttu-id="90c93-430">Откройте  **\_Layout.Mobile.cshtml** файл, расположенный в **представления\общие**.</span><span class="sxs-lookup"><span data-stu-id="90c93-430">Open the **\_Layout.Mobile.cshtml** file located in **Views\Shared**.</span></span>
3. <span data-ttu-id="90c93-431">Найдите элемент div с равным роли данных &quot;страницы&quot; и обновить **данных темы** для &quot; **e**&quot;.</span><span class="sxs-lookup"><span data-stu-id="90c93-431">Find the div element with the data-role set to &quot;page&quot; and update the **data-theme** to &quot;**e**&quot;.</span></span>


    [!code-html[Main](whats-new-in-aspnet-mvc-4/samples/sample13.html)]
4. <span data-ttu-id="90c93-432">Нажмите клавишу **сочетание клавиш CTRL + S** для сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="90c93-432">Press **CTRL + S** to save the changes.</span></span>
5. <span data-ttu-id="90c93-433">Обновить список узлов в **эмулятор Windows Phone** и обратите внимание, новая схема цветов.</span><span class="sxs-lookup"><span data-stu-id="90c93-433">Refresh the site in the **Windows Phone Emulator** and notice the new colors scheme.</span></span>

    <span data-ttu-id="90c93-434">![Макет мобильных устройств с другой цветовой схемы](whats-new-in-aspnet-mvc-4/_static/image27.png "мобильных макет с другой цветовой схемы")</span><span class="sxs-lookup"><span data-stu-id="90c93-434">![Mobile layout with a different color scheme](whats-new-in-aspnet-mvc-4/_static/image27.png "Mobile layout with a different color scheme")</span></span>

    <span data-ttu-id="90c93-435">*Макет мобильных устройств с другой цветовой схемы*</span><span class="sxs-lookup"><span data-stu-id="90c93-435">*Mobile layout with a different color scheme*</span></span>

<a id="Task_4_-_Using_the_View-Switcher_Component_and_the_Browser_Overriding_Features"></a>
#### <a name="task-4---using-the-view-switcher-component-and-the-browser-overriding-features"></a><span data-ttu-id="90c93-436">Задача 4 - с помощью переключателя представление компонента и браузер переопределение функций</span><span class="sxs-lookup"><span data-stu-id="90c93-436">Task 4 - Using the View-Switcher Component and the Browser Overriding Features</span></span>

<span data-ttu-id="90c93-437">Соглашение для веб-страниц, оптимизированные для мобильных устройств — Добавление ссылки, текст которых стоит как представление рабочего стола или режиме весь сайт, который позволяет пользователям перейти рабочего стола версии страницы.</span><span class="sxs-lookup"><span data-stu-id="90c93-437">A convention for mobile-optimized web pages is to add a link whose text is something like Desktop view or Full site mode that lets users switch to a desktop version of the page.</span></span> <span data-ttu-id="90c93-438">В пакете jQuery.Mobile.MVC образец **-переключателя** компонента для этой цели используется в  **\_Layout.Mobile.cshtml** представления.</span><span class="sxs-lookup"><span data-stu-id="90c93-438">The jQuery.Mobile.MVC package includes a sample **view-switcher** component for this purpose used in the **\_Layout.Mobile.cshtml** view.</span></span>

<span data-ttu-id="90c93-439">![Ссылку, чтобы переключиться в представление рабочего стола](whats-new-in-aspnet-mvc-4/_static/image28.png "ссылку, чтобы переключиться в представление рабочего стола")</span><span class="sxs-lookup"><span data-stu-id="90c93-439">![Link to switch to Desktop View](whats-new-in-aspnet-mvc-4/_static/image28.png "Link to switch to Desktop View")</span></span>

<span data-ttu-id="90c93-440">*Ссылку для переключения в представление рабочего стола*</span><span class="sxs-lookup"><span data-stu-id="90c93-440">*Link to switch to Desktop View*</span></span>

<span data-ttu-id="90c93-441">Новая функция, называемая использует переключателя **переопределения браузера**.</span><span class="sxs-lookup"><span data-stu-id="90c93-441">The view switcher uses a new feature called **Browser Overriding**.</span></span> <span data-ttu-id="90c93-442">Эта функция позволяет приложению рассматривать запросы, как если бы они поступали от той, которую они фактически получены другой браузер (агент пользователя).</span><span class="sxs-lookup"><span data-stu-id="90c93-442">This feature lets your application treat requests as if they were coming from a different browser (user agent) than the one they are actually coming from.</span></span>

<span data-ttu-id="90c93-443">В этой задаче будет изучено пример реализации просмотреть переключатель добавления, jQuery.Mobile.MVC и новый браузер переопределение функции в ASP.NET MVC 4.</span><span class="sxs-lookup"><span data-stu-id="90c93-443">In this task, you will explore the sample implementation of a view-switcher added by jQuery.Mobile.MVC and the new browser overriding features in ASP.NET MVC 4.</span></span>

1. <span data-ttu-id="90c93-444">Переключитесь в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="90c93-444">Switch back to Visual Studio.</span></span>
2. <span data-ttu-id="90c93-445">Откройте  **\_Layout.Mobile.cshtml** представление, расположенную под **одну** папки и обратите внимание, адресуемый как частичное представление компонента представления переключателя.</span><span class="sxs-lookup"><span data-stu-id="90c93-445">Open the **\_Layout.Mobile.cshtml** view located under the **Views\Shared** folder and notice the view-switcher component being referenced as a partial view.</span></span>

    <span data-ttu-id="90c93-446">![Мобильные макета с помощью переключателя представление компонента](whats-new-in-aspnet-mvc-4/_static/image29.png "мобильных макета с помощью переключателя компонента")</span><span class="sxs-lookup"><span data-stu-id="90c93-446">![Mobile layout using View-Switcher component](whats-new-in-aspnet-mvc-4/_static/image29.png "Mobile layout using View-Switcher component")</span></span>

    <span data-ttu-id="90c93-447">*Мобильные макета с помощью переключателя компонента*</span><span class="sxs-lookup"><span data-stu-id="90c93-447">*Mobile layout using View-Switcher component*</span></span>
3. <span data-ttu-id="90c93-448">Откройте  **\_ViewSwitcher.cshtml** частичного представления.</span><span class="sxs-lookup"><span data-stu-id="90c93-448">Open the **\_ViewSwitcher.cshtml** partial view.</span></span>

    <span data-ttu-id="90c93-449">Частичное представление использует новый метод **ViewContext.HttpContext.GetOverriddenBrowser()** для определения источника веб-запроса и отображения соответствующую ссылку для переключения, либо для просмотра рабочего стола или мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="90c93-449">The partial view uses the new method **ViewContext.HttpContext.GetOverriddenBrowser()** to determine the origin of the web request and show the corresponding link to switch either to the Desktop or Mobile views.</span></span>

    <span data-ttu-id="90c93-450">**GetOverridenBrowser** возвращает **HttpBrowserCapabilitiesBase** экземпляра, соответствующего агента пользователя, заданных в настоящее время для запроса (фактические или переопределения).</span><span class="sxs-lookup"><span data-stu-id="90c93-450">The **GetOverridenBrowser** method returns an **HttpBrowserCapabilitiesBase** instance that corresponds to the user agent currently set for the request (actual or overridden).</span></span> <span data-ttu-id="90c93-451">Это значение можно использовать для получения свойств, таких как **IsMobileDevice**.</span><span class="sxs-lookup"><span data-stu-id="90c93-451">You can use this value to get properties such as **IsMobileDevice**.</span></span>

    <span data-ttu-id="90c93-452">![Частичное представление ViewSwitcher](whats-new-in-aspnet-mvc-4/_static/image30.png "ViewSwitcher частичного представления")</span><span class="sxs-lookup"><span data-stu-id="90c93-452">![ViewSwitcher partial view](whats-new-in-aspnet-mvc-4/_static/image30.png "ViewSwitcher partial view")</span></span>

    <span data-ttu-id="90c93-453">*Частичное представление ViewSwitcher*</span><span class="sxs-lookup"><span data-stu-id="90c93-453">*ViewSwitcher partial view*</span></span>
4. <span data-ttu-id="90c93-454">Откройте **ViewSwitcherController.cs** класс находится в **контроллеров** папки.</span><span class="sxs-lookup"><span data-stu-id="90c93-454">Open the **ViewSwitcherController.cs** class located in the **Controllers** folder.</span></span> <span data-ttu-id="90c93-455">Ознакомьтесь с этой SwitchView действие вызывается по ссылке в компоненте ViewSwitcher и обратите внимание, новые методы HttpContext.</span><span class="sxs-lookup"><span data-stu-id="90c93-455">Check out that SwitchView action is called by the link in the ViewSwitcher component, and notice the new HttpContext methods.</span></span>

    - <span data-ttu-id="90c93-456">**HttpContext.ClearOverridenBrowser()** метод удаляет все переопределенные агенты пользователя для текущего запроса.</span><span class="sxs-lookup"><span data-stu-id="90c93-456">The **HttpContext.ClearOverridenBrowser()** method removes any overridden user agent for the current request.</span></span>
    - <span data-ttu-id="90c93-457">**HttpContext.SetOverridenBrowser()** метод переопределяет значение агента пользователя запроса, с указанием указанного агента пользователя.</span><span class="sxs-lookup"><span data-stu-id="90c93-457">The **HttpContext.SetOverridenBrowser()** method overrides the request's actual user agent value using the specified user agent.</span></span>  
        <span data-ttu-id="90c93-458">![Контроллер ViewSwitcher](whats-new-in-aspnet-mvc-4/_static/image31.png "ViewSwitcher контроллера")</span><span class="sxs-lookup"><span data-stu-id="90c93-458">![ViewSwitcher Controller](whats-new-in-aspnet-mvc-4/_static/image31.png "ViewSwitcher Controller")</span></span>  
<span data-ttu-id="90c93-459">*ViewSwitcher контроллера*</span><span class="sxs-lookup"><span data-stu-id="90c93-459">*ViewSwitcher Controller*</span></span>

        <span data-ttu-id="90c93-460">Переопределение браузера является основной функцией ASP.NET MVC 4, который можно получить и даже если не установить пакет jQuery.Mobile.MVC.</span><span class="sxs-lookup"><span data-stu-id="90c93-460">Browser Overriding is a core feature of ASP.NET MVC 4, which is also available even if you do not install the jQuery.Mobile.MVC package.</span></span> <span data-ttu-id="90c93-461">Тем не менее эта функция влияет только на просмотр, макет и частичного представления, и он не влияет на функциональные возможности, которые зависят от объекта Request.Browser.</span><span class="sxs-lookup"><span data-stu-id="90c93-461">However, this feature affects only view, layout, and partial-view, and it does not affect any of the features that depend on the Request.Browser object.</span></span>

<a id="Task_5_-_Adding_the_View-Switcher_in_the_Desktop_View"></a>
#### <a name="task-5---adding-the-view-switcher-in-the-desktop-view"></a><span data-ttu-id="90c93-462">Задача 5 - Добавление переключателем представлений в представлении рабочего стола</span><span class="sxs-lookup"><span data-stu-id="90c93-462">Task 5 - Adding the View-Switcher in the Desktop View</span></span>

<span data-ttu-id="90c93-463">В этой задаче будет обновлена формата рабочего стола для включения переключателем представлений.</span><span class="sxs-lookup"><span data-stu-id="90c93-463">In this task, you will update the desktop layout to include the view-switcher.</span></span> <span data-ttu-id="90c93-464">Это позволит мобильных пользователей, чтобы вернуться в представление для мобильных устройств при просмотре представление рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="90c93-464">This will allow mobile users to go back to the mobile view when browsing the desktop view.</span></span>

1. <span data-ttu-id="90c93-465">Обновить список узлов в **эмулятор Windows Phone**.</span><span class="sxs-lookup"><span data-stu-id="90c93-465">Refresh the site in the **Windows Phone Emulator**.</span></span>
2. <span data-ttu-id="90c93-466">Щелкните **представление рабочего стола** ссылку в верхней части галереи.</span><span class="sxs-lookup"><span data-stu-id="90c93-466">Click on the **Desktop view** link at the top of the gallery.</span></span> <span data-ttu-id="90c93-467">Обратите внимание, что в представлении рабочего стола, чтобы разрешить вернуться к представлению мобильных устройств не-переключателя.</span><span class="sxs-lookup"><span data-stu-id="90c93-467">Notice there is no view-switcher in the desktop view to allow you return to the mobile view.</span></span>
3. <span data-ttu-id="90c93-468">Вернитесь в Visual Studio и откройте  **\_Layout.cshtml** представления.</span><span class="sxs-lookup"><span data-stu-id="90c93-468">Go back to Visual Studio and open the **\_Layout.cshtml** view.</span></span>
4. <span data-ttu-id="90c93-469">Найдите раздел входа и вставить вызов для подготовки к просмотру  **\_ViewSwitcher** частичного представления ниже  **\_LogOnPartial** частичного представления.</span><span class="sxs-lookup"><span data-stu-id="90c93-469">Find the login section and insert a call to render the **\_ViewSwitcher** partial view below the **\_LogOnPartial** partial view.</span></span> <span data-ttu-id="90c93-470">Затем нажмите клавишу **сочетание клавиш CTRL + S** для сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="90c93-470">Then, press **CTRL + S** to save the changes.</span></span>


    [!code-cshtml[Main](whats-new-in-aspnet-mvc-4/samples/sample14.cshtml)]
5. <span data-ttu-id="90c93-471">Нажмите клавишу **сочетание клавиш CTRL + S** для сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="90c93-471">Press **CTRL + S** to save the changes.</span></span>
6. <span data-ttu-id="90c93-472">Обновите страницу в эмуляторе Windows Phone и дважды щелкните на экране, чтобы увеличить масштаб.</span><span class="sxs-lookup"><span data-stu-id="90c93-472">Refresh the page in the Windows Phone Emulator and double-click the screen to zoom in.</span></span> <span data-ttu-id="90c93-473">Обратите внимание, что теперь на домашней странице отображаются **представление для мобильных устройств** ссылку, которая переходит от мобильных устройств для рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="90c93-473">Notice that the home page now shows the **Mobile view** link that switches from mobile to desktop view.</span></span>

    <span data-ttu-id="90c93-474">![Просмотр переключателя, отображаются в представлении рабочего стола](whats-new-in-aspnet-mvc-4/_static/image32.png "переключателя отображается в представлении рабочего стола")</span><span class="sxs-lookup"><span data-stu-id="90c93-474">![View Switcher rendered in desktop view](whats-new-in-aspnet-mvc-4/_static/image32.png "View Switcher rendered in desktop view")</span></span>

    <span data-ttu-id="90c93-475">*Просмотреть переключатель отображается в представлении рабочего стола*</span><span class="sxs-lookup"><span data-stu-id="90c93-475">*View Switcher rendered in desktop view*</span></span>
7. <span data-ttu-id="90c93-476">Снова перейдите в представление для мобильных устройств и перейдите к **о** страницы (http://localhost [порт] / Home/о).</span><span class="sxs-lookup"><span data-stu-id="90c93-476">Switch to the Mobile view again and browse to **About** page (http://localhost[port]/Home/About).</span></span> <span data-ttu-id="90c93-477">Обратите внимание, что, даже если еще не создан для представления About.Mobile.cshtml, о программе страницы с использованием мобильных макета (\_Layout.Mobile.cshtml).</span><span class="sxs-lookup"><span data-stu-id="90c93-477">Notice that, even if you haven't created an About.Mobile.cshtml view, the About page is displayed using the mobile layout (\_Layout.Mobile.cshtml).</span></span>

    <span data-ttu-id="90c93-478">![О странице](whats-new-in-aspnet-mvc-4/_static/image33.png "о странице")</span><span class="sxs-lookup"><span data-stu-id="90c93-478">![About page](whats-new-in-aspnet-mvc-4/_static/image33.png "About page")</span></span>

    <span data-ttu-id="90c93-479">*О странице*</span><span class="sxs-lookup"><span data-stu-id="90c93-479">*About page*</span></span>
8. <span data-ttu-id="90c93-480">Наконец откройте сайт в веб-браузер для настольных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="90c93-480">Finally, open the site in a desktop Web browser.</span></span> <span data-ttu-id="90c93-481">Обратите внимание, что ни один из предыдущих обновлений повлияла представление рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="90c93-481">Notice that none of the previous updates has affected the desktop view.</span></span>

    <span data-ttu-id="90c93-482">![Коллекция фотографий представление рабочего стола](whats-new-in-aspnet-mvc-4/_static/image34.png "представление рабочего стола Коллекция фотографий")</span><span class="sxs-lookup"><span data-stu-id="90c93-482">![PhotoGallery desktop view](whats-new-in-aspnet-mvc-4/_static/image34.png "PhotoGallery desktop view")</span></span>

    <span data-ttu-id="90c93-483">*Коллекция фотографий представление рабочего стола*</span><span class="sxs-lookup"><span data-stu-id="90c93-483">*PhotoGallery desktop view*</span></span>

<a id="Task_6_-_Creating_New_Display_Modes"></a>
#### <a name="task-6---creating-new-display-modes"></a><span data-ttu-id="90c93-484">Задача 6. Создание нового режимы отображения</span><span class="sxs-lookup"><span data-stu-id="90c93-484">Task 6 - Creating New Display Modes</span></span>

<span data-ttu-id="90c93-485">Новая функция режимов отображения для работы приложения выберите представления, в зависимости от браузера, создающего запрос.</span><span class="sxs-lookup"><span data-stu-id="90c93-485">The new display modes feature lets an application select views depending on the browser that is generating the request.</span></span> <span data-ttu-id="90c93-486">Например, если браузер на компьютере запросы на домашней странице, приложение возвращает **Views\Home\Index.cshtml** шаблона.</span><span class="sxs-lookup"><span data-stu-id="90c93-486">For example, if a desktop browser requests the Home page, the application will return the **Views\Home\Index.cshtml** template.</span></span> <span data-ttu-id="90c93-487">Затем, если мобильный браузер запрашивает домашнюю страницу, приложение возвращает **Views\Home\Index.mobile.cshtml** шаблона.</span><span class="sxs-lookup"><span data-stu-id="90c93-487">Then, if a mobile browser requests the Home page, the application will return the **Views\Home\Index.mobile.cshtml** template.</span></span>

<span data-ttu-id="90c93-488">В этой задаче вы создадите пользовательского макета для устройств iPhone и будет необходимо смоделировать запросы из устройства iPhone.</span><span class="sxs-lookup"><span data-stu-id="90c93-488">In this task, you will create a customized layout for iPhone devices, and you will have to simulate requests from iPhone devices.</span></span> <span data-ttu-id="90c93-489">Для этого можно использовать либо эмулятор или эмулятор iPhone (как [должен быть электрический Mobile симулятор](http://www.electricplum.com/)) или в браузере с надстройками, изменяющие агента пользователя.</span><span class="sxs-lookup"><span data-stu-id="90c93-489">To do this, you can use either an iPhone emulator/simulator (like [Electric Mobile Simulator](http://www.electricplum.com/)) or a browser with add-ons that modify the user agent.</span></span> <span data-ttu-id="90c93-490">Инструкции о том, как задать строку агента пользователя в обозревателе Safari для эмуляции iPhone см. в разделе [как предоставить Safari представьте это IE](http://www.davidalison.com/2008/05/how-to-let-safari-pretend-its-ie.html) в блоге Дэвида Alison.</span><span class="sxs-lookup"><span data-stu-id="90c93-490">For instructions on how to set the user agent string in an Safari browser to emulate an iPhone, see [How to let Safari pretend it's IE](http://www.davidalison.com/2008/05/how-to-let-safari-pretend-its-ie.html) in David Alison's blog.</span></span>

<span data-ttu-id="90c93-491">**Обратите внимание, что эта задача является необязательным, и можно перейти в лаборатории. без его выполнения.**</span><span class="sxs-lookup"><span data-stu-id="90c93-491">**Notice that this task is optional and you can continue throughout the lab without executing it.**</span></span>

1. <span data-ttu-id="90c93-492">В Visual Studio нажмите клавишу **SHIFT** + **F5** остановить отладку приложения.</span><span class="sxs-lookup"><span data-stu-id="90c93-492">In Visual Studio, press **SHIFT** + **F5** to stop debugging the application.</span></span>
2. <span data-ttu-id="90c93-493">Откройте **Global.asax.cs** и добавьте следующий код с помощью инструкции.</span><span class="sxs-lookup"><span data-stu-id="90c93-493">Open **Global.asax.cs** and add the following using statement.</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample15.cs)]
3. <span data-ttu-id="90c93-494">Добавьте следующий выделенный код в приложение\_Start-метод.</span><span class="sxs-lookup"><span data-stu-id="90c93-494">Add the following highlighted code into the Application\_Start method.</span></span>

    <span data-ttu-id="90c93-495">(Фрагмент - кода *ASP.NET MVC 4 лаборатории - Ex03 - iPhone DisplayMode*)</span><span class="sxs-lookup"><span data-stu-id="90c93-495">(Code Snippet - *ASP.NET MVC 4 Lab - Ex03 - iPhone DisplayMode*)</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample16.cs)]

    <span data-ttu-id="90c93-496">Вы зарегистрировали новый **DefaultDisplayMode с именем &quot;iPhone&quot;**, внутри статического **DisplayModeProvider.Instance.Modes** статического списка, который будет сопоставлена с каждого входящего запроса.</span><span class="sxs-lookup"><span data-stu-id="90c93-496">You have registered a new **DefaultDisplayMode named &quot;iPhone&quot;**, within the static **DisplayModeProvider.Instance.Modes** static list, that will be matched against each incoming request.</span></span> <span data-ttu-id="90c93-497">Если входящий запрос содержит строку &quot;iPhone&quot;, ASP.NET MVC поиск представлений, имя которого содержит &quot;iPhone&quot; суффикс.</span><span class="sxs-lookup"><span data-stu-id="90c93-497">If the incoming request contains the string &quot;iPhone&quot;, ASP.NET MVC will find the views whose name contain the &quot;iPhone&quot; suffix.</span></span> <span data-ttu-id="90c93-498">Параметр 0 указывает, как определенные новый режим; Например, данное представление является более точным определением, чем обычные &quot;.mobile&quot; правилом, которое сопоставляет запросы от мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="90c93-498">The 0 parameter indicates how specific is the new mode; for instance, this view is more specific than the general &quot;.mobile&quot; rule that matches requests from mobile devices.</span></span>

    <span data-ttu-id="90c93-499">После выполнения этого кода, если в браузере iPhone создает запрос, приложение будет использовать **представления\общие\\_Layout.iPhone.cshtml** макет, вы создадите в следующих шагах.</span><span class="sxs-lookup"><span data-stu-id="90c93-499">After this code runs, when an iPhone browser generates a request, your application will use the **Views\Shared\\_Layout.iPhone.cshtml** layout you will create in the next steps.</span></span>

    > [!NOTE]
    > <span data-ttu-id="90c93-500">Этот способ проверки запроса для iPhone был упрощен в целях демонстрации и может не работать должным образом для каждой строки агента пользователя iPhone (для тестирования пример — с учетом регистра).</span><span class="sxs-lookup"><span data-stu-id="90c93-500">This way of testing the request for iPhone has been simplified for demo purposes and might not work as expected for every iPhone user agent string (for example test is case sensitive).</span></span>
4. <span data-ttu-id="90c93-501">Создать копию  **\_Layout.Mobile.cshtml** файла в **представления\общие** папку и переименуйте копию для &quot;  **\_Layout.iPhone.csthml** &quot;.</span><span class="sxs-lookup"><span data-stu-id="90c93-501">Create a copy of the **\_Layout.Mobile.cshtml** file in the **Views\Shared** folder and rename the copy to &quot;**\_Layout.iPhone.csthml**&quot;.</span></span>
5. <span data-ttu-id="90c93-502">Откройте  **\_Layout.iPhone.csthml** создан на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="90c93-502">Open **\_Layout.iPhone.csthml** you created in the previous step.</span></span>
6. <span data-ttu-id="90c93-503">Найдите элемент div с атрибутом роли данных, равным **страницы** и измените **данных темы** атрибут &quot; **a**&quot;.</span><span class="sxs-lookup"><span data-stu-id="90c93-503">Find the div element with the data-role attribute set to **page** and change the **data-theme** attribute to &quot;**a**&quot;.</span></span>


    [!code-cshtml[Main](whats-new-in-aspnet-mvc-4/samples/sample17.cshtml)]

    <span data-ttu-id="90c93-504">Теперь имеется 3 макеты в приложении ASP.NET MVC 4:</span><span class="sxs-lookup"><span data-stu-id="90c93-504">Now you have 3 layouts in your ASP.NET MVC 4 application:</span></span>

    1. <span data-ttu-id="90c93-505">**\_Layout.cshtml**: макет по умолчанию, используемый для браузеров настольных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="90c93-505">**\_Layout.cshtml**: default layout used for desktop browsers.</span></span>
    2. <span data-ttu-id="90c93-506">**\_Layout.Mobile.cshtml**: макет по умолчанию, используемый для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="90c93-506">**\_Layout.mobile.cshtml**: default layout used for mobile devices.</span></span>
    3. <span data-ttu-id="90c93-507">**\_Layout.iPhone.cshtml**: определенного макета для устройств iPhone, с помощью другой цветовой схемы для различения \_Layout.mobile.cshtml.</span><span class="sxs-lookup"><span data-stu-id="90c93-507">**\_Layout.iPhone.cshtml**: specific layout for iPhone devices, using a different color scheme to differentiate from \_Layout.mobile.cshtml.</span></span>
7. <span data-ttu-id="90c93-508">Нажмите клавишу **F5** для запуска приложения и перейдите на сайт в **эмулятор Windows Phone**.</span><span class="sxs-lookup"><span data-stu-id="90c93-508">Press **F5** to run the application and browse the site in the **Windows Phone Emulator**.</span></span>
8. <span data-ttu-id="90c93-509">Откройте **iPhone симулятор** (см. [приложении C](#AppendixC) инструкции о том, как установить и настроить эмулятор iPhone) и перейти на сайт слишком.</span><span class="sxs-lookup"><span data-stu-id="90c93-509">Open an **iPhone simulator** (see [Appendix C](#AppendixC) for instructions on how to install and configure an iPhone simulator), and browse to the site too.</span></span> <span data-ttu-id="90c93-510">Обратите внимание, что каждый телефона использует указанный шаблон.</span><span class="sxs-lookup"><span data-stu-id="90c93-510">Notice that each phone is using the specific template.</span></span>

    ![Using-different-Views-For-Each-Mobile-device2](whats-new-in-aspnet-mvc-4/_static/image35.png)

    <span data-ttu-id="90c93-512">*С помощью различных представлений для каждого мобильного устройства*</span><span class="sxs-lookup"><span data-stu-id="90c93-512">*Using different views for each mobile device*</span></span>

<a id="Exercise4"></a>

<a id="Exercise_4_Using_Asynchronous_Controllers"></a>
### <a name="exercise-4-using-asynchronous-controllers"></a><span data-ttu-id="90c93-513">Упражнение 4: Использование асинхронных контроллеров</span><span class="sxs-lookup"><span data-stu-id="90c93-513">Exercise 4: Using Asynchronous Controllers</span></span>

<span data-ttu-id="90c93-514">Microsoft .NET Framework 4.5 предоставляет новые возможности языка C# и Visual Basic для предоставления новой платформы для асинхронности в программировании .NET.</span><span class="sxs-lookup"><span data-stu-id="90c93-514">Microsoft .NET Framework 4.5 introduces new language features in C# and Visual Basic to provide a new foundation for asynchrony in .NET programming.</span></span> <span data-ttu-id="90c93-515">Этот новый foundation делает асинхронное программирование аналогично - и примерно так же просто, как и - синхронное.</span><span class="sxs-lookup"><span data-stu-id="90c93-515">This new foundation makes asynchronous programming similar to - and about as straightforward as - synchronous programming.</span></span> <span data-ttu-id="90c93-516">Теперь имеется возможность написать асинхронные методы действия в ASP.NET MVC 4 с помощью **AsyncController и контроллеры** класса.</span><span class="sxs-lookup"><span data-stu-id="90c93-516">You are now able to write asynchronous action methods in ASP.NET MVC 4 by using the **AsyncController** class.</span></span> <span data-ttu-id="90c93-517">Асинхронные методы действия можно использовать для долго выполняющихся, не связаны с ЦП запросов.</span><span class="sxs-lookup"><span data-stu-id="90c93-517">You can use asynchronous action methods for long-running, non-CPU bound requests.</span></span> <span data-ttu-id="90c93-518">Это предотвращает блокировку веб-сервера от выполнения операций во время обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="90c93-518">This avoids blocking the Web server from performing work while the request is being processed.</span></span> <span data-ttu-id="90c93-519">AsyncController и контроллеры класс обычно используется для длительных вызовы веб-службы.</span><span class="sxs-lookup"><span data-stu-id="90c93-519">The AsyncController class is typically used for long-running Web service calls.</span></span>

<span data-ttu-id="90c93-520">В этом упражнении объясняет основы асинхронных операций в ASP.NET MVC 4.</span><span class="sxs-lookup"><span data-stu-id="90c93-520">This exercise explains the basics of asynchronous operation in ASP.NET MVC 4.</span></span> <span data-ttu-id="90c93-521">Если вы хотите подробно, можно извлечь следующую статью: [ [https://msdn.microsoft.com/en-us/library/ee728598%28v=vs.100%29.aspx](https://msdn.microsoft.com/en-us/library/ee728598%28v=vs.100%29.aspx)](https://msdn.microsoft.com/en-us/library/ee728598%28v=vs.100%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90c93-521">If you want a deeper dive, you can check out the following article: [[https://msdn.microsoft.com/en-us/library/ee728598%28v=vs.100%29.aspx](https://msdn.microsoft.com/en-us/library/ee728598%28v=vs.100%29.aspx)](https://msdn.microsoft.com/en-us/library/ee728598%28v=vs.100%29.aspx)</span></span>

<a id="Task_1_-_Implementing_an_Asynchronous_Controller"></a>
#### <a name="task-1---implementing-an-asynchronous-controller"></a><span data-ttu-id="90c93-522">Задача 1 - реализации асинхронного контроллера</span><span class="sxs-lookup"><span data-stu-id="90c93-522">Task 1 - Implementing an Asynchronous Controller</span></span>

1. <span data-ttu-id="90c93-523">Откройте **начать** решений, расположенный **источника/Ex4-Async иBegin/** папки.</span><span class="sxs-lookup"><span data-stu-id="90c93-523">Open the **Begin** solution located at **Source/Ex4-Async/Begin/** folder.</span></span> <span data-ttu-id="90c93-524">В противном случае можно продолжить использование **окончания** решения получен путем выполнения в предыдущем упражнении.</span><span class="sxs-lookup"><span data-stu-id="90c93-524">Otherwise, you might continue using the **End** solution obtained by completing the previous exercise.</span></span>

    1. <span data-ttu-id="90c93-525">Если вы открыли указанных **начать** решение, необходимо будет загрузить несколько отсутствующих пакетов NuGet прежде чем продолжить.</span><span class="sxs-lookup"><span data-stu-id="90c93-525">If you opened the provided **Begin** solution, you will need to download some missing NuGet packages before continue.</span></span> <span data-ttu-id="90c93-526">Чтобы сделать это, нажмите кнопку **проекта** и выбрать пункт **управление пакетами NuGet**.</span><span class="sxs-lookup"><span data-stu-id="90c93-526">To do this, click the **Project** menu and select **Manage NuGet Packages**.</span></span>
    2. <span data-ttu-id="90c93-527">В **управление пакетами NuGet** диалоговое окно, нажмите кнопку **восстановить** чтобы скачивать отсутствующие пакеты.</span><span class="sxs-lookup"><span data-stu-id="90c93-527">In the **Manage NuGet Packages** dialog, click **Restore** in order to download missing packages.</span></span>
    3. <span data-ttu-id="90c93-528">Наконец, постройте решение, нажав кнопку **построения** | **построить решение**.</span><span class="sxs-lookup"><span data-stu-id="90c93-528">Finally, build the solution by clicking **Build** | **Build Solution**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="90c93-529">Одним из преимуществ использования NuGet является у вас не указан для отправки всех библиотек в вашем проекте, уменьшив размер проекта.</span><span class="sxs-lookup"><span data-stu-id="90c93-529">One of the advantages of using NuGet is that you don't have to ship all the libraries in your project, reducing the project size.</span></span> <span data-ttu-id="90c93-530">С помощью NuGet Power Tools указав версий пакета в файле Packages.config можно для загрузки всех необходимых библиотек первый раз, при запуске проекта.</span><span class="sxs-lookup"><span data-stu-id="90c93-530">With NuGet Power Tools, by specifying the package versions in the Packages.config file, you will be able to download all the required libraries the first time you run the project.</span></span> <span data-ttu-id="90c93-531">Вот почему необходимо будет выполнить эти шаги после открытия существующего решения в этой лаборатории.</span><span class="sxs-lookup"><span data-stu-id="90c93-531">This is why you will have to run these steps after you open an existing solution from this lab.</span></span>
2. <span data-ttu-id="90c93-532">Откройте **HomeController.cs** класса из **контроллеров** папки.</span><span class="sxs-lookup"><span data-stu-id="90c93-532">Open the **HomeController.cs** class from the **Controllers** folder.</span></span>
3. <span data-ttu-id="90c93-533">Добавьте следующий код с помощью инструкции.</span><span class="sxs-lookup"><span data-stu-id="90c93-533">Add the following using statement.</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample18.cs)]
4. <span data-ttu-id="90c93-534">Обновление **HomeController** наследование от класса **AsyncController и контроллеры**.</span><span class="sxs-lookup"><span data-stu-id="90c93-534">Update the **HomeController** class to inherit from **AsyncController**.</span></span> <span data-ttu-id="90c93-535">Контроллеры, которые являются производными от AsyncController и контроллеры позволяют ASP.NET выполнять обработку асинхронных запросов, и они могут обслуживать синхронные методы действия.</span><span class="sxs-lookup"><span data-stu-id="90c93-535">Controllers that derive from AsyncController enable ASP.NET to process asynchronous requests, and they can still service synchronous action methods.</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample19.cs)]
5. <span data-ttu-id="90c93-536">Добавить **async** ключевое слово **индекс** метод и сделать его возвращаемый тип **задачи&lt;ActionResult&gt;**.</span><span class="sxs-lookup"><span data-stu-id="90c93-536">Add the **async** keyword to the **Index** method and make it return the type **Task&lt;ActionResult&gt;**.</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample20.cs)]

    > [!NOTE]
    > <span data-ttu-id="90c93-537">**Async** ключевое слово является одним из .NET Framework 4.5 предоставляет новые ключевые слова; он сообщает компилятору, что этот метод содержит асинхронного кода.</span><span class="sxs-lookup"><span data-stu-id="90c93-537">The **async** keyword is one of the new keywords the .NET Framework 4.5 provides; it tells the compiler that this method contains asynchronous code.</span></span> <span data-ttu-id="90c93-538">Объект **задачи** представляет асинхронную операцию, которая может выполняться в некоторый момент в будущем.</span><span class="sxs-lookup"><span data-stu-id="90c93-538">A **Task** object represents an asynchronous operation that may complete at some point in the future.</span></span>
6. <span data-ttu-id="90c93-539">Замените **клиента. GetAsync()** вызов с полной async версии с помощью await ключевое слово, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="90c93-539">Replace the **client.GetAsync()** call with the full async version using await keyword as shown below.</span></span>

    <span data-ttu-id="90c93-540">(Фрагмент - кода *GetAsync ASP.NET MVC 4 лаборатории - Ex04 -*)</span><span class="sxs-lookup"><span data-stu-id="90c93-540">(Code Snippet - *ASP.NET MVC 4 Lab - Ex04 - GetAsync*)</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample21.cs)]

    > [!NOTE]
    > <span data-ttu-id="90c93-541">В предыдущей версии, вы использовали **результат** свойство из **задачи** объекта, чтобы блокировать поток до возврата результата (версия sync).</span><span class="sxs-lookup"><span data-stu-id="90c93-541">In the previous version, you were using the **Result** property from the **Task** object to block the thread until the result is returned (sync version).</span></span>
    > 
    > <span data-ttu-id="90c93-542">Добавление **await** ключевое слово сообщает компилятору, чтобы асинхронно ожидать задачи, возвращаемой из вызова метода.</span><span class="sxs-lookup"><span data-stu-id="90c93-542">Adding the **await** keyword tells the compiler to asynchronously wait for the task returned from the method call.</span></span> <span data-ttu-id="90c93-543">Это означает, что остальной части кода выполняется как обратный вызов только после завершения ожидающей метод.</span><span class="sxs-lookup"><span data-stu-id="90c93-543">This means that the rest of the code will be executed as a callback only after the awaited method completes.</span></span> <span data-ttu-id="90c93-544">Другой обстоятельством является не необходимо изменить в блок try-catch, чтобы обеспечить работоспособность: исключения, которые происходят в фоновом режиме или на переднем плане по-прежнему будет перехвачено без дополнительных действий с помощью обработчика, предоставляемых платформой.</span><span class="sxs-lookup"><span data-stu-id="90c93-544">Another thing to notice is that you do not need to change your try-catch block in order to make this work: the exceptions that happen in background or in foreground will still be caught without any extra work using a handler provided by the framework.</span></span>
7. <span data-ttu-id="90c93-545">Изменить код, чтобы продолжить асинхронную реализацию путем замены строки с новым кодом, как показано ниже</span><span class="sxs-lookup"><span data-stu-id="90c93-545">Change the code to continue with the asynchronous implementation by replacing the lines with the new code as shown below</span></span>

    <span data-ttu-id="90c93-546">(Фрагмент - кода *ReadAsStringAsync ASP.NET MVC 4 лаборатории - Ex04 -*)</span><span class="sxs-lookup"><span data-stu-id="90c93-546">(Code Snippet - *ASP.NET MVC 4 Lab - Ex04 - ReadAsStringAsync*)</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample22.cs)]
8. <span data-ttu-id="90c93-547">Запустите приложение.</span><span class="sxs-lookup"><span data-stu-id="90c93-547">Run the application.</span></span> <span data-ttu-id="90c93-548">Можно заметить существенных изменений, но код не будет блокировать поток из пула потоков, делая лучше использования ресурсов сервера и повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="90c93-548">You will notice no major changes, but your code will not block a thread from the thread pool making a better usage of the server resources and improving performance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="90c93-549">Дополнительные сведения о новых асинхронных средств программирования в лаборатории &quot; **асинхронное программирование в .NET 4.5 с C# и Visual Basic** &quot; включены в пакет средств Visual Studio обучения.</span><span class="sxs-lookup"><span data-stu-id="90c93-549">You can learn more about the new asynchronous programming features in the lab &quot;**Asynchronous Programming in .NET 4.5 with C# and Visual Basic**&quot; included in the Visual Studio Training Kit.</span></span>

<a id="Task_2_-_Handling_Time-Outs_with_Cancellation_Tokens"></a>
#### <a name="task-2---handling-time-outs-with-cancellation-tokens"></a><span data-ttu-id="90c93-550">Задача 2 - обработка времени ожидания, токены отмены</span><span class="sxs-lookup"><span data-stu-id="90c93-550">Task 2 - Handling Time-Outs with Cancellation Tokens</span></span>

<span data-ttu-id="90c93-551">Асинхронные методы действия, возвращающих экземпляры задач также могут поддерживать истечение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="90c93-551">Asynchronous action methods that return Task instances can also support time-outs.</span></span> <span data-ttu-id="90c93-552">В этой задаче будет обновлять код метода индекс для обработки времени ожидания сценария, с помощью токена отмены.</span><span class="sxs-lookup"><span data-stu-id="90c93-552">In this task, you will update the Index method code to handle a time-out scenario using a cancellation token.</span></span>

1. <span data-ttu-id="90c93-553">Вернитесь в Visual Studio и нажмите клавишу **SHIFT + F5** остановить отладку.</span><span class="sxs-lookup"><span data-stu-id="90c93-553">Go back to Visual Studio and press **SHIFT + F5** to stop debugging.</span></span>
2. <span data-ttu-id="90c93-554">Добавьте следующий оператор using **HomeController.cs** файла.</span><span class="sxs-lookup"><span data-stu-id="90c93-554">Add the following using statement to the **HomeController.cs** file.</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample23.cs)]
3. <span data-ttu-id="90c93-555">Обновление действия индекса для получения **CancellationToken** аргумент.</span><span class="sxs-lookup"><span data-stu-id="90c93-555">Update the Index action to receive a **CancellationToken** argument.</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample24.cs)]
4. <span data-ttu-id="90c93-556">Обновление **GetAsync** вызов передать токен отмены.</span><span class="sxs-lookup"><span data-stu-id="90c93-556">Update the **GetAsync** call to pass the cancellation token.</span></span>

    <span data-ttu-id="90c93-557">(Фрагмент - кода *SendAsync - Ex04 - лаборатории ASP.NET MVC 4 с CancellationToken*)</span><span class="sxs-lookup"><span data-stu-id="90c93-557">(Code Snippet - *ASP.NET MVC 4 Lab - Ex04 - SendAsync with CancellationToken*)</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample25.cs)]
5. <span data-ttu-id="90c93-558">Украшение *индекс* метод с **AsyncTimeout** атрибуту присвоено значение 500 миллисекунд и **HandleError** настроен для обработки атрибута  **TaskCanceledException** путем перенаправления **TimedOut** представления.</span><span class="sxs-lookup"><span data-stu-id="90c93-558">Decorate the *Index* method with an **AsyncTimeout** attribute set to 500 milliseconds and a **HandleError** attribute configured to handle **TaskCanceledException** by redirecting to a **TimedOut** view.</span></span>

    <span data-ttu-id="90c93-559">(Фрагмент - кода *атрибуты ASP.NET MVC 4 лаборатории - Ex04 -*)</span><span class="sxs-lookup"><span data-stu-id="90c93-559">(Code Snippet - *ASP.NET MVC 4 Lab - Ex04 - Attributes*)</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample26.cs)]
6. <span data-ttu-id="90c93-560">Откройте **PhotoController** класс и обновление **коллекции** метод задержки в миллисекундах выполнения 1000 (1 секунда), для имитации длительной задачи.</span><span class="sxs-lookup"><span data-stu-id="90c93-560">Open the **PhotoController** class and update the **Gallery** method to delay the execution 1000 miliseconds (1 second) to simulate a long running task.</span></span>


    [!code-csharp[Main](whats-new-in-aspnet-mvc-4/samples/sample27.cs)]
7. <span data-ttu-id="90c93-561">Откройте **Web.config** файл и включите настраиваемых ошибок, добавив следующий элемент.</span><span class="sxs-lookup"><span data-stu-id="90c93-561">Open the **Web.config** file and enable custom errors by adding the following element.</span></span>


    [!code-xml[Main](whats-new-in-aspnet-mvc-4/samples/sample28.xml)]
8. <span data-ttu-id="90c93-562">Создание нового представления в **представления\общие** с именем **TimedOut** и использовать макет по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="90c93-562">Create a new view in **Views\Shared** named **TimedOut** and use the default layout.</span></span> <span data-ttu-id="90c93-563">В обозревателе решений щелкните правой кнопкой мыши **представления\общие** папку и выберите **добавить | Представление**.</span><span class="sxs-lookup"><span data-stu-id="90c93-563">In the Solution Explorer, right-click the **Views\Shared** folder and select **Add | View**.</span></span>

    <span data-ttu-id="90c93-564">![С помощью различных представлений для каждого мобильного устройства](whats-new-in-aspnet-mvc-4/_static/image36.png "с помощью различных представлений для каждого мобильного устройства")</span><span class="sxs-lookup"><span data-stu-id="90c93-564">![Using different views for each mobile device](whats-new-in-aspnet-mvc-4/_static/image36.png "Using different views for each mobile device")</span></span>

    <span data-ttu-id="90c93-565">*С помощью различных представлений для каждого мобильного устройства*</span><span class="sxs-lookup"><span data-stu-id="90c93-565">*Using different views for each mobile device*</span></span>
9. <span data-ttu-id="90c93-566">Обновление **TimedOut** просматривать содержимое, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="90c93-566">Update the **TimedOut** view content as shown below.</span></span>


    [!code-cshtml[Main](whats-new-in-aspnet-mvc-4/samples/sample29.cshtml)]
10. <span data-ttu-id="90c93-567">Запустите приложение и перейдите в корневой URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="90c93-567">Run the application and navigate to the root URL.</span></span> <span data-ttu-id="90c93-568">Как вы добавили **Thread.Sleep** 1000 миллисекунд, возникнет ошибка времени ожидания, созданные **AsyncTimeout** атрибута и catch **HandleError** атрибут.</span><span class="sxs-lookup"><span data-stu-id="90c93-568">As you have added a **Thread.Sleep** of 1000 milliseconds, you will get a time-out error, generated by the **AsyncTimeout** attribute and catch by the **HandleError** attribute.</span></span>

    <span data-ttu-id="90c93-569">![Исключение обрабатывается](whats-new-in-aspnet-mvc-4/_static/image37.png "исключение обрабатывается")</span><span class="sxs-lookup"><span data-stu-id="90c93-569">![Time-out exception handled](whats-new-in-aspnet-mvc-4/_static/image37.png "Time-out exception handled")</span></span>

    <span data-ttu-id="90c93-570">*Исключение обрабатывается*</span><span class="sxs-lookup"><span data-stu-id="90c93-570">*Time-out exception handled*</span></span>

> [!NOTE]
> <span data-ttu-id="90c93-571">Кроме того, можно развернуть это приложение на веб-сайтов Windows Azure ниже [приложение D: публикации приложения ASP.NET MVC 4 с помощью веб-развертывания](#AppendixD).</span><span class="sxs-lookup"><span data-stu-id="90c93-571">Additionally, you can deploy this application to Windows Azure Web Sites following [Appendix D: Publishing an ASP.NET MVC 4 Application using Web Deploy](#AppendixD).</span></span>


<a id="Summary"></a>

<a id="Summary"></a>
## <a name="summary"></a><span data-ttu-id="90c93-572">Сводка</span><span class="sxs-lookup"><span data-stu-id="90c93-572">Summary</span></span>

<span data-ttu-id="90c93-573">В этом практическая работа вы встречающейся некоторые новые компоненты находятся в ASP.NET MVC 4.</span><span class="sxs-lookup"><span data-stu-id="90c93-573">In this hands-on-lab, you've observed some of the new features resident in ASP.NET MVC 4.</span></span> <span data-ttu-id="90c93-574">Обсуждались следующие понятия:</span><span class="sxs-lookup"><span data-stu-id="90c93-574">The following concepts have been discussed:</span></span>

- <span data-ttu-id="90c93-575">Воспользоваться преимуществами расширений для ASP.NET MVC проект шаблоны, в том числе нового шаблона проекта приложений для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="90c93-575">Take advantage of the enhancements to the ASP.NET MVC project templates-including the new mobile application project template</span></span>
- <span data-ttu-id="90c93-576">Использовать атрибут просмотра HTML5 и медиа-запросами CSS для улучшения отображения на мобильных устройствах</span><span class="sxs-lookup"><span data-stu-id="90c93-576">Use the HTML5 viewport attribute and CSS media queries to improve the display on mobile devices</span></span>
- <span data-ttu-id="90c93-577">Используйте jQuery Mobile для прогрессивного улучшения и для создания оптимизированных для сенсорных экранов веб-интерфейса</span><span class="sxs-lookup"><span data-stu-id="90c93-577">Use jQuery Mobile for progressive enhancements and for building touch-optimized web UI</span></span>
- <span data-ttu-id="90c93-578">Создавать мобильные особых представлений</span><span class="sxs-lookup"><span data-stu-id="90c93-578">Create mobile-specific views</span></span>
- <span data-ttu-id="90c93-579">Использовать компонент представления переключателя для переключения между представлениями мобильные и Классические приложения</span><span class="sxs-lookup"><span data-stu-id="90c93-579">Use the view-switcher component to toggle between mobile and desktop views in the application</span></span>
- <span data-ttu-id="90c93-580">Создание асинхронных контроллеров с помощью поддержки задач</span><span class="sxs-lookup"><span data-stu-id="90c93-580">Create asynchronous controllers using task support</span></span>

<a id="AppendixA"></a>

<a id="Appendix_A_Using_Code_Snippets"></a>
## <a name="appendix-a-using-code-snippets"></a><span data-ttu-id="90c93-581">Приложение а. Использование фрагментов кода</span><span class="sxs-lookup"><span data-stu-id="90c93-581">Appendix A: Using Code Snippets</span></span>

<span data-ttu-id="90c93-582">С помощью фрагментов кода у вас есть весь код, который требуется под рукой.</span><span class="sxs-lookup"><span data-stu-id="90c93-582">With code snippets, you have all the code you need at your fingertips.</span></span> <span data-ttu-id="90c93-583">Документ лаборатории сообщает только при их использовании, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="90c93-583">The lab document will tell you exactly when you can use them, as shown in the following figure.</span></span>

<span data-ttu-id="90c93-584">![Фрагменты кода Visual Studio для вставки кода в проекте](whats-new-in-aspnet-mvc-4/_static/image38.png "фрагменты кода с помощью Visual Studio вставьте код в проект")</span><span class="sxs-lookup"><span data-stu-id="90c93-584">![Using Visual Studio code snippets to insert code into your project](whats-new-in-aspnet-mvc-4/_static/image38.png "Using Visual Studio code snippets to insert code into your project")</span></span>

<span data-ttu-id="90c93-585">*Фрагменты кода Visual Studio для вставки кода в проекте*</span><span class="sxs-lookup"><span data-stu-id="90c93-585">*Using Visual Studio code snippets to insert code into your project*</span></span>

<span data-ttu-id="90c93-586">***Добавление фрагмента кода, с помощью клавиатуры (только C#)***</span><span class="sxs-lookup"><span data-stu-id="90c93-586">***To add a code snippet using the keyboard (C# only)***</span></span>

1. <span data-ttu-id="90c93-587">Поместите курсор в место вставки кода.</span><span class="sxs-lookup"><span data-stu-id="90c93-587">Place the cursor where you would like to insert the code.</span></span>
2. <span data-ttu-id="90c93-588">Начните вводить имя фрагмента (без пробелов и дефисы).</span><span class="sxs-lookup"><span data-stu-id="90c93-588">Start typing the snippet name (without spaces or hyphens).</span></span>
3. <span data-ttu-id="90c93-589">Смотрите, как IntelliSense отображает, совпадающие с именами фрагменты.</span><span class="sxs-lookup"><span data-stu-id="90c93-589">Watch as IntelliSense displays matching snippets' names.</span></span>
4. <span data-ttu-id="90c93-590">Выберите правильный фрагмент (или продолжите ввод, пока не будет выделен весь фрагмент имени).</span><span class="sxs-lookup"><span data-stu-id="90c93-590">Select the correct snippet (or keep typing until the entire snippet's name is selected).</span></span>
5. <span data-ttu-id="90c93-591">Нажмите клавишу Tab дважды, чтобы вставить фрагмент в положении курсора.</span><span class="sxs-lookup"><span data-stu-id="90c93-591">Press the Tab key twice to insert the snippet at the cursor location.</span></span>

<span data-ttu-id="90c93-592">![Начните вводить имя фрагмента](whats-new-in-aspnet-mvc-4/_static/image39.png "начните вводить имя фрагмента")</span><span class="sxs-lookup"><span data-stu-id="90c93-592">![Start typing the snippet name](whats-new-in-aspnet-mvc-4/_static/image39.png "Start typing the snippet name")</span></span>

<span data-ttu-id="90c93-593">*Начните вводить имя фрагмента*</span><span class="sxs-lookup"><span data-stu-id="90c93-593">*Start typing the snippet name*</span></span>

<span data-ttu-id="90c93-594">![Нажмите клавишу Tab, чтобы выделить выделенный фрагмент](whats-new-in-aspnet-mvc-4/_static/image40.png "нажмите клавишу Tab, чтобы выделить выделенный фрагмент")</span><span class="sxs-lookup"><span data-stu-id="90c93-594">![Press Tab to select the highlighted snippet](whats-new-in-aspnet-mvc-4/_static/image40.png "Press Tab to select the highlighted snippet")</span></span>

<span data-ttu-id="90c93-595">*Нажмите клавишу Tab, чтобы выделить выделенный фрагмент*</span><span class="sxs-lookup"><span data-stu-id="90c93-595">*Press Tab to select the highlighted snippet*</span></span>

<span data-ttu-id="90c93-596">![Снова нажмите клавишу Tab и фрагмент будет расширен](whats-new-in-aspnet-mvc-4/_static/image41.png "будет расширен, снова нажмите клавишу Tab и фрагмента кода")</span><span class="sxs-lookup"><span data-stu-id="90c93-596">![Press Tab again and the snippet will expand](whats-new-in-aspnet-mvc-4/_static/image41.png "Press Tab again and the snippet will expand")</span></span>

<span data-ttu-id="90c93-597">*Снова нажмите клавишу Tab и фрагмент будет расширен*</span><span class="sxs-lookup"><span data-stu-id="90c93-597">*Press Tab again and the snippet will expand*</span></span>

<span data-ttu-id="90c93-598">***Добавление фрагмента кода, с помощью мыши (C#, Visual Basic и XML)***</span><span class="sxs-lookup"><span data-stu-id="90c93-598">***To add a code snippet using the mouse (C#, Visual Basic and XML)***</span></span>

1. <span data-ttu-id="90c93-599">Щелкните правой кнопкой мыши место вставки фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="90c93-599">Right-click where you want to insert the code snippet.</span></span>
2. <span data-ttu-id="90c93-600">Выберите **вставить фрагмент** следуют **Мои фрагменты кода**.</span><span class="sxs-lookup"><span data-stu-id="90c93-600">Select **Insert Snippet** followed by **My Code Snippets**.</span></span>
3. <span data-ttu-id="90c93-601">Выберите соответствующий фрагмент из списка, щелкнув по ней.</span><span class="sxs-lookup"><span data-stu-id="90c93-601">Pick the relevant snippet from the list, by clicking on it.</span></span>

<span data-ttu-id="90c93-602">![Щелкните правой кнопкой мыши место для вставки фрагмента кода и выбора вставить фрагмент](whats-new-in-aspnet-mvc-4/_static/image42.png "место для вставки фрагмента кода и выбора вставить фрагмент кода щелкните правой кнопкой мыши")</span><span class="sxs-lookup"><span data-stu-id="90c93-602">![Right-click where you want to insert the code snippet and select Insert Snippet](whats-new-in-aspnet-mvc-4/_static/image42.png "Right-click where you want to insert the code snippet and select Insert Snippet")</span></span>

<span data-ttu-id="90c93-603">*Щелкните правой кнопкой мыши в место вставки фрагмента кода и выберите Вставить фрагмент*</span><span class="sxs-lookup"><span data-stu-id="90c93-603">*Right-click where you want to insert the code snippet and select Insert Snippet*</span></span>

<span data-ttu-id="90c93-604">![Выберите из списка, соответствующего фрагмента, щелкнув его](whats-new-in-aspnet-mvc-4/_static/image43.png "выбрать соответствующий фрагмент из списка, щелкнув по ней")</span><span class="sxs-lookup"><span data-stu-id="90c93-604">![Pick the relevant snippet from the list, by clicking on it](whats-new-in-aspnet-mvc-4/_static/image43.png "Pick the relevant snippet from the list, by clicking on it")</span></span>

<span data-ttu-id="90c93-605">*Выберите соответствующий фрагмент из списка, щелкнув по ней*</span><span class="sxs-lookup"><span data-stu-id="90c93-605">*Pick the relevant snippet from the list, by clicking on it*</span></span>

<a id="AppendixB"></a>

<a id="Appendix_B_Installing_Visual_Studio_Express_2012_for_Web"></a>
## <a name="appendix-b-installing-visual-studio-express-2012-for-web"></a><span data-ttu-id="90c93-606">Приложение б. Установка Visual Studio Express 2012 для Web</span><span class="sxs-lookup"><span data-stu-id="90c93-606">Appendix B: Installing Visual Studio Express 2012 for Web</span></span>

<span data-ttu-id="90c93-607">Можно установить **Microsoft Visual Studio Express 2012 для Web** или другой &quot;Express&quot; версию, используя  **[Microsoft Web Platform Installer](https://www.microsoft.com/web/downloads/platform.aspx)** .</span><span class="sxs-lookup"><span data-stu-id="90c93-607">You can install **Microsoft Visual Studio Express 2012 for Web** or another &quot;Express&quot; version using the **[Microsoft Web Platform Installer](https://www.microsoft.com/web/downloads/platform.aspx)**.</span></span> <span data-ttu-id="90c93-608">Следующие инструкции описывают действия, необходимые для установки *Visual studio Express 2012 для Web* с помощью *Microsoft Web Platform Installer*.</span><span class="sxs-lookup"><span data-stu-id="90c93-608">The following instructions guide you through the steps required to install *Visual studio Express 2012 for Web* using *Microsoft Web Platform Installer*.</span></span>

1. <span data-ttu-id="90c93-609">Последовательно выберите пункты [ [https://go.microsoft.com/?linkid=9810169](https://go.microsoft.com/?linkid=9810169)](https://go.microsoft.com/?linkid=9810169).</span><span class="sxs-lookup"><span data-stu-id="90c93-609">Go to [[https://go.microsoft.com/?linkid=9810169](https://go.microsoft.com/?linkid=9810169)](https://go.microsoft.com/?linkid=9810169).</span></span> <span data-ttu-id="90c93-610">Кроме того, если вы уже установили установщика веб-платформы, можно открыть его и выполните поиск продукта &quot; *Visual Studio Express 2012 для Web с пакетом Windows Azure SDK*&quot;.</span><span class="sxs-lookup"><span data-stu-id="90c93-610">Alternatively, if you already have installed Web Platform Installer, you can open it and search for the product &quot;*Visual Studio Express 2012 for Web with Windows Azure SDK*&quot;.</span></span>
2. <span data-ttu-id="90c93-611">Щелкните **установить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="90c93-611">Click on **Install Now**.</span></span> <span data-ttu-id="90c93-612">Если у вас **Web Platform Installer** вы будете перенаправлены, чтобы загрузить и установить ее сначала.</span><span class="sxs-lookup"><span data-stu-id="90c93-612">If you do not have **Web Platform Installer** you will be redirected to download and install it first.</span></span>
3. <span data-ttu-id="90c93-613">Один раз **Web Platform Installer** открыто, нажмите кнопку **установить** для запуска программы установки.</span><span class="sxs-lookup"><span data-stu-id="90c93-613">Once **Web Platform Installer** is open, click **Install** to start the setup.</span></span>

    <span data-ttu-id="90c93-614">![Установка Visual Studio Express](whats-new-in-aspnet-mvc-4/_static/image44.png "установка Visual Studio Express")</span><span class="sxs-lookup"><span data-stu-id="90c93-614">![Install Visual Studio Express](whats-new-in-aspnet-mvc-4/_static/image44.png "Install Visual Studio Express")</span></span>

    <span data-ttu-id="90c93-615">*Установка Visual Studio Express*</span><span class="sxs-lookup"><span data-stu-id="90c93-615">*Install Visual Studio Express*</span></span>
4. <span data-ttu-id="90c93-616">Чтение всех продуктов лицензий и условия и нажмите кнопку **принимаю** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="90c93-616">Read all the products' licenses and terms and click **I Accept** to continue.</span></span>

    ![Принятие условий лицензионного соглашения](whats-new-in-aspnet-mvc-4/_static/image45.png)

    <span data-ttu-id="90c93-618">*Принятие условий лицензионного соглашения*</span><span class="sxs-lookup"><span data-stu-id="90c93-618">*Accepting the license terms*</span></span>
5. <span data-ttu-id="90c93-619">Дождитесь завершения процесса загрузки и установки.</span><span class="sxs-lookup"><span data-stu-id="90c93-619">Wait until the downloading and installation process completes.</span></span>

    ![Ход установки](whats-new-in-aspnet-mvc-4/_static/image46.png)

    <span data-ttu-id="90c93-621">*Ход выполнения установки*</span><span class="sxs-lookup"><span data-stu-id="90c93-621">*Installation progress*</span></span>
6. <span data-ttu-id="90c93-622">По завершении установки нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="90c93-622">When the installation completes, click **Finish**.</span></span>

    ![Установка завершена](whats-new-in-aspnet-mvc-4/_static/image47.png)

    <span data-ttu-id="90c93-624">*Установка завершена*</span><span class="sxs-lookup"><span data-stu-id="90c93-624">*Installation completed*</span></span>
7. <span data-ttu-id="90c93-625">Нажмите кнопку **выхода** закрыть установщик веб-платформы.</span><span class="sxs-lookup"><span data-stu-id="90c93-625">Click **Exit** to close Web Platform Installer.</span></span>
8. <span data-ttu-id="90c93-626">Чтобы открыть Visual Studio Express для Web, перейдите к **запустить** экрана и начинается запись &quot; **VS Express**&quot;, выберите команду **VS Express для Web** Плитка.</span><span class="sxs-lookup"><span data-stu-id="90c93-626">To open Visual Studio Express for Web, go to the **Start** screen and start writing &quot;**VS Express**&quot;, then click on the **VS Express for Web** tile.</span></span>

    ![VS Express для Web плитки](whats-new-in-aspnet-mvc-4/_static/image48.png)

    <span data-ttu-id="90c93-628">*VS Express для Web плитки*</span><span class="sxs-lookup"><span data-stu-id="90c93-628">*VS Express for Web tile*</span></span>

<a id="AppendixC"></a>

<a id="Appendix_C_Installing_WebMatrix_2_and_iPhone_Simulator"></a>
## <a name="appendix-c-installing-webmatrix-2-and-iphone-simulator"></a><span data-ttu-id="90c93-629">Приложение в. Установка WebMatrix 2 и iPhone симулятор</span><span class="sxs-lookup"><span data-stu-id="90c93-629">Appendix C: Installing WebMatrix 2 and iPhone Simulator</span></span>

<span data-ttu-id="90c93-630">Для запуска веб-узла на устройстве iPhone имитацию можно использовать расширения WebMatrix &quot;должен быть электрический симулятор Mobile для iPhone&quot;.</span><span class="sxs-lookup"><span data-stu-id="90c93-630">To run your site in a simulated iPhone device you can use the WebMatrix extension &quot;Electric Mobile Simulator for the iPhone&quot;.</span></span> <span data-ttu-id="90c93-631">Кроме того можно настроить то же самое расширение, для запуска имитатора из Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="90c93-631">Also, you can configure the same extension to run the simulator from Visual Studio 2012.</span></span>

<a id="ApxCTask1"></a>

<a id="Task_1_-_Installing_WebMatrix_2"></a>
#### <a name="task-1---installing-webmatrix-2"></a><span data-ttu-id="90c93-632">Задача 1. Установка WebMatrix 2</span><span class="sxs-lookup"><span data-stu-id="90c93-632">Task 1 - Installing WebMatrix 2</span></span>

1. <span data-ttu-id="90c93-633">Последовательно выберите пункты [ [https://go.microsoft.com/?linkid=9809776](https://go.microsoft.com/?linkid=9809776)](https://go.microsoft.com/?linkid=9810169).</span><span class="sxs-lookup"><span data-stu-id="90c93-633">Go to [[https://go.microsoft.com/?linkid=9809776](https://go.microsoft.com/?linkid=9809776)](https://go.microsoft.com/?linkid=9810169).</span></span> <span data-ttu-id="90c93-634">Кроме того, если вы уже установили установщика веб-платформы, можно открыть его и выполните поиск продукта &quot; *WebMatrix 2*&quot;.</span><span class="sxs-lookup"><span data-stu-id="90c93-634">Alternatively, if you already have installed Web Platform Installer, you can open it and search for the product &quot;*WebMatrix 2*&quot;.</span></span>
2. <span data-ttu-id="90c93-635">Щелкните **установить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="90c93-635">Click on **Install Now**.</span></span> <span data-ttu-id="90c93-636">Если у вас **Web Platform Installer** вы будете перенаправлены, чтобы загрузить и установить ее сначала.</span><span class="sxs-lookup"><span data-stu-id="90c93-636">If you do not have **Web Platform Installer** you will be redirected to download and install it first.</span></span>
3. <span data-ttu-id="90c93-637">Один раз **Web Platform Installer** открыто, нажмите кнопку **установить** для запуска программы установки.</span><span class="sxs-lookup"><span data-stu-id="90c93-637">Once **Web Platform Installer** is open, click **Install** to start the setup.</span></span>

    <span data-ttu-id="90c93-638">![Установка WebMatrix 2](whats-new-in-aspnet-mvc-4/_static/image49.png "Установка WebMatrix 2")</span><span class="sxs-lookup"><span data-stu-id="90c93-638">![Install WebMatrix 2](whats-new-in-aspnet-mvc-4/_static/image49.png "Install WebMatrix 2")</span></span>

    <span data-ttu-id="90c93-639">*Установка WebMatrix 2*</span><span class="sxs-lookup"><span data-stu-id="90c93-639">*Install WebMatrix 2*</span></span>
4. <span data-ttu-id="90c93-640">Чтение всех продуктов лицензий и условия и нажмите кнопку **принимаю** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="90c93-640">Read all the products' licenses and terms and click **I Accept** to continue.</span></span>

    <span data-ttu-id="90c93-641">![Принятие условий лицензионного соглашения](whats-new-in-aspnet-mvc-4/_static/image50.png "принятие условий лицензионного соглашения")</span><span class="sxs-lookup"><span data-stu-id="90c93-641">![Accepting the license terms](whats-new-in-aspnet-mvc-4/_static/image50.png "Accepting the license terms")</span></span>

    <span data-ttu-id="90c93-642">*Принятие условий лицензионного соглашения*</span><span class="sxs-lookup"><span data-stu-id="90c93-642">*Accepting the license terms*</span></span>
5. <span data-ttu-id="90c93-643">Дождитесь завершения процесса загрузки и установки.</span><span class="sxs-lookup"><span data-stu-id="90c93-643">Wait until the downloading and installation process completes.</span></span>

    <span data-ttu-id="90c93-644">![Ход выполнения установки](whats-new-in-aspnet-mvc-4/_static/image51.png "ход выполнения установки")</span><span class="sxs-lookup"><span data-stu-id="90c93-644">![Installation progress](whats-new-in-aspnet-mvc-4/_static/image51.png "Installation progress")</span></span>

    <span data-ttu-id="90c93-645">*Ход выполнения установки*</span><span class="sxs-lookup"><span data-stu-id="90c93-645">*Installation progress*</span></span>
6. <span data-ttu-id="90c93-646">По завершении установки нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="90c93-646">When the installation completes, click **Finish**.</span></span>

    <span data-ttu-id="90c93-647">![Установка завершена](whats-new-in-aspnet-mvc-4/_static/image52.png "Установка завершена")</span><span class="sxs-lookup"><span data-stu-id="90c93-647">![Installation completed](whats-new-in-aspnet-mvc-4/_static/image52.png "Installation completed")</span></span>

    <span data-ttu-id="90c93-648">*Установка завершена*</span><span class="sxs-lookup"><span data-stu-id="90c93-648">*Installation completed*</span></span>
7. <span data-ttu-id="90c93-649">Нажмите кнопку **выхода** закрыть установщик веб-платформы.</span><span class="sxs-lookup"><span data-stu-id="90c93-649">Click **Exit** to close Web Platform Installer.</span></span>

<a id="ApxCTask2"></a>

<a id="Task_2_-_Installing_the_iPhone_Simulator_Extension"></a>
#### <a name="task-2---installing-the-iphone-simulator-extension"></a><span data-ttu-id="90c93-650">Задача 2 - Установка iPhone симулятор расширения</span><span class="sxs-lookup"><span data-stu-id="90c93-650">Task 2 - Installing the iPhone Simulator Extension</span></span>

1. <span data-ttu-id="90c93-651">Запустите **WebMatrix** и откройте любой существующий веб-сайт или создайте новую.</span><span class="sxs-lookup"><span data-stu-id="90c93-651">Run **WebMatrix** and open any existing Web site or create a new one.</span></span>
2. <span data-ttu-id="90c93-652">Нажмите кнопку **запуска** кнопку **Главная** ленты и выберите **добавить новую**.</span><span class="sxs-lookup"><span data-stu-id="90c93-652">Click the **Run** button from the **Home** ribbon and select **Add new**.</span></span>

    <span data-ttu-id="90c93-653">![Добавление нового расширения WebMatrix](whats-new-in-aspnet-mvc-4/_static/image53.png "Добавление нового расширения WebMatrix")</span><span class="sxs-lookup"><span data-stu-id="90c93-653">![Adding new WebMatrix extension](whats-new-in-aspnet-mvc-4/_static/image53.png "Adding new WebMatrix extension")</span></span>

    <span data-ttu-id="90c93-654">*Добавление нового расширения WebMatrix*</span><span class="sxs-lookup"><span data-stu-id="90c93-654">*Adding new WebMatrix extension*</span></span>
3. <span data-ttu-id="90c93-655">Выберите **iPhone симулятор** и нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="90c93-655">Select **iPhone Simulator** and click **Install**.</span></span>

    <span data-ttu-id="90c93-656">![Просмотр расширения WebMatrix](whats-new-in-aspnet-mvc-4/_static/image54.png "расширения WebMatrix, просмотр")</span><span class="sxs-lookup"><span data-stu-id="90c93-656">![Browsing WebMatrix extensions](whats-new-in-aspnet-mvc-4/_static/image54.png "Browsing WebMatrix extensions")</span></span>

    <span data-ttu-id="90c93-657">*Просмотр расширения WebMatrix*</span><span class="sxs-lookup"><span data-stu-id="90c93-657">*Browsing WebMatrix extensions*</span></span>
4. <span data-ttu-id="90c93-658">Сведения о пакете, щелкните **установить** для продолжения установки расширения.</span><span class="sxs-lookup"><span data-stu-id="90c93-658">In the package details, click **Install** to continue with the extension installation.</span></span>

    <span data-ttu-id="90c93-659">![iPhone расширения симулятор](whats-new-in-aspnet-mvc-4/_static/image55.png "iPhone симулятор расширения")</span><span class="sxs-lookup"><span data-stu-id="90c93-659">![iPhone Simulator extension](whats-new-in-aspnet-mvc-4/_static/image55.png "iPhone Simulator extension")</span></span>

    <span data-ttu-id="90c93-660">*iPhone симулятор расширения*</span><span class="sxs-lookup"><span data-stu-id="90c93-660">*iPhone Simulator extension*</span></span>
5. <span data-ttu-id="90c93-661">Прочтите и примите лицензионное соглашение расширения.</span><span class="sxs-lookup"><span data-stu-id="90c93-661">Read and accept the extension EULA.</span></span>

    <span data-ttu-id="90c93-662">![Расширения WebMatrix лицензионное соглашение](whats-new-in-aspnet-mvc-4/_static/image56.png "расширения WebMatrix лицензионное соглашение")</span><span class="sxs-lookup"><span data-stu-id="90c93-662">![WebMatrix extension EULA](whats-new-in-aspnet-mvc-4/_static/image56.png "WebMatrix extension EULA")</span></span>

    <span data-ttu-id="90c93-663">*Расширения WebMatrix лицензионное соглашение*</span><span class="sxs-lookup"><span data-stu-id="90c93-663">*WebMatrix extension EULA*</span></span>
6. <span data-ttu-id="90c93-664">Теперь можно запустить веб-сайта из WebMatrix с помощью iPhone имитатор параметр.</span><span class="sxs-lookup"><span data-stu-id="90c93-664">Now, you can run your Web site from WebMatrix using the iPhone Simulator option.</span></span>

    <span data-ttu-id="90c93-665">![Запустить с помощью iPhone](whats-new-in-aspnet-mvc-4/_static/image57.png "запустить с помощью iPhone")</span><span class="sxs-lookup"><span data-stu-id="90c93-665">![Run using iPhone](whats-new-in-aspnet-mvc-4/_static/image57.png "Run using iPhone")</span></span>

    <span data-ttu-id="90c93-666">*Запустить с помощью iPhone*</span><span class="sxs-lookup"><span data-stu-id="90c93-666">*Run using iPhone*</span></span>

<a id="ApxCTask3"></a>

<a id="Task_3_-_Configuring_Visual_Studio_2012_to_run_iPhone_Simulator"></a>
#### <a name="task-3---configuring-visual-studio-2012-to-run-iphone-simulator"></a><span data-ttu-id="90c93-667">Задача 3. Настройка Visual Studio 2012 для запуска симулятора iPhone</span><span class="sxs-lookup"><span data-stu-id="90c93-667">Task 3 - Configuring Visual Studio 2012 to run iPhone Simulator</span></span>

1. <span data-ttu-id="90c93-668">Откройте **Visual Studio 2012** и открыть любой веб-сайт или создайте новый проект.</span><span class="sxs-lookup"><span data-stu-id="90c93-668">Open **Visual Studio 2012** and open any Web site or create a new project.</span></span>
2. <span data-ttu-id="90c93-669">Щелкните стрелку вниз, с помощью выполнения кнопки и выберите **перейти с**.</span><span class="sxs-lookup"><span data-stu-id="90c93-669">Click the down arrow from the Run button and select **Browse with**.</span></span>

    <span data-ttu-id="90c93-670">![Просмотр с помощью](whats-new-in-aspnet-mvc-4/_static/image58.png "просмотреть с помощью")</span><span class="sxs-lookup"><span data-stu-id="90c93-670">![Browse with](whats-new-in-aspnet-mvc-4/_static/image58.png "Browse with")</span></span>

    <span data-ttu-id="90c93-671">*Просмотр с помощью*</span><span class="sxs-lookup"><span data-stu-id="90c93-671">*Browse with*</span></span>
3. <span data-ttu-id="90c93-672">В &quot;просмотр с помощью&quot; диалоговое окно, нажмите кнопку **добавить**.</span><span class="sxs-lookup"><span data-stu-id="90c93-672">In the &quot;Browse With&quot; dialog, click **Add**.</span></span>
4. <span data-ttu-id="90c93-673">В &quot;добавить программу&quot; диалогового окна, используйте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="90c93-673">In the &quot;Add Program&quot; dialog, use the following values:</span></span>

    - <span data-ttu-id="90c93-674">**Программа**: C:\Users\*{CurrentUser}*\AppData\Local\Microsoft\WebMatrix\Extensions\20\iPhoneSimulator\ElectricMobileSim\ElectricMobileSim.exe *(соответствующим образом обновить путь)*</span><span class="sxs-lookup"><span data-stu-id="90c93-674">**Program**: C:\Users\*{CurrentUser}*\AppData\Local\Microsoft\WebMatrix\Extensions\20\iPhoneSimulator\ElectricMobileSim\ElectricMobileSim.exe *(update the path accordingly)*</span></span>
    - <span data-ttu-id="90c93-675">**Аргументы**: &quot;1&quot;</span><span class="sxs-lookup"><span data-stu-id="90c93-675">**Arguments**: &quot;1&quot;</span></span>
    - <span data-ttu-id="90c93-676">**Понятное имя**: iPhone симулятора</span><span class="sxs-lookup"><span data-stu-id="90c93-676">**Friendly name**: iPhone Simulator</span></span>

    <span data-ttu-id="90c93-677">![Добавление программы](whats-new-in-aspnet-mvc-4/_static/image59.png "Добавление программы")</span><span class="sxs-lookup"><span data-stu-id="90c93-677">![Add program](whats-new-in-aspnet-mvc-4/_static/image59.png "Add program")</span></span>

    <span data-ttu-id="90c93-678">*Добавьте программу, чтобы перейти с*</span><span class="sxs-lookup"><span data-stu-id="90c93-678">*Add program to browse with*</span></span>
5. <span data-ttu-id="90c93-679">Нажмите кнопку **ОК** и закрыть все диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="90c93-679">Click **OK** and close the dialogs.</span></span>
6. <span data-ttu-id="90c93-680">Теперь имеется возможность запустить веб-приложений в симуляторе iPhone из Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="90c93-680">Now you are able to run your Web applications in the iPhone simulator from Visual Studio 2012.</span></span>

    <span data-ttu-id="90c93-681">![Просмотр с помощью iPhone симулятор](whats-new-in-aspnet-mvc-4/_static/image60.png "просмотреть с помощью iPhone симулятора")</span><span class="sxs-lookup"><span data-stu-id="90c93-681">![Browse with iPhone Simulator](whats-new-in-aspnet-mvc-4/_static/image60.png "Browse with iPhone Simulator")</span></span>

    <span data-ttu-id="90c93-682">*Просмотр с помощью iPhone симулятора*</span><span class="sxs-lookup"><span data-stu-id="90c93-682">*Browse with iPhone Simulator*</span></span>

<a id="AppendixD"></a>

<a id="Appendix_D_Publishing_an_ASPNET_MVC_4_Application_using_Web_Deploy"></a>
## <a name="appendix-d-publishing-an-aspnet-mvc-4-application-using-web-deploy"></a><span data-ttu-id="90c93-683">Приложение г. публикация приложения ASP.NET MVC 4 с помощью веб-развертывания</span><span class="sxs-lookup"><span data-stu-id="90c93-683">Appendix D: Publishing an ASP.NET MVC 4 Application using Web Deploy</span></span>

<span data-ttu-id="90c93-684">В этом приложении будет показано, как создать новый веб-сайт на портале управления Windows Azure и публикация приложения, получить, выполнив в лаборатории преимуществами средство публикации веб-развертывания, предоставленного Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="90c93-684">This appendix will show you how to create a new web site from the Windows Azure Management Portal and publish the application you obtained by following the lab, taking advantage of the Web Deploy publishing feature provided by Windows Azure.</span></span>

<a id="ApxDTask1"></a>

<a id="Task_1_-_Creating_a_New_Web_Site_from_the_Windows_Azure_Portal"></a>
#### <a name="task-1---creating-a-new-web-site-from-the-windows-azure-portal"></a><span data-ttu-id="90c93-685">Задача 1. Создание нового веб-узла с Windows Azure Portal</span><span class="sxs-lookup"><span data-stu-id="90c93-685">Task 1 - Creating a New Web Site from the Windows Azure Portal</span></span>

1. <span data-ttu-id="90c93-686">Последовательно выберите пункты [портала управления Windows Azure](https://manage.windowsazure.com/) и войдите с использованием учетных данных Майкрософт, связанную с вашей подпиской.</span><span class="sxs-lookup"><span data-stu-id="90c93-686">Go to the [Windows Azure Management Portal](https://manage.windowsazure.com/) and sign in using the Microsoft credentials associated with your subscription.</span></span>

    > [!NOTE]
    > <span data-ttu-id="90c93-687">С помощью Windows Azure можно бесплатно размещения 10 веб-сайтов ASP.NET и затем масштабирование по мере увеличения трафика.</span><span class="sxs-lookup"><span data-stu-id="90c93-687">With Windows Azure you can host 10 ASP.NET Web Sites for free and then scale as your traffic grows.</span></span> <span data-ttu-id="90c93-688">Вы можете зарегистрироваться [здесь](http://aka.ms/aspnet-hol-azure).</span><span class="sxs-lookup"><span data-stu-id="90c93-688">You can sign up [here](http://aka.ms/aspnet-hol-azure).</span></span>

    <span data-ttu-id="90c93-689">![Войдите на портал Windows Azure](whats-new-in-aspnet-mvc-4/_static/image61.png "входа на портал Windows Azure")</span><span class="sxs-lookup"><span data-stu-id="90c93-689">![Log on to Windows Azure portal](whats-new-in-aspnet-mvc-4/_static/image61.png "Log on to Windows Azure portal")</span></span>

    <span data-ttu-id="90c93-690">*Выполните вход на портале управления Windows Azure*</span><span class="sxs-lookup"><span data-stu-id="90c93-690">*Log on to Windows Azure Management Portal*</span></span>
2. <span data-ttu-id="90c93-691">Нажмите кнопку **New** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="90c93-691">Click **New** on the command bar.</span></span>

    <span data-ttu-id="90c93-692">![Создание нового веб-сайта](whats-new-in-aspnet-mvc-4/_static/image62.png "создания нового веб-сайта")</span><span class="sxs-lookup"><span data-stu-id="90c93-692">![Creating a new Web Site](whats-new-in-aspnet-mvc-4/_static/image62.png "Creating a new Web Site")</span></span>

    <span data-ttu-id="90c93-693">*Создание нового веб-сайта*</span><span class="sxs-lookup"><span data-stu-id="90c93-693">*Creating a new Web Site*</span></span>
3. <span data-ttu-id="90c93-694">Нажмите кнопку **вычислений** | **веб-сайт**.</span><span class="sxs-lookup"><span data-stu-id="90c93-694">Click **Compute** | **Web Site**.</span></span> <span data-ttu-id="90c93-695">Выберите **быстрое создание** параметр.</span><span class="sxs-lookup"><span data-stu-id="90c93-695">Then select **Quick Create** option.</span></span> <span data-ttu-id="90c93-696">Укажите URL-адрес доступен для нового веб-сайта и нажмите кнопку **Создание веб-сайта**.</span><span class="sxs-lookup"><span data-stu-id="90c93-696">Provide an available URL for the new web site and click **Create Web Site**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="90c93-697">Веб-приложение, работающее в облаке, вы можете управлять размещается веб-сайта Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="90c93-697">A Windows Azure Web Site is the host for a web application running in the cloud that you can control and manage.</span></span> <span data-ttu-id="90c93-698">Параметр быстрого создания позволяет развернуть завершенное веб-приложение для Windows Azure веб-сайта из вне портала.</span><span class="sxs-lookup"><span data-stu-id="90c93-698">The Quick Create option allows you to deploy a completed web application to the Windows Azure Web Site from outside the portal.</span></span> <span data-ttu-id="90c93-699">Он не включает действия по настройке базы данных.</span><span class="sxs-lookup"><span data-stu-id="90c93-699">It does not include steps for setting up a database.</span></span>

    <span data-ttu-id="90c93-700">![Создание нового веб-сайта с помощью быстрого создания](whats-new-in-aspnet-mvc-4/_static/image63.png "создания нового веб-сайта с помощью быстрого создания")</span><span class="sxs-lookup"><span data-stu-id="90c93-700">![Creating a new Web Site using Quick Create](whats-new-in-aspnet-mvc-4/_static/image63.png "Creating a new Web Site using Quick Create")</span></span>

    <span data-ttu-id="90c93-701">*Создание нового веб-сайта с помощью быстрого создания*</span><span class="sxs-lookup"><span data-stu-id="90c93-701">*Creating a new Web Site using Quick Create*</span></span>
4. <span data-ttu-id="90c93-702">Подождите, пока новый **веб-сайт** создается.</span><span class="sxs-lookup"><span data-stu-id="90c93-702">Wait until the new **Web Site** is created.</span></span>
5. <span data-ttu-id="90c93-703">После создания веб-сайта по ссылке **URL-адрес** столбца.</span><span class="sxs-lookup"><span data-stu-id="90c93-703">Once the Web Site is created click the link under the **URL** column.</span></span> <span data-ttu-id="90c93-704">Проверьте, что новый веб-сайт работает.</span><span class="sxs-lookup"><span data-stu-id="90c93-704">Check that the new Web Site is working.</span></span>

    <span data-ttu-id="90c93-705">![Просмотр новых веб-сайт](whats-new-in-aspnet-mvc-4/_static/image64.png "просмотра на новый веб-сайт")</span><span class="sxs-lookup"><span data-stu-id="90c93-705">![Browsing to the new web site](whats-new-in-aspnet-mvc-4/_static/image64.png "Browsing to the new web site")</span></span>

    <span data-ttu-id="90c93-706">*Просмотр новых веб-сайт*</span><span class="sxs-lookup"><span data-stu-id="90c93-706">*Browsing to the new web site*</span></span>

    <span data-ttu-id="90c93-707">![Веб-сайта под управлением](whats-new-in-aspnet-mvc-4/_static/image65.png "веб-сайта под управлением")</span><span class="sxs-lookup"><span data-stu-id="90c93-707">![Web site running](whats-new-in-aspnet-mvc-4/_static/image65.png "Web site running")</span></span>

    <span data-ttu-id="90c93-708">*Запуск веб-сайта*</span><span class="sxs-lookup"><span data-stu-id="90c93-708">*Web site running*</span></span>
6. <span data-ttu-id="90c93-709">Вернитесь на портал и щелкните имя веб-сайта в разделе **имя** столбец для отображения страницы управления.</span><span class="sxs-lookup"><span data-stu-id="90c93-709">Go back to the portal and click the name of the web site under the **Name** column to display the management pages.</span></span>

    <span data-ttu-id="90c93-710">![Открытие страницы управления веб-сайт](whats-new-in-aspnet-mvc-4/_static/image66.png "Открытие страниц управления веб-сайта")</span><span class="sxs-lookup"><span data-stu-id="90c93-710">![Opening the web site management pages](whats-new-in-aspnet-mvc-4/_static/image66.png "Opening the web site management pages")</span></span>

    <span data-ttu-id="90c93-711">*Открытие страницы управления веб-сайта*</span><span class="sxs-lookup"><span data-stu-id="90c93-711">*Opening the Web Site management pages*</span></span>
7. <span data-ttu-id="90c93-712">В **панели мониторинга** в разделе **беглого** щелкните **загрузить профиль публикации** ссылку.</span><span class="sxs-lookup"><span data-stu-id="90c93-712">In the **Dashboard** page, under the **quick glance** section, click the **Download publish profile** link.</span></span>

    > [!NOTE]
    > <span data-ttu-id="90c93-713">*Профиль публикации* содержит все сведения, необходимые для публикации веб-приложения на веб-сайте Windows Azure для каждого разрешенного метода публикации.</span><span class="sxs-lookup"><span data-stu-id="90c93-713">The *publish profile* contains all of the information required to publish a web application to a Windows Azure website for each enabled publication method.</span></span> <span data-ttu-id="90c93-714">Профиль публикации содержит URL-адреса, учетные данные пользователя и строк базы данных, необходимых для подключения и проверки подлинности с каждой из конечных точек, для которых включен метода публикации.</span><span class="sxs-lookup"><span data-stu-id="90c93-714">The publish profile contains the URLs, user credentials and database strings required to connect to and authenticate against each of the endpoints for which a publication method is enabled.</span></span> <span data-ttu-id="90c93-715">**Microsoft WebMatrix 2**, **Microsoft Visual Studio Express для Web** и **Microsoft Visual Studio 2012** поддерживают чтение профилей публикации для автоматизации настройки этих программ для Публикация веб-приложений на веб-сайтов Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="90c93-715">**Microsoft WebMatrix 2**, **Microsoft Visual Studio Express for Web** and **Microsoft Visual Studio 2012** support reading publish profiles to automate configuration of these programs for publishing web applications to Windows Azure websites.</span></span>

    <span data-ttu-id="90c93-716">![Профиль публикации веб-сайт загрузки](whats-new-in-aspnet-mvc-4/_static/image67.png "профиль публикации веб-сайта загрузки")</span><span class="sxs-lookup"><span data-stu-id="90c93-716">![Downloading the web site publish profile](whats-new-in-aspnet-mvc-4/_static/image67.png "Downloading the web site publish profile")</span></span>

    <span data-ttu-id="90c93-717">*Профиль публикации веб-сайта загрузки*</span><span class="sxs-lookup"><span data-stu-id="90c93-717">*Downloading the Web Site publish profile*</span></span>
8. <span data-ttu-id="90c93-718">Загрузите файл профиля публикации в известном расположении.</span><span class="sxs-lookup"><span data-stu-id="90c93-718">Download the publish profile file to a known location.</span></span> <span data-ttu-id="90c93-719">Далее в этом упражнении вы увидите как использовать этот файл для публикации веб-приложения для веб-сайтов, Windows Azure из Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="90c93-719">Further in this exercise you will see how to use this file to publish a web application to a Windows Azure Web Sites from Visual Studio.</span></span>

    <span data-ttu-id="90c93-720">![Сохранить файл профиля публикации](whats-new-in-aspnet-mvc-4/_static/image68.png "Сохранение профиля публикации")</span><span class="sxs-lookup"><span data-stu-id="90c93-720">![Saving the publish profile file](whats-new-in-aspnet-mvc-4/_static/image68.png "Saving the publish profile")</span></span>

    <span data-ttu-id="90c93-721">*Сохранить файл профиля публикации*</span><span class="sxs-lookup"><span data-stu-id="90c93-721">*Saving the publish profile file*</span></span>

<a id="ApxDTask2"></a>

<a id="Task_2_-_Configuring_the_Database_Server"></a>
#### <a name="task-2---configuring-the-database-server"></a><span data-ttu-id="90c93-722">Задача 2 - Настройка сервера базы данных</span><span class="sxs-lookup"><span data-stu-id="90c93-722">Task 2 - Configuring the Database Server</span></span>

<span data-ttu-id="90c93-723">Если приложение использует SQL Server базы данных, необходимо будет создать сервер базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="90c93-723">If your application makes use of SQL Server databases you will need to create a SQL Database server.</span></span> <span data-ttu-id="90c93-724">Если вы хотите развернуть простое приложение, которое не использует SQL Server может пропустить эту задачу.</span><span class="sxs-lookup"><span data-stu-id="90c93-724">If you want to deploy a simple application that does not use SQL Server you might skip this task.</span></span>

1. <span data-ttu-id="90c93-725">Сервер базы данных SQL необходимо для хранения базы данных приложения.</span><span class="sxs-lookup"><span data-stu-id="90c93-725">You will need a SQL Database server for storing the application database.</span></span> <span data-ttu-id="90c93-726">Можно просматривать серверы базы данных SQL из подписки на портале управления Windows Azure в **баз данных Sql** | **серверы** | **сервера Панель мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="90c93-726">You can view the SQL Database servers from your subscription in the Windows Azure Management portal at **Sql Databases** | **Servers** | **Server's Dashboard**.</span></span> <span data-ttu-id="90c93-727">Если у вас на сервер, созданный, можно создать ее, используя **добавить** кнопки на панели команд.</span><span class="sxs-lookup"><span data-stu-id="90c93-727">If you do not have a server created, you can create one using the **Add** button on the command bar.</span></span> <span data-ttu-id="90c93-728">Обратите внимание **имя сервера и URL-адрес, имя входа администратора и пароль**, как будет использовать их в следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="90c93-728">Take note of the **server name and URL, administrator login name and password**, as you will use them in the next tasks.</span></span> <span data-ttu-id="90c93-729">Не следует создавать базу данных, как он будет создан в более поздней стадии.</span><span class="sxs-lookup"><span data-stu-id="90c93-729">Do not create the database yet, as it will be created in a later stage.</span></span>

    <span data-ttu-id="90c93-730">![Панель мониторинга базы данных SQL Server](whats-new-in-aspnet-mvc-4/_static/image69.png "панель мониторинга базы данных SQL Server")</span><span class="sxs-lookup"><span data-stu-id="90c93-730">![SQL Database Server Dashboard](whats-new-in-aspnet-mvc-4/_static/image69.png "SQL Database Server Dashboard")</span></span>

    <span data-ttu-id="90c93-731">*Панель мониторинга базы данных SQL Server*</span><span class="sxs-lookup"><span data-stu-id="90c93-731">*SQL Database Server Dashboard*</span></span>
2. <span data-ttu-id="90c93-732">В следующей задаче требуется проверить подключение к базе данных из Visual Studio, по этой причине необходимо включить локальный IP-адреса в список серверов **разрешенные IP-адреса**.</span><span class="sxs-lookup"><span data-stu-id="90c93-732">In the next task you will test the database connection from Visual Studio, for that reason you need to include your local IP address in the server's list of **Allowed IP Addresses**.</span></span> <span data-ttu-id="90c93-733">Чтобы сделать это, нажмите кнопку **Настройка**, выберите IP-адрес из **текущий IP-адрес клиента** и вставьте его на **начальный IP-адрес** и **конечный IP-адрес** текстовые поля и нажмите кнопку ![add-client-ip-address-ok-button](whats-new-in-aspnet-mvc-4/_static/image70.png) кнопки.</span><span class="sxs-lookup"><span data-stu-id="90c93-733">To do that, click **Configure**, select the IP address from **Current Client IP Address** and paste it on the **Start IP Address** and **End IP Address** text boxes and click the ![add-client-ip-address-ok-button](whats-new-in-aspnet-mvc-4/_static/image70.png) button.</span></span>

    ![Добавление IP-адрес клиента](whats-new-in-aspnet-mvc-4/_static/image71.png)

    <span data-ttu-id="90c93-735">*Добавление IP-адрес клиента*</span><span class="sxs-lookup"><span data-stu-id="90c93-735">*Adding Client IP Address*</span></span>
3. <span data-ttu-id="90c93-736">Один раз **IP-адрес клиента** добавляется разрешенных IP-адресов выберите на **Сохранить** для подтверждения изменения.</span><span class="sxs-lookup"><span data-stu-id="90c93-736">Once the **Client IP Address** is added to the allowed IP addresses list, click on **Save** to confirm the changes.</span></span>

    ![Подтверждение изменений](whats-new-in-aspnet-mvc-4/_static/image72.png)

    <span data-ttu-id="90c93-738">*Подтверждение изменений*</span><span class="sxs-lookup"><span data-stu-id="90c93-738">*Confirm Changes*</span></span>

<a id="ApxDTask3"></a>

<a id="Task_3_-_Publishing_an_ASPNET_MVC_4_Application_using_Web_Deploy"></a>
#### <a name="task-3---publishing-an-aspnet-mvc-4-application-using-web-deploy"></a><span data-ttu-id="90c93-739">Задача 3. публикация приложения ASP.NET MVC 4 с помощью веб-развертывания</span><span class="sxs-lookup"><span data-stu-id="90c93-739">Task 3 - Publishing an ASP.NET MVC 4 Application using Web Deploy</span></span>

1. <span data-ttu-id="90c93-740">Вернитесь в решении ASP.NET MVC 4.</span><span class="sxs-lookup"><span data-stu-id="90c93-740">Go back to the ASP.NET MVC 4 solution.</span></span> <span data-ttu-id="90c93-741">В **обозревателе решений**, щелкните правой кнопкой мыши проект веб-сайта и выберите **публикации**.</span><span class="sxs-lookup"><span data-stu-id="90c93-741">In the **Solution Explorer**, right-click the web site project and select **Publish**.</span></span>

    <span data-ttu-id="90c93-742">![Публикация приложения](whats-new-in-aspnet-mvc-4/_static/image73.png "публикация приложения")</span><span class="sxs-lookup"><span data-stu-id="90c93-742">![Publishing the Application](whats-new-in-aspnet-mvc-4/_static/image73.png "Publishing the Application")</span></span>

    <span data-ttu-id="90c93-743">*Публикация веб-сайта*</span><span class="sxs-lookup"><span data-stu-id="90c93-743">*Publishing the web site*</span></span>
2. <span data-ttu-id="90c93-744">Импортируйте профиль публикации, сохраненный в первой задаче.</span><span class="sxs-lookup"><span data-stu-id="90c93-744">Import the publish profile you saved in the first task.</span></span>

    <span data-ttu-id="90c93-745">![Импорт профиля публикации](whats-new-in-aspnet-mvc-4/_static/image74.png "Импорт профиля публикации")</span><span class="sxs-lookup"><span data-stu-id="90c93-745">![Importing the publish profile](whats-new-in-aspnet-mvc-4/_static/image74.png "Importing the publish profile")</span></span>

    <span data-ttu-id="90c93-746">*Импорт профиля публикации*</span><span class="sxs-lookup"><span data-stu-id="90c93-746">*Importing publish profile*</span></span>
3. <span data-ttu-id="90c93-747">Нажмите кнопку **Проверка подключения**.</span><span class="sxs-lookup"><span data-stu-id="90c93-747">Click **Validate Connection**.</span></span> <span data-ttu-id="90c93-748">После завершения проверки нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="90c93-748">Once Validation is complete click **Next**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="90c93-749">Проверка завершена, как только вы увидите зеленый флажок рядом с "Проверить подключение".</span><span class="sxs-lookup"><span data-stu-id="90c93-749">Validation is complete once you see a green checkmark appear next to the Validate Connection button.</span></span>

    <span data-ttu-id="90c93-750">![Проверка подключения](whats-new-in-aspnet-mvc-4/_static/image75.png "Проверка подключения")</span><span class="sxs-lookup"><span data-stu-id="90c93-750">![Validating connection](whats-new-in-aspnet-mvc-4/_static/image75.png "Validating connection")</span></span>

    <span data-ttu-id="90c93-751">*Проверка подключения*</span><span class="sxs-lookup"><span data-stu-id="90c93-751">*Validating connection*</span></span>
4. <span data-ttu-id="90c93-752">В **параметры** в разделе **баз данных** статьи, нажмите кнопку рядом с текстового поля для подключения к базе данных (т. е. **DefaultConnection**).</span><span class="sxs-lookup"><span data-stu-id="90c93-752">In the **Settings** page, under the **Databases** section, click the button next to your database connection's textbox (i.e. **DefaultConnection**).</span></span>

    <span data-ttu-id="90c93-753">![Конфигурация веб-развертывания](whats-new-in-aspnet-mvc-4/_static/image76.png "конфигурация веб-развертывания")</span><span class="sxs-lookup"><span data-stu-id="90c93-753">![Web deploy configuration](whats-new-in-aspnet-mvc-4/_static/image76.png "Web deploy configuration")</span></span>

    <span data-ttu-id="90c93-754">*Конфигурация веб-развертывания*</span><span class="sxs-lookup"><span data-stu-id="90c93-754">*Web deploy configuration*</span></span>
5. <span data-ttu-id="90c93-755">Настройте подключение к базе данных следующим образом.</span><span class="sxs-lookup"><span data-stu-id="90c93-755">Configure the database connection as follows:</span></span>

    - <span data-ttu-id="90c93-756">В **имя сервера** введите ваш URL-адрес сервера базы данных SQL с помощью *tcp:* префикс.</span><span class="sxs-lookup"><span data-stu-id="90c93-756">In the **Server name** type your SQL Database server URL using the *tcp:* prefix.</span></span>
    - <span data-ttu-id="90c93-757">В **имя пользователя** введите имя входа администратора сервера.</span><span class="sxs-lookup"><span data-stu-id="90c93-757">In **User name** type your server administrator login name.</span></span>
    - <span data-ttu-id="90c93-758">В **пароль** введите пароль входа администратора сервера.</span><span class="sxs-lookup"><span data-stu-id="90c93-758">In **Password** type your server administrator login password.</span></span>
    - <span data-ttu-id="90c93-759">Введите имя новой базы данных, например: *MVC4SampleDB*.</span><span class="sxs-lookup"><span data-stu-id="90c93-759">Type a new database name, for example: *MVC4SampleDB*.</span></span>

    <span data-ttu-id="90c93-760">![Настройка строки подключения назначения](whats-new-in-aspnet-mvc-4/_static/image77.png "Настройка целевой строки подключения")</span><span class="sxs-lookup"><span data-stu-id="90c93-760">![Configuring destination connection string](whats-new-in-aspnet-mvc-4/_static/image77.png "Configuring destination connection string")</span></span>

    <span data-ttu-id="90c93-761">*Настройка целевой строки подключения*</span><span class="sxs-lookup"><span data-stu-id="90c93-761">*Configuring destination connection string*</span></span>
6. <span data-ttu-id="90c93-762">Затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="90c93-762">Then click **OK**.</span></span> <span data-ttu-id="90c93-763">Когда появится запрос на создание базы данных щелкните **Да**.</span><span class="sxs-lookup"><span data-stu-id="90c93-763">When prompted to create the database click **Yes**.</span></span>

    <span data-ttu-id="90c93-764">![Создание базы данных](whats-new-in-aspnet-mvc-4/_static/image78.png "Создание строки базы данных")</span><span class="sxs-lookup"><span data-stu-id="90c93-764">![Creating the database](whats-new-in-aspnet-mvc-4/_static/image78.png "Creating the database string")</span></span>

    <span data-ttu-id="90c93-765">*Создание базы данных*</span><span class="sxs-lookup"><span data-stu-id="90c93-765">*Creating the database*</span></span>
7. <span data-ttu-id="90c93-766">Строка подключения, который будет использоваться для подключения к базе данных SQL в Windows Azure отображается внутри текстового поля по умолчанию соединения.</span><span class="sxs-lookup"><span data-stu-id="90c93-766">The connection string you will use to connect to SQL Database in Windows Azure is shown within Default Connection textbox.</span></span> <span data-ttu-id="90c93-767">Затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="90c93-767">Then click **Next**.</span></span>

    <span data-ttu-id="90c93-768">![Строка подключения, указывающий базу данных SQL](whats-new-in-aspnet-mvc-4/_static/image79.png "строку соединения, указывающий базу данных SQL")</span><span class="sxs-lookup"><span data-stu-id="90c93-768">![Connection string pointing to SQL Database](whats-new-in-aspnet-mvc-4/_static/image79.png "Connection string pointing to SQL Database")</span></span>

    <span data-ttu-id="90c93-769">*Строка подключения, указывающий базу данных SQL*</span><span class="sxs-lookup"><span data-stu-id="90c93-769">*Connection string pointing to SQL Database*</span></span>
8. <span data-ttu-id="90c93-770">В **предварительного просмотра** щелкните **публикации**.</span><span class="sxs-lookup"><span data-stu-id="90c93-770">In the **Preview** page, click **Publish**.</span></span>

    <span data-ttu-id="90c93-771">![Публикация веб-приложения](whats-new-in-aspnet-mvc-4/_static/image80.png "публикации веб-приложения")</span><span class="sxs-lookup"><span data-stu-id="90c93-771">![Publishing the web application](whats-new-in-aspnet-mvc-4/_static/image80.png "Publishing the web application")</span></span>

    <span data-ttu-id="90c93-772">*Публикация веб-приложения*</span><span class="sxs-lookup"><span data-stu-id="90c93-772">*Publishing the web application*</span></span>
9. <span data-ttu-id="90c93-773">После завершения процесса публикации в браузере по умолчанию откроется опубликованного веб-узла.</span><span class="sxs-lookup"><span data-stu-id="90c93-773">Once the publishing process finishes, your default browser will open the published web site.</span></span>

    <span data-ttu-id="90c93-774">![Публикации приложения в Windows Azure](whats-new-in-aspnet-mvc-4/_static/image81.png "публикации приложения в Windows Azure")</span><span class="sxs-lookup"><span data-stu-id="90c93-774">![Application published to Windows Azure](whats-new-in-aspnet-mvc-4/_static/image81.png "Application published to Windows Azure")</span></span>

    <span data-ttu-id="90c93-775">*Приложения, опубликованные в Windows Azure*</span><span class="sxs-lookup"><span data-stu-id="90c93-775">*Application published to Windows Azure*</span></span>