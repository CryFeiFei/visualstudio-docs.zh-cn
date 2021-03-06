---
title: 在调试器中查看变量占用的内存 |Microsoft Docs
ms.custom: H1Hack27Feb2017
ms.date: 10/04/2018
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.memory
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- Memory window
- strings [Visual Studio], viewing
- debugger [Visual Studio], Memory window
- memory [Visual Studio], debugging
- debugging [Visual Studio], Memory window
- buffers, viewing
ms.assetid: 7f7a0439-10e4-4966-bb2d-51f04cda4fe2
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: cdf8e5fc5ee0ac34b4c295f6cc593e0a93b548ae
ms.sourcegitcommit: a7de99f36e9ead7ea9e9bac23c88d05ddfc38b00
ms.translationtype: MTE95
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2018
ms.locfileid: "52257255"
---
# <a name="use-the-memory-windows-in-the-visual-studio-debugger-c-c-visual-basic-f"></a>使用 Visual Studio 调试器中的内存窗口 (C#，c + +、 Visual Basic 中， F#)

在调试期间，**内存**窗口将显示你的应用使用的内存空间。 

调试器窗口等**观看**，**自动**，**局部变量**，并**快速监视**对话框显示在特定于存储的变量在内存中的位置。 **内存**窗口显示在整体结构。 内存视图适用于检查大片的数据 （缓冲区和大的字符串，例如） 不显示在其他窗口中很好的。 

**内存**窗口并不局限于显示数据。 它包括数据、 代码和的无用随机位未分配的内存中的内存空间中显示的所有内容。  

**内存**窗口不可用的脚本或 SQL 调试。 这些语言不能识别内存概念。  
  
## <a name="open-a-memory-window"></a>打开内存窗口  
  
像其他调试器窗口中，**内存**windows 仅在调试会话期间都可用。 

>[!IMPORTANT]
>若要启用**内存**windows**启用地址级调试**必须在所选**工具** > **选项**（或**调试** > **选项**) >**调试** > **常规**。 

**若要打开内存窗口**
  
1. 请确保**启用地址级调试**中选择**工具** > **选项**(或**调试** > **选项**) >**调试** > **常规**。 
   
1. 开始调试通过选择绿色箭头，按**F5**，或选择**调试** > **开始调试**。  
   
2. 下**调试** > **Windows** > **内存**，选择**内存 1**，**内存 2**，**内存 3**，或**内存 4**。 (某些版本的[!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]产品/服务只有一个**内存**窗口。)  

## <a name="move-around-in-the-memory-window"></a>在内存窗口中移动  

一台计算机的地址空间很大，并且您可以轻松地丢失你的位置，通过滚动**内存**窗口。 

较高的内存地址显示在窗口的底部。 若要查看较高的地址，向下滚动。 若要查看较低的地址，请向上滚动。  

你可以立即转到中的指定地址**内存**窗口中通过使用拖放，或输入中的地址**地址**字段。 **地址**字段接受的字母数字地址和表达式的计算结果为地址，如`e.User.NonroamableId`。 

若要强制立即重新计算的表达式中的**地址**字段中，选择的舍入箭头**自动重新计算**图标。 

默认情况下**内存**窗口将**地址**用作活动表达式，将在应用运行时重新计算的表达式。 活动表达式可能很有用，例如，若要查看所指向的指针变量的内存。  

**若要使用拖放以移动到的内存位置：**  
   
1. 在任何调试器窗口中，选择内存地址或包含内存地址的指针变量。  
   
2. 地址或指针中的拖放**内存**窗口。 该地址随后会出现**地址**字段中，并**内存**窗口调整，以在顶部显示该地址。 
  
**若要通过在地址字段中输入其移动到的内存位置：**
  
- 地址或表达式中的键入或粘贴**地址**字段并按**Enter**，或从下拉列表中选择**地址**字段。 **内存**窗口调整，以在顶部显示该地址。
  
## <a name="customize-the-memory-window"></a>自定义内存窗口 

默认情况下，内存内容以十六进制格式显示为 1 字节整数，窗口宽度决定了显示的列数。 可以自定义的方式**内存**窗口显示内存内容。  
  
**若要更改内存内容的格式：**  
  
-  在中右击**内存**窗口中，并从上下文菜单中选择所需的格式。  
  
**若要更改内存窗口中的列数：**
  
- 选择向下箭头旁边**列**字段，然后选择要显示，或选择的列数**自动**根据窗口宽度自动调整。  
  
如果不希望的内容**内存**窗口更改为您的应用程序运行时，可以关闭活动表达式计算。 

**若要切换活动计算：**  
  
- 在中右击**内存**窗口中，然后选择**自动重新计算**的上下文菜单中。 

  >[!NOTE]
  >Live 表达式评估具有切换功能，并且默认情况下，因此选择位于**自动重新计算**会将其关闭。 选择**自动重新计算**再次开启。 
  
可以隐藏或显示在顶部工具栏**内存**窗口。 不将有权**地址**字段或其他工具时隐藏工具栏。  
  
**若要切换工具栏上显示：**  
  
- 在中右击**内存**窗口中，然后选择**显示工具栏**的上下文菜单中。 工具栏将出现或不出现，具体取决于它先前的状态。  
  
## <a name="follow-a-pointer-through-memory"></a>跟踪内存中的指针  

在本机代码应用中，可以将寄存器名称用作活动表达式。 例如，可以使用堆栈指针跟踪堆栈。  
  
**若要跟踪内存中的指针：**
  
1. 在中**内存**窗口**地址**字段中，输入一个指针表达式，为当前作用域中。 根据所使用的语言，可能必须取消引用指针。  
  
2. 按 **Enter**。  
   
   当使用调试命令如**步骤**，在显示的内存地址**地址**字段，然后在顶部**内存**窗口将自动更改为指针更改。  
  
## <a name="see-also"></a>请参阅  
 [在调试器中查看数据](../debugger/viewing-data-in-the-debugger.md)