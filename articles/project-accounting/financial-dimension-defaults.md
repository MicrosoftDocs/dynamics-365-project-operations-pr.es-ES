---
title: Valores predeterminados de dimensiones financieras
description: Este tema proporciona información sobre cómo configurar los valores predeterminados de la dimensión financiera.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131904"
---
# <a name="financial-dimension-defaults"></a>Valores predeterminados de dimensiones financieras

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Dynamics 365 Project Operations usa el marco [Dimensiones financieras](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) en Dynamics 365 Finance para proporcionar información adicional sobre las transacciones del libro mayor auxiliar y del libro mayor general del proyecto.

Las dimensiones financieras predeterminadas se pueden establecer en un cliente, una fuente de financiación del proyecto, un hito, una línea de contrato del proyecto o un proyecto.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Definir dimensiones financieras predeterminadas para un cliente

Los valores predeterminados de la dimensión del cliente se especifican en Finance. Complete los pasos siguientes para establecer los valores predeterminados de dimensión.

1. Vaya a **Clientes** > **Clientes** > **Todos los clientes**.
2. Sobre la página **Clientes**, en la pestaña **Dimensiones financieras**, establezca los valores de la dimensión financiera para un cliente específico.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Definir dimensiones financieras predeterminadas para contratos de proyectos

Los contratos de proyecto se crean y mantienen en Common Data Service (CDS). Los atributos contables para los contratos de proyecto se establecen en el módulo **Gestión de proyectos y contabilidad** en Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Establecer dimensiones financieras para una fuente de financiación de proyectos

1. Vaya a **Gestión de proyectos y contabilidad** > **Proyectos** > **Contratos de proyecto**.
2. Seleccione el registro que desea actualizar y en la pestaña **Contrato de proyecto**, seleccione **Mostrar contabilidad predeterminada**.
3. Expanda **Información relacionada** y seleccione la pestaña **Fuentes de financiamiento**.
4. Estalbezca los valores predeterminados de dimensiones financieras. Observe que las dimensiones financieras usan los valores predeterminados de la cuenta del cliente.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Establecer dimensiones financieras para una línea de contrato de proyectos

1. Vaya a **Gestión de proyectos y contabilidad** > **Proyectos** > **Contratos de proyecto**.
2. Seleccione el registro que desea actualizar y en la pestaña **Contrato de proyecto**, seleccione **Mostrar contabilidad predeterminada**.
3. Expanda **Información relacionada** y seleccione la pestaña **Líneas de contrato**.
4. Estalbezca los valores predeterminados de dimensiones financieras. Los valores predeterminados de la dimensión financiera son aplicables y solo se pueden usar con líneas de contrato de precio fijo (hito).

Estos valores predeterminados se utilizan en transacciones a cuenta del proyecto y líneas de factura relacionadas.

## <a name="define-default-financial-dimensions-for-projects"></a>Definir dimensiones financieras predeterminadas para proyectos

Los proyectos se crean y mantienen en CDS. Los atributos contables para proyectos se establecen en el módulo **Gestión de proyectos y contabilidad** en Finance.

1. Vaya a **Gestión de proyectos y contabilidad** > **Proyectos** > **Todos los proyectos**.
2. Seleccione el registro que desea actualizar y en la pestaña **Proyecto**, seleccione **Mostrar contabilidad predeterminada**.
3. Expanda **Información relacionada** y seleccione la pestaña **Configuración**.
4. Estalbezca los valores predeterminados de dimensiones financieras. Observe que las dimensiones financieras usan los valores predeterminados de la cuenta del cliente. Si el proyecto está asociado con una línea de contrato con varios clientes de contrato de proyecto, el cliente principal se utiliza para las dimensiones financieras predeterminadas.

Las dimensiones financieras predeterminadas del proyecto se utilizan para establecer los valores predeterminados de las líneas de diario para las transacciones de tiempo, gastos y tarifas en el **Diario de integración de Project Operations** y en las líneas de factura de proyectos relacionados.
