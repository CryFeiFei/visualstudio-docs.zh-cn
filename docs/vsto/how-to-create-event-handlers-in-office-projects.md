---
title: 如何： 在 Office 项目中创建事件处理程序
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Visual Basic [Office development in Visual Studio], event handlers
- event handlers [Office development in Visual Studio]
- Visual C# [Office development in Visual Studio], event handlers
- events [Office development in Visual Studio]
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 8b7e55ee7f094ad104d9c8eb6ef3057621bcccee
ms.sourcegitcommit: 34f7d23ce3bd140dcae875b602d5719bb4363ed1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "35254239"
---
# <a name="how-to-create-event-handlers-in-office-projects"></a>如何： 在 Office 项目中创建事件处理程序
  有几种方法在 Visual Basic 和 C# 中创建事件处理程序。 在设计视图中，可以通过双击控件，创建默认控件的事件处理程序或使用的事件窗格**属性**窗口控件上创建的任何事件处理程序。 但是，如果要在代码视图中，您可能不想要切换到设计视图若要创建事件处理程序。  
  
 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]  
  
 [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]  
  
### <a name="to-create-an-event-handler-in-visual-basic"></a>若要在 Visual Basic 中创建一个事件处理程序  
  
1.  从**类名**在代码编辑器的顶部下拉列表中，选择想要为对象创建的事件处理程序。  
  
    > [!NOTE]  
    >  如果你想要创建的事件处理程序`ThisDocument`或`ThisWorkbook`，必须选择 **（ThisDocument 事件）** 或 **（ThisWorkbook 事件）** 中**类名**下拉列表  
  
2.  从**方法名称**下拉列表顶部的代码编辑器中，选择该事件。  
  
     Visual Studio 创建的事件处理程序，并将插入点移动到新创建的事件处理程序。 如果事件处理程序已存在，插入点移动到现有的事件处理程序。  
  
### <a name="to-create-an-event-handler-in-c"></a>若要在 C# 中创建一个事件处理程序  
  
1.  创建中的事件委托**启动**通过键入一个空格后, 跟的限定的事件名称，然后键入类的事件**+=** 之后没有空格。 例如：  
  
     `this.<object name>.<event name> +=`  
  
2.  在代码行末尾，按 TAB 键两次。  
  
     Visual Studio 会自动完成的代码行，创建事件处理程序，并将插入点移动到新创建的事件处理程序。  
  
## <a name="see-also"></a>请参阅  
 [在 Office 解决方案中编写代码](../vsto/writing-code-in-office-solutions.md)   
 [演练： 针对 NamedRange 控件的事件进行编程](../vsto/walkthrough-programming-against-events-of-a-namedrange-control.md)   
 [生成 Office 解决方案](../vsto/building-office-solutions.md)  
  
  