---
title: IDebugExceptionEvent2::CanPassToDebuggee | Documentos de Microsoft
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugExceptionEvent2::CanPassToDebuggee
helpviewer_keywords:
- IDebugExceptionEvent2::CanPassToDebuggee
ms.assetid: ae4bbe0a-fbe1-49be-a310-ea64279a434b
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 7233d6ee9b1f82d72717df9284221fca65673391
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47582200"
---
# <a name="idebugexceptionevent2canpasstodebuggee"></a>IDebugExceptionEvent2::CanPassToDebuggee
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [IDebugExceptionEvent2::CanPassToDebuggee](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee).  
  
Determina si el motor de depuración (DE) es compatible con la opción de pasar esta excepción al programa que se está depurando cuando se reanuda la ejecución.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp#  
HRESULT CanPassToDebuggee(  
   void  
);  
```  
  
```csharp  
int CanPassToDebuggee();  
```  
  
## <a name="return-value"></a>Valor devuelto  
 Devuelve una `S_OK` (la excepción puede pasarse al programa) o `S_FALSE` (la excepción no se pueden pasar).  
  
## <a name="remarks"></a>Comentarios  
 La DE debe tener una acción predeterminada para pasar al lado depurado. El IDE puede recibir el [IDebugExceptionEvent2](../../../extensibility/debugger/reference/idebugexceptionevent2.md) evento y llamar a la [continuar](../../../extensibility/debugger/reference/idebugprocess3-continue.md) método sin llamar a la `CanPassToDebuggee` método. Por lo tanto, la DE debe tener un caso predeterminado para pasar la excepción o no.  
  
## <a name="see-also"></a>Vea también  
 [IDebugExceptionEvent2](../../../extensibility/debugger/reference/idebugexceptionevent2.md)   
 [Continue](../../../extensibility/debugger/reference/idebugprocess3-continue.md)
