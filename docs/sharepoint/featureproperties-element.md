---
title: FeatureProperties (elemento) | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- FeatureProperties element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: f9b893ce699dd86f309a05fad83560cc42439551
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/21/2019
ms.locfileid: "56619373"
---
# <a name="featureproperties-element"></a>FeatureProperties (elemento)
  Una colección de valores de propiedad que se incluyen con una característica cuando se implementa en SharePoint. Una vez implementada la característica, puede tener acceso a los valores de propiedad en el código.

## <a name="syntax"></a>Sintaxis

```xml
<FeatureProperties>
  <FeatureProperty.../>
</FeatureProperties>
```

## <a name="attributes-and-elements"></a>Atributos y elementos
 En las siguientes secciones se describen los atributos, los elementos secundarios y los elementos primarios.

### <a name="attributes"></a>Atributos
 Ninguno.

### <a name="child-elements"></a>Elementos secundarios

|Elemento|Descripción|
|-------------|-----------------|
|[FeatureProperty](../sharepoint/featureproperty-element.md)|Elemento opcional.<br /><br /> Representa una propiedad personalizada, en formato de clave/valor.|

### <a name="parent-elements"></a>Elementos primarios

|Elemento|Descripción|
|-------------|-----------------|
|[ProjectItem](../sharepoint/projectitem-element.md)|Representa un elemento de proyecto de SharePoint. Este elemento, el elemento raíz necesario de la `.spdata` archivo.|

## <a name="remarks"></a>Comentarios
 Para obtener más información acerca de las propiedades de característica, consulte [proporcionar información de empaquetado e implementación de elementos de proyecto](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md).

## <a name="element-information"></a>Información de elemento

|Elemento|Descripción|
|-------------|-----------------|
|**Espacio de nombres**|http<nolink>://schemas.microsoft.com/VisualStudio/<br>2010/SharePointTools/SharePointProjectItemModel|
|**Nombre de esquema**|Esquema de elemento de proyecto de SharePoint|
|**Archivo de validación**|ProjectItemModelSchema.xsd|
|**Puede estar vacío**|No|

## <a name="see-also"></a>Vea también
- [Referencia de esquemas de elemento de proyecto de SharePoint](../sharepoint/sharepoint-project-item-schema-reference.md)
- [Proporcionar información de empaquetado e implementación de elementos de proyecto](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md)
