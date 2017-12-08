---
title: "“列出反汇编”命令 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: debug.listdisassembly
helpviewer_keywords:
- Debug.ListDisassembly command
- list disassembly command
ms.assetid: eb363e35-e86a-4121-966f-991210c27e2a
caps.latest.revision: "13"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: f37d62a906a0f528a821586470615a63f055af23
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2017
---
# <a name="list-disassembly-command"></a>“列出反汇编”命令
开始调试进程，并允许指定如何处理错误。  
  
## <a name="syntax"></a>语法  
  
```  
Debug.ListDisassembly [/count:number] [/endaddress:expression]  
[/codebytes:yes|no] [/source:yes|no] [/symbolnames:yes|no]  
[/linenumbers:yes|no]  
```  
  
## <a name="switches"></a>开关  
 每个开关都可以使用其完整形式或缩写形式来调用。  
  
 /count: `number` [or] /c: `number` [or] /length: `number` [or] /l: `number`  
 可选。 要显示的指令数。 默认值为 8。  
  
 /endaddress: `expression` [or] /e: `expression`  
 可选。 停止反汇编的地址。  
  
 /codebytes:`yes`&#124;`no` [or] /bytes:`yes`&#124;`no` [or] /b:`yes`&#124;`no`  
 可选。 指示是否显示代码字节。 默认值是 `no`。  
  
 /source:`yes`&#124;`no` [or] /s:`yes`&#124;`no`  
 可选。 指示是否显示源代码。 默认值是 `no`。  
  
 /symbolnames:`yes`&#124;`no` [or] /names:`yes`&#124;`no` [or] /n:`yes`&#124;`no`  
 可选。 指示是否显示符号名称。 默认值是 `yes`。  
  
 [/linenumbers:`yes`&#124;`no`]  
 可选。 启用查看与源代码关联的行号。 /source 开关必须具有 `yes` 的值来使用 /linenumbers 开关。  
  
## <a name="example"></a>示例  
  
```  
>Debug.ListDisassembly  
```  
  
## <a name="see-also"></a>另请参阅  
 [“列出调用堆栈”命令](../../ide/reference/list-call-stack-command.md)   
 [“列出线程”命令](../../ide/reference/list-threads-command.md)   
 [Visual Studio 命令](../../ide/reference/visual-studio-commands.md)   
 [“命令”窗口](../../ide/reference/command-window.md)   
 [“查找/命令”框](../../ide/find-command-box.md)   
 [Visual Studio 命令别名](../../ide/reference/visual-studio-command-aliases.md)