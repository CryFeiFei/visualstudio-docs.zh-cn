---
title: Detach | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: d9d1b52c-7f28-467d-b1e0-512afc4e46c9
caps.latest.revision: "8"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 97d48bdcfe663fe5434622775add890166663276
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2017
---
# <a name="detach"></a>Detach
VSPerfCmd.exe“Detach”选项可断开探查器与指定进程或所有进程（如果未指定）的连接。 必须已使用采样方法初始化分析。  
  
 使用“Launch”或“Attach”选项启动的分析可以使用“Detach”断开连接。 使用后续的“Attach”命令可以重新附加探查器。  
  
 “Detach”不会关闭分析数据文件。 使用“Shutdown”选项结束分析并关闭数据文件。  
  
> [!NOTE]
>  如果已使用“Crosssession”选项指定“Start”选项，则对 VSPerfCmd /Attach 或 VSPerfCmd /Detach 的任何调用也必须指定“Crosssession”。  
  
## <a name="syntax"></a>语法  
  
```  
VSPerfCmd.exe /Detach[:PIDs|ProcessNames]  
```  
  
#### <a name="parameters"></a>参数  
 `PIDs|ProcessNames`  
 `PID` - 一个或多个进程的数字系统标识符。  
  
 `ProcessNames` - 进程的名称。 如果命名进程的多个实例正在运行，结果不可预知。  
  
 用逗号分隔多个进程。  
  
 如果未指定进程，则探查器会从所有分析的进程拆离。  
  
## <a name="valid-options"></a>有效选项  
 以下“VSPerfCmd”选项可以与单独命令行上的“Attach”选项组合。  
  
 Crosssession  
 允许分析登录会话以外的会话中的应用程序。 如果同时指定“Start”选项和“Crosssession”选项，则为必需。  
  
## <a name="example"></a>示例  
 在此示例中，“Detach”命令挂起分析，而“Shutdown”命令关闭探查器数据文件。  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
VSPerfCmd.exe /Launch:TestApp.exe  
;REM Excercise the application  
VSPerfCmd.exe /Detach  
VSPerfCmd.exe /Shutdown  
```  
  
## <a name="see-also"></a>另请参阅  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [分析独立应用程序](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [分析 ASP.NET Web 应用程序](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [分析服务](../profiling/command-line-profiling-of-services.md)