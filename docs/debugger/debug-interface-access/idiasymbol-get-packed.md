---
title: 'Idiasymbol:: Get_packed |Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_packed method
ms.assetid: e42ff368-56c4-49a2-8676-f80e349efa21
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c17d60509345e1a51df615c0d2aca90e32d055f9
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49835847"
---
# <a name="idiasymbolgetpacked"></a>IDiaSymbol::get_packed
检索指定用户定义数据类型 (UDT) 是否打包的标志。  
  
## <a name="syntax"></a>语法  
  
```C++  
HRESULT get_packed (   
   BOOL* pRetVal  
);  
```  
  
#### <a name="parameters"></a>参数  
 `pRetVal`  
 [out]返回`TRUE`打包用户定义的类型; 否则，返回`FALSE`。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则为返回`S_FALSE`或错误代码。  
  
> [!NOTE]
>  返回值为`S_FALSE`表示该属性不是可用于符号。  
  
## <a name="remarks"></a>备注  
 打包的 UDT 的所有成员都位于尽可能靠近且没有干扰填充到内存边界对齐方式。  
  
## <a name="see-also"></a>请参阅  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)