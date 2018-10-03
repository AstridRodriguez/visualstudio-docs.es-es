---
title: Modificación del Shell aislado mediante el uso de la. Archivo de Vsct | Documentos de Microsoft
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Visual Studio shell, isolated mode%2C .vsct file
ms.assetid: 6d147c2d-10e9-400e-b8ce-5566287b41ba
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 0606d28f151f0d9c85980121e3129bd9204c61b8
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47582783"
---
# <a name="modifying-the-isolated-shell-by-using-the-vsct-file"></a>Modificación del Shell aislado mediante el uso de la. Archivo de Vsct
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [modificando el aislado Shell por mediante el. Archivo de Vsct](https://docs.microsoft.com/visualstudio/extensibility/modifying-the-isolated-shell-by-using-the-dot-vsct-file).  
  
El proyecto de interfaz de usuario para un proyecto de Visual Studio shell aislado contiene un archivo .vsct que le permite especificar qué comandos individuales y grupos de aplicaciones están disponibles en la aplicación. El siguiente es un extracto de un archivo .vsct sin modificar.  
  
```  
<!-- <Define name="No_WindowListCommand"/> -->  
<!-- <Define name="No_MoreWindowsCommand"/> -->  
<!-- <Define name="No_PaneNextPaneCommand"/> -->  
<!-- <Define name="No_PanePrevPaneCommand"/> -->  
```  
  
 De forma predeterminada, se incluyen la mayoría de los comandos y grupos de comandos. Para excluir un comando o un grupo de comandos, simplemente quite ese comando o un grupo.  
  
 Por ejemplo, para quitar el panel siguiente y comandos de panel anterior, quite el `No_PaneNextPaneCommand` y `No_PanePrevPaneCommand` entradas:  
  
```  
  
<Define name="No_PaneNextPaneCommand"/> <Define name="No_PanePrevPaneCommand"/>  
  
```  
  
 Para obtener más ejemplo estas personalizaciones, consulte [Tutorial: crear una aplicación básica de Shell aislado](../extensibility/walkthrough-creating-a-basic-isolated-shell-application.md).  
  
## <a name="referenced-files"></a>Archivos que se hace referencia  
 El archivo .vsct predeterminado para una aplicación hace referencia a los siguientes archivos. Estos archivos se encuentran en el subdirectorio \VisualStudioIntegration\Common\Inc\ del directorio de instalación del SDK de Visual Studio.  
  
|Archivo|Descripción|  
|----------|-----------------|  
|wbids.h|Identidades de la interfaz de usuario para el paquete Web examinar.|  
|AppIDCmdUsed.vsct|Tabla de comandos para los elementos principales de la interfaz de usuario de Visual Studio.|  
|EmulatorCmdUsed.vsct|Tabla de comandos para elementos de interfaz de usuario de emulación de editor Emacs y breve.|  
|Vsdebugguids.h|Define los GUID de los comandos, página de opciones y otras características del depurador de Visual Studio.|  
|VsDbgCmdUsed.vsct|Tabla de comandos para el depurador.|  
  
 El archivo AppIDCmdUsed.vsct incluye elementos de interfaz de usuario de Visual Studio en función de los símbolos definidos en el archivo .vsct la aplicación.  
  
 Para obtener más información, consulte [diseño de tabla de comandos XML (. Archivos Vsct)](../extensibility/internals/designing-xml-command-table-dot-vsct-files.md) y [referencia del esquema XML de VSCT](../extensibility/vsct-xml-schema-reference.md).  
  
## <a name="see-also"></a>Vea también  
 [Shell aislado de Visual Studio](../extensibility/visual-studio-isolated-shell.md)
