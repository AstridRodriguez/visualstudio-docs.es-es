---
title: Elemento TaskBody (MSBuild) | Microsoft Docs
ms.date: 03/13/2017
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- TaskBody element [MSBuild]
- <TaskBody> element [MSBuild]
ms.assetid: 49d8741b-f1ea-4470-94fd-a1ac27341a6a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c95761dd87d9d8d36aaff228d6395547bc07fe41
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "55015711"
---
# <a name="taskbody-element-msbuild"></a>Elemento TaskBody (MSBuild)
Contiene los datos que se pasen a `UsingTask` `TaskFactory`. Para más información, consulte [Elemento UsingTask (MSBuild)](../msbuild/usingtask-element-msbuild.md).  

 \<Project>  
 \<UsingTask>  
 \<TaskBody>  

## <a name="syntax"></a>Sintaxis  

```xml
<TaskBody Evaluate="true/false" />  
```  

## <a name="attributes-and-elements"></a>Atributos y elementos  
 En las siguientes secciones se describen los atributos, los elementos secundarios y los elementos primarios.  

### <a name="attributes"></a>Atributos  

|Atributo|Descripción|  
|---------------|-----------------|  
|`Evaluate`|Atributo Boolean opcional.<br /><br /> Si es `true`, MSBuild evalúa los elementos internos y expande los elementos y las propiedades antes de pasar la información a `TaskFactory` cuando se crea una instancia de la tarea.|  

### <a name="child-elements"></a>Elementos secundarios  

|Elemento|Descripción|  
|-------------|-----------------|  
|Datos|El texto entre las etiquetas `TaskBody` se envía textual a `TaskFactory`.|  

### <a name="parent-elements"></a>Elementos primarios  

| Elemento | Descripción |
| - | - |
| [UsingTask](../msbuild/usingtask-element-msbuild.md) | Proporciona una manera de registrar las tareas en [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]. Puede haber cero o más elementos `UsingTask` en un proyecto. |

## <a name="example"></a>Ejemplo  
 En el ejemplo siguiente se muestra cómo usar el elemento `TaskBody` con un atributo `Evaluate`.  

```xml  
<UsingTask TaskName="MyTask" AssemblyName="My.Assembly" TaskFactory="MyTaskFactory">  
       <ParameterGroup>  
              <Parameter1 ParameterType="System.String" Required="False" Output="False"/>  
              <Parameter2 ParameterType="System.Int" Required="True" Output="False"/>  
              ...  
</ParameterGroup>  
       <TaskBody Evaluate="true">  
      ... Task factory-specific data ...  
       </TaskBody>  
</UsingTask>  
```  

## <a name="see-also"></a>Vea también  
 [Tareas](../msbuild/msbuild-tasks.md)   
 [Referencia de tareas](../msbuild/msbuild-task-reference.md)   
 [Referencia de esquema de archivo de proyecto](../msbuild/msbuild-project-file-schema-reference.md)
