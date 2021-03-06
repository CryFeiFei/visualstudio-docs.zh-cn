---
title: 要解码的 URI 不有效编码 |Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: ''
ms.suite: ''
ms.technology:
- javascript
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VS.WebClient.Help.SCRIPT5025
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 029e0790-ffd1-496d-8700-3b3dbac1b6fd
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2d37ca55dfd701aaeba2af729511a5ae6a4fa5f4
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49841814"
---
# <a name="the-uri-to-be-decoded-is-not-a-valid-encoding"></a>要解码的 URI 不是有效编码
你试图解码格式不正确的 URI （统一资源标识符）。 Uri 具有特殊的语法;大多数非字母数字字符必须进行编码，才可以在 URI 中使用。 可以使用`encodeURI`并`encodeURIComponent`方法来创建一个 URI，从正常[!INCLUDE[javascript](../../javascript/includes/javascript-md.md)]字符串。  
  
 完整的 URI 组成一系列组件和分隔符。 常规形式为：  
  
```JavaScript  
<Scheme>:<first>/<second>;<third>?<fourth>  
```  
  
 在尖括号中的名称表示组件，并":"，"/"，";"和"？"是保留的字符用作分隔符。  
  
### <a name="to-correct-this-error"></a>更正此错误  
  
-   请确保要解码有效的 Uri。 您不能进行解码正常[!INCLUDE[javascript](../../javascript/includes/javascript-md.md)]字符串，因为它们可能包含无效字符。  
  
## <a name="see-also"></a>请参阅  
 [decodeURI 函数](../../javascript/reference/decodeuri-function-javascript.md)   
 [decodeURIComponent 函数](../../javascript/reference/decodeuricomponent-function-javascript.md)