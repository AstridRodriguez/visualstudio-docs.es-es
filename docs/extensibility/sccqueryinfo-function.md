---
title: SccQueryInfo (función) | Documentos de Microsoft
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccQueryInfo
helpviewer_keywords:
- SccQueryInfo function
ms.assetid: 3973d336-a9b7-41a2-a4e6-bb8184a96aaf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: eccb75d593208b63681f585a37daa1665cdf9f4e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "55006833"
---
# <a name="sccqueryinfo-function"></a>SccQueryInfo (Función)
Esta función obtiene información de estado para un conjunto de archivos seleccionados en el control de código fuente.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp  
SCCRTN SccQueryInfo(  
   LPVOID  pvContext,  
   LONG    nFiles,  
   LPCSTR* lpFileNames,  
   LPLONG  lpStatus  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 pvContext  
 [in] La estructura de contexto de complemento de control de origen.  
  
 nFiles  
 [in] Número de archivos especificados en el `lpFileNames` matriz y la longitud de la `lpStatus` matriz.  
  
 lpFileNames  
 [in] Una matriz de nombres de archivos que se va a consultar.  
  
 lpStatus  
 [in, out] Una matriz en el que el complemento de control de origen devuelve las marcas de estado para cada archivo. Para obtener más información, consulte [código de estado de archivo](../extensibility/file-status-code-enumerator.md).  
  
## <a name="return-value"></a>Valor devuelto  
 La implementación de complemento de control de origen de esta función debe devolver uno de los valores siguientes:  
  
|Valor|Descripción|  
|-----------|-----------------|  
|SCC_OK|La consulta era correcta.|  
|SCC_E_ACCESSFAILURE|Hubo un problema con el acceso al sistema de control de origen, probablemente debido a problemas de red o de contención. Se recomienda un reintento.|  
|SCC_E_PROJNOTOPEN|El proyecto no está abierto en el control de código fuente.|  
|SCC_E_NONSPECIFICERROR|Error no específico.|  
  
## <a name="remarks"></a>Comentarios  
 Si `lpFileName` es una cadena vacía, actualmente no hay ninguna información de estado para la actualización. En caso contrario, es el nombre de ruta de acceso completa del archivo para el que puede haber cambiado la información de estado.  
  
 La matriz de valor devuelta puede ser una máscara de bits de `SCC_STATUS_xxxx` bits. Para obtener más información, consulte [código de estado de archivo](../extensibility/file-status-code-enumerator.md). Un sistema de control de código fuente puede no admitir todos los tipos de bits. Por ejemplo, si `SCC_STATUS_OUTOFDATE` no está disponible, pero no está establecido el bit.  
  
 Al usar esta función para desproteger archivos, tenga en cuenta lo siguiente `MSSCCI` requisitos de estado:  
  
-   `SCC_STATUS_OUTBYUSER` se establece cuando el usuario actual ha desprotegido el archivo.  
  
-   `SCC_STATUS_CHECKEDOUT` no se puede establecer a menos que `SCC_STATUS_OUTBYUSER` está establecido.  
  
-   `SCC_STATUS_CHECKEDOUT` solo se establece cuando el archivo está desprotegido en el directorio de trabajo designado.  
  
-   Si el archivo está desprotegido por el usuario actual en un directorio que no sea el directorio de trabajo, `SCC_STATUS_OUTBYUSER` está establecida pero `SCC_STATUS_CHECKEDOUT` no es.  
  
## <a name="see-also"></a>Vea también  
 [Funciones de API de complemento de Control de código fuente](../extensibility/source-control-plug-in-api-functions.md)   
 [Código de estado de archivo](../extensibility/file-status-code-enumerator.md)