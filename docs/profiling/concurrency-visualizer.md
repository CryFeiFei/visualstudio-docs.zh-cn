---
title: "并发可视化工具 | Microsoft Docs"
ms.custom: 
ms.date: 07/11/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- vs.cv.performance.viewnavigation
- vs.cv.overview
- vs.cv.performance.gettingstarted
- vs.cv.gettingstarted
helpviewer_keywords: Concurrency Visualizer, Concurrency Visualizer
ms.assetid: ae5879a0-1e1a-455a-ba72-148e57f59289
caps.latest.revision: "31"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 9b76decbfcb314733d0b195baeda24474e9574d2
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2017
---
# <a name="concurrency-visualizer"></a>并发可视化工具
> [!NOTE]
>  对于 Visual Studio，并发可视化工具是可选扩展。 从以下链接下载并发可视化工具和并发可视化工具收集工具：  
>   
>  -   下载 [Visual Studio 2015 的并发可视化工具](https://visualstudiogallery.msdn.microsoft.com/a6c24ce9-beec-4545-9261-293061436ee9)扩展。  
> -   下载              [Visual Studio 2015 的并发可视化工具收集工具](http://www.microsoft.com/en-in/download/details.aspx?id=49103)。  
>   
>      [并发可视化工具命令行实用工具(CVCollectionCmd)](../profiling/concurrency-visualizer-command-line-utility-cvcollectioncmd.md) 使你能够从命令行收集跟踪，可以在 Visual Studio 2015 的并发可视化工具中查看该命令行。 该工具可以在未安装 Visual Studio 的计算机上使用。  
  
 使用并发可视化工具，可以检查多线程应用的执行方式。 并发可视化工具中的视图提供图形、表格和文本形式的数据，可表明程序中的线程与整个系统之间的时态关系。 可以使用并发可视化工具查找性能瓶颈、CPU 利用率不足、线程争用、跨内核线程迁移、同步延迟、DirectX 活动、I/O 重叠区域和其他信息。 这些视图通过将其图形输出与调用堆栈和源代码关联在一起，提供可操作数据。  

> [!NOTE]
>  并发可视化工具目前不支持 Visual Studio 2017。 并发可视化工具不支持 Web 项目。  
  
 并发可视化工具依赖 [Windows 事件跟踪](http://go.microsoft.com/fwlink/?LinkId=234579) 功能。  
  
## <a name="related-topics"></a>相关主题  
  
|标题|描述|  
|-----------|-----------------|  
|[使用率视图](../profiling/utilization-view.md)|介绍如何在所有处理器中查看和分析系统活动。|  
|[“线程”视图](../profiling/threads-view-parallel-performance.md)|介绍如何分析程序中线程之间的交互。|  
|[“核心”视图](../profiling/cores-view.md)|介绍如何分析跨越核心的线程迁移。|  
|[性能不佳的多线程应用程序的常见模式](../profiling/common-patterns-for-poorly-behaved-multithreaded-applications.md)|描述若干常见模式并展示其在并发可视化工具中的显示方式。|  
|[Visual Studio 博客中的并行开发](http://go.microsoft.com/fwlink/?LinkId=235385)|提供关于并发可视化工具的提示和最佳做法。|  
|[性能报告视图](../profiling/performance-report-views.md)|提供有关 Visual Studio 分析工具报告和视图的参考信息。|  
|[并发可视化工具 SDK](../profiling/concurrency-visualizer-sdk.md)|描述如何检测你的源代码，以便在并发可视化工具中显示附加信息。|  
|[并发可视化工具命令行实用工具 (CVCollectionCmd)](../profiling/concurrency-visualizer-command-line-utility-cvcollectioncmd.md)|描述如何使用并发可视化工具命令行实用程序 (CVCollectionCmd.exe) 在未安装 Visual Studio 的计算机上收集并处理跟踪信息。|  
  
## <a name="see-also"></a>另请参阅  
 [使用 Visual Studio 分析](../profiling/index.md)  
 [分析功能简介](../profiling/profiling-feature-tour.md)