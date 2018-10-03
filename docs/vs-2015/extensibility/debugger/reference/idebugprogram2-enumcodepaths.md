---
title: IDebugProgram2::EnumCodePaths | Documentos de Microsoft
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
- IDebugProgram2::EnumCodePaths
helpviewer_keywords:
- IDebugProgram2::EnumCodePaths
ms.assetid: fb100c3c-9c29-4d63-bd1f-a3e531cb395f
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: c2f18a95fb63b0db7ea5e4a3a34a663ac1a5ad6c
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47567010"
---
# <a name="idebugprogram2enumcodepaths"></a>IDebugProgram2::EnumCodePaths
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [IDebugProgram2::EnumCodePaths](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugprogram2-enumcodepaths).  
  
Recupera una lista de las rutas de acceso del código para una posición determinada en un archivo de origen.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp#  
HRESULT EnumCodePaths(   
   LPCOLESTR            pszHint,  
   IDebugCodeContext2*  pStart,  
   IDebugStackFrame2*   pFrame,  
   BOOL                 fSource,  
   IEnumCodePaths2**    ppEnum,  
   IDebugCodeContext2** ppSafety  
);  
```  
  
```csharp  
int EnumCodePaths(   
   string                 pszHint,  
   IDebugCodeContext2     pStart,  
   IDebugStackFrame2      pFrame,  
   Int                    fSource,  
   out IEnumCodePaths2    ppEnum,  
   out IDebugCodeContext2 ppSafety  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `pszHint`  
 [in] La palabra situada bajo el cursor en el **origen** o **desensamblado** vista en el IDE.  
  
 `pStart`  
 [in] Un [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) objeto que representa el contexto de código actual.  
  
 `pFrame`  
 [in] Un [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md) objeto que representa el marco de pila asociada con el punto de interrupción actual.  
  
 `fSource`  
 [in] Distinto de cero (`TRUE`) si se encuentra en la **origen** vista, o cero (`FALSE`) si se encuentra en la **desensamblado** vista.  
  
 `ppEnum`  
 [out] Devuelve un [IEnumCodePaths2](../../../extensibility/debugger/reference/ienumcodepaths2.md) objeto que contiene una lista de las rutas de acceso del código.  
  
 `ppSafety`  
 [out] Devuelve un [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) objeto que representa un contexto de código adicional que se establecerá como un punto de interrupción en caso de ruta de acceso de código seleccionado se omite. Esto puede ocurrir en el caso de una expresión booleana cortocircuita, por ejemplo.  
  
## <a name="return-value"></a>Valor devuelto  
 Si es correcto, devuelve `S_OK`; en caso contrario, devuelve un código de error.  
  
## <a name="remarks"></a>Comentarios  
 Una ruta de acceso de código describe el nombre de un método o función que se llamó para llegar al punto actual en la ejecución del programa. Una lista de las rutas de código representa la pila de llamadas.  
  
## <a name="see-also"></a>Vea también  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IEnumCodePaths2](../../../extensibility/debugger/reference/ienumcodepaths2.md)   
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)   
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)
