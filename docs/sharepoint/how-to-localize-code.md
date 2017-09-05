---
title: "C&#243;mo: Localizar c&#243;digo"
ms.custom: ""
ms.date: "02/02/2017"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "office-development"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "VB"
  - "CSharp"
helpviewer_keywords: 
  - "localizar código [desarrollo de SharePoint en Visual Studio]"
  - "desarrollo de SharePoint en Visual Studio, adaptar"
ms.assetid: 0e852052-5ad4-4517-81cf-8865ec304441
caps.latest.revision: 17
author: "kempb"
ms.author: "kempb"
manager: "ghogen"
caps.handback.revision: 16
---
# C&#243;mo: Localizar c&#243;digo
  El código sin localizar usa valores de cadena codificados de forma rígida.  Para localizar cadenas de código, sustitúyalas por llamadas a <xref:System.Web.HttpContext.GetGlobalResourceObject%2A>, que es un método que hace referencia a los recursos localizados.  
  
## Adaptar código  
  
#### Para localizar el código  
  
1.  En el **Explorador de soluciones**, abra el menú contextual para un elemento de proyecto y, a continuación, elija **Agregar**, **Módulo**.  
  
     Elija la plantilla **Archivo de recursos**.  
  
    > [!NOTE]  
    >  Asegúrese de agregar el archivo de recursos a un elemento de proyecto de SharePoint para que esté disponible la propiedad Tipo de implementación.  Esta propiedad es necesaria más adelante en este procedimiento.  
  
2.  Asigne al archivo de recursos del idioma predeterminado el nombre que desee y agréguele la extensión .resx, por ejemplo, MyAppResources.resx.  
  
3.  Repita los pasos 1 y 2 para agregar archivos de recursos independientes al elemento de proyecto de SharePoint: uno para cada idioma localizado.  
  
     Use el mismo nombre base para cada archivo de recursos localizado, pero agregue el identificador de la referencia cultural.  Por ejemplo, el nombre del archivo de recursos localizado en alemán será MyAppResources.de\-DE.resx.  
  
4.  Abra cada uno de los archivos de recursos y agregue las cadenas localizadas.  Use los mismos identificadores de cadena en cada archivo.  
  
5.  Cambie el valor de la propiedad **Tipo de implementación** de cada archivo de recursos a **AppGlobalResource** para que cada uno de los archivos se implemente en la carpeta App\_GlobalResources del servidor.  
  
6.  Deje el valor de la propiedad **Acción de compilación** de cada archivo como **Recurso incrustado**.  
  
     Los recursos incrustados se compilan en el archivo DLL del proyecto.  
  
7.  Compile el proyecto para crear los archivos DLL satélite de recursos.  
  
8.  En el **Diseñador de paquetes**, elija la pestaña **Opciones avanzadas** y después agregue el ensamblado satélite.  
  
9. En el cuadro **Ubicación**, especifique delante de la ruta de acceso de la ubicación una carpeta con el identificador de referencia cultural, por ejemplo de\-DE\\*Project Item Name*.resources.dll.  
  
10. Si la solución aún no hace referencia el ensamblado System.Web, agregue una referencia y una directiva del código al espacio de nombres <xref:System.Web>.  
  
11. Busque todas las cadenas codificadas de forma rígida en el código visibles para los usuarios, como texto de la interfaz de usuario, errores y texto del mensaje.  Reemplácelas por una llamada al método <xref:System.Web.HttpContext.GetGlobalResourceObject%2A> utilizando la sintaxis siguiente:  
  
    ```  
    HttpContext.GetGlobalResourceObject("Resource File Name", "String ID")  
    ```  
  
12. Elija la tecla F5 para compilar y ejecutar la aplicación.  
  
13. En SharePoint, cambie el idioma de presentación predeterminado.  
  
     Las cadenas localizadas aparecen en la aplicación.  Para mostrar los recursos localizados, el servidor de SharePoint debe tener instalado el paquete de idioma que coincide con la referencia cultural del archivo de recursos.  
  
## Vea también  
 [Localizar soluciones de SharePoint](../sharepoint/localizing-sharepoint-solutions.md)   
 [Cómo: Localizar una característica](../sharepoint/how-to-localize-a-feature.md)   
 [Cómo: Localizar el marcado ASPX](../sharepoint/how-to-localize-aspx-markup.md)   
 [Cómo: Agregar un archivo de recursos](../sharepoint/how-to-add-a-resource-file.md)  
  
  