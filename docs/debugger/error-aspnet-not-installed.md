---
title: 'Error: ASP.NET no está instalado | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.http_not_supported
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Web applications, errors
- debugger, Web application errors
- error messages, ASP.NET
- ASP.NET, installation error messages
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- aspnet
ms.openlocfilehash: 09c10019f4a3efd369398964eb1cf957968b4d10
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "54976503"
---
# <a name="error-aspnet-not-installed"></a>Error: ASP.NET no está instalado
Este error se produce si [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] no está correctamente instalado en el equipo en el que intenta depurar. Esto puede significar que nunca se instaló [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] o que se instaló [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] antes que IIS.  
  
### <a name="to-reinstall-aspnet"></a>Para reinstalar ASP.NET  
  
1. Desde una ventana del símbolo del sistema, ejecute el siguiente comando:  
  
   ```cmd
   \WINDOWS\Microsoft.NET\Framework\version\aspnet_regiis -i  
   ```  
  
    donde *versión* representa el número de versión de .NET Framework instalada en el equipo, por ejemplo, v1.0.370. Puede determinar la versión de .NET framework consultando el `\WINDOWS\Microsoft.NET\Framework` directory.  
  
   > [!NOTE]
   >  En Windows Server 2003, puede instalar [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] mediante el subprograma **Agregar o quitar programas** del Panel de control.  
  
## <a name="see-also"></a>Vea también  
 [Depurar aplicaciones web: errores y solución de problemas](../debugger/debugging-web-applications-errors-and-troubleshooting.md)
