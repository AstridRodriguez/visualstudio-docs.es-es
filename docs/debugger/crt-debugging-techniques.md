---
title: Técnicas de depuración de CRT | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- c.runtime.debugging
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging [CRT]
- CRT, debugging
- debugging [C++], CRT debug support
ms.assetid: 9be561f6-14a8-44ff-925d-d911d5b8e6ff
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8dedb7a35e95cc9efc68cbd947b415b4499a8fa9
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "54943921"
---
# <a name="crt-debugging-techniques"></a>Técnicas de depuración de CRT
Si está depurando un programa que utiliza la biblioteca en tiempo de ejecución de C, estas técnicas de depuración podrían resultar útiles.  
  
## <a name="in-this-section"></a>En esta sección  
 [Uso de la biblioteca de depuración CRT](../debugger/crt-debug-library-use.md)  
 Describe las capacidades de depuración suministradas por la biblioteca en tiempo de ejecución de C y proporciona instrucciones para obtener acceso a las herramientas.  
  
 [Macros para los informes](../debugger/macros-for-reporting.md)  
 Proporciona información sobre las macros **_RPTn** y **_RPTFn** (definidas en CRTDBG.H), que reemplazan el uso de instrucciones `printf` para la depuración.  
  
 [Versiones de depuración de las funciones de asignación del montón](../debugger/debug-versions-of-heap-allocation-functions.md)  
 Analiza las versiones especiales de depuración de las funciones de asignación del montón: cómo asigna CRT las llamadas, las ventajas de llamarlas explícitamente, cómo evitar la conversión, el seguimiento de los tipos independientes de asignaciones en bloques cliente, y el resultado de no definir _DEBUG.  
  
 [Detalles del montón de depuración de CRT](../debugger/crt-debug-heap-details.md)  
 Proporciona vínculos a temas de administración de memoria y el montón de depuración, tipos de bloques en el montón de depuración, uso del montón de depuración, funciones que informan del estado del montón y seguimiento de solicitudes de asignación en el montón.  
  
 [Creación de funciones de enlace de depuración](../debugger/debug-hook-function-writing.md)  
 Enumera una lista de vínculos a temas como: funciones de asociación a bloques cliente, funciones de enlace de asignación, enlaces de asignación y asignaciones de memoria de CRT, y funciones de enlace para informes.  
  
 [Buscar pérdidas de memoria con la biblioteca de CRT](../debugger/finding-memory-leaks-using-the-crt-library.md)  
 Explica técnicas para detectar y aislar pérdidas de memoria mediante el depurador y la biblioteca en tiempo de ejecución de C.  
  
## <a name="related-sections"></a>Secciones relacionadas  
 [Depuración de código nativo](../debugger/debugging-native-code.md)  
 Describe algunas técnicas y problemas de depuración comunes de las aplicaciones de C y C++.  
  
 [Seguridad del depurador](../debugger/debugger-security.md)  
 Proporciona recomendaciones para una depuración más segura.