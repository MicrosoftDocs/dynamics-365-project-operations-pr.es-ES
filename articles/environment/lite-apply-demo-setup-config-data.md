---
title: Aplicar datos de configuración y configuración de demostración (lite)
description: Este tema proporciona información sobre cómo aplicar la configuración de demostración y los datos de configuración para las operaciones de proyecto.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 421c9d28088c92617687641d93b3ad5d6bfea73c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642114"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Aplicar datos de configuración y configuración de demostración para Project Operations (lite) 

_**Implementación simplificada: facturación de oferta a proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Requisitos previos

Antes de comenzar la configuración, debe tener un entorno de Common Data Service (CDS) aprovisionado para Dynamics 365 Project Operations.


## <a name="instructions"></a>Instrucciones

1. Descargar el [Paquete de datos maestros](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Navegue a la carpeta *ProjOpsDemoDataSetupAndMaster - Integrated CMT* y ejecute el archivo ejecutable *DataMigrationUtility*.
3. En la página 1 del Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** y luego seleccione **Continuar**.

![Migración de la configuración](./media/1ConfigurationMigration.png)

4. En la página 2 del asistente CMT, seleccione **Microsoft 365** como **Tipo de implementación**.
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

-   Moneda
-   Cuenta
-   Unidad organizativa
-   CONTACTO
-   Grupo fiscal
-   Grupo de clientes
-   Unidad
-   Unidad de venta
-   Lista de precios
-   Lista de precios de parámetros de proyecto 
-   Frecuencia de facturación
-   Categoría de recurso reservable
-   Categoría de transacción
-   Categoría de gastos
-   Precio de rol
-   Precio de categoría de transacciones
-   Característica
-   Recurso reservable
-   Asociación de categoría de recurso reservable
-   Característica del recurso reservable

![Completar importación](./media/6CompleteImport.png)
