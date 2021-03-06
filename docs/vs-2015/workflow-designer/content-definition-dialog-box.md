---
title: Cuadro de diálogo Definición de contenido | Documentos de Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- MessageContent.UI
ms.assetid: 7e4237c3-90a1-4149-bd8a-3643d1dde0df
caps.latest.revision: 3
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 0c0fffed6bbb8d9690f96679d910d5ac4a3b631e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/12/2018
ms.locfileid: "49176129"
---
# <a name="content-definition-dialog-box"></a>Definición de contenido (cuadro de diálogo)
El **definición de contenido** cuadro de diálogo se usa en [!INCLUDE[wfd1](../includes/wfd1-md.md)] para configurar el **contenido** propiedades de la <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.SendReply>, y <xref:System.ServiceModel.Activities.ReceiveReply> actividades. [!INCLUDE[crabout](../includes/crabout-md.md)] los diseñadores de actividad que utilizan este cuadro, vea el [enviar](../workflow-designer/send-activity-designer.md), [recepción](../workflow-designer/receive-activity-designer.md), [ReceiveAndSendReply](../workflow-designer/receiveandsendreply-template-designer.md), y [SendAndReceiveReply](../workflow-designer/sendandreceivereply-template-designer.md) temas.  
  
 La tabla siguiente describen los elementos de interfaz de usuario de la **inicializar correlación** cuadro de diálogo.  
  
|Elemento de la interfaz de usuario|Descripción|  
|----------------|-----------------|  
|**Mensaje**|Especifica el contenido del mensaje con el **los datos del mensaje** cuadro de texto de expresión y el tipo mediante el uso de la **tipo de mensaje** cuadro de lista desplegable. De forma predeterminada, el **definición de contenido** usa el <xref:System.ServiceModel.Activities.ReceiveMessageContent>, que espera un <xref:System.ServiceModel.Channels.Message> o un tipo dentro de la definición de servicio de flujo de trabajo de contrato de mensaje.|  
|**Parámetros**|Haga clic en el **parámetros** botón de radio usar <xref:System.ServiceModel.Activities.ReceiveParametersContent>, que espera un contrato de datos. Utilice la cuadrícula de datos para establecer una colección genérica de par clave-valor <xref:System.Activities.OutArgument> cuyos valores se asignen a parámetros de variables en el flujo de trabajo actual.|  
  
 El **definición de contenido** cuadro de diálogo se usa por la **enviar**, **recepción**, **ReceiveAndSendReply**, y  **SendAndReceiveReply** diseñadores. El acceso a los mismos es similar en todos los casos; se usará Receive para ilustrar el procedimiento.  
  
 El **recepción** Diseñador de actividad se puede arrastrar desde el **cuadro de herramientas** y colocarlo en la [!INCLUDE[wfd2](../includes/wfd2-md.md)] superficie donde se coloquen normalmente las actividades. Esto crea una actividad <xref:System.ServiceModel.Activities.Receive> con una propiedad <xref:System.Activities.Activity.DisplayName%2A> predeterminada de Receive. Seleccione el **recepción** Diseñador de actividad y haga clic en el botón de puntos suspensivos situado junto al texto (contenido) para el **contenido** propiedad en la cuadrícula de propiedades para el **definición de contenido**cuadro de diálogo.  
  
 Se puede especificar el contenido dentro de la **mensaje** sección un <xref:System.ServiceModel.Activities.ReceiveMessageContent> actividad o dentro la **parámetro** sección un <xref:System.ServiceModel.Activities.ReceiveParametersContent> actividad.  
  
## <a name="see-also"></a>Vea también  
 [Ayuda de la interfaz de usuario del Diseñador de flujo de trabajo](../workflow-designer/workflow-designer-ui-help.md)