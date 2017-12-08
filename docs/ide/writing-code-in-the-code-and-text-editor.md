---
title: "在代码编辑器中编写代码 | Microsoft Docs"
ms.custom: 
ms.date: 09/27/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.texteditor
dev_langs:
- JScript
- VB
- CSharp
helpviewer_keywords:
- code editor, word wrap
- outlining
- code, editing
- squiggles
- code editor, outlining
- code editor, error and warning markers
- word wrap
- code editor, syntax coloring
- code editor, go to definition
- diff
- code editor [Visual Studio]
- code editor, diff
- error and warning markers
- code editor, navigation bar
- code editor, customizing
- comment selection
- code editor, tabify
- brace matching
- code editor, line numbers
- printing
- code editor, brace matching
- code editor, squiggles
- code editor, features
- line numbers
- go to definition
- syntax coloring
- code editor, go to
- code editor, comparing files
- code editor, zoom
- code editor
- code files
- go to line
- tabify
- zoom
- go to
- line break characters
- code editor, virtual space
- code editor, change tracking
- code editor, comment selection
- code editor, printing
- virtual space
- code editor, line break characters
- code editor, go to line
- code
ms.assetid: cb53ab9a-5b76-4759-b9e8-7bf32298ecbe
caps.latest.revision: "44"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: bb8229cffc2a3e30e3ce5a3a42af7e1673d11f3d
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2017
---
# <a name="write-code-in-the-code-editor"></a>在代码编辑器中编写代码
Visual Studio 编辑器提供了许多功能，可方便你更加轻松地编写和管理代码和文本。 可通过使用大纲显示来展开和折叠不同的代码块。 可通过使用 IntelliSense、“对象浏览器”以及调用层次结构，了解有关代码的详细信息。 可使用“转到”、“转到定义”和“查找所有引用”等功能查找代码。 可以将插入代码块和代码片段，并且可以通过“使用时生成” 等功能生成代码。 如果之前从未用过 Visual Studio 编辑器，请参阅[编辑代码](https://www.visualstudio.com/features/ide-vs)进行快速概览。  

 可以使用多种不同的方式查看自己的代码。 默认情况下，“解决方案资源管理器” 显示按文件组织的代码。 可以单击窗口底部的“类视图”选项卡，查看按类组织的代码。

 可以搜索和替换单个或多个文件中的文本。 有关详细信息，请参阅[查找和替换文本](../ide/finding-and-replacing-text.md)。 可以使用正则表达式来查找和替换文本。 有关详细信息，请参阅[在 Visual Studio 中使用正则表达式](../ide/using-regular-expressions-in-visual-studio.md)。  

 不同的 Visual Studio 语言提供不同的功能集，在某些情况下，同样的功能在不同语言中的行为也会有所不同。 功能说明中已指出多数差异，但如需有关详细信息，可以参阅特定 Visual Studio 语言相关章节。  

> [!IMPORTANT]
>  正在使用的 Visual Studio 版本和设置可能会影响 IDE 中的功能。 它们可能与本主题中介绍的功能有所不同。  

## <a name="editor-features"></a>编辑器功能  

|||  
|-|-|  
|语法着色|用不同颜色对代码和标记文件中某些语法元素着色，从而将它们区分开来。 例如，关键字（如 C# 中的 `using` 和 Visual Basic 中的 `Imports` ）用一种颜色，类型（如 `Console` 和 `Uri`用另一种颜色。 也为其他语法元素（如字符串文本和注释）着色。 C++ 使用颜色来区分类型、枚举、宏以及其他标记。<br /><br /> 可以看到每种类型的默认颜色，并且可以更改可从“工具”菜单打开的 [Fonts and Colors, Environment, Options Dialog Box](../ide/reference/fonts-and-colors-environment-options-dialog-box.md)中任意特定语法元素的颜色  。|  
|错误和警告标记|添加代码和生成解决方案时，可能会看到 (a) 不同颜色的波浪下划线（称为波形曲线）或者 (b) 灯泡显示在你的代码中。 红色波浪线表示语法错误，蓝色表示编译器错误，绿色表示警告，而紫色表示其他类型的错误。 [灯泡](../ide/perform-quick-actions-with-light-bulbs.md) 建议了问题的修补程序，并简化修补程序的应用。<br /><br /> 可在“工具/选项/环境/字体和颜色”  对话框中看到每种错误和警告曲线的默认颜色。 查找“语法错误” 、“编译器错误” 、“警告” 和“其他错误” 。|  
|括号匹配|插入点放置在代码文件中的左大括号上时，将突出显示左大括号和右大括号。 此功能可为你提供有关错放或丢失大括号的即时反馈。 可以使用“自动突出显示分隔符”  设置来启用或禁用大括号匹配（“工具/选项/文本编辑器”）。 可以在“字体和颜色”  设置中更改突出显示颜色（“工具/选项/环境”）。 查找“大括号匹配（突出显示）”  或“大括号匹配（方括号）” 。|  
|结构可视化工具|在代码文件中，成对的大括号用虚线相连，方便你更加轻松地辨别左大括号和右大括号对。 这样一来，你可以在代码库中更快速地找到代码。 可以使用“工具”/“选项”/“文本编辑器”/“常规”页上“显示”部分中的“显示结构准则”启用或禁用这些代码行。|
|行号|可在代码窗口的左边距中显示行号。 默认情况下不显示行号。 可在“文本编辑器的所有语言”  设置中启用此选项（“工具/选项/文本编辑器/所有语言”）。 可以通过更改各编程语言的设置来显示其行号（“工具/选项/文本编辑器/\<语言>”）。 对于要打印的行号，必须在“打印”对话框中选择“包括行号”。|  
|更改跟踪|左边距的颜色使你能够跟踪在文件中所做的更改。 打开文件后所做的未保存的更改将由左边距上的黄色栏（称为选定内容的边距）表示。 保存更改后（但在关闭文件前），该栏将变为绿色。 如果在保存文件后撤消更改，则该栏将变为橙色。 若要禁用和启用此功能，请在“文本编辑器”  设置中更改“跟踪更改”  选项（“工具/选项/文本编辑器”）。|  
|选择代码和文本|可以在标准的连续流模式或框模式中选择文本，你将在其中选择一个矩形部分的文本而非一组文本行。 若要在框模式中进行选择，请在将鼠标拖到选定内容上时按下 Alt 键（或按 Alt + Shift + \<箭头键>）。 选定内容包括由所选范围中第一个字符和最后一个字符所定义的矩形内的所有字符。 键入或粘贴到所选区域内的任何内容均将在每行中的相同点插入。|  
|缩放|可以通过按住 CTRL 键并移动鼠标滚轮（或按 CTRL + SHIFT + . 进行放大，CTRL + SHIFT + , 进行缩小）在任何代码窗口中进行放大或缩小。 可以使用代码窗口左下角的“缩放”框设置特定的缩放百分比。 缩放功能不适用于工具窗口。|  
|虚空格|默认情况下，Visual Studio 编辑器中的行在最后一个字符后结束，从而行尾的向右键会将光标移到下一行的开头。 在某些其他编辑器中，行并不在最后一个字符后结束，你可以将光标放置在行上的任意位置。 可以在“工具/选项/文本编辑器/所有语言”  设置中启用编辑器中的虚空格。 请注意，可以启用“虚空格”  或“自动换行” 之一，但不能同时启用这两者。|  
|打印|打印文件时，可以使用“打印”  对话框中的选项来包括行号或隐藏折叠的代码区域。 在“页面设置”  对话框中，还可以通过选择“页面页眉” 来打印完整路径及文件名。<br /><br /> 可以在“工具/选项/环境/字体和颜色”  对话框中设置颜色打印选项。 在“显示以下对象的设置”  列表中选择“打印机”  ，以自定义彩色打印。 可以为打印文件而非编辑文件指定不同的颜色。|  
|全局撤消和重做|“编辑”  菜单上的“撤消上次全局操作”  和“重做上一全局操作”  命令可撤消或重做影响多个文件的全局操作。 全局操作包括重命名类或命名空间、在解决方案中执行查找和替换操作、重构数据库或更改多个文件的任何其他操作。 可对当前 Visual Studio 会话中的操作应用全局撤消和重做命令（甚至在关闭应用操作的解决方案之后）。|  

## <a name="advanced-editing-features"></a>高级编辑功能  
 可以在“编辑/高级”  子菜单中找到许多高级功能。 并非所有这些功能都可用于所有类型的代码文件。  

|||  
|-|-|  
|设置文档的格式|设置适当的代码行缩进，并移动大括号以分隔文档中的行。|  
|设置选定内容的格式|设置适当的代码行缩进，并移动大括号以分隔选定内容中的行。|  
|将选定行中的空格替换为制表符|在适当的位置将前导空格更改为选项卡。|  
|将选定行中的制表符替换为空格|将前导制表符更改为空格。 如果要将文件中的所有空格都转换为制表符（或将所有制表符转换为空格），可以使用 `Edit.ConvertSpacesToTabs` 和 `Edit.ConvertTabsToSpaces` 命令。 这些命令不会出现在 Visual Studio 菜单中，但可以从快速访问窗口或命令窗口中进行调用。|  
|转换为大写|将选定内容中的所有字符更改为大写；如果未选择任何内容，则将插入点处的字符更改为大写。|  
|转换为小写|将选定内容中的所有字符更改为小写；如果未选择任何内容，则将插入点处的字符更改为小写。|  
|将选定行上移|将选定行上移一行。 快捷键：ALT + 向上箭头。|
|将选定行下移|将选定行下移一行。 快捷键：ALT + 向下箭头。|
|验证文档|验证 JScript 代码文件。|  
|删除水平空白|删除当前行末尾的制表符或空格。|  
|查看空白|将空格显示为上移的点，将制表符显示为箭头。 文件末尾将显示为矩形标志符号。 如果已选择“工具/选项/文本编辑器/所有语言/自动换行/显示可见的自动换行标志符号”  ，则也将显示该标志符号。|  
|自动换行|使文档中的所有行在代码窗口中均可见。 可以在“文本编辑器的所有语言”设置中禁用和启用自动换行（“工具/选项/文本编辑器/所有语言”）。|  
|注释选定内容|向选定内容或当前行添加注释字符。|  
|取消注释选定内容|从选定内容或当前行删除注释字符。|  
|增加行缩进|向所选行或当前行添加一个制表符（或等效空格）。|  
|减少行缩进|从所选行或当前行删除一个制表符（或等效空格）。|  
|选择标记|在包含标记（如 XML 或 HTML）的文档中选择标记。|  
|选择标记内容|在包含标记（如 XML 或 HTML）的文档中选择内容。|  

## <a name="navigate-and-find-code"></a>导航和查找代码  
可以使用多种不同的方式在代码编辑器中移动，包括向后和向前导航至之前的插入点、查看类型或成员的定义以及使用导航栏跳转到特定方法。 有关详细信息，请参阅[导航代码](navigating-code.md)。  

## <a name="finding-references-in-your-code-base"></a>在代码库中查找引用  
若要在整个代码库中查找引用特定代码元素的位置，可以使用“查找所有引用”命令。 此外，在单击类型或成员时，“引用突出显示”功能会自动突出显示该类型或成员的所有引用。 有关详细信息，请参阅[在代码中查找引用](finding-references.md)。  

## <a name="customize-the-editor"></a>自定义编辑器  
可以与其他开发者共享 Visual Studio 设置，可以让自己的设置符合某一标准，也可以使用“工具”菜单上的“导入和导出设置向导”命令恢复 Visual Studio 默认设置。 在“导入和导出设置向导”中，可以更改选定常规设置或语言以及项目专属设置。

若要定义新热键或重新定义现有热键，请依次转到“工具”、“选项”、“环境”和“键盘”。 有关热键的详细信息，请参阅[默认键盘快捷键](../ide/default-keyboard-shortcuts-in-visual-studio.md)。  

若要详细了解如何自定义编辑器，请参阅[自定义编辑器](../ide/customizing-the-editor.md)。 若要了解语言专用编辑器选项，请参阅[将 Visual Studio 开发环境用于 C#](../csharp-ide/using-the-visual-studio-development-environment-for-csharp.md) 和[选项、文本编辑器、JavaScript、格式](../ide/reference/options-text-editor-javascript-formatting.md)。

## <a name="see-also"></a>另请参阅  
 [Visual Studio IDE](../ide/visual-studio-ide.md)