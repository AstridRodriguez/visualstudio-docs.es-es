---
title: "Generación de un método en Visual Studio | Microsoft Docs"
ms.custom: 
ms.date: 01/26/2018
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.topic: article
author: gewarren
ms.author: gewarren
manager: ghogen
ms.workload:
- dotnet
ms.openlocfilehash: 6fbee2d6ea0a6d95d6d71114dc116cfaa1ede74e
ms.sourcegitcommit: 205d15f4558315e585c67f33d5335d5b41d0fcea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2018
---
# <a name="generate-a-method-in-visual-studio"></a>Generación de un método en Visual Studio

Esta generación de código se aplica a:

- C#

- Visual Basic

**Qué:** Le permite agregar inmediatamente un método a una clase.

**Cuándo:** Introduce un nuevo método y desea declararlo de manera adecuada y de inmediato.

**Por qué:** Podría declarar el método y los parámetros antes de usarlo; sin embargo, esta característica generará la declaración automáticamente.

## <a name="how-to"></a>Procedimiento

1. Coloque el cursor en la línea donde haya un subrayado ondulado de color rojo. Este subrayado ondulado de color rojo señala un método que aún no existe.

   - C#:

    ![Código resaltado (C#)](media/method-highlight-cs.png)

   - Visual Basic:

    ![Código resaltado (VB)](media/method-highlight-vb.png)

1. A continuación, realice alguno de los siguientes procedimientos:

   - **Teclado**
     - Presione **Ctrl +.** para activar el menú **Acciones rápidas y refactorizaciones**.
   - **Mouse**
     - Haga clic con el botón derecho y seleccione el menú **Acciones rápidas y refactorizaciones**.
     - Mantenga el mouse sobre el subrayado ondulado de color rojo y haga clic en el botón ![de icono Bombilla](media/bulb-cs.png) que aparece.
     - Haga clic en el botón ![de icono Bombilla](media/bulb-cs.png) que aparece en el margen izquierdo si el cursor de texto ya está en la línea con el subrayado ondulado de color rojo.

    ![Vista previa de la generación de método](media/method-preview-cs.png)

1. Seleccione **Generar método** en el menú desplegable.

   > [!TIP]
   > Use el vínculo **Vista previa de los cambios** en la parte inferior de la ventana de vista previa [para ver todos los cambios ](../../ide/preview-changes.md) que se aplicarán antes de realizar la selección.

   El método se crea con los parámetros que se deducen de su uso.

   - C#:

      ![Resultado de la generación de método (C#)](media/method-result-cs.png)

   - Visual Basic:

      ![Resultado de la generación de método (VB)](media/method-result-vb.png)

## <a name="see-also"></a>Vea también

[Generación de código](../code-generation-in-visual-studio.md)  
[Vista previa de cambios](../../ide/preview-changes.md)