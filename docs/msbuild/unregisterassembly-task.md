---
title: UnregisterAssembly (Tarea) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#UnregisterAssembly
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, UnregisterAssembly task
- UnregisterAssembly task [MSBuild]
ms.assetid: 04f549dd-3591-4dda-9c3a-cf6ede9df2c3
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 518c8ea976783d2771500302e8f0ecce560e11b2
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "54961262"
---
# <a name="unregisterassembly-task"></a>UnregisterAssembly (tarea)
Elimina del Registro los ensamblados especificados para la interoperabilidad COM. Invierte la [tarea RegisterAssembly](../msbuild/registerassembly-task.md).  
  
## <a name="parameters"></a>Parámetros  
 En la siguiente tabla se describen los parámetros de la tarea `UnregisterAssembly` .  
  
|Parámetro|Descripción|  
|---------------|-----------------|  
|`Assemblies`|Parámetro <xref:Microsoft.Build.Framework.ITaskItem>`[]` opcional.<br /><br /> Especifica los ensamblados que se eliminarán del Registro.|  
|`AssemblyListFile`|Parámetro <xref:Microsoft.Build.Framework.ITaskItem> opcional.<br /><br /> Contiene información sobre el estado entre las tareas `RegisterAssembly` y `UnregisterAssembly`. Impide que la tarea intente eliminar del Registro un ensamblado que no se pudo registrar en la tarea `RegisterAssembly`.<br /><br /> Si se especifica este parámetro, se omiten los parámetros `Assemblies` y `TypeLibFiles`.|  
|`TypeLibFiles`|Parámetro de salida <xref:Microsoft.Build.Framework.ITaskItem>`[]` opcional.<br /><br /> Elimina del Registro la biblioteca de tipos especificada del ensamblado especificado. **Nota:**  Este parámetro solo es necesario si el nombre de archivo de la biblioteca de tipos es diferente al nombre del ensamblado.|  
  
## <a name="remarks"></a>Comentarios  
 No es necesario disponer de un ensamblado para que esta tarea se realice correctamente. Si intenta eliminar del Registro un ensamblado que no existe, la tarea se realizará correctamente y se mostrará una advertencia. Esto se debe a que esta tarea se encarga de quitar el registro del ensamblado del Registro. Si el ensamblado no existe, no se encontrará en el Registro, por lo que la tarea ha conseguido su propósito.  
  
 Además de los parámetros mencionados anteriormente, esta tarea hereda los parámetros de la clase <xref:Microsoft.Build.Tasks.AppDomainIsolatedTaskExtension>, que a su vez hereda de la clase <xref:System.MarshalByRefObject>. La clase `MarshalByRefObject` proporciona la misma funcionalidad que la clase <xref:Microsoft.Build.Utilities.Task>, pero se pueden crear instancias de esta clase en su propio dominio de aplicación.  
  
## <a name="example"></a>Ejemplo  
 En el ejemplo siguiente se utiliza la tarea `UnregisterAssembly` para eliminar del Registro el ensamblado en la ruta de acceso especificada por las propiedades `OutputPath` y `FileName`, si existe.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <PropertyGroup>  
        <OutputPath>\Output\</OutputPath>  
        <FileName>MyFile.dll</FileName>  
    </PropertyGroup>  
    <Target Name="UnregisterAssemblies">  
        <UnregisterAssembly  
            Condition="Exists('$(OutputPath)$(FileName)')"  
            Assemblies="$(OutputPath)$(FileName)" />  
    </Target>  
  
</Project>  
```  
  
## <a name="see-also"></a>Vea también  
 [RegisterAssembly (tarea)](../msbuild/registerassembly-task.md)   
 [Tareas](../msbuild/msbuild-tasks.md)   
 [Referencia de tareas](../msbuild/msbuild-task-reference.md)