---
title: 导出并保存代码图
ms.date: 05/16/2018
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-ide-modeling
ms.workload:
- multiple
ms.openlocfilehash: abfe8d6160d023a99e9a49480baada9acb0c8243
ms.sourcegitcommit: 209c2c068ff0975994ed892b62aa9b834a7f6077
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/17/2018
ms.locfileid: "34268369"
---
# <a name="share-code-maps"></a>共享代码图

作为 Visual Studio 项目的一部分，图像，或为 XPS 文件，可以保存代码图。

## <a name="share-a-code-map-with-other-visual-studio-users"></a>与其他 Visual Studio 用户共享代码图

使用“文件”  菜单保存代码图。

-或-

若要将代码图作为特定项目的一部分图工具栏上，选择**共享** > **移动\<CodeMapName > 到.dgml**，然后选择你想要保存项目映射。

![将映射移动到另一个项目中](../modeling/media/codemapsmovemapmenu.png)

Visual Studio 将 map 作为 *.dgml*可以与 Visual Studio Enterprise 和 Visual Studio Professional 的其他用户共享的文件。

> [!NOTE]
> 在与使用 Visual Studio Professional 的用户共享代码图之前，请确保展开所有组、显示隐藏节点和跨组链接，并检索希望其他人在你的代码图上查看的所有已删除的节点。 否则，其他用户将无法查看这些项目。
>
> 保存建模项目中的代码图或从建模项目复制到其他位置的代码图时，可能会出现以下错误：
>
> “无法在项目目录外保存 *fileName* 。 不支持链接的项。”
>
> Visual Studio 将显示错误，但还是会创建保存的版本。 若要避免错误，请在建模项目外创建代码图。 然后，可将图形保存到所需的位置。 若只是将文件复制到解决方案中的其他位置，那么尝试保存图形将不起作用。

## <a name="export-a-code-map-as-an-image"></a>代码图导出为图像

在代码图导出为图像时，可以将其复制到其他应用程序，如 Microsoft Word 或 PowerPoint。

1. 在代码图工具栏上，选择**共享** > **作为映像的电子邮件**或**复制图像**。

2. 将该图像粘贴到另一个应用程序中。

## <a name="export-the-map-as-an-xps-file"></a>将代码图导出为 XPS 文件

在代码图导出为 XPS 文件时，你可以看到它在 Internet Explorer 等的 XML 或 XAML 查看器。

1. 在代码图工具栏上，选择**共享** > **电子邮件为可移植 XPS**或**另存为可移植 XPS**。

2. 浏览到你要保存文件的位置。

3. 对代码图命名。 请确保**另存为类型**框设置为**XPS 文件 (\*.xps)**。 选择“保存” 。

## <a name="see-also"></a>请参阅

- [使用代码图中的映射相关性](../modeling/map-dependencies-across-your-solutions.md)