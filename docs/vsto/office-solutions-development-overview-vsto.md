---
title: "Office 解决方案开发概述 (VSTO)"
ms.custom: ""
ms.date: "02/02/2017"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "office-development"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
helpviewer_keywords: 
  - "主互操作程序集，Office"
  - "Visual Studio 中的 Office 开发，有关开发解决方案"
ms.assetid: 5dfc519f-a851-4661-8d2b-47e0d221e10e
caps.latest.revision: 69
author: "kempb"
ms.author: "kempb"
manager: "ghogen"
caps.handback.revision: 68
---
# Office 解决方案开发概述 (VSTO)
  通过将 Microsoft Office 用作解决方案的前端，你可以利用熟悉的 Microsoft Office 用户界面和工具，例如 Word 中的文字处理功能、Excel 的数据分析功能、数据分析功能和 Outlook 的电子邮件管理功能。 你可以在 Visual Studio 中开发解决方案以自定义 Office 应用程序并添加业务流程所需的特定功能。 例如，你可以将 Word 转化为协定生成器，收集可进行编辑或不可编辑的预存在部件外部的协定。 通过使用 Excel，你可以为不同项目创建定制的自动化预算工作表。 你的用户也可以脱机使用 Office 解决方案，使复杂的解决方案比起在使用基于 Web 的体系结构时更简单实用。  
  
 本主题概述了你可以通过 Visual Studio 中 Office 开发人员工具提供的 Visual Studio Tools for Office \(VSTO\) 模板创建的 Office 解决方案的类型。 有关如何使用 Office 进行开发的常规信息，请参见 [Office 开发人员中心](https://dev.office.com/)。  
  
## 选择 Office 项目类型  
 [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] 提供了基于 VSTO 的 Office 开发的以下类型项目模板：  
  
-   **文档级自定义项**与特定文档相关联。  
  
-   **VSTO Add\-ins** 与应用程序自身相关联。  
  
 若要确定这些项目类型中的哪一个最适合你的解决方案，可思考一下你想要代码仅在打开特定文档时运行还是想只要运行应用程序就提供代码。 有关项目模板的详细信息，请参阅 [Office 项目模板概述](../vsto/office-project-templates-overview.md)。  
  
 可以创建的项目类型取决于在开发计算机上已安装的 Office 应用程序。 有关详细信息，请参阅[按 Office 应用程序和项目类型提供的功能](../vsto/features-available-by-office-application-and-project-type.md)。  
  
### 文档级自定义项  
 文档级自定义项包含与 Microsoft Office Word 或 Microsoft Office Excel 中的单个文档、工作簿或模板相关联的程序集。 打开关联的文档时，就会加载程序集。 仅当打开关联的文档时，才提供创建的自定义项中的功能。 自定义项不能进行应用程序范围内的更改，例如打开任何文档时显示新菜单项或功能区选项卡。  
  
 [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] 包括可帮助你创建文档级自定义项的工具。 你自定义的文档在 [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] 中作为设计界面承载，以便在其上通过拖放控件设计文档。 文档级项目中还提供许多其他 [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] 功能，例如“Windows 窗体”控件、拖放数据绑定和集成的调试器。  
  
 有关自定义项的详细信息，请参阅以下主题：  
  
-   [Excel 文档级自定义项编程入门](../vsto/getting-started-programming-document-level-customizations-for-excel.md)  
  
-   [Word 文档级自定义项编程入门](../vsto/getting-started-programming-document-level-customizations-for-word.md)  
  
-   [文档级自定义项的体系结构](../vsto/architecture-of-document-level-customizations.md)  
  
### VSTO 外接程序  
 VSTO 外接程序包含与 Microsoft Office 应用程序相关联的程序集。 通常情况下，启动相关联的应用程序时，VSTO 外接程序就会运行，但是用户还可以在运行应用程序之后加载 VSTO 外接程序。 无论打开哪一个文档，所创建的 VSTO 外接程序中的功能都可用于应用程序自身。  
  
 [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] 包括可帮助你创建 VSTO 外接程序的工具。 外接程序项目包含一个表示 VSTO 外接程序的自动生成的类。 此类提供的属性和事件可用于访问主机应用程序的对象模型并在加载和关闭 VSTO 外接程序时运行代码。 VSTO 外接程序项目中还提供许多其他 [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] 功能，例如 Windows 窗体和集成的调试器。  
  
 有关 VSTO 外接程序的详细信息，请参阅以下主题：  
  
-   [VSTO 外接程序编程入门](../vsto/getting-started-programming-vsto-add-ins.md)  
  
-   [VSTO 外接程序的体系结构](../vsto/architecture-of-vsto-add-ins.md)  
  
## 通过使用主互操作程序集自动化 Office 应用程序  
 通过编写访问应用程序对象模型的代码，你可以以编程方式将 Office 应用程序的功能合并到你的解决方案。 对象模型是通过各种属性和方法公开功能的类的排列。 每个 Office 应用程序的对象模型都不同。  
  
 若要使用通过 [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] 中的 Office 开发工具创建的解决方案中的 Office 应用程序的对象模型，必须使用该应用程序的主互操作程序集 \(PIA\)。 PIA 可使解决方案中的托管代码与 Office 应用程序基于 COM 的对象模型进行交互。  
  
 必须在开发计算机上的全局程序集缓存中安装并注册 Office PIA 才能执行大多数开发任务。 有关详细信息，请参阅[将计算机配置为开发 Office 解决方案](../vsto/configuring-a-computer-to-develop-office-solutions.md)。 若要运行 VSTO Office 解决方案，无需在最终用户计算机上安装 Office PIA。 有关更多信息，请参见[设计和创建 Office 解决方案](../vsto/designing-and-creating-office-solutions.md)。  
  
 有关使用 VSTO Office 解决方案中的 PIA 的详细信息，请参阅以下主题：  
  
-   [在 Office 解决方案中编写代码](../vsto/writing-code-in-office-solutions.md)  
  
-   [Office 主互操作程序集](../vsto/office-primary-interop-assemblies.md)  
  
## 在最终用户计算机上运行 Microsoft VSTO Office 解决方案  
 当创建 VSTO Office 解决方案时，请考虑部署要求可能影响开发选择的方式。  
  
### 部署选项  
 使用 ClickOnce 或 Windows Installer 部署通过使用 [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] 中的 Office 开发工具创建的解决方案。 通过 ClickOnce 部署，你可以创建自行更新解决方案，以最少的用户交互进行安装和运行。 Windows Installer \(.msi\) 文件可以轻松分发给最终用户计算机，或通过使用 Systems Management Server \(SMS\) 进行分发。 有关部署 VSTO Office 解决方案的详细信息，请参阅[部署 Office 解决方案](../vsto/deploying-an-office-solution.md)。  
  
### 安装必备程序  
 在最终用户可以运行你通过使用 [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] 中的 Office 开发工具创建的解决方案之前，必须在其计算机上安装某些必备组件。 如果通过使用 ClickOnce 或通过创建 Windows Installer 文件部署解决方案，则可以使用你的解决方案安装这些必备组件。 有关详细信息，请参阅 [用于部署的 Office 解决方案必备组件](http://msdn.microsoft.com/zh-cn/9f672809-43a3-40a1-9057-397ce3b5126e)以及[如何：在最终用户计算机上安装必备组件以运行 Office 解决方案](http://msdn.microsoft.com/zh-cn/74dd2c52-838f-4abf-b2b4-4d7b0c2a0a98)。  
  
### 安全性  
 当安装和加载 VSTO Office 解决方案时，将由 [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] 对该解决方案强制进行一系列安全性检查。 这些检查包括验证部署清单的位置是否受信任或用于对部署清单签名的证书是否受信任。 有关详细信息，请参阅[保护 Office 解决方案的安全](../vsto/securing-office-solutions.md)。  
  
## 请参阅  
 [入门（Visual Studio 中的 Office 开发）](../vsto/getting-started-office-development-in-visual-studio.md)   
 [文档级自定义项的体系结构](../vsto/architecture-of-document-level-customizations.md)   
 [VSTO 外接程序的体系结构](../vsto/architecture-of-vsto-add-ins.md)   
 [Excel 文档级自定义项编程入门](../vsto/getting-started-programming-document-level-customizations-for-excel.md)   
 [Word 文档级自定义项编程入门](../vsto/getting-started-programming-document-level-customizations-for-word.md)   
 [VSTO 外接程序编程入门](../vsto/getting-started-programming-vsto-add-ins.md)  
  
  