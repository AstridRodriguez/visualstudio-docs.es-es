---
title: IEnumDebugPropertyInfo::GetCount | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IEnumDebugPropertyInfo.GetCount
apilocation:
- scrobj.dll
helpviewer_keywords:
- IEnumDebugPropertyInfo::GetCount
ms.assetid: 83a3becd-8533-4880-9c4f-193227ff25a9
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e9270e389cc176719dcde51ef04af3a1da9f7ef7
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/16/2019
ms.locfileid: "54344543"
---
# <a name="ienumdebugpropertyinfogetcount"></a>IEnumDebugPropertyInfo::GetCount
Obtiene el número de `DebugPropertyInfo` estructuras en el enumerador.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp
HRESULT GetCount (  
   ULONG* pcelt  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `pcelt`  
 [out] Devuelve el número de `DebugPropertyInfo` estructuras en el enumerador.  
  
## <a name="return-value"></a>Valor devuelto  
 Devuelve un válidas `HRESULT`, normalmente `S_OK`.  
  
## <a name="see-also"></a>Vea también  
 [IEnumDebugPropertyInfo (interfaz)](../../winscript/reference/ienumdebugpropertyinfo-interface.md)   
 [DebugPropertyInfo (Estructura)](../../winscript/reference/debugpropertyinfo-structure.md)