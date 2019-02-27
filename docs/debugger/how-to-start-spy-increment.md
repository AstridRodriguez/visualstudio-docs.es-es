---
title: 'Cómo: iniciar Spy ++ | Microsoft Docs'
ms.date: 12/16/2018
ms.topic: conceptual
helpviewer_keywords:
- Spy++, starting
ms.assetid: 1d36813a-dc2a-4fda-9b3d-a38928a62ced
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 91eda74b4f83f38434117ab1217d0a20d66d2842
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MTE95
ms.contentlocale: es-ES
ms.lasthandoff: 02/22/2019
ms.locfileid: "56712455"
---
# <a name="how-to-start-spy"></a>Cómo: Iniciar Spy++

Puede iniciar Spy ++ desde Visual Studio o en un símbolo del sistema.

 Al iniciar Spy ++, si se muestra un mensaje para solicitar permiso para realizar cambios en el equipo, seleccione **Sí**.

> [!NOTE]
>  Puede ejecutar una única instancia de Spy ++. Si intenta iniciar una segunda instancia, simplemente hace que la instancia en ejecución obtener el foco.

## <a name="prerequisites"></a>Requisitos previos

Spy ++ requiere los siguientes componentes. Puede seleccionar estos componentes desde el instalador de Visual Studio seleccionando el **componentes individuales** ficha y, a continuación, seleccione los siguientes componentes.

* En la depuración y pruebas, seleccione **herramientas de generación de perfiles de C++**
* En las actividades de desarrollo, seleccione **características principales de C++ de Visual Studio**

Si ha realizado algún cambio, siga las indicaciones para instalar estos componentes.

## <a name="start-spy-from-visual-studio"></a>Iniciar Spy ++ desde Visual Studio

En el **herramientas** menú, seleccione **Spy ++**.

Dado que Spy ++ se ejecuta de forma independiente, después de iniciarla puede cerrar Visual Studio.

> [!NOTE]
>  Al registrar los mensajes con Spy ++, provocaría el sistema operativo realice más lentamente.

## <a name="start-spy-at-a-command-prompt"></a>Iniciar Spy ++ en un símbolo del sistema

1.  En una ventana del símbolo del sistema, cambie los directorios a la carpeta que contiene spyxx.exe. Normalmente, es la ruta de acceso a esta carpeta... \\ *Carpeta de instalación de visual Studio*\Common7\Tools\\.

2.  Escriba **spyxx.exe**.

## <a name="see-also"></a>Vea también
- [Usar Spy++](../debugger/using-spy-increment.md)
- [Vistas de Spy++](../debugger/spy-increment-views.md)
- [Referencia de Spy++](../debugger/spy-increment-reference.md)