---
title: Requisitos de artículos para contratos de proyectos con múltiples fuentes de financiación
description: Este tema brinda información sobre cómo configurar y usar los requisitos de artículos con múltiples fuentes de financiación.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d4af03e02d3c2eb0d442e6213ff5b9cf583d54b3
ms.sourcegitcommit: 30242d7754bca300b594b0887eb4212d10bea1c4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2022
ms.locfileid: "8728119"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Requisitos de artículos para contratos de proyectos con múltiples fuentes de financiación

_**Se aplica a:** Project Operations para escenarios basados en existencias/producción_

Algunos acuerdos contractuales para entregables basados en proyectos pueden requerir múltiples fuentes de financiación. Este tema explica cómo seleccionar y configurar las fuentes de financiación deseadas cuando se requieren múltiples fuentes para un proyecto o contrato de proyecto.

## <a name="terminology"></a>Terminología

- **Fuente de financiación**: la entidad que financia el trabajo del contrato del proyecto. Esta entidad puede ser una organización interna o una cuenta de facturación externa (cliente o concesión).
- **Cliente del proyecto**: la entidad a la que se entrega el trabajo del proyecto.
- **Cuenta de factura**: la entidad externa que paga por el trabajo del proyecto.

## <a name="example"></a>Ejemplo

Contoso ha ganado un contrato de renovación de equipos con dos de sus clientes: Adatum US y Adatum Corporate. El contrato incluye hardware y servicios de instalación que se entregarán a Adatum US (el cliente del proyecto). El hardware será financiado por Adatum Corporate (cuenta de factura 1), y el trabajo de instalación será financiado por Adatum US (cuenta de factura 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Configurar reglas predeterminadas de cuentas de facturas para requisitos de artículos

### <a name="prerequisites"></a>Requisitos previos

- Finanzas y operaciones de Microsoft Dynamics 365 Finance, **versión 10.0.27 o posterior**, es necesario para utilizar requisitos de artículos que tienen varias cuentas de facturación.
- Su administrador del sistema debe habilitar la característica **Permitir requisitos de artículos con múltiples fuentes de financiación para escenarios basados en producción/almacenamiento de Project Operations** en el espacio de trabajo **Gestión de características**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Configurar las reglas de incumplimiento de la cuenta de factura

Para configurar las reglas de incumplimiento de la cuenta de factura, siga estos pasos:

1. Vaya a **Gestión y contabilidad de proyectos** \> **Configuración** \> **Parámetros de gestión de proyectos y contabilidad**.
1. En la pestaña **General**, en la sección **Pedidos de ventas y requisitos de artículos**, configure la opción **Permitir proyectos con múltiples fuentes de financiación** en **Sí**.
1. En el campo **Cliente predeterminado**, especifique cuando el cliente de entrega del proyecto en el requisito del artículo proviene de manera predeterminada:

    - **De la fuente de financiación**: el cliente de entrega del proyecto predeterminado proviene de la fuente de financiación. Si se asocian varias fuentes de financiación con el contrato del proyecto, se utilizará la primera fuente de financiación de la lista.
    - **Del proyecto**: el cliente de entrega de proyecto predeterminado proviene del cliente seleccionado en el campo **Cuenta de registro del proyecto**.

1. Opcional: establezca o cambie la cuenta de facturación predeterminada en los registros del proyecto:

    1. Vaya a **Gestión de proyectos y contabilidad** \> **Proyectos** \> **Todos los proyectos** y abra los detalles del registro del proyecto.
    2. En la pestaña **General**, establezca o actualice el campo **Cuenta de factura predeterminada**. La cuenta que especifique se usará como la cuenta de facturación predeterminada para los nuevos requisitos de artículos que se creen para el proyecto. Si deja el campo en blanco, la cuenta de factura de la primera fuente de financiación del contrato del proyecto se utilizará de forma predeterminada. Sin embargo, los usuarios podrán cambiar la cuenta cuando guarden el registro.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Seleccione la cuenta de facturación que se usará al crear un requisito de artículo

Para seleccionar la cuenta de facturación que se usará al crear un requisito de artículo, siga estos pasos.

1. Vaya a **Gestión de proyectos y contabilidad** \> **Proyectos** \> **Todos los proyectos** y seleccione el registro del proyecto.
1. En la pestaña **Plan**, seleccione **Requisitos del artículo**.
1. Cree un nuevo registro de requisitos de artículos.

    - De forma predeterminada, el campo **Cuenta de factura** del registro se establece en la cuenta de factura que se establece para el proyecto. Puede cambiar el valor del campo **Cuenta de factura** y luego guardar el registro. Después de guardar el registro, ya no puede actualizar el valor **Cuenta de factura**. Si debe actualizar el valor **Cuenta de factura** para el requisito del artículo, elimine el requisito del artículo existente y luego cree uno nuevo que tenga el valor deseado.
    - Por defecto, el campo **Cliente** para el requisito del artículo se establece en función del valor **Cliente por defecto** que se establece en la página **Parámetros contables y de gestión de proyectos**.

    Cuando se guarda el registro de requisitos del artículo, el sistema lo asocia con el registro de cabecera **Pedido de ventas de requisitos de artículo**. Si ningún encabezado de pedido de ventas abierto tiene la cuenta de factura seleccionada, el sistema creará una y le asociará la línea de requisitos del artículo.

> [!NOTE]
> Los requisitos del artículo siempre se facturan en su totalidad a la cuenta de facturación que se establece en el registro. Actualmente, el sistema no admite reglas de asignación de fondos que tengan requisitos de artículos y no dividirá el registro en función de la configuración de las reglas de asignación de fondos.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Crear un requisito de artículo a partir de un registro de previsión de artículos

Para crear un requisito de artículo a partir de un registro de previsión de artículos, siga estos pasos.

1. Vaya a **Gestión de proyectos y contabilidad** \> **Proyectos** \> **Todos los proyectos** y seleccione el registro del proyecto.
1. En la pestaña **Plan**, seleccione **Previsiones del artículo**.
1. Cree un nuevo registro de previsiones de artículos.
1. Opcional: en la pestaña **Proyecto**, en el campo **Fuente de financiación**, seleccione la cuenta de factura deseada.
1. Seleccione **Crear requisito de artículo** y confirme el mensaje que reciba.

    > [!NOTE]
    > El sistema copia el valor **Fuente de financiación** del registro de previsión del artículo al registro de requisitos del artículo recién creado.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>La cuenta de factura es la predeterminada cuando el sistema crea automáticamente un requisito de artículo a partir de una línea de pedido de compra

Si la opción **Crear requisito de artículo** está configurada en **Sí** en la página **Parámetros contables y de gestión de proyectos**, el sistema crea automáticamente un requisito de artículo cuando se guarda una nueva línea de pedido de compra del proyecto. Por defecto, los campos **Cuenta de factura** y **Requisito del artículo** se establecen en el valor del campo **Cuenta de factura predeterminada** del registro del proyecto. Actualmente, el sistema no admite la actualización o el cambio de la cuenta de facturación para registros de este tipo.
