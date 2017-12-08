---
title: "测试区域 4： 签入 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- source control [Visual Studio SDK], checking items in
- source control plug-ins, checking items in
ms.assetid: d0329fa8-7a8d-4d30-b67b-6f2a97b75a30
caps.latest.revision: "11"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 3694e8f4a8cdbdac147df3d6e60324888bccf048
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2017
---
# <a name="test-area-4-check-in"></a>测试区域 4： 签入
此源代码管理插件测试区域涉及将已更新的项目发送到的版本存储区通过**签入**命令。  
  
## <a name="command-menu-access"></a>命令菜单访问  
 以下[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]集成的开发环境菜单路径使用的测试用例。  
  
##### <a name="check-in"></a>登记：  
 **文件**，**源代码管理**，**签入**。  
  
 **文件**，**签入**。  
  
 快捷菜单上，**签入**。  
  
## <a name="common-expected-behavior"></a>常见的预期的行为  
  
-   项目和文件添加到解决方案或项目源代码管理下的出现在**签入**对话框中和**挂起签入**窗口。  
  
-   后签入中，添加的项显示在源代码管理中。  
  
-   后签入中，已更新的项目将正确版本控制的存储中。  
  
## <a name="test-cases"></a>测试用例  
 以下是有关签入测试区域的特定测试用例。  
  
### <a name="case-4a-modified-items"></a>案例 4a： 修改项目  
 介绍了如何通过在操作中检查更新已被修改的源控件下的文件。  
  
|操作|测试步骤|若要验证的预期的结果|  
|------------|----------------|--------------------------------|  
|修改已被签出的文本文件，仅文件签入 (**签入**对话框)|1.用一个文本文件中创建新项目。<br />2.将解决方案添加到源代码管理。<br />3.签出和修改文本的文件。<br />4.通过签入对话框中签入 (**文件**，**源代码管理**，**签入**)。|常见的预期的行为。|  
|修改已被签出的文本文件，仅文件签入 (**挂起签入**窗口)|1.用一个文本文件中创建新项目。<br />2.将解决方案添加到源代码管理。<br />3.签出和修改文本的文件。<br />4.通过签入**挂起签入**窗口。|常见的预期的行为。|  
  
### <a name="case-4b-adding-files"></a>案例 4b： 将文件添加  
 当将文件添加到某个项目或解决方案一个项，项目或解决方案必须还更改。 因此父文件也已签出，并且必须被签入才能完成添加。  
  
|操作|测试步骤|若要验证的预期的结果|  
|------------|----------------|--------------------------------|  
|将一个文本文件添加并签入的所有内容 (**签入**对话框)|1.创建新项目。<br />2.将解决方案添加到源代码管理。<br />3.将文本文件添加到项目。<br />4.如果系统提示，请接受签出的项目。<br />5.选择中的解决方案**解决方案资源管理器**。<br />6.通过签入**签入**对话框。|常见的预期的行为。|  
|将一个文本文件添加并签入的所有内容 (**挂起签入**窗口)|1.创建新项目。<br />2.将解决方案添加到源代码管理。<br />3.将文本文件添加到项目。<br />4.如果系统提示，请接受签出的项目。<br />5.从解决方案签入**挂起签入**窗口。|常见的预期的行为|  
  
### <a name="case-4c-adding-projects"></a>案例 4c： 添加项目  
 当向解决方案添加一个项目，还必须更改解决方案。 因此，该解决方案文件还签出和必须签入才能完成添加。  
  
|操作|测试步骤|若要验证的预期的结果|  
|------------|----------------|--------------------------------|  
|将项目添加到源代码管理下的空白解决方案 (**签入**对话框)|1.创建一个空白解决方案。<br />2.将解决方案添加到源代码管理。<br />3.添加新项目。<br />4.如果系统提示，请接受签出的解决方案。<br />5.通过签入**签入**对话框。|常见的预期的行为。|  
|将项目添加到源代码管理下的空白解决方案 (**挂起签入**窗口)|1.创建一个空白解决方案。<br />2.将解决方案添加到源代码管理。<br />3.添加新项目。<br />4.如果系统提示，请接受签出的解决方案。<br />5.从解决方案签入**挂起签入**窗口。|常见的预期的行为。|  
  
## <a name="see-also"></a>另请参阅  
 [源代码管理插件的测试指南](../../extensibility/internals/test-guide-for-source-control-plug-ins.md)