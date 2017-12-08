---
title: "“符号路径”命令 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: debug.symbolpath
helpviewer_keywords:
- symbol path command
- Debug.SymbolPath command
- SymbolPath command
ms.assetid: b697ef2d-3f5d-40df-b113-7068a5bec0d4
caps.latest.revision: "9"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: d446779e4f84bf19e965393f9fa1142c7e4e166a
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2017
---
# <a name="symbol-path-command"></a>“符号路径”命令
设置调试器的目录列表，以搜索符号。  
  
## <a name="syntax"></a>语法  
  
```  
Debug.SymbolPath pathname1;pathname2;... pathnameN  
```  
  
## <a name="arguments"></a>参数  
 `pathname`  
 可选。 调试器路径列表的分号分隔列表，用于搜索符号。  
  
## <a name="remarks"></a>备注  
 如果没有指定 `pathname`，该命令将列出当前符号路径。  
  
## <a name="example"></a>示例  
 该示例向符号目录的列表添加两条路径。  
  
```  
Debug.SymbolPath C:\Symbol Path 1;C:\Symbol Path 2  
```  
  
## <a name="example"></a>示例  
 该示例显示当前符号路径的分号分隔列表。  
  
```  
Debug.SymbolPath  
```  
  
## <a name="see-also"></a>另请参阅  
 [“命令”窗口](../../ide/reference/command-window.md)   
 [Visual Studio 命令](../../ide/reference/visual-studio-commands.md)