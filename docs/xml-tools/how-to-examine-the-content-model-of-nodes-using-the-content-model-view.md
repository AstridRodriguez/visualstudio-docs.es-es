---
title: Examinar el modelo de contenido de los nodos mediante la vista de modelo de contenido en el Diseñador de esquemas XML
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: c42ddac8-b0e3-48d6-9832-112a19d6c104
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3d188ef947c8c789f8de032522d43c09660f2ded
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/08/2019
ms.locfileid: "55920917"
---
# <a name="how-to-examine-the-content-model-of-nodes-using-the-content-model-view"></a>Filtrar Examinar el modelo de contenido de los nodos mediante la vista de modelo de contenido

En este tema se describe cómo explorar los nodos mediante el [vista modelo de contenido](../xml-tools/content-model-view.md).

## <a name="to-create-a-new-xsd-file-and-display-the-root-element-in-the-content-model-view"></a>Para crear un nuevo archivo XSD y mostrar el elemento raíz en el vista Modelo de contenido

1.  Cree un nuevo archivo de esquema XML.

2.  Haga clic en **Use el Editor XML para ver y editar el archivo de esquema XML subyacente** en la vista inicio.

3.  Copie el código de ejemplo de esquema XML de [esquema XML de ejemplo: esquema de pedido de compra](../xml-tools/sample-xsd-file-purchase-order-schema.md) y péguelo para reemplazar el código que se ha agregado el nuevo archivo XSD de forma predeterminada.

4.  Seleccione el `purchaseOrder` elemento en el Explorador de esquema haciendo clic con el `purchaseOrder` elemento en el Editor XML y seleccionando **mostrar en explorador XML**.

5.  Haga clic en el `purchaseOrder` en el Explorador de XML y seleccione **mostrar en vista de modelo de contenido**.

     La vista Modelo de contenido muestra el elemento `purchaseOrder` en la superficie de diseño.

6.  Expanda los nodos `shipTo`, `billTo` y `items` haciendo doble clic en cada nodo o haciendo clic en la flecha doble situada a la derecha de cada nodo.

     Los nodos del elemento `purchaseOrder` se expanden y puede ver el modelo de contenido del elemento.

7.  Haga clic en cualquier nodo situado debajo del elemento `purchaseOrder` y busque en la barra de ruta de navegación dónde se encuentra el nodo seleccionado dentro del conjunto de esquemas.

8.  Haga clic en el **Mostrar documentación** botón en la barra de herramientas de XSD para ver la documentación. También puede hacer clic con el botón secundario en la superficie de diseño para ver la documentación.

9. Haga clic el `purchaseOrder` nodo y seleccione **generar XML de ejemplo** para ver el documento de instancia XML.