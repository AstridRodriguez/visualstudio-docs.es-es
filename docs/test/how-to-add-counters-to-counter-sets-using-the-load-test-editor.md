---
title: Agregar contadores a conjuntos de contadores para pruebas de carga en Visual Studio | Microsoft Docs
ms.date: 10/19/2016
ms.topic: article
helpviewer_keywords:
- counters, counter sets
- counter sets
- load tests, counter sets
ms.assetid: e17d0e71-f982-4fc1-a2df-a1065d37473d
author: gewarren
ms.author: gewarren
manager: ghogen
ms.technology: vs-ide-test
ms.openlocfilehash: dc3a8600201b8724f7fbe6c711941b477398528d
ms.sourcegitcommit: 900ed1e299cd5bba56249cef8f5cf3981b10cb1c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2018
---
# <a name="how-to-add-counters-to-counter-sets-using-the-load-test-editor"></a>Cómo: Agregar contadores a conjuntos de contadores usando el Editor de prueba de carga

Cuando se crea una prueba de carga con el **Asistente para prueba de carga**, se agrega un conjunto inicial de contadores. Este conjunto inicial de contadores ofrece una serie de conjuntos de contadores predefinidos para la prueba de carga. Para obtener más información, consulte [Especificar los conjuntos de contadores y las reglas de umbral para equipos en una prueba de carga](../test/specify-counter-sets-and-threshold-rules-for-load-testing.md).

> [!NOTE]
>  Si las pruebas de carga se distribuyen entre varios equipos remotos, los contadores de controlador y de agente se asignan automáticamente a los conjuntos de contadores de controlador y de agente. Para obtener más información sobre cómo usar máquinas remotas en la prueba de carga, vea [Controladores y agentes de prueba](configure-test-agents-and-controllers-for-load-tests.md).

 Los contadores se administran en el **Editor de pruebas de carga**. Los conjuntos de contadores que ya se han agregado a la prueba están visibles en el nodo **Conjuntos de contadores** de la prueba de carga. Después de crear una prueba de carga, puede agregar nuevos contadores a los conjuntos de contadores existentes.

## <a name="to-add-counters-to-a-counter-set"></a>Para agregar contadores a un conjunto de contadores

1.  Abra una prueba de carga.

2.  Expanda el nodo **Conjuntos de contadores**. Todos los conjuntos de contadores que se hayan agregado a la prueba de carga estarán visibles.

    > [!NOTE]
    > El árbol jerárquico de pruebas de carga también incluye el nodo **Parámetros de ejecución**. Este nodo incluye el nodo **Asignaciones de conjuntos de contadores**, que muestra todos los equipos y los conjuntos de contadores que se asignan a esos equipos.

3.  Haga clic con el botón derecho en un conjunto de contadores existente y, a continuación, elija **Agregar contadores**.

     Se mostrará el cuadro de diálogo **Elegir contadores de rendimiento**.

4.  En el cuadro combinado desplegable **Equipo**, escriba el nombre del equipo con el que desee realizar la asignación. También puede seleccionar uno de los equipos de la lista desplegable.

    > [!NOTE]
    > Como los conjuntos de contadores deben asignarse a un equipo antes de que se recopilen los datos de rendimiento, debe especificar un equipo donde recopilar los datos de rendimiento.

5.  Seleccione una **Categoría de rendimiento** para filtrar las categorías de contadores de datos de rendimiento. Verá dos columnas de datos para seleccionar contadores de rendimiento.

    > [!NOTE]
    > Algunas categorías de rendimiento exigirán también que seleccione una instancia. Por ejemplo, si selecciona un contador de SQL, deberá seleccionar también una instancia de SQL, puesto que puede haber más de una instancia de SQL instalada en el equipo de destino.

6.  Seleccione un contador y una instancia para agregar al conjunto de contadores personalizado.

     \- o -

     Seleccione el botón de radio **Todos los contadores** para seleccionar todos los contadores disponibles.

7.  Elija **Aceptar**.

    > [!NOTE]
    > Otra forma de agregar contadores a un conjunto de contadores consiste en elegir el botón secundario en un contador o categoría de contador existente, elegir Copiar y, a continuación, pegar el contador o la categoría en un nodo de conjuntos de contadores distinto. Si se copian contadores adicionales que no son necesarios, pueden eliminarse.

## <a name="see-also"></a>Vea también

- [Especificar los conjuntos de contadores y las reglas de umbral para equipos en una prueba de carga](../test/specify-counter-sets-and-threshold-rules-for-load-testing.md)
- [Configurar los parámetros de ejecución de pruebas de carga](../test/configure-load-test-run-settings.md)