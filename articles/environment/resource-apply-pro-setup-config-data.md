---
title: Configurar y aplicar datos de configuración en Common Data Service
description: Este tema proporciona información sobre cómo instalar y aplicar los datos de configuración en Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6fb91de30a2414fa7dd8dba47b28cf4824948565
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594737"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Configurar y aplicar datos de configuración en Common Data Service 

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_



## <a name="prerequisites"></a>Requisitos previos

Antes de comenzar a configurar los datos en Common Data Service (CDS), se deben cumplir los siguientes requisitos previos:

1.  Aprovisione un entorno de CDS y un entorno de Dynamics 365 Finance para Project Operations.
2.  La información de la entidad jurídica de Dynamics 365 Finance se comparte con el entorno de CDS. Esto significa que la entidad **Empresa** en CDS tiene los siguientes registros de empresa:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Instalar la configuración y los datos de configuración

1. Descargue, desbloquee y descomprima el [Paquete de instalación y datos de configuración](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).
2. Navegue a la carpeta descomprimida y ejecute el archivo ejecutable *DataMigrationUtility*.
3. En la página 1 del Asistente de migración de configuración (CMT) de Common Data Service, seleccione **Importar datos** y luego seleccione **Continuar**.

![Migración de la configuración.](./media/1ConfigurationMigration.png)

4. En la página 2 del asistente CMT, seleccione **Microsoft 365** como **Tipo de implementación**.
5. Seleccione las casillas **Mostrar una lista de organizaciones disponibles** y **Mostrar avanzadas**.
6. Seleccione la región de su inquilino, introduzca sus credenciales y luego seleccione **Iniciar sesión**.

![Inicio de sesión de la configuración.](./media/2ConfigurationSignin.png)

7. En la página 3, en la lista de organizaciones del inquilino, seleccione la organización a la que desea importar los datos de demostración y seleccione **Iniciar sesión**.
8. En la página 4, seleccione el archivo zip *SampleSetupAndConfigData* en la carpeta descomprimida.

![Selección de archivo zip.](./media/3ZipFile.png)

![Seleccionar un archivo.](./media/4SelectAFile.png)

9. Después de seleccionar el archivo zip, seleccione **Importar datos**.

![Importar datos.](./media/5ImportData.png)

10. La importación se ejecutará durante aproximadamente de dos a diez minutos, según la velocidad de su red. Una vez finalizada la importación, salga del asistente de CMT. 
11. Compruebe si su organización dispone de datos en las siguientes 26 entidades:

  - Moneda
  - Plan de cuentas
  - Calendario fiscal
  - Tipos de cambio de divisas
  - Día de pago
  - Multivencimientos
  - Condiciones de pago
  - Unidad organizativa
  - CONTACTO
  - Grupo fiscal
  - Grupo de clientes
  - Grupo de proveedores
  - Unidad
  - Unidad de venta
  - Lista de precios
  - Lista de precios de parámetros de proyecto
  - Frecuencia de facturación
  - Categoría de recurso reservable
  - Categoría de transacción
  - Categoría de gastos
  - Precio de rol
  - Precio de categoría de transacciones
  - Característica
  - Recurso reservable
  - Asociación de categoría de recurso reservable
  - Característica del recurso que se puede reservar

![Completar importación.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Actualizar configuraciones de operaciones de proyecto

1. Vaya al entorno CE. Puede encontrarlo abriendo el [Centro de administración de Power Platform](https://admin.powerplatform.microsoft.com/environments), seleccionando el entorno y luego seleccionando **Abrir entorno**. 

![Abrir entorno.](./media/7OpenEnvironment.png)

2. Vaya a **Proyectos** > **Recursos** y luego seleccione **Nuevo** para crear un recurso que se pueda reservar para su usuario.

![Recursos que se pueden reservar.](./media/8BookableResources.png)

3. En la pestaña **General**, seleccione su usuario administrador. Verifique que la zona horaria coincida con la que se encuentra. 

![Nuevo recurso reservable.](./media/9NewBookableResource.png)

4. En la pestaña **Planificación** del campo **Empresa**, elija la empresa **USPM** y luego seleccione **Guardar**. 

![Pestaña de programación.](./media/10SchedulingTab.png)

5. Seleccione la pestaña **Horas de trabajo**.  

![Horas laborables.](./media/11WorkHours.png)

6. Haga doble clic en cualquier valor del calendario y seleccione **Editar** > **Todos los eventos de la serie**. 

![Calendario de trabajo.](./media/12WorkCalendar.png)

7. Cambie el horario laboral a un día laborable de ocho (8) horas, marque los fines de semana como días no laborables y asegúrese de que la zona horaria coincida con la suya. 
8. Seleccione **Guardar y cerrar**.

![Actualizar calendario.](./media/13UpdateCalendar.png)

9. Vaya a **Configuración** > **Plantillas de calendario** y seleccione **Nueva**.
 
 ![Plantillas de calendario.](./media/14CalendarTemplates.png)
 
 10. Introduzca un nombre, seleccione el recurso de plantilla que creó y luego seleccione **Guardar**. 
 
 ![Guardar plantilla de calendario.](./media/15SaveCalendarTemplate.png)
 
 11. Vaya a **Parámetros** y haga doble clic en el registro. 
 
 ![Parámetros de proyecto.](./media/16ProjectParameters.png)
 
12. Actualice los siguientes campos:

 - **Empresa predeterminada**: USPM
 - **Unidad organizativa predeterminada**: Contoso Robotics Global
 - **Frecuencia de facturación**: séptimo y último día
 - **Plantilla de horas de trabajo**: cambia a la plantilla que creó.

13. Seleccione **Guardar**. 

![Parámetros de proyecto actualizados.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
