---
title: IDebugProgram2::GetProcess | Documentos de Microsoft
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProgram2::GetProcess
helpviewer_keywords:
- IDebugProgram2::GetProcess
ms.assetid: 1d602485-ebaf-451c-9165-f2e226f20a90
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b1dcfc207a485a3b1eb5ec24930f613692fac69e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "54962987"
---
# <a name="idebugprogram2getprocess"></a>IDebugProgram2::GetProcess
Obtener el proceso que se ejecuta este programa en.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp  
HRESULT GetProcess(  
   IDebugProcess2** ppProcess  
);  
```  
  
```csharp  
int GetProcess(  
   out IDebugProcess2 ppProcess  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `ppProcess`  
 [out] Devuelve el [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) interfaz que representa el proceso.  
  
## <a name="return-value"></a>Valor devuelto  
 Si es correcto, devuelve `S_OK`; en caso contrario, devuelve un código de error.  
  
## <a name="remarks"></a>Comentarios  
 A menos que implemente un motor de depuración (DE) la [IDebugEngineLaunch2](../../../extensibility/debugger/reference/idebugenginelaunch2.md) interfaz, la implementación de la DE este método siempre debe devolver `E_NOTIMPL` porque no puede determinar a DE proceso que se está ejecutando en y, por tanto, no se puede satisfacer una implementación de este método.  
  
 Implementar el `IDebugEngineLaunch2` interfaz significa que la DE debe saber cómo crear un proceso; por lo tanto, la implementación del DE la [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) es capaz de saber qué proceso se ejecuta en la interfaz.  
  
## <a name="see-also"></a>Vea también  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [IDebugEngineLaunch2](../../../extensibility/debugger/reference/idebugenginelaunch2.md)