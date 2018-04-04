---
title: Crear una aplicación Node.js y React - Visual Studio | Microsoft Docs
description: En este tutorial, se crea una aplicación Node.js y React en Visual Studio.
ms.custom: mvc
ms.date: 02/19/2018
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-nodejs
ms.tgt_pltfrm: ''
ms.topic: tutorial
ms.devlang: javascript
author: mikejo5000
ms.author: mikejo
manager: ghogen
dev_langs:
- JavaScript
ms.workload:
- nodejs
ms.openlocfilehash: 3c0b387e29df6bc46b8a7c3e79ccb50fa16e3ed6
ms.sourcegitcommit: e01ccb5ca4504a327d54f33589911f5d8be9c35c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2018
---
# <a name="tutorial-create-a-nodejs-and-react-app-in-visual-studio"></a>Tutorial: Crear una aplicación Node.js y React en Visual Studio
Visual Studio permite crear fácilmente un proyecto de Node.js y aprovechar IntelliSense y otras características integradas compatibles con Node.js. En este tutorial para Visual Studio, se crea un proyecto de aplicación web de Node.js a partir de una plantilla de Visual Studio. A continuación, se crea una aplicación sencilla con React. 

En este tutorial aprenderá a:
> [!div class="checklist"]
> * Crear un proyecto de Node.js
> * Agregar paquetes de npm
> * Agregar código de React a la aplicación
> * Transpilar JSX
> * Asociar el depurador

## <a name="prerequisites"></a>Requisitos previos

* Debe tener instalado Visual Studio y la carga de trabajo de desarrollo de Node.js.

    Si todavía no tiene instalado Visual Studio, puede descargarlo de forma gratuita en [esta página](http://www.visualstudio.com).

    Si necesita instalar la carga de trabajo pero ya tiene Visual Studio, haga clic en el vínculo **Abrir el instalador de Visual Studio** en el panel izquierdo del cuadro de diálogo **Nuevo proyecto**. Se iniciará el Instalador de Visual Studio. Elija la carga de trabajo **Desarrollo de Node.js** y, después, haga clic en **Modificar**.

* Debe tener instalado el runtime de Node.js.

    Si todavía no lo tiene instalado, instale la versión LTS desde el sitio web de [Node.js](https://nodejs.org/en/download/). En general, Visual Studio detecta automáticamente el entorno de ejecución de Node.js instalado. Si no detecta un runtime instalado, puede configurar el proyecto para que haga referencia al runtime instalado en la página de propiedades (después de crear un proyecto, haga clic con el botón derecho en el nodo del proyecto y elija **Propiedades**).

    Este tutorial se ha probado con la versión 8.9.4.

## <a name="create-a-project"></a>Crear un proyecto
En primer lugar, cree un proyecto de aplicación web de Node.js.

1. Abra Visual Studio 2017.  

1. En la barra de menús superior, seleccione **Archivo** > **Nuevo** > **Proyecto...**  

1. En el panel de la izquierda del cuadro de diálogo **Nuevo proyecto**, expanda **JavaScript** y después seleccione **Node.js**. En el panel central, elija **Aplicación web en blanco de Node.js**, escriba el nombre **NodejsWebAppBlank** y después haga clic en **Aceptar**.   

     Si no ve la plantilla de proyecto **Aplicación web en blanco de Node.js**, deberá instalar primero la carga de trabajo de desarrollo de Node.js. 

    Visual Studio crea la solución y abre el proyecto.

    ![Proyecto de Node.js en el Explorador de soluciones](../nodejs/media/tutorial-nodejs-react-project-structure.png)  

    - El proyecto está resaltado en negrita. Tiene el nombre que le asignó en el cuadro de diálogo **Nuevo proyecto**. En el sistema de archivos, este proyecto se representa mediante un archivo *.njsproj* en la carpeta del proyecto. Para establecer propiedades y variables de entorno asociadas al proyecto, haga clic con el botón derecho en el proyecto y elija **Propiedades**. Puede hacer recorridos de ida y vuelta con otras herramientas de desarrollo, dado que el archivo de proyecto no realiza cambios personalizados en el origen del proyecto Node.js.

    - En el nivel superior se encuentra una solución, que de forma predeterminada tiene el mismo nombre que el proyecto. Una solución, representada por un archivo *.sln* en el disco, es un contenedor para uno o más proyectos relacionados.

    - En el nodo npm se muestran todos los paquetes npm instalados. Puede hacer clic con el botón derecho en el nodo npm para buscar e instalar paquetes npm mediante un cuadro de diálogo.

    - Los archivos de proyecto como *server.js* se muestran en el nodo del proyecto. *server.js* es el archivo de inicio del proyecto.

## <a name="add-npm-packages"></a>Agregar paquetes de npm

Esta aplicación requiere una serie de módulos de npm para ejecutarse correctamente.

* react
* react-dom
* express
* ruta de acceso
* ts-loader
* typescript
* webpack
* webpack-cli

1. En el Explorador de soluciones (panel derecho), haga clic con el botón derecho en el nodo **npm** del proyecto y elija **Instalar nuevos paquetes de NPM**.

    En el cuadro de diálogo **Instalar nuevos paquetes de NPM**, puede elegir instalar la versión más reciente del paquete o especificar una versión. Si decide instalar la versión actual de estos paquetes, pero experimenta errores inesperados más adelante, puede que necesite instalar las versiones exactas de paquete que se indican más adelante en estas instrucciones.

1. En el cuadro de diálogo **Instalar nuevos paquetes de NPM**, busque el paquete React y haga clic en **Instalar paquete** para instalarlo.

    ![Instalar paquetes de npm](../nodejs/media/tutorial-nodejs-react-install-packages.png)

    En la ventana **Salida** se muestra el progreso de la instalación del paquete. Una vez instalado, el paquete aparece en el nodo **npm**.

    El archivo *package.json* del proyecto se actualiza con la nueva información de paquete, incluida su versión.

1. En lugar de usar la interfaz de usuario para buscar y agregar el resto de los paquetes de uno en uno, pegue el siguiente código en package.json. Reemplace la sección `dependencies` por el código siguiente:

    ```js
    "dependencies": {
      "express": "4.16.2",
      "path": "0.12.7",
      "react": "16.2.0",
      "react-dom": "16.2.0",
      "ts-loader": "4.0.1",
      "typescript": "2.7.2",
      "webpack": "4.1.1",
      "webpack-cli": "2.0.11"
    }
    ```

1. Haga clic con el botón derecho en el nodo **npm** del proyecto y elija **Instalar los paquetes de NPM que faltan**.

    En la ventana **Salida** se muestra el progreso de instalación de los paquetes.

    Estos son los módulos npm tal y como aparecen en el Explorador de soluciones después de su instalación.

    ![paquetes npm](../nodejs/media/tutorial-nodejs-react-npm-modules.png) 

    > [!NOTE]
    > Si prefiere instalar paquetes npm con la línea de comandos, haga clic con el botón derecho en el nodo del proyecto y seleccione **Abrir símbolo del sistema aquí**. Utilice los comandos estándar de Node.js para instalar los paquetes.

## <a name="add-project-files"></a>Agregar archivos de proyecto

En estos pasos, agregará cuatro nuevos archivos al proyecto.

* *app.tsx*
* *webpack-config.js*
* *index.html*
* *tsconfig.json*

Para esta sencilla aplicación, los nuevos archivos de proyecto se agregan en la raíz del proyecto. (Por lo general y en la mayoría de las aplicaciones, los archivos se agregan en las subcarpetas, ajustando en consecuencia las referencias de la ruta de acceso relativa).

1. En el Explorador de soluciones, haga clic con el botón derecho en el proyecto **NodejsWebAppBlank** y elija **Agregar** > **Nuevo elemento**.

1. En el cuadro de diálogo **Agregar nuevo elemento**, elija **Archivo JSX de TypeScript**, escriba el nombre *app.tsx* y haga clic en **Aceptar**.

1. Repita estos pasos para agregar *webpack-config.js*.

1. Repita los mismos pasos para agregar *index.html* al proyecto. En lugar de un archivo JavaScript, elija **Archivo HTML**.

1. Repita los mismos pasos para agregar *tsconfig.json* al proyecto. En lugar de un archivo JavaScript, elija **Archivo de configuración JSON de TypeScript**.

## <a name="add-app-code"></a>Agregar código de aplicación

1. Abra *server.js* y reemplace el código por lo siguiente:

    ```javascript
    'use strict';
    var http = require('http');
    var path = require('path');
    var express = require('express');

    var app = express();

    var staticPath = path.join(__dirname, '/');
    app.use(express.static(staticPath));

    // Allows you to set port in the project properties.
    app.set('port', process.env.PORT || 3000);

    var server = app.listen(app.get('port'), function() {
        console.log('listening');
    });
    ```

   El código anterior usa Express para iniciar Node.js como el servidor de aplicaciones web. Este código establece el puerto en el número de puerto que está configurado en las propiedades del proyecto (el valor predeterminado es 1337). Para abrir las propiedades del proyecto, haga clic con el botón derecho en el Explorador de soluciones y elija **Propiedades**.

1. Abra *app.tsx* y agregue el siguiente código:

    ```javascript
    declare var require: any
    
    var React = require('react');
    var ReactDOM = require('react-dom');

    class Hello extends React.Component {
        render() {
            return (
                <h1>Welcome to React!!</h1>
            );
        }
    }

    ReactDOM.render(<Hello />, document.getElementById('root'));
    ```

    El código anterior usa la sintaxis JSX y React para mostrar un mensaje sencillo.

1. Abra *index.html* y reemplace la sección **body** por el siguiente código:

    ```html
    <body>
        <div id="root"></div>
        <!-- scripts -->
        <script src="./dist/app-bundle.js"></script>
    </body>
    ```

    Esta página HTML carga *app-bundle.js*, que contiene el código JSX y React transpilado a JavaScript sin formato. Actualmente, *app-bundle.js* es un archivo vacío. En la sección siguiente, se configuran las opciones para transpilar el código.

## <a name="configure-webpack-and-typescript-compiler-options"></a>Configure las opciones de compilador de TypeScript y webpack

En los pasos anteriores, se agregó *webpack-config.js* al proyecto. A continuación, se agrega código de configuración de webpack. Se agrega una configuración de webpack simple que especifica un archivo de entrada (*app.tsx*) y un archivo de salida (*app-bundle.js*) para agrupar y transpilar JSX a JavaScript sin formato. Para transpilar, también se configuran algunas opciones del compilador TypeScript. Este código es una configuración básica que sirve como introducción al compilador TypeScript y webpack.

1. En el Explorador de soluciones, abra *webpack-config.js* y agregue el código siguiente.

    ```json
    module.exports = {
        devtool: 'source-map',
        entry: "./app.tsx",
        mode: "development",
        output: {
            filename: "./app-bundle.js"
        },
        resolve: {
            extensions: ['.Webpack.js', '.web.js', '.ts', '.js', '.jsx', '.tsx']
        },
        module: {
            rules: [
                {
                    test: /\.tsx$/,
                    exclude: /(node_modules|bower_components)/,
                    use: {
                        loader: 'ts-loader'
                    }
                }
            ]
        }
    }
    ```

    El código de configuración de webpack indica a Webpack que utilice el cargador de TypeScript para transpilar el JSX.

1. Abra tsconfig.json y agregue el código siguiente, que especifica las opciones del compilador TypeScript:

    ```json
    {
      "compilerOptions": {
        "noImplicitAny": false,
        "module": "commonjs",
        "noEmitOnError": true,
        "removeComments": false,
        "sourceMap": true,
        "target": "es5",
        "jsx": "react"
      },
      "exclude": [
        "node_modules"
      ],
      "files": [
        "app.tsx"
      ]
    }
    ```

    app.tsx se especifica como el archivo de origen.

## <a name="transpile-the-jsx"></a>Transpilar el JSX

1. En el Explorador de soluciones, haga clic con el botón derecho en el nodo del proyecto y elija **	Abrir símbolo del sistema aquí**.

1. En el símbolo del sistema, escriba el siguiente comando:

    `node_modules\.bin\webpack app.tsx --config webpack-config.js`

    La ventana del símbolo del sistema muestra el resultado.

    ![Ejecutar webpack](../nodejs/media/tutorial-nodejs-react-run-webpack.png) 

    Si ve algún error en lugar de la salida anterior, debe solucionarlo para que funcione la aplicación. Si las versiones del paquete npm son diferentes de las versiones que se muestran en este tutorial, esa puede ser una fuente de errores. Una manera de corregir errores es usar las versiones exactas que se muestran en los pasos anteriores. Además, si una o varias de estas versiones del paquete están en desuso y producen un error, deberá instalar una versión más reciente para corregir los errores.

1. En el Explorador de soluciones, haga clic con el botón derecho en el nodo del proyecto y elija **Agregar** > **Carpeta existente** y, a continuación, elija la carpeta *dist* y haga clic en **Seleccionar carpeta**.

    Visual Studio agrega la carpeta *dist* al proyecto, que contiene *app-bundle.js* y *app-bundle.js.map*.

1. Abra *app-bundle.js.* para ver el código de JavaScript transpilado.

1. Si se le pide que vuelva a cargar archivos modificados externamente, haga clic en **Sí a todo**.

    ![Cargar archivos modificados](../nodejs/media/tutorial-nodejs-react-reload-files.png) 

Cada vez que realice cambios en *app.tsx*, debe volver a ejecutar el comando webpack.

## <a name="run-the-app"></a>Ejecutar la aplicación

1. Asegúrese de que Chrome está seleccionado como destino de depuración actual.

    ![Seleccionar Chrome como destino de depuración](../nodejs/media/tutorial-nodejs-react-debug-target.png)  

1. Para ejecutar la aplicación, presione **F5** (**Depurar** > **Iniciar depuración**) o en el botón de flecha verde.

    Se abre una ventana de consola de Node.js que muestra el puerto en el que escucha el depurador.

    Visual Studio abre la aplicación con el archivo de inicio, *server.js*.

    ![Ejecutar React en el explorador](../nodejs/media/tutorial-nodejs-react-running-react.png) 

1. Cierre la ventana del explorador.

1. Cierre la ventana de la consola.

## <a name="set-a-breakpoint-and-run-the-app"></a>Establecer un punto de interrupción y ejecutar la aplicación

1. En *server.js*, haga clic en el margen interno a la izquierda de la declaración `staticPath` para establecer un punto de interrupción:

    ![Establecer un punto de interrupción](../nodejs/media/tutorial-nodejs-react-set-breakpoint.png) 

    Los puntos de interrupción son la característica más básica y esencial para una depuración confiable. Un punto de interrupción indica dónde Visual Studio debe suspender la ejecución de código para poder echar un vistazo a los valores de las variables o al comportamiento de la memoria, o determinar si se está ejecutando o no una bifurcación de código. 

1. Para ejecutar la aplicación, presione **F5** (**Depurar** > **Iniciar depuración**).

    El depurador se detiene en el punto de interrupción establecido (la instrucción actual está marcada en amarillo). Ahora, puede inspeccionar el estado de la aplicación desplazando el puntero sobre las variables que están actualmente en el ámbito, con ventanas del depurador como **Locales** e **Inspección**.

1. Presione **F5** para continuar la aplicación.

1. Si quiere utilizar las herramientas de desarrollo de Chrome, presione **F12**. Puede usar estas herramientas para examinar el DOM e interactuar con la aplicación mediante la consola de JavaScript.

1. Cierre el explorador web y la consola.

## <a name="set-and-hit-a-breakpoint-in-the-client-side-react-code"></a>Establecer y alcanzar un punto de interrupción en el código React del lado cliente

En la sección anterior se asoció el depurador al código Node.jse del lado servidor. Para asociar el depurador de Visual Studio y establecer puntos de interrupción en el código React del cliente, el depurador necesita ayuda para identificar el proceso correcto. Esta es una manera de habilitar esta opción.

1. Cierre todas las ventanas de Chrome.

1. Abra el comando **Ejecutar** desde el botón **Inicio** de Windows (haga clic con el botón derecho y elija **Ejecutar**) y escriba el comando siguiente:

    `chrome.exe --remote-debugging-port=9222`

    Chrome se inicia con la depuración habilitada.

1. Cambie a Visual Studio y establezca un punto de interrupción en el código *app-bundle.js* en la función `render()`, tal como se muestra en la siguiente ilustración:

    ![Establecer un punto de interrupción](../nodejs/media/tutorial-nodejs-react-set-breakpoint-client-code.png) 

1. Con Chrome seleccionado como destino de depuración en Visual Studio, presione **Ctrl + F5** (**Depurar** > **Iniciar sin depurar**) para ejecutar la aplicación en el explorador.

    La aplicación se abre en una nueva pestaña del explorador.

1. Elija **Depurar** > **Asociar al proceso**.

1. En el cuadro de diálogo **Asociar al proceso**, elija **Código Webkit** en el campo **Asociar a**, y escriba **chrome** en el cuadro de filtro para filtrar los resultados de la búsqueda.

1. Seleccione el proceso de Chrome con puerto de host correcto (1337 en este ejemplo) y haga clic en **Asociar**.

    ![Asociar al proceso](../nodejs/media/tutorial-nodejs-react-attach-to-process.png) 

    Sabrá que el depurador se ha asociado correctamente cuando el Explorador DOM y la Consola de JavaScript se abran correctamente en Visual Studio. Estas herramientas de depuración son similares a las herramientas de desarrollo de Chrome y a las herramientas F12 para Edge.

1. Dado que el código ya se ejecuta con el punto de interrupción, actualice la página del explorador para alcanzar el punto de interrupción.

    Mientras está en pausa en el depurador, puede pasar el mouse sobre las variables y usar las ventanas del depurador para examinar el estado de la aplicación. Para avanzar el depurador, puede ejecutar el código paso a paso (**F5**, **F10** y **F11**).

    En función del estado del entorno y el explorador, puede alcanzar el punto de interrupción en app-bundle.js o en su ubicación asignada en app.tsx. En cualquier caso, puede ejecutar paso a paso el código y examinar las variables. (Si tiene que interrumpir el código en un archivo *.tsx* y no es capaz de hacerlo, pruebe a usar la instrucción `debugger;` o establezca puntos de interrupción en las herramientas de desarrollo de Chrome).

    > [!TIP]
    > Una vez que se asocia al proceso la primera vez siguiendo estos pasos, puede volver a asociar rápidamente al mismo proceso en Visual Studio 2017 si selecciona **Depurar** > **Reasociar al proceso**.

## <a name="next-steps"></a>Pasos siguientes 

En este tutorial ha aprendido a crear una aplicación Node.js y React, a transpilar JSX y a depurar. Para obtener más información sobre las Herramientas de Node.js para Visual Studio, consulte la página Wiki.

> [!div class="nextstepaction"]
> [Herramientas de Node.js para Visual Studio](https://github.com/Microsoft/nodejstools)