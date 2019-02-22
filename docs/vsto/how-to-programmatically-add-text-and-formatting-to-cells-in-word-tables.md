---
title: Filtrar Agregar texto y formato a celdas de tablas de Word mediante programación
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- cells, adding text and formatting
- text [Office development in Visual Studio], adding to Word tables
- formatting [Office development in Visual Studio]
- tables [Office development in Visual Studio], adding text and formatting
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 983b2939d652c20c3fbcb42dd8caded802495c8d
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/21/2019
ms.locfileid: "56614654"
---
# <a name="how-to-programmatically-add-text-and-formatting-to-cells-in-word-tables"></a>Filtrar Agregar texto y formato a celdas de tablas de Word mediante programación
  Cada tabla consta de una colección de celdas. Cada objeto <xref:Microsoft.Office.Interop.Word.Cell> individual representa una celda de la tabla. Se hace referencia a cada celda mediante su ubicación en la tabla. Este ejemplo hace referencia a la celda ubicada en la primera fila y la primera columna de la tabla, le añade texto y le aplica formato.

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

## <a name="to-add-text-and-formatting-to-cells"></a>Para agregar texto y formato a celdas

1.  Haga referencia a la celda por su ubicación en la tabla, agregue texto a la celda y aplique el formato.

     El siguiente ejemplo de código se puede usar en una personalización de nivel de documento. Para usar este ejemplo, ejecútelo desde la clase `ThisDocument` del proyecto.

     [!code-vb[Trin_VstcoreWordAutomation#97](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#97)]
     [!code-csharp[Trin_VstcoreWordAutomation#97](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#97)]

     El siguiente ejemplo de código se puede usar en un complemento de VSTO. En este ejemplo se usa el documento activo. Para usar este ejemplo, ejecútelo desde la clase `ThisAddIn` del proyecto.

     [!code-vb[Trin_VstcoreWordAutomationAddIn#97](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationAddIn/ThisAddIn.vb#97)]
     [!code-csharp[Trin_VstcoreWordAutomationAddIn#97](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationAddIn/ThisAddIn.cs#97)]

## <a name="see-also"></a>Vea también
- [Cómo: Crear tablas de Word mediante programación](../vsto/how-to-programmatically-create-word-tables.md)
- [Cómo: Agregar filas y columnas a las tablas de Word mediante programación](../vsto/how-to-programmatically-add-rows-and-columns-to-word-tables.md)
- [Cómo: Rellenar tablas de Word con propiedades de documento mediante programación](../vsto/how-to-programmatically-populate-word-tables-with-document-properties.md)
