---
title: Búsqueda de referencias en el código
ms.date: 09/26/2017
ms.topic: conceptual
helpviewer_keywords:
- code editor, find all references
- find all references
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 777e8519077cebc162b1bad575a6ffcf976c4db4
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/08/2019
ms.locfileid: "55908886"
---
# <a name="find-references-in-your-code"></a>Búsqueda de referencias en el código

Puede usar el comando **Buscar todas las referencias** para buscar dónde se hace referencia a elementos de código específicos en todo el código base. El comando **Buscar todas las referencias** está disponible en el menú contextual (clic en el botón derecho) del elemento del que quiere buscar referencias. O bien, si prefiere usar el teclado, presione **MAYÚS+F12**.

Los resultados aparecen en una ventana de herramientas denominada **<element> references**, donde *element* es el nombre del elemento que está buscando. Una barra de herramientas en esta ventana **Referencias** le permite hacer lo siguiente:
- Cambiar el ámbito de la búsqueda en una lista desplegable. Puede buscar solo en los documentos modificados o en toda la solución.
- Copiar el elemento seleccionado al que se hace referencia mediante el botón **Copiar**.
- Seleccionar botones para ir a la ubicación siguiente o anterior en la lista, o presionar las teclas **F8** y **Mayús + F8** para hacerlo.
- Quitar los filtros en los resultados devueltos mediante el botón **Borrar todos los filtros**.
- Cambiar la forma en que se agrupan los elementos devueltos mediante una opción de la lista desplegable **Agrupar por:**.
- Conservar la ventana de los resultados de la búsqueda actual mediante el botón **Mantener resultados**. Al hacer clic en este botón, los resultados de la búsqueda actual permanecen en esta ventana y los resultados de la búsqueda nueva aparecen en una ventana de herramientas nueva.
- Buscar cadenas en los resultados de la búsqueda mediante la entrada de texto en el cuadro de texto **Búsqueda en Buscar todas las referencias**.

También puede mantener el puntero sobre cualquier resultado de la búsqueda para obtener una vista previa de la referencia.

![Ventana de herramientas Buscar todas las referencias](../ide/media/vside_findallreferences.png)

## <a name="navigate-to-references"></a>Navegar a referencias
Puede usar los métodos siguientes para navegar a referencias en la ventana **Referencias**:

- Presione **F8** para ir a la referencia siguiente, o **Mayús + F8** para ir a la referencia anterior.
- Presione la tecla **Entrar** en una referencia, o haga doble clic en ella para ir a ella en el código.
- En el menú contextual de una referencia, seleccione los comandos **Ir a ubicación anterior** o **Ir a ubicación siguiente**.
- Presione las teclas de **flecha arriba** y **flecha abajo** (si están habilitadas en el cuadro de diálogo **Opciones**). Para habilitar esta característica, vaya a la barra de menús y elija **Herramientas** > **Opciones** > **Entorno** > **Pestañas y ventanas** > **Pestaña de vista previa**. Después, active las casillas **Permitir que se abran nuevos archivos en la pestaña de vista previa** y **Vista previa de archivos seleccionados en Resultados de búsqueda**.

## <a name="change-reference-groupings"></a>Cambiar las agrupaciones de referencia
De forma predeterminada, las referencias se agrupan por proyecto y, luego, por definición. Aun así, puede cambiar este orden de agrupación si cambia la configuración de la lista desplegable **Agrupar por:** en la barra de herramientas. Por ejemplo, puede cambiarlo del valor predeterminado **Proyecto y luego definición** a **Definición y luego Proyecto** o a otros valores.

**Definición** y **Proyecto** son las dos agrupaciones predeterminadas que se usan, pero puede agregar otras mediante el comando **Agrupación** en el menú contextual del elemento seleccionado. Puede ser útil agregar más agrupaciones si su solución tiene una gran cantidad de archivos y rutas de acceso.

## <a name="see-also"></a>Vea también

- [Navegar por el código](../ide/navigating-code.md)