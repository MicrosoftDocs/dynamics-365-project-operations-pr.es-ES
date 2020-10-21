---
title: Aplicar datos de configuración y de preparación de demostración
description: Este tema proporciona información sobre cómo aplicar la configuración de demostración y los datos de configuración para las operaciones de proyecto.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949087"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Aplique la configuración de demostración y los datos de configuración para la implementación simplificada de Project Operations: facturación de oferta a proforma

_**Implementación simplificada: facturación de oferta a proforma_

1. Descargar el [Paquete de datos maestros](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Navegue a la carpeta *ProjOpsDemoDataSetupAndMaster - Integrated CMT* y ejecute el archivo ejecutable *DataMigrationUtility*.
3. En la página 1 del Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** y luego seleccione **Continuar**.

![Migración de la configuración](./media/1ConfigurationMigration.png)

4. En la página 2 del asistente CMT, seleccione **Office 365** como **Tipo de implementación**.
5. Seleccione las casillas **Mostrar una lista de organizaciones disponibles** y **Mostrar avanzadas**.
6. Seleccione la región de su inquilino, introduzca sus credenciales y luego seleccione **Iniciar sesión**.

![Inicio de sesión de configuración](./media/2ConfigurationSignin.png)

7. En la página 3, en la lista de organizaciones del inquilino, seleccione a qué organización desea importar los datos de demostración y luego seleccione **Iniciar sesión**.
8. En la página 4, seleccione el archivo zip *MasterAndSetupData* de la carpeta descomprimida *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.

![Archivo Zip](./media/3ZipFile.png)

![Seleccione un archivo](./media/4SelectAFile.png)

9. Después de seleccionar el archivo zip, seleccione **Importar datos**.

![Importar datos](./media/5ImportData.png)

10. La importación se ejecutará durante aproximadamente de dos a diez minutos, según la velocidad de su red. Una vez finalizada, salga del asistente de CMT. 
11. Compruebe si su organización dispone de datos en las siguientes 20 entidades:

- Divisa
- Unidad organizativa
- CONTACTO
- Grupo fiscal
- Grupo de clientes
- Unidad
- Unidad de venta
- Lista de precios
- Lista de precios de parámetros de proyecto
- Frecuencia de facturación
- Detalle de frecuencia de factura
- Categoría de recurso reservable
- Categoría de transacción
- Categoría de gastos
- Precio de rol
- Precio de categoría de transacciones
- Característica
- Recurso reservable
- Asociación de categoría de recurso reservable
- Característica del recurso reservable

![Completar importación](./media/6CompleteImport.png)
