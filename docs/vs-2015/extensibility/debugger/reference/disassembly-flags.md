---
title: DISASSEMBLY_FLAGS | Microsoft Docs
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
- DISASSEMBLY_FLAGS
helpviewer_keywords:
- DISASSEMBLY_FLAGS enumeration
ms.assetid: c1ec5a4d-5d42-4660-932c-7348550140cb
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 85c5e4a5b0cc5dbdcff5750ce5c87d170bb9bd20
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47575542"
---
# <a name="disassemblyflags"></a>DISASSEMBLY_FLAGS
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [DISASSEMBLY_FLAGS](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/disassembly-flags).  
  
Especifica las marcas de desensamblado.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp#  
enum enum_DISASSEMBLY_FLAGS {   
   DF_DOCUMENTCHANGE     = 0x00000001,  
   DF_DISABLED           = 0x00000002,  
   DF_INSTRUCTION_ACTIVE = 0x00000004,  
   DF_DATA               = 0x00000008,  
   DF_HASSOURCE          = 0x00000010,  
   DF_DOCUMENT_CHECKSUM  = 0x00000020  
};  
typedef DWORD DISASSEMBLY_FLAGS;  
```  
  
```csharp  
public enum enum_DISASSEMBLY_FLAGS {   
   DF_DOCUMENTCHANGE     = 0x00000001,  
   DF_DISABLED           = 0x00000002,  
   DF_INSTRUCTION_ACTIVE = 0x00000004,  
   DF_DATA               = 0x00000008,  
   DF_HASSOURCE          = 0x00000010,  
   DF_DOCUMENT_CHECKSUM  = 0x00000020  
};  
```  
  
## <a name="members"></a>Miembros  
 DF_DOCUMENTCHANGE  
 Indica que esta instrucción está en un documento diferente que el anterior.  
  
 DF_DISABLED  
 Indica que no se ejecutará esta instrucción.  
  
 DF_INSTRUCTION_ACTIVE  
 Indica que esta instrucción es una de las instrucciones que se ejecutará siguientes (puede haber más de uno).  
  
 DF_DATA  
 Indica que esta instrucción es realmente datos (sin codificar).  
  
 DF_HASSOURCE  
 Indica que esta instrucción tiene código fuente. Algunas instrucciones, por ejemplo, el código de la colección de elementos no utilizados o generación de perfiles, no tengan ningún origen correspondiente.  
  
 DF_DOCUMENT_CHECKSUM  
 Indica que `bstrDocumentUrl` campo contiene datos de la suma de comprobación después de la dirección URL del documento. Consulte la sección Comentarios para el [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md) estructura de cómo se almacenan los datos de la suma de comprobación.  
  
## <a name="remarks"></a>Comentarios  
 Usar como el `dwFlags` miembro de la [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md) estructura.  
  
 Estas marcas se pueden combinar con un bit a bit `OR`.  
  
## <a name="requirements"></a>Requisitos  
 Encabezado: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Ensamblado: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vea también  
 [Enumeraciones](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md)
