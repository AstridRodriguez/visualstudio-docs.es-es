---
title: Filtrar Introducción a la personalización de la cinta de opciones
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- custom Ribbon, adding Ribbon to project
- Ribbon [Office development in Visual Studio], adding
- Ribbon [Office development in Visual Studio], customizing
- customizing the Ribbon, adding Ribbon to project
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 14c4ff1e8bf443351f835d74d44b49bbb61e0321
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/21/2019
ms.locfileid: "56640121"
---
# <a name="how-to-get-started-customizing-the-ribbon"></a>Procedimiento Introducción a la personalización de la cinta de opciones
  Para personalizar la cinta de opciones de una aplicación de Microsoft Office, agregue un **cinta (diseñador Visual)** o **cinta (XML)** a un proyecto de Office.

 [!INCLUDE[appliesto_ribbon](../vsto/includes/appliesto-ribbon-md.md)]

### <a name="to-add-a-ribbon-to-a-project"></a>Para agregar una cinta de opciones a un proyecto

1. En el **proyecto** menú, haga clic en **Agregar nuevo elemento**.

2. En el **Agregar nuevo elemento** cuadro de diálogo, seleccione **cinta (diseñador Visual)** o **cinta (XML)**. Para obtener más información acerca de estas plantillas, consulte [información general de la cinta de opciones](../vsto/ribbon-overview.md).

3. En el **nombre** , escriba un nombre para el elemento de la cinta de opciones.

    Los nombres no pueden contener los caracteres siguientes:

   -   Almohadilla (#)

   -   Porcentaje (%)

   -   "Y" comercial (&)

   -   Asterisco (*)

   -   Barra vertical (|)

   -   Barra diagonal inversa (\\)

   -   Dos puntos (:)

   -   Comillas dobles (")

   -   Menor que (\<)

   -   Mayor que (>)

   -   Signo de interrogación (?)

   -   Barra diagonal (/)

   -   Espacios iniciales o finales (' ')

   -   Nombres reservados para Windows o DOS como ("nul", "aux", "Configurar", "com1", "lpt1" etc.)

4. Haga clic en **Aceptar**.

   El elemento de la cinta de opciones aparece en **el Explorador de soluciones**. Para obtener información sobre los pasos siguientes, vea [información general de la cinta de opciones](../vsto/ribbon-overview.md).

## <a name="see-also"></a>Vea también
- [Obtener acceso a la cinta de opciones en tiempo de ejecución](../vsto/accessing-the-ribbon-at-run-time.md)
- [Diseñador de la cinta](../vsto/ribbon-designer.md)
- [Ribbon XML](../vsto/ribbon-xml.md)
- [Tutorial: Crear una pestaña personalizada usando el Diseñador de cinta de opciones](../vsto/walkthrough-creating-a-custom-tab-by-using-the-ribbon-designer.md)
- [Tutorial: Crear una pestaña personalizada usando XML de cinta de opciones](../vsto/walkthrough-creating-a-custom-tab-by-using-ribbon-xml.md)
