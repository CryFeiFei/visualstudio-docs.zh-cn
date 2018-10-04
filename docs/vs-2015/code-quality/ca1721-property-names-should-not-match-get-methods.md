---
title: CA1721： 属性名不应与 get 方法 |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- CA1721
- PropertyNamesShouldNotMatchGetMethods
helpviewer_keywords:
- CA1721
- PropertyNamesShouldNotMatchGetMethods
ms.assetid: 45a0e853-1f06-4688-af1b-cc634409e295
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 78a87e13b7c97dbe3d6487a721b9b439892bae7f
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/24/2018
ms.locfileid: "47587509"
---
# <a name="ca1721-property-names-should-not-match-get-methods"></a>CA1721：属性名不应与 get 方法冲突
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[CA1721： 属性名不应与 get 方法](https://docs.microsoft.com/visualstudio/code-quality/ca1721-property-names-should-not-match-get-methods)。

|||
|-|-|
|TypeName|PropertyNamesShouldNotMatchGetMethods|
|CheckId|CA1721|
|类别|Microsoft.Naming|
|是否重大更改|重大|

## <a name="cause"></a>原因
 公共或受保护成员的名称以 Get，否则匹配公共或受保护的属性的名称。 例如，包含名为 GetColor 和名为 Color 的属性的方法的类型与此规则冲突。

## <a name="rule-description"></a>规则说明
 Get 方法和属性应具有明确表示其功能的名称。

 命名约定提供了通用的外观对于库面向公共语言运行时。 这将减少所需了解新的软件库，并使客户进一步库由在托管代码开发具有专业知识的人员的时间。

## <a name="how-to-fix-violations"></a>如何解决冲突
 更改名称，以便与前缀为 Get 方法的名称不匹配。

## <a name="when-to-suppress-warnings"></a>何时禁止显示警告
 不禁止显示此规则发出的警告。

> [!NOTE]
>  如果 Get 方法由实现 IExtenderProvider 接口可能排除此警告。

## <a name="example"></a>示例
 下面的示例包含方法和属性都与此规则冲突。

 [!code-csharp[FxCop.Naming.GetMethod#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Naming.GetMethod/cs/FxCop.Naming.GetMethod.cs#1)]
 [!code-vb[FxCop.Naming.GetMethod#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Naming.GetMethod/vb/FxCop.Naming.GetMethod.vb#1)]

## <a name="related-rules"></a>相关的规则
 [CA1024：在适用处使用属性](../code-quality/ca1024-use-properties-where-appropriate.md)


