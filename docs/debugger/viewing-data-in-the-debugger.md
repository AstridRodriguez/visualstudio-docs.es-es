---
title: Crear vistas personalizadas de los datos en el depurador | Microsoft Docs
ms.date: 01/09/2019
ms.topic: conceptual
f1_keywords:
- vs.debug
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- debugging [Visual Studio], inspecting programs
- debugger, viewing data
ms.assetid: 13e1105f-f987-402e-9108-ec6ac12be042
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0e7d64cc1ae937ee7e68d04c95b56cc02c7612d8
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MTE95
ms.contentlocale: es-ES
ms.lasthandoff: 02/22/2019
ms.locfileid: "56710492"
---
# <a name="create-custom-views-of-data-in-the-visual-studio-debugger-c-visual-basic-c"></a>Crear vistas personalizadas de los datos en el depurador de Visual Studio (C#, Visual Basic, C++)

El [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] depurador proporciona muchas herramientas para inspeccionar y modificar el estado del programa. La mayoría de estas herramientas sólo funcionan en el modo de interrupción.

## <a name="create-custom-views-of-data-in-variable-windows-and-datatips"></a>Crear vistas personalizadas de datos en ventanas de variables y la información sobre datos

 Muchos de los [ventanas del depurador](../debugger/debugger-windows.md), como el **automático** y **inspección** windows, le permiten inspeccionar variables. Puede personalizar los tipos de forma nativos, los objetos administrados, y sus propios tipos que se muestran en las ventanas de variables del depurador y en [DataTips](../debugger/view-data-values-in-data-tips-in-the-code-editor.md). Para obtener más información, consulte [crear vistas personalizadas de los objetos nativos](../debugger/create-custom-views-of-native-objects.md) y [crear vistas personalizadas de objetos](../debugger/create-custom-views-of-dot-managed-objects.md).

## <a name="create-custom-visualizers"></a>Crear visualizadores personalizados

 Los visualizadores le permiten ver el contenido de un objeto o variable de forma significativa. En el depurador de Visual Studio, un visualizador hace referencia a las diferentes ventanas que se pueden abrir con la lupa ![VisualizerIcon](../debugger/media/dbg-tips-visualizer-icon.png "icono visualizador") icono. Por ejemplo, el visualizador HTML muestra cómo una cadena HTML se interpreta y se mostraría en un explorador. Puede tener acceso a los visualizadores desde información sobre datos, la **inspección** ventana, el **automático** ventana y el **variables locales** ventana. El **Inspección rápida** cuadro de diálogo también proporciona un visualizador. Para obtener más información, vea [Crear visualizadores personalizados](../debugger/create-custom-visualizers-of-data.md).

## <a name="see-also"></a>Vea también

- [Primer vistazo al depurador](../debugger/debugger-feature-tour.md)
- [Ventana Comandos](../ide/reference/command-window.md)
- [Seguridad del depurador](../debugger/debugger-security.md)