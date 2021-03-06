---
title: Instalación fuera de la carpeta de extensiones con VSIX v3 | Documentos de Microsoft
ms.date: 11/09/2016
ms.topic: conceptual
ms.assetid: 913c3745-8aa9-4260-886e-a05aecfb2225
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fc8d0ccac452d82ed1a2f5fbce7c88fd82efc1d7
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "54983110"
---
# <a name="installing-outside-the-extensions-folder"></a>Instalación fuera de la carpeta de extensiones

A partir de Visual Studio 2017 y VSIX v3 (versión 3), ahora existe compatibilidad para la instalación de los recursos de extensión fuera de la carpeta de extensiones. Actualmente, se habilitan las siguientes ubicaciones como ubicaciones de instalación válida (donde [INSTALLDIR] está asignada al directorio de instalación de la instancia de Visual Studio):

* \MSBuild [INSTALLDIR]
* [INSTALLDIR]\Xml\Schemas
* [INSTALLDIR]\Common7\IDE\PublicAssemblies
* [INSTALLDIR]\Licenses
* [INSTALLDIR]\Common7\IDE\ReferenceAssemblies
* [INSTALLDIR]\Common7\IDE\RemoteDebugger
* [INSTALLDIR]\Common7\IDE\VC\VCTargets

>**Nota:** El formato VSIX no permiten instalar fuera de la estructura de carpeta de instalación de VS.

Para admitir la instalación de estos directorios, la extensión VSIX debe instalarse "por instancia por equipo". Esta opción puede habilitarse activando la casilla "todos los usuarios" en el diseñador extension.vsixmanifest:

![Compruebe todos los usuarios](media/check-all-users.png)

## <a name="how-to-set-the-installroot"></a>Cómo establecer el valor de InstallRoot

Para establecer los directorios de instalación, puede usar el **propiedades** ventana de Visual Studio. Por ejemplo, puede establecer el `InstallRoot` propiedad de una referencia de proyecto a una de las ubicaciones anteriores:

![propiedades de la raíz de instalación](media/install-root-properties.png)

Esto agregará algunos metadatos correspondiente `ProjectReference` propiedad dentro del archivo .csproj del proyecto VSIX:

```xml
 <ProjectReference Include="..\ClassLibrary1\ClassLibrary1.csproj">
        <Project>{69a979f1-eba2-43e7-9346-0e56e803508b}</Project>
        <Name>ClassLibrary1</Name>
        <InstallRoot>PublicAssemblies</InstallRoot>
 </ProjectReference>
```

>**Nota:** Puede editar el archivo .csproj directamente, si lo prefiere.

## <a name="how-to-set-a-subpath-under-the-installroot"></a>Cómo establecer una subruta en el valor de InstallRoot

Si desea instalar en una subruta de acceso bajo la `InstallRoot`, puede hacerlo estableciendo la `VsixSubPath` al igual que la propiedad la `InstallRoot` propiedad. Por ejemplo, digamos que queremos que los resultados de la referencia proyecto para instalar en ' [INSTALLDIR]\MSBuild\MyCompany\MySDK\1.0'. Esto se logra fácilmente con el Diseñador de propiedades:

![subruta de acceso set](media/set-subpath.png)

Los cambios correspondientes de .csproj tendrá este aspecto:

```xml
<ProjectReference Include="..\ClassLibrary1\ClassLibrary1.csproj">
       <Project>{69a979f1-eba2-43e7-9346-0e56e803508b}</Project>
       <Name>ClassLibrary1</Name>
       <InstallRoot>MSBuild</InstallRoot>
       <VSIXSubPath>MyCompany\MySDK\1.0</VSIXSubPath>
</ProjectReference>
```

## <a name="extra-information"></a>Información adicional

Se aplican los cambios de propiedad diseñador a algo más que las referencias de proyecto; puede establecer el `InstallRoot` metadatos para los elementos dentro de su proyecto (con los mismos métodos que se ha descrito anteriormente).
