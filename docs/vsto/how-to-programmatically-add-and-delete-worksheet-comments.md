---
title: "如何： 以编程方式添加和删除工作表注释 |Microsoft 文档"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ranges, comments
- worksheets, comments
- comments, worksheets
ms.assetid: 3408ce22-a7b7-4e2b-bfc1-dc24d679ee73
caps.latest.revision: "53"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: c2c9e2111e02bb9669b7e915bb170e4607932978
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-programmatically-add-and-delete-worksheet-comments"></a>如何：以编程方式添加和删除工作表注释
  可以以编程方式在 Microsoft Office Excel 工作表中添加和删除注释。 可以仅向单个单元格而非多单元格区域添加注释。  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
## <a name="adding-and-deleting-a-comment-in-a-document-level-project"></a>在文档级项目中添加和删除注释  
 下面的示例假定名为 <xref:Microsoft.Office.Tools.Excel.NamedRange> 的工作表上存在名为 `dateComment` 的单单元格 `Sheet1`控件。  
  
#### <a name="to-add-a-new-comment-to-a-named-range"></a>向命名区域添加新的注释  
  
1.  调用 <xref:Microsoft.Office.Tools.Excel.NamedRange.AddComment%2A> 控件的 <xref:Microsoft.Office.Tools.Excel.NamedRange> 方法并提供注释文本。 必须将此代码置于 `Sheet1` 类中。  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#30](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#30)]
     [!code-vb[Trin_VstcoreExcelAutomation#30](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#30)]  
  
#### <a name="to-delete-a-comment-from-a-named-range"></a>删除命名区域中的注释  
  
1.  验证区域中是否存在注释并将其删除。 必须将此代码置于 `Sheet1` 类中。  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#29](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#29)]
     [!code-vb[Trin_VstcoreExcelAutomation#29](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#29)]  
  
## <a name="adding-and-deleting-a-comment-in-an-vsto-add-in-project"></a>在 VSTO 外接程序项目中添加和删除注释  
 下面的示例假定活动的工作表上存在名为 <xref:Microsoft.Office.Interop.Excel.Range> 的单单元格 `dateComment` 。  
  
#### <a name="to-add-a-new-comment-to-an-excel-range"></a>向 Excel 区域添加新的注释  
  
1.  调用 <xref:Microsoft.Office.Interop.Excel.Range.AddComment%2A> 的 <xref:Microsoft.Office.Interop.Excel.Range> 方法并提供注释文本。  
  
     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#20](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#20)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#20](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#20)]  
  
#### <a name="to-delete-a-comment-from-an-excel-range"></a>删除 Excel 区域中的注释  
  
1.  验证区域中是否存在注释并将其删除。  
  
     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#19](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#19)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#19](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#19)]  
  
## <a name="see-also"></a>另请参阅  
 [使用工作表](../vsto/working-with-worksheets.md)   
 [如何： 以编程方式显示工作表注释](../vsto/how-to-programmatically-display-worksheet-comments.md)   
 [NamedRange 控件](../vsto/namedrange-control.md)  
  
  