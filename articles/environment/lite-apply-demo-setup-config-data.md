---
title: Aplicar datos de configuración y configuración de demostración (lite)
description: Este artículo proporciona información sobre cómo aplicar datos de instalación y configuración para Project Operations.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811047"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Aplicar datos de configuración y configuración de demostración para Project Operations (lite) 

_**Implementación simplificada: facturación de oferta a proforma_



## <a name="prerequisites"></a>Requisitos previos

Antes de comenzar la configuración, debe tener un entorno de Dataverse aprovisionado para Dynamics 365 Project Operations.


## <a name="instructions"></a>Instrucciones

1. Descargar el [Paquete de datos de instalación](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Vaya a la carpeta *ProjOpsSampleSetupData - CE solo CMT* y ejecute el archivo ejecutable *DataMigrationUtility*.
1. En la página 1 del Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** y luego seleccione **Continuar**.

    ![Migración de la configuración.](./media/1ConfigurationMigration.png)

1. En la página 2 del asistente CMT, seleccione **Microsoft 365** como **Tipo de implementación**.
1. Seleccione las casillas **Mostrar una lista de organizaciones disponibles** y **Mostrar avanzadas**.
1. Seleccione la región de su inquilino, introduzca sus credenciales y luego seleccione **Iniciar sesión**.

   ![Inicio de sesión de la configuración.](./media/2ConfigurationSignin.png)

1. En la página 3, en la lista de organizaciones del inquilino, seleccione a qué organización desea importar los datos de demostración y luego seleccione **Iniciar sesión**.
1. En la página 4, seleccione el archivo zip *SampleSetupAndConfigData* de la carpeta descomprimida, *ProjOpsSampleSetupData - CE solo CMT*.

   ![Archivo Zip.](./media/3ZipFile.png)

   ![Seleccionar un archivo.](./media/4SelectAFile.png)

1. Después de seleccionar el archivo zip, seleccione **Importar datos**.

   ![Importar datos.](./media/5ImportData.png)

1. La importación se ejecutará durante aproximadamente de dos a diez minutos, según la velocidad de su red. Una vez finalizada, salga del asistente de CMT. 
1. Compruebe si su organización dispone de datos en las siguientes 18 entidades:

    -   Moneda
    -   Cuenta
    -   Unidad organizativa
    -   CONTACTO
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
    -   Característica del recurso que se puede reservar

    ![Completar importación.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
