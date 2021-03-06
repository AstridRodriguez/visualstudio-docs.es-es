---
title: ISimpleConnectionPoint (interfaz) | Documentos de Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- ISimpleConnectionPoint interface
ms.assetid: f632a82f-942d-4291-963e-e9fa2b162493
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4a756fa3f933f4adff56c41a86aee19a0a2a93aa
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/16/2019
ms.locfileid: "54346415"
---
# <a name="isimpleconnectionpoint-interface"></a>ISimpleConnectionPoint (Interfaz)
Proporciona una manera sencilla de describir y enumerar los eventos se activa en un punto de conexión determinado. Esta interfaz también permite enlazar fácilmente un `IDispatch` objeto a esos eventos. Esta interfaz es implementada por el proceso de depuración Manager (PDM) y consumida por los motores de scripts.  
  
 Esta interfaz está disponible desde `IDebugHelper::CreateSimpleConnectionPoint`.  
  
 Además de los métodos heredados de `IUnknown`, el `ISimpleConnectionPoint` interfaz expone los métodos siguientes.  
  
## <a name="methods-in-vtable-order"></a>Métodos en orden de Vtable  
  
|Método|Descripción|  
|------------|-----------------|  
|[ISimpleConnectionPoint::Advise](../../winscript/reference/isimpleconnectionpoint-advise.md)|Establece una conexión entre el objeto de punto de conexión simple y el receptor del cliente.|  
|[ISimpleConnectionPoint::DescribeEvents](../../winscript/reference/isimpleconnectionpoint-describeevents.md)|Devuelve el identificador DISPID y el nombre para cada evento en un intervalo especificado de eventos.|  
|[ISimpleConnectionPoint::GetEventCount](../../winscript/reference/isimpleconnectionpoint-geteventcount.md)|Devuelve el número de eventos que se exponen en esta interfaz.|  
|[ISimpleConnectionPoint::Unadvise](../../winscript/reference/isimpleconnectionpoint-unadvise.md)|Finaliza una conexión de consulta previamente establecida mediante `ISimpleConnectionPoint::Advise`.|  
  
## <a name="see-also"></a>Vea también  
 [IDebugProperty (Interfaz)](../../winscript/reference/idebugproperty-interface.md)