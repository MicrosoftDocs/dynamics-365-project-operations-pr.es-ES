---
title: Configurar subcontratistas como recursos reservables
description: Este artículo explica cómo configurar y mantener recursos de subcontratistas que se crean a partir de usuarios y contactos en el sistema, para que puedan asociarse con subcontratos en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 727508c41c190c3703e9cd1420066fa0e551f147
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522723"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Configurar subcontratistas como recursos reservables

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Siga estos pasos para configurar subcontratistas como recursos que se pueden reservar en Microsoft Dynamics 365 Project Operations.

1. Vaya a **Proyecto** \> **Recursos** y seleccione **Nuevo**.
2. En la página **Nuevo recurso que se puede reservar**, en el campo **Tipo de recurso**, seleccione una de las siguientes opciones:

    - **Usuario** – Seleccione este tipo de recurso si el subcontratista debe acceder a Project Operations para introducir tiempo o gastos. Si selecciona **Usuario**, el subcontratista requiere una licencia válida para acceder al sistema.
    - **Contacto** o **Cuenta** – Seleccione uno de estos tipos de recursos si el subcontratista no requiere acceso a Project Operations, pero debe estar disponible para asignaciones de tareas o reservas en proyectos. Ninguno de estos tipos de recursos proporciona acceso al sistema. Seleccione **Cuenta** para representar a la empresa del proveedor como un recurso que se puede reservar. Seleccione **Contacto** para representar a los empleados individuales del proveedor.

3. Según el tipo de recurso que seleccionó, se le solicitará que seleccione el usuario, la cuenta o el registro de contacto correspondiente.
4. En el campo **Tipo de trabajador**, seleccione el "Trabajador contratado" para configurar el subcontratista como un recurso que se puede reservar.

    > [!NOTE]
    > Si deja el campo **Tipo de trabajador** en blanco, el recurso que se puede reservar se considerará un empleado.

5. Si seleccionó **Trabajador contratado** como tipo de trabajador, seleccione el proveedor para el que trabaja el recurso.
6. Seleccione la zona horaria del recurso y luego seleccione **Guardar**. Para asignar una plantilla de horas de trabajo al recurso que se puede reservar, puede seleccionar **Establecer calendario** en la página de la lista **Recurso que se puede reservar**.

Para asociarse con una línea de subcontrato, un recurso reservable debe cumplir estas condiciones:

- El recurso reservable debe ser un trabajador contratado.
- Un recurso reservable del tipo de recurso **Contacto** debe estar asociado a la cuenta del proveedor como contacto. Un recurso reservable del tipo de recurso **Usuario** no tiene que estar asociado a la cuenta del proveedor como contacto.
- El valor del campo **Proveedor** del recurso reservable debe coincidir con el valor del campo **Proveedor** para el subcontrato.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Actualice el tipo de asignación de trabajadores y proveedores para los recursos reservables

El campo **Tipo de trabajador** de un recurso reservable determina si el recurso reservable es un trabajador contratado o un empleado. El campo **Proveedor** define la cuenta de proveedor a la que está asociado el recurso reservable. Al asociar un recurso reservable a un proveedor como contacto, indica que el contacto es un empleado de la empresa del proveedor.

Si los campos **Tipo de trabajador** y **Proveedor** de un recurso reservable se modifican, los cambios afectan las validaciones futuras de los nuevos registros que crea el recurso que se puede reservar, como las entradas de tiempo. Sin embargo, los cambios no invalidan los registros existentes.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
