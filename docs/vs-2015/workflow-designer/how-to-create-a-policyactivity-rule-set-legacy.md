---
title: 如何： 创建 PolicyActivity 规则集 （旧版） |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- PolicyActivity activity, creating rule sets
- Rule Set Editor dialog box
- PolicyActivity activity, selecting rule sets
- Select Rule Set dialog box
- rule sets, creating for PolicyActivity
ms.assetid: f272489d-3342-4511-8b59-6a0fd7a42d70
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 7ab49957d830bf558a9dddf55cdc5e8c2f3f75d2
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49194618"
---
# <a name="how-to-create-a-policyactivity-rule-set-legacy"></a>如何：创建 PolicyActivity 规则集（旧版）
本主题介绍如何使用面向 [!INCLUDE[wfd1](../includes/wfd1-md.md)] 或 [!INCLUDE[netfx35_long](../includes/netfx35-long-md.md)] 的旧 [!INCLUDE[vstecwinfx](../includes/vstecwinfx-md.md)] 来创建策略活动规则集。  
  
 拖动后**策略**活动项从**工具箱**到工作流设计图面上，你将想要选择现有规则或创建新规则集为[PolicyActivity](http://go.microsoft.com/fwlink?LinkID=65019)活动。 选择现有规则集通过使用[选择设置规则对话框 （旧版）](../workflow-designer/select-rule-set-dialog-box-legacy.md)并使用创建规则集[规则设置编辑器对话框 （旧版）](../workflow-designer/rule-set-editor-dialog-box-legacy.md)。  
  
> [!NOTE]
>  您可以打开[规则设置编辑器对话框 （旧版）](../workflow-designer/rule-set-editor-dialog-box-legacy.md)直接通过双击对话框[PolicyActivity](http://go.microsoft.com/fwlink?LinkID=65019)是工作流设计图面的活动。  
  
### <a name="to-select-or-create-a-rule-set-for-a-policyactivity-activity"></a>为 PolicyActivity 活动选择或创建规则集  
  
1.  右键单击[PolicyActivity](http://go.microsoft.com/fwlink?LinkID=65019)，然后单击**属性**以打开**属性**窗口。  
  
2.  单击**RuleSetReference**属性。  
  
3.  执行下列操作之一：  
  
    -   单击**RuleSetReference**省略号 **[...]**，然后选择现有规则中设置[选择设置规则对话框 （旧版）](../workflow-designer/select-rule-set-dialog-box-legacy.md)。 然后转到步骤 10。  
  
         - 或 -  
  
    -   键入规则集的名称。 单击**RuleSetReference**省略号 **[...]**，然后选择**编辑**中[选择设置规则对话框 （旧版）](../workflow-designer/select-rule-set-dialog-box-legacy.md)。  
  
         或  
  
    -   键入规则集的名称。 展开**RuleSetReference**属性，然后选择省略号 **[...]** 中**RuleSet 定义**属性。  
  
         [规则设置编辑器对话框 （旧版）](../workflow-designer/rule-set-editor-dialog-box-legacy.md)随即打开。  
  
4.  在中[规则设置编辑器对话框 （旧版）](../workflow-designer/rule-set-editor-dialog-box-legacy.md)，单击**添加规则**将新规则添加到规则集。  
  
5.  输入**名称**，**优先级**，并**重新评估**属性，或保留默认值。  
  
6.  输入的文本**条件**。  
  
7.  输入的文本**Then 动作**并**Else 操作**。  
  
8.  单击**添加规则**再次以添加另一个规则。  
  
9. 完成后单击“确定” 。  
  
## <a name="see-also"></a>请参阅  
 [PolicyActivity](http://go.microsoft.com/fwlink?LinkID=65019)   
 [选择规则集对话框 （旧版）](../workflow-designer/select-rule-set-dialog-box-legacy.md)   
 [规则集编辑器对话框 （旧版）](../workflow-designer/rule-set-editor-dialog-box-legacy.md)   
 [使用 Policy 活动](http://go.microsoft.com/fwlink?LinkID=65004)   
 [旧版工作流活动](../workflow-designer/legacy-workflow-activities.md)