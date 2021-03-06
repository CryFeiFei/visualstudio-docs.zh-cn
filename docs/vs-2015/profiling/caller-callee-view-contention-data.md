---
title: “调用方 - 被调用方”视图 - 争用数据 | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Caller/Callee view
ms.assetid: a18a1b1b-9b39-43c7-b1f3-708fd20376f6
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0e226cb5a44923e73d64a9374eb1d170e18d2428
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/16/2018
ms.locfileid: "51797606"
---
# <a name="caller--callee-view----contention-data"></a>“调用方/被调用方”视图 - 争用数据
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

“调用方/被调用方”视图显示所选函数及其父函数和子函数的争用信息。 “调用方/被调用方”视图包含三个网格。  
  
 **当前函数**在中间网格中显示，其显示所选函数的争用信息。 值包括该函数的所有阻塞争用。  
  
 **调用当前函数的函数**在顶部网格中显示，其显示调用方（父）函数对所选（当前）函数的值的各个调用。  
  
 **由当前函数调用的函数**在底部网格中显示，当前函数调用子函数时，它会显示所选函数的被调用方（子）函数的争用信息。  
  
|列|描述|  
|------------|-----------------|  
|**Type**|函数的上下文：<br /><br /> -   **0** - 当前函数<br />-   **1** - 调用当前函数的函数<br />-   **2** - 当前函数调用的函数<br /><br /> 仅在 [VSPerfReport](../profiling/vsperfreport.md) 命令行报表中。|  
|**独占阻塞的时间**|-   对于当前函数，为阻止此函数在函数体中执行代码的时间。 不包含此函数调用的函数中阻塞的时间。<br />-   对于调用方函数，为此函数调用当前函数时当前函数的部分独占阻塞的时间。<br />-   对于被调用方函数，为当前函数调用此函数时阻止此函数执行其自身代码的时间。 不包含被调用方函数调用的子函数中阻塞的时间。|  
|**独占阻塞的时间百分比**|此上下文中此函数的独占阻塞的时间占分析运行中所有阻塞的时间的百分比。|  
|**独占争用**|-   对于当前函数，为阻止此函数在函数体中执行代码的次数。 不包含在此函数调用的函数中发生的争用。<br />-   对于调用方函数，为此函数调用当前函数时出现的当前函数的独占争用数。<br />-   对于被调用方函数，为当前函数调用此函数时阻止此函数在函数体中执行代码的次数。 不包含在被调用方函数调用的函数中发生的争用。|  
|**独占争用数百分比**|此上下文中此函数的独占争用占分析运行中的所有争用的百分比。|  
|**函数地址**|函数地址或标记。|  
|**函数名**|该函数的完全限定名。|  
|**非独占阻塞的时间**|- 对于当前函数，为阻止此函数或此函数调用的其中一个函数执行的时间。 包含当前函数调用的函数中阻塞的时间。<br />- 对于调用方函数，为此函数调用当前函数时当前函数的部分非独占阻塞的时间。<br />- 对于被调用方函数，为当前函数调用此函数时阻止此函数或此函数调用的其中一个函数执行的时间。 包含被调用方函数调用的函数中阻塞的时间。|  
|**非独占阻塞的时间百分比**|此上下文中此函数的非独占阻塞时间占分析运行中的所有阻塞时间的百分比。|  
|**非独占争用**|- 对于当前函数，为阻止此函数或此函数调用的其中一个函数执行的次数。 包含在此函数调用的函数中发生的争用。<br />- 对于调用方函数，为此函数调用当前函数时出现的当前函数的非独占争用数。<br />- 对于被调用方函数，为当前函数调用此函数时阻止此函数或此函数调用的其中一个函数执行的次数。 包含在被调用方函数调用的函数中发生的争用。|  
|**非独占争用数百分比**|此上下文中此函数的独占争用占分析运行中的所有争用的百分比。|  
|**函数行号**|此函数在源文件中的起始行号。|  
|**模块名**|函数所在模块的名称。|  
|**模块路径**|函数所在模块的路径。|  
|**进程 ID**|其中出现争用的进程的进程 ID (PID)。|  
|**进程名**|进程的名称。|  
|**根函数名**|当前函数的名称。 仅在 [VSPerfReport](../profiling/vsperfreport.md) 命令行报表中。|  
|**源文件**|此函数的定义所在的源文件。|  
  
## <a name="see-also"></a>请参阅  
 [如何：自定义报告视图列](../profiling/how-to-customize-report-view-columns.md)   
 [“调用方/被调用方”视图](../profiling/caller-callee-view.md)   
 [“调用方/被调用方”视图 - 采样数据](../profiling/caller-callee-view-sampling-data.md)   
 [“调用方/被调用方”视图 - .NET 内存检测数据](../profiling/caller-callee-view-net-memory-instrumentation-data.md)   
 [“调用方/被调用方”视图 - .NET 内存采样数据](../profiling/caller-callee-view-dotnet-memory-sampling-data.md)   
 [“调用方/被调用方”视图 - 检测数据](../profiling/caller-callee-view-instrumentation-data.md)



