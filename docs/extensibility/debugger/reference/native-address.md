---
title: NATIVE_ADDRESS |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- NATIVE_ADDRESS
helpviewer_keywords:
- NATIVE_ADDRESS structure
ms.assetid: 7a0cd085-bfc8-45cc-a3d4-4459070e207a
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 751b4dfc641b017a4dc3f47f90b95e8447a2b1c6
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49840423"
---
# <a name="nativeaddress"></a>NATIVE_ADDRESS
此结构表示本机地址。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef struct _tagNATIVE_ADDRESS {  
   DWORD unknown;  
} NATIVE_ADDRESS;  
```  
  
```csharp  
public struct NATIVE_ADDRESS {  
   public uint unknown;  
}  
```  
  
## <a name="terms"></a>术语  
 未知  
 （这其中的含义取决于运行时和操作系统） 本机地址。  
  
## <a name="remarks"></a>备注  
 此结构是中的联合的一部分[DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)结构时`dwKind`字段`DEBUG_ADDRESS_UNION`结构设置为`ADDRESS_KIND_NATIVE`(从值[ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md)枚举）。  
  
## <a name="requirements"></a>要求  
 标头： sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>请参阅  
 [结构和联合](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)