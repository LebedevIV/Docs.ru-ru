---
uid: web-forms/overview/deployment/configuring-team-foundation-server-for-web-deployment/configuring-team-foundation-server-for-web-deployment
title: "Настройка Team Foundation Server для веб-развертывание | Документы Microsoft"
author: jrjlee
description: "Этого учебника показано, как настроить Team Foundation Server (TFS) 2010 для построения решений и развертывания веб-содержимого на различных целевых средах. Это..."
ms.author: aspnetcontent
manager: wpickett
ms.date: 05/04/2012
ms.topic: article
ms.assetid: ff55233a-e795-4007-a4fc-861fe1bb590b
ms.technology: dotnet-webforms
ms.prod: .net-framework
msc.legacyurl: /web-forms/overview/deployment/configuring-team-foundation-server-for-web-deployment/configuring-team-foundation-server-for-web-deployment
msc.type: authoredcontent
ms.openlocfilehash: 72f60841a1381380c0ea6167077420f960180dc7
ms.sourcegitcommit: 9a9483aceb34591c97451997036a9120c3fe2baf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2017
---
<a name="configuring-team-foundation-server-for-web-deployment"></a>Настройка Team Foundation Server для развертывания веб-приложения
====================
по [Джейсон Lee](https://github.com/jrjlee)

[Скачать PDF](https://msdnshared.blob.core.windows.net/media/MSDNBlogsFS/prod.evol.blogs.msdn.com/CommunityServer.Blogs.Components.WeblogFiles/00/00/00/63/56/8130.DeployingWebAppsInEnterpriseScenarios.pdf)

> Этого учебника показано, как настроить Team Foundation Server (TFS) 2010 для построения решений и развертывания веб-содержимого на различных целевых средах. Это включает в себя сценарии непрерывной интеграции (CI), где развертывании содержимого автоматически каждый раз, когда разработчик вносит изменение. Он также может включать триггер запуска вручную сценарии, где администратор может понадобиться запуска развертывания в промежуточной среде определенные сборки после построения и проверки проверяется в тестовой среде. Подразделы в этом учебнике проведет вас через процесс вся конфигурация, включая:
> 
> - Порядок создания нового командного проекта в Team Foundation Server.
> - Как добавлять содержимое в систему управления версиями.
> - Сведения о настройке сервера для поддержки непрерывной Интеграции и развертывания сборки.
> - Как создать определение сборки, включающее логики развертывания.
> - Сведения о настройке разрешений для автоматического развертывания.
> 
> Итальянский преобразования этих учебников, посетите [http://www.lucamorelli.it](http://www.lucamorelli.it).


В учебнике предполагается, что вы установили TFS 2010 и создания коллекции командных проектов в процессе начальной настройки. [Руководство по установке Team Foundation для Visual Studio 2010](https://go.microsoft.com/?linkid=9805132) предоставляет подробные рекомендации для этих задач.

## <a name="context"></a>Контекст

Это формирует часть серию учебников, в зависимости от требования к развертыванию enterprise вымышленная компания Fabrikam, Inc. Этот учебник ряд использует образец решения & #x 2014; [диспетчера контактов](../web-deployment-in-the-enterprise/the-contact-manager-solution.md) решения & #x 2014; для представления веб-приложения с реалистичных уровень сложности, включая приложения ASP.NET MVC 3, Windows Службы Communication Foundation (WCF) и проект базы данных.

Метод развертывания, в основе этих учебников основан на разбиение проекта файл подход, описанный в [основные сведения о процессе сборки](../web-deployment-in-the-enterprise/understanding-the-build-process.md), в которой процесс построения управляется двух проектов файлы & #x 2014; один с построение инструкции, которые применяются для каждой целевой среде и, содержащий параметры построения и развертывания конкретной среды. Во время построения файла проекта среды объединяется в файл проекта зависит от среды, образуют полный набор инструкций построения.

## <a name="scenario-overview"></a>Общие сведения о сценарии

Общие сценарии для этих учебников описан в [корпоративного веб-развертывания: Обзор сценария](../deploying-web-applications-in-enterprise-scenarios/enterprise-web-deployment-scenario-overview.md). Рекомендуется просмотреть в этом разделе, прежде чем приступить к работе в этом учебнике.

## <a name="how-to-use-this-tutorial"></a>Как использовать этот учебник

Если это первый раз выполнения задач, описанных в этом учебнике, или если вы хотите выполнить примеры, используя образец решения, будет работать через разделы учебника в порядке. Кроме того можно использовать разделы как рекомендации для выполнения конкретных задач. Этот учебник содержит следующие темы:

- [Создание командного проекта в Team Foundation Server](creating-a-team-project-in-tfs.md). Командный проект является основной единицей для системы управления версиями, управление процессами и сборки в TFS. Необходимо создать командный проект, прежде чем добавлять содержимое в систему управления версиями или создание определений построения.
- [Добавление содержимого в систему управления версиями](adding-content-to-source-control.md). После создания командного проекта можно добавлять содержимое в систему управления версиями. Необходимо добавить проектов и решений, вместе с любой внешней зависимости перед началом настройки построений.
- [Настройка TFS сервер построения для развертывания веб-](configuring-a-tfs-build-server-for-web-deployment.md). Если вы хотите создавать содержимое командного проекта, необходимо настроить на сервере построений. В большинстве случаев это должно быть на отдельном компьютере из установки TFS. Чтобы настроить сервер сборки, необходимо установите и настройка службы построения TFS, установите Visual Studio 2010, создания контроллеров и агентов построения, установить все продукты и компоненты, которые коде необходимы для успешного построения и установить Internet Information Services (IIS) веб-средства развертывания (Web Deploy).
- [Создание определения построения, поддерживающего развертывание](creating-a-build-definition-that-supports-deployment.md). Перед запуском очереди или активации сборки в TFS, необходимо создать по крайней мере одним определением построения командного проекта. Определение построения определяет каждый аспект сборки, включая какие действия должны быть включены в сборку, какие события должны запускать сборки и где Team Build должны отправлять выходные данные сборки. Можно настроить определения построения для запуска пользовательских файлов проекта Microsoft Build Engine (MSBuild), который позволяет включать логику развертывания в автоматических построениях.
- [Развертывание конкретную сборку](deploying-a-specific-build.md). В множество сценариев будет необходимо для развертывания конкретной сборки, а не последнюю сборку к целевой среде. В этом случае можно настроить определение сборки, развертывает содержимое из конкретного транзитный каталог.
- [Настройка разрешений для команды построения развертывания](configuring-permissions-for-team-build-deployment.md). Если служба сборки для развертывания содержимого в процессе автоматизированной сборки, необходимо предоставить различные разрешения учетной записи службы построения на любой целевой веб-серверов и серверов баз данных.

## <a name="key-technologies"></a>Основные технологии

Этот учебник посвящен использовать эти продукты и технологии для поддержки автоматизированной сборки и развертывания веб-приложения:

- Visual Studio Team Foundation Server 2010
- Team Build и MSBuild
- Web Deploy

При использовании Windows Server 2008 R2, IIS 7.5, SQL Server 2008 R2, ASP.NET 4.0 и ASP.NET MVC 3 также упоминаются учебника.

## <a name="other-tutorials-in-this-series"></a>Другие учебники по этой серии

Это входит в состав последовательности пять учебники на веб-развертывания корпоративного уровня. Ниже перечислены другие учебники ряда:

- [Развертывание веб-приложений в корпоративных сценариях](../deploying-web-applications-in-enterprise-scenarios/deploying-web-applications-in-enterprise-scenarios.md). Это вводная содержимое предоставляет контекстные фона для учебника ряда. Он описывает сценарий учебника, и показано, как задачи и пошаговые руководства, описанные на протяжении ряда помещаются в более широкого процесса управления жизненным циклом приложений (ALM).
- [Веб-развертывания на предприятии](../web-deployment-in-the-enterprise/web-deployment-in-the-enterprise.md). Этот учебник содержит общие сведения о файлах проектов MSBuild, конвейер публикации Web (WPP), веб-развертывания и других связанных технологий. Объясняется, как можно использовать эти средства вместе Управление процессами развертывания сложной системы.
- [Настройка серверов для развертывания веб-](../configuring-server-environments-for-web-deployment/configuring-server-environments-for-web-deployment.md). Этот учебник описывается настройка серверов Windows для поддержки различных сценариев развертывания, включая удаленный веб-развертывания пакета, используя службу агента веб-развертывания (удаленный агент) или веб-обработчик развертывания и развертывания удаленной базы данных. Оно содержит инструкции о выборе метода соответствующие развертывания для вашей рабочей среде и описываются способы использования веб-фермы (WFF) реплицировать развернутых веб-приложений на веб-серверах в ферме серверов.
- [Расширенный корпоративного веб-развертывания](../advanced-enterprise-web-deployment/advanced-enterprise-web-deployment.md). Этот учебник описывает, как выполнять различные более сложных задач развертывания, таких как Настройка развертывания базы данных для нескольких сред, за исключением файлов и папок из развертывания и получение веб-приложения в автономный режим во время развертывания .

>[!div class="step-by-step"]
[Вперед](creating-a-team-project-in-tfs.md)