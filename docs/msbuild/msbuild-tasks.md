---
title: "MSBuild 任务 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- tasks
- MSBuild, tasks
ms.assetid: 5d3cc4a7-e5db-4f73-b707-8b6882fddcf8
caps.latest.revision: "18"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: fc2afbe7b0226cb5983aa3022ff4b24ac31fe7aa
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2017
---
# <a name="msbuild-tasks"></a>MSBuild 任务
生成平台需要能够在生成过程中执行任意数量的操作。 [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] 使用 *任务* 以执行这些操作。 任务是由 [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] 用于执行原子生成操作的可执行代码单元。  
  
## <a name="task-logic"></a>任务逻辑  
 [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] XML 项目文件格式本身无法完全执行生成操作，因此必须在项目文件之外实现任务逻辑。  
  
 任务的执行逻辑作为 .NET 类实现，此类实现 <xref:Microsoft.Build.Framework> 命名空间中定义的 <xref:Microsoft.Build.Framework.ITask> 接口。  
  
 任务类还定义项目文件中的任务可用的输入和输出参数。 通过在 [Task](../msbuild/task-element-msbuild.md) 元素上放置具有相同名称的对应属性，可在项目文件中访问由任务类公开的所有公共可设置的非静态非抽象属性。  
  
 可以通过创作一个实现 <xref:Microsoft.Build.Framework.ITask> 接口的托管类来编写自己的任务。 有关详细信息，请参阅[任务写入](../msbuild/task-writing.md)。  
  
## <a name="executing-a-task-from-a-project-file"></a>从项目文件执行任务  
 在项目文件中执行任务前，必须先通过 [UsingTask](../msbuild/usingtask-element-msbuild.md) 元素将执行任务的程序集中的类型映射到任务名称。 这使 [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] 在项目文件中找到任务时，能了解查找任务的执行逻辑的位置。  
  
 若要在 [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] 项目文件中执行任务，请创建一个与任务同名的元素，并将其指定为 `Target` 元素的子元素。 如果任务接受了参数，这些参数将作为元素的属性进行传递。  
  
 [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] 项列表和属性都可用作参数。 例如，以下代码调用 `MakeDir` 任务，并将 `MakeDir` 对象的 `Directories` 属性的值设置为上一示例中声明的 `BuildDir` 属性的值。  
  
```xml  
<Target Name="MakeBuildDirectory">  
    <MakeDir  
        Directories="$(BuildDir)" />  
</Target>  
```  
  
 任务还可将信息返回到项目文件，该信息可存储在项或属性中以供稍后使用。 例如，以下代码调用 `Copy` 任务，并将来自 `CopiedFiles` 输出属性的信息存储在 `SuccessfullyCopiedFiles` 项列表中。  
  
```xml  
<Target Name="CopyFiles">  
    <Copy  
        SourceFiles="@(MySourceFiles)"  
        DestinationFolder="@(MyDestFolder)">  
        <Output  
            TaskParameter="CopiedFiles"  
            ItemName="SuccessfullyCopiedFiles"/>  
     </Copy>  
</Target>  
```  
  
## <a name="included-tasks"></a>包括的任务  
 [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] 附带了许多任务，例如用于复制文件的[复制](../msbuild/copy-task.md)、用于创建目录的 [MakeDir](../msbuild/makedir-task.md) 以及用于编译 [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] 源代码文件的 [Csc](../msbuild/csc-task.md)。 若要了解可用任务的完整列表以及用法信息，请参阅[任务参考](../msbuild/msbuild-task-reference.md)。  
  
## <a name="overridden-tasks"></a>覆盖的任务  
 [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] 在多个位置查找任务。 第一个位置位于存储在 .NET Framework 目录中扩展名为 .OverrideTasks 的文件中。 这些文件中的任务会覆盖具有相同名称的其他任何任务，包括项目文件中的任务。 第二个位置位于 .NET Framework 目录中扩展名为 .Tasks 的文件中。 如果在这些位置中找不到任务，则会使用项目文件中的任务。  
  
## <a name="see-also"></a>另请参阅  
 [MSBuild 概念](../msbuild/msbuild-concepts.md)   
 [MSBuild](../msbuild/msbuild.md)   
 [任务写入](../msbuild/task-writing.md)   
 [内联任务](../msbuild/msbuild-inline-tasks.md)