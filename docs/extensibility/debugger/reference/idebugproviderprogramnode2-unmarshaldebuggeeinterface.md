---
title: IDebugProviderProgramNode2::UnmarshalDebuggeeInterface | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
helpviewer_keywords:
- IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
ms.assetid: 2e4653c5-10f1-493c-9973-f31d266c5d48
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1af69580293e4ff37d0a23e3050955c96cc8f10b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "54988277"
---
# <a name="idebugproviderprogramnode2unmarshaldebuggeeinterface"></a>IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
Obtiene una interfaz especificada a través de los límites del proceso.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp  
HRESULT UnmarshalDebuggeeInterface(  
   REFIID riid,  
   void** ppvObject  
);  
```  
  
```csharp  
int UnmarshalDebuggeeInterface(  
   ref Guid   riid,  
   out IntPtr ppvObject  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `riid`  
 [in] GUID de la interfaz para obtener.  
  
 `ppvObject`  
 [out] Devuelve el objeto que implementa la interfaz deseada. [C++] se puede convertir directamente en el tipo de interfaz deseado. [C#] use la <xref:System.Runtime.InteropServices.Marshal.GetObjectForIUnknown%2A> método para obtener la interfaz deseada.  
  
## <a name="return-value"></a>Valor devuelto  
 Si es correcto, devuelve `S_OK`; en caso contrario, devuelve un código de error.  
  
## <a name="remarks"></a>Comentarios  
 Este método se utiliza cuando se ejecuta el motor de depuración en el [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] espacio de proceso y el programa que se está depurando se ejecuta en su propio espacio de proceso.  
  
## <a name="see-also"></a>Vea también  
 [IDebugProviderProgramNode2](../../../extensibility/debugger/reference/idebugproviderprogramnode2.md)