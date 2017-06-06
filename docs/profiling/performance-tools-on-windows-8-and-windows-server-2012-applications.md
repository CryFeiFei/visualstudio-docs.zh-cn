---
title: "分析 Windows 8 和 Windows Server 2012 应用程序 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a704215d-d252-4087-921b-ac81ebe2a9c9
caps.latest.revision: 15
author: "mikejo5000"
ms.author: "mikejo"
manager: "ghogen"
caps.handback.revision: 13
---
# <a name="performance-tools-on-windows-8-and-windows-server-2012-applications"></a>Windows 8 和 Windows Server 2012 应用程序上的性能工具
Windows 8 和 Windows Server 2012 中增强的安全功能需要对 Visual Studio 性能工具在这些平台上收集数据的方式进行重大更改。 Windows 应用商店应用程序也需要新的收集技术。 本主题介绍针对 Windows 8 和 Windows Server 2012 平台上的性能工具的更改。  
  
> [!NOTE]
>  其他受支持的 Windows 版本（Windows 7、Windows Server 2008 R2）的性能工具未更改。  
  
##  <a name="a-namebkmkinthistopica-in-this-topic"></a><a name="BKMK_In_this_topic"></a> 主题内容  
 [从 Visual Studio IDE 收集有关 Windows 应用商店应用的数据](#BKMK_Profiling_Windows_Store_apps_from_the_Visual_Studio_IDE)  
  
 [从 Visual Studio IDE 收集有关在 Windows 8 桌面上或 Windows Server 2012 上运行的应用的数据](#BKMK_Profiling_apps_running_on_the_Windows_8_desktop_or_on_Windows_Server_2012_from_the_Visual_Studio_IDE)  
  
-   [从 Visual Studio IDE 使用采样收集有关在 Windows 8 桌面上或 Windows Server 2012 上运行的应用的数据](#BKMK_Profiling_apps_running_on_the_Windows_8_desktop_or_on_Windows_Server_2012_by_using_sampling_from_the_Visual_Studio_IDE)  
  
 [从命令行分析](#BKMK_Profiling_from_the_command_line)  
  
 [收集层交互 (TIP) 数据](#BKMK_Collecting_tier_interaction__TIP__data)  
  
##  <a name="a-namebkmkprofilingwindowsstoreappsfromthevisualstudioidea-collecting-data-on-windows-store-apps-from-the-visual-studio-ide"></a><a name="BKMK_Profiling_Windows_Store_apps_from_the_Visual_Studio_IDE"></a> 从 Visual Studio IDE 收集有关 Windows 应用商店应用的数据  
 分析在 JavaScript 和 HTML 5 中编写的 Windows 应用商店应用程序时，应收集 JavaScript 代码的检测数据。 分析在 Visual C++、Visual C# 或 Visual Basic 中编写的 Windows 应用商店应用程序或组件时，应收集本机代码和托管代码的采样数据。 可以在本地或远程计算机上分析应用。  
  
 分析 Windows 应用商店应用程序时不支持这些分析功能和选项：  
  
-   使用采样方法分析 JavaScript 应用。  
  
-   使用检测方法分析托管代码和本机代码。  
  
-   并发分析  
  
-   .NET 内存分析  
  
-   层交互分析 (TIP)  
  
-   采样选项，如设置采样事件和计时间隔，或收集其他性能计数器数据。  
  
-   检测选项，如收集性能和窗口计数器数据，或指定其他命令行选项。  
  
 有关分析 Windows 应用商店应用的详细信息，请参阅以下主题：  
  
 [在本地计算机上运行 Windows 应用商店应用](../debugger/run-windows-store-apps-on-the-local-machine.md)  
  
 [在远程计算机上运行 Windows 应用商店应用](../debugger/run-windows-store-apps-on-a-remote-machine.md)  
  
 [分析工具](profiling-tools.md)  
  
-   [JavaScript 内存](../profiling/javascript-memory.md)
  
-   [分析本地计算机上的 Windows 应用商店应用中的 Visual C++、Visual C# 和 Visual Basic 代码](http://msdn.microsoft.com/en-us/2d0c939e-0bac-48c5-b727-46f6c6113060)  
  
-   [分析远程设备上的 Windows 应用商店应用中的 Visual C++、Visual C# 和 Visual Basic 代码](http://msdn.microsoft.com/en-us/b932a2be-11b0-40fd-b996-75c6b6a79d22)  
  
-   [分析 Windows 应用商店应用中的 Visual C++、Visual C# 和 Visual Basic 代码的性能数据](http://msdn.microsoft.com/en-us/5de4a413-d924-425f-afc4-e1ecfb0fca18)  
  
 [主题内容](#BKMK_In_this_topic)  
  
##  <a name="a-namebkmkprofilingappsrunningonthewindows8desktoporonwindowsserver2012fromthevisualstudioidea-collecting-data-on-apps-running-on-the-windows-8-desktop-or-on-windows-server-2012-from-the-visual-studio-ide"></a><a name="BKMK_Profiling_apps_running_on_the_Windows_8_desktop_or_on_Windows_Server_2012_from_the_Visual_Studio_IDE"></a> 从 Visual Studio IDE 收集有关在 Windows 8 桌面上或 Windows Server 2012 上运行的应用的数据  
 针对 Windows 8，使用检测方法进行分析并未更改。  
  
 使用采样方法时不支持层交互分析 (TIP)。  
  
###  <a name="a-namebkmkprofilingappsrunningonthewindows8desktoporonwindowsserver2012byusingsamplingfromthevisualstudioidea-collecting-data-on-apps-running-on-the-windows-8-desktop-or-on-windows-server-2012-by-using-sampling-from-the-visual-studio-ide"></a><a name="BKMK_Profiling_apps_running_on_the_Windows_8_desktop_or_on_Windows_Server_2012_by_using_sampling_from_the_Visual_Studio_IDE"></a> 从 Visual Studio IDE 使用采样收集有关在 Windows 8 桌面上或 Windows Server 2012 上运行的应用的数据  
 使用采样方法分析 Windows 8 桌面应用程序或 Windows Server 2012 应用程序时不支持这些分析功能和选项。  
  
-   层交互分析 (TIP)。 使用检测时支持收集 TIP 数据。  
  
-   采样选项，如设置采样事件和计时间隔，或收集其他性能计数器数据。  
  
##  <a name="a-namebkmkprofilingfromthecommandlinea-profiling-from-the-command-line"></a><a name="BKMK_Profiling_from_the_command_line"></a> 从命令行分析  
 你使用两个命令行工具收集 Windows 8 和 Windows Server 2012 设备上的分析数据，这些设备包括未安装 Visual Studio 的设备：  
  
|工具名称|描述|  
|---------------|-----------------|  
|[VSPerf](../profiling/vsperf.md)|从 Windows 应用商店应用程序收集分析数据，并从 Windows 8 桌面应用程序和 Windows Server 2012 应用程序收集采样分析数据。|  
|[VSPerfCmd](../profiling/vsperfcmd.md)|从在 Windows 8 桌面和 Windows Server 2012 上运行的应用收集检测、并发和层交互分析数据。 从之前版本的 Windows 收集所有类型的分析数据。|  
  
 这两个工具都随 Visual Studio 一起安装以用于本地计算机。  
  
 若要分析未安装 Visual Studio 的设备上的应用程序，请执行以下操作之一：  
  
-   从 [MSDN 网站](http://go.microsoft.com/fwlink/?LinkID=219549)上下载这些工具作为 Visual Studio 远程工具的一部分。  
  
-   从你的 Visual Studio 计算机复制并运行独立探查器工具安装程序。 安装程序位于 *%VSInstallDir%* **\Team Tools\Performance Tools\Setups** 文件夹。 为远程计算机的操作系统 (x86/x64) 选择安装程序。  
  
> [!NOTE]
>  若要收集 TIP 分析数据，必须从远程计算机上的 Visual Studio 计算机安装独立探查器。  
  
 当从命令行分析 Windows 8 和 Windows Server 2012 应用程序时不支持这些分析功能和选项：  
  
-   通过将采样模式与 [VSPerfASPNetCmd](../profiling/vsperfaspnetcmd.md) 一同使用，从 Windows 8 和 Windows Server 2012 Web 应用收集数据。  
  
-   通过使用 VsPerfCmd.exe 收集采样数据。  
  
-   采样选项，如设置采样事件和计时间隔，或收集其他性能计数器数据。  
  
##  <a name="a-namebkmkcollectingtierinteractiontipdataa-collecting-tier-interaction-tip-data"></a><a name="BKMK_Collecting_tier_interaction__TIP__data"></a> 收集层交互 (TIP) 数据  
 层交互分析提供有关多层应用程序函数执行时间的附加信息，这些应用程序通过 ADO.NET 服务与数据库进行通信。 仅针对同步函数调用收集数据。  
  
 **Visual Studio 版本**  
  
 可以使用 [!INCLUDE[vsUltLong](../code-quality/includes/vsultlong_md.md)]、[!INCLUDE[vsPreLong](../code-quality/includes/vsprelong_md.md)] 或 [!INCLUDE[vs_pro_current_short](../profiling/includes/vs_pro_current_short_md.md)] 收集层交互分析数据。 但是，只能在 [!INCLUDE[vsUltLong](../code-quality/includes/vsultlong_md.md)] 和 [!INCLUDE[vsPreLong](../code-quality/includes/vsprelong_md.md)] 中查看层交互分析数据。  
  
 **Windows 8 和 Windows Server 2012**  
  
1.  若要从在 Windows 8 桌面或 Windows Server 2012 上运行的应用中收集层交互数据，必须使用检测方法。  
  
2.  不能收集 Windows 应用商店应用的层交互数据。  
  
3.  您可以在所有分析方法中包含有关其他支持的 Windows 版本的层交互数据。  
  
 **性能向导和性能资源管理器**  
  
 必须从性能资源管理器将层交互数据收集选项添加到性能运行。 还必须将项目、可执行文件或网站添加到性能资源管理器的目标节点。 请参阅[收集层交互数据](../profiling/collecting-tier-interaction-data.md)。  
  
 **在远程计算机上收集 TIP 数据**  
  
 若要在远程计算机上收集层交互数据，必须从 Visual Studio 计算机上的 *%VSInstallDir%***\Team Tools\Performance Tools\Setups** 文件夹中将 **vs_profiler_***\<Platform>***_***\<Language>***.exe** 文件复制到远程计算机上并进行安装。 不能使用[远程调试](../debugger/remote-debugging.md)下载包中的分析工具。  
  
 可以使用 [VSPerfCmd](../profiling/vsperfcmd.md) 或 [VSPerfASPNetCmd](../profiling/vsperfaspnetcmd.md) 收集分析数据。  
  
 **TIP 报告**  
  
 只能在 [!INCLUDE[vsUltLong](../code-quality/includes/vsultlong_md.md)] 或 [!INCLUDE[vsPreLong](../code-quality/includes/vsprelong_md.md)] IDE 中查看层交互数据。 通过 [VSPerfReport](../profiling/vsperfreport.md) 生成的基于文件的层交互报告不可用。  
  
## <a name="see-also"></a>另请参阅  
 [性能资源管理器](../profiling/performance-explorer.md)   
 [配置性能会话](../profiling/configuring-performance-sessions.md)   
 [从命令行分析](../profiling/using-the-profiling-tools-from-the-command-line.md)


<!--HONumber=Feb17_HO4-->

