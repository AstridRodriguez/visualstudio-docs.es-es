---
title: 'Preparación de la depuración: Servicios de Windows | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- FSharp
- VB
- CSharp
- C++
- VB
- CSharp
helpviewer_keywords:
- debugging [Visual Studio], Windows services
- Windows Service applications, debugging
ms.assetid: ac0a99f7-ec3d-4a20-b17f-698a817fdcc2
caps.latest.revision: 23
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7b189c1533e112c023ce2da24ed61fe228c09fda
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47567385"
---
# <a name="debugging-preparation-windows-services"></a>Preparación de la depuración: servicios de Windows
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [preparar la depuración: servicios de Windows](https://docs.microsoft.com/visualstudio/debugger/debugging-preparation-windows-services).  
  
Un servicio de Windows es un programa que se ejecuta en segundo plano en Microsoft Windows. Como ejemplos pueden citarse el servicio Telnet y el servicio de hora de Windows (que actualiza el reloj visible del equipo). Un servicio de Windows no se puede ejecutar desde [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]; debe ejecutarse dentro del contexto del Administrador de control de servicios. Para obtener más información, consulte [crear servicios de Windows](http://msdn.microsoft.com/library/0f5e2cbb-d95d-477c-b2b5-4b990e6b86ff), [depurar aplicaciones de servicios de Windows](http://msdn.microsoft.com/library/63ab0800-0f05-4f1e-88e6-94c73fd920a2), y [Windows Service Applications](http://msdn.microsoft.com/library/ba72d648-9553-4849-b829-069ad5ea014b).  
  
## <a name="see-also"></a>Vea también  
 [Depurar código administrado](../debugger/debugging-managed-code.md)   
 [Tipos de proyectos de C#, F# y Visual Basic](../debugger/debugging-preparation-csharp-f-hash-and-visual-basic-project-types.md)   
 [Configuración de proyectos para configuraciones de depuración en C#](../debugger/project-settings-for-csharp-debug-configurations.md)   
 [Configuración de proyectos para una configuración de depuración en Visual Basic](../debugger/project-settings-for-a-visual-basic-debug-configuration.md)   
 [Cómo: Depurar el método OnStart](../debugger/how-to-debug-the-onstart-method.md)


