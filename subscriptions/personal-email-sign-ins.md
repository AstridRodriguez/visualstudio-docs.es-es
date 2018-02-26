---
title: "Aparición de correos electrónicos personales en Microsoft Business Center"
Author: evanwindom
Ms.author: jaunger
Manager: evelynp
Ms.date: 1/23/2018
Ms.topic: Get-Started-Article
Description: "Visual Studio Subscriptions – Why Am I Seeing Hotmail or Gmail Addresses for My Subscribers?"
Ms.prod: vs-subscription
Ms.technology: vs-subscriptions
Searchscope: VS Subscription
ms.openlocfilehash: 2bfe2f39d432be5fc6ff7b24be2a218d02fce961
ms.sourcegitcommit: b18844078a30d59014b48a9c247848dea188b0ee
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2018
---
# <a name="visual-studio-subscriptions--why-am-i-seeing-hotmail-or-gmail-addresses-for-my-subscribers"></a>Suscripciones de Visual Studio: ¿por qué aparecen direcciones de Hotmail o Gmail para mis suscriptores? 

A medida que las empresas se van migrando desde Microsoft Business Center al nuevo [Portal de administración de suscripciones](https://manage.visualstudio.com) de Visual Studio, los administradores pueden sorprenderse de ver que la "dirección de correo electrónico de inicio de sesión" de algunos suscriptores es una dirección de correo electrónico de otro proveedor, como Hotmail, Gmail o Yahoo.

## <a name="cause"></a>Motivo

Esta situación puede darse como consecuencia de los procesos de inicio de sesión asociados a la anterior experiencia de suscriptor de MSDN. Los usuarios se han migrado desde Microsoft Business Center al nuevo portal sin modificaciones. Es posible que algunos administradores no se hayan percatado de que los usuarios habían estado utilizando cuentas personales para acceder a los beneficios de su suscripción. Antes de las migraciones de suscriptores de Visual Studio, que se completaron en 2016, se requerían dos acciones para usar correctamente una suscripción a Visual Studio:
1. El administrador "asignaba" la suscripción a un suscriptor individual, que usaba su dirección de correo electrónico profesional o educativa.
2. El suscriptor "activaba" la suscripción.

Durante el proceso de activación del suscriptor:
1. Se requería una cuenta Microsoft (MSA) para iniciar sesión.
2. En caso de que el suscriptor no intentara usar su cuenta profesional o educativa (por ejemplo, John@contoso.com) como MSA, este podía crear una nueva cuenta o aprovechar alguna existente.
3. Como resultado, la "dirección de correo electrónico de inicio de sesión" no coincidía con la "dirección de asignación".

> [!NOTE] 
> La nueva experiencia de suscriptor en [https://my.visualstudio.com](https://my.visualstudio.com?wt.mc_id=o~msft~docs) admite los tipos de identidad profesional/educativa y de cuenta Microsoft (MSA).

Por último, debido a que la migración del administrador toma datos de Microsoft Business Center con respecto a la "dirección de correo electrónico de inicio de sesión" para completar la nueva experiencia de administración de los suscriptores, los administradores recientemente migrados podría ver estas cuentas personales, que previamente no habían percibido, debido a algunos cambios en la interfaz de usuario que hacen esta información más visible.

## <a name="solution"></a>Soluciones

Para corregir el problema, debe modificar la información del suscriptor para actualizar sus direcciones de correo electrónico de inicio de sesión.  Las modificaciones pueden hacerse de una en una o todas a la vez. Para obtener más información, visite [Edición de las asignaciones de suscripción](/visualstudio/subscriptions/edit-license).  

Una vez que haya actualizado las direcciones de correo electrónico de los suscriptores, debería informarles de que ha cambiado su información de inicio de sesión.  