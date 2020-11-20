---
title: Instalación de datos de ejemplo
description: En este tema se proporciona información sobre instalar datos de ejemplo en Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 3c9cca7aa9d85bb38e48820b361ba07923ceddbd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132444"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Instalación de datos de ejemplo para la aplicación Project Service

Para ayudarle a crear sus propios entornos de demostración, Microsoft ofrece los paquetes descargables de datos de ejemplo que muestran las capacidades de sus aplicaciones. Hay dos tipos de paquetes de datos de ejemplo:
- datos de referencia/de configuración
- datos de demostración (referencia/configuración y datos transaccionales como órdenes de trabajo y proyectos)

Los paquetes de datos de **referencia** de ejemplo son descargables en tres paquetes diferentes, por lo que puede instalar datos solo para Project Service o solo para Field Service o bien puede instalar datos de ejemplo para ambas aplicaciones al mismo tiempo.

Los paquetes de datos de configuración/de referencia de ejemplo son:

- [**V902PSMasterData** - Solo Project Service versión 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - Solo Field Service versión 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x y Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

El paquete de datos de **demostración** más reciente es:

 - [**FPSDemoData** - Field Service 8.x y Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Las instrucciones de instalación difieren ligremente en los usuarios para crear y configurar la sección pero el resto está igual que en la anterior [**entrada de blog**](https://aka.ms/fpsdemodatablog). Este paquete incluye un conjunto de datos de demostración reducido y tarda aproximadamente 3 horas en instalarse.

Los paquetes de datos de ejemplo solo se encuentran disponibles en inglés.

> [!IMPORTANT]
> **No hay forma de desinstalar los datos de ejemplo.** Solo debe instalar estos paquetes en sistemas de demostración, evaluación, formación o pruebas. Tenga en cuenta también que no se admite instalar un paquete individual y, a continuación instalar otro paquete individual. (Es decir no puede instalar **FSMasterData** seguido de **PSMasterData**, o viceversa). Si ve que necesita de datos de ejemplo para ambas aplicaciones en cualquier momento en el futuro, debe instalar el paquete **v902FPSMasterData**.

Al instalar los paquetes cualquiera de los paquetes de datos de ejemplo, el proceso de instalación realiza las siguientes acciones:

- Crea o define parámetros predeterminados para usar Project Service, Field Service, o ambas aplicaciones (si corresponde).

- Importa datos de ejemplo para las aplicaciones, como recursos reservables, los roles específicos de la aplicación, ventas y listas de precios de coste, unidades organizativas, los registros de proceso de ventas, y otras entidades para mostrar las capacidades clave.  

Con el paquete de **datos de demostración**, obtiene los datos transaccionales anteriores y adicionales como órdenes de trabajo y proyectos.

¿Quiere saber qué capacidades puede demostrar con los datos de ejemplo? Consulte el escenario ficticio Fabrikam Robotics en [Notas técnicas](#technical-notes).

Si tiene preguntas sobre estos la instalación de estos paquetes de datos de ejemplo [envíenos un correo electrónico a fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Requisitos

El protocolo de instalación asume lo siguiente sobre la instancia de destino (organización):

- El idioma base es Inglés y la divisa base el dólar americano (USD,$).

- La organización aún no tiene datos de Project Service o Field Service, o sólo tiene datos predeterminados básicos que vienen con cualquier nueva organización.

- La versión adecuada de la aplicación empresarial ya está instalada:
       
    - **Para FPSDemoData o v902FPSMasterData:** La organización tiene Field Service versión 8.x y Project Service versión 3.x instaladas.

    - **Para v902PSMasterData:** La organización tiene Project Service versión 3.x instalada.

    - **Para v902FSMasterData:** La organización tiene Field Service versión 8.x instalada.

> [!NOTE]
> Si necesita instalar los datos de ejemplo sobre un entorno de prueba o demostración de Project Service o Field Service existente que ya tiene datos (no recomendado), deberá suspender los controles previos de seguridad realizados por el instalador. Para obtener más información, consulte las notas técnicas a continuación.

## <a name="prepare-for-installation"></a>Preparar para la instalación

Debe ejecutar el instalador en un equipo con una versión de Windows reciente (Windows 10 preferida).

Debe planificar para que el equipo permanezca conectado a una red, y para que la instalación se ejecute un máximo de **1 hora** para **datos de configuración/referencia**. (Normalmente la instalación tarda unos 30 minutos para **FPSMasterData**, que incluye datos de ejemplo para ambas aplicaciones). Para **FPSDemoData**, la instalación tarda unas **3 horas**.

El equipo debe tener la función de protector de pantalla desactivada. De lo contrario, las credenciales de sesión para la instalación se pueden perder cuando se active el protector de pantalla (a menos que mantenga la sesión activa todo el tiempo).

> [!div class="mx-imgBorder"]
> ![Captura de pantalla de la configuración del protector de pantalla con el protector de pantalla desactivado](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Descargar y desempaquetar

El instalador de los datos de ejemplo de Project Service y Field Service se distribuye como ejecutable autoextraíble. Los nombres de archivo pueden variar según el paquete de datos de ejemplo, pero por lo demás los pasos son los mismos para el paquete que instale.

Después de descargar un paquete, ejecute el archivo .exe y, a continuación acepte las condiciones para desempaquetar el archivo zip comprimido. Entonces deberá extraer el contenido de ese archivo en una carpeta en el equipo.

En función del sistema operativo y de la configuración de seguridad, es posible que deba realizar los siguientes pasos después de desempaquetar el archivo zip:

1. Busque y haga clic con el botón secundario en el archivo **FPSDemoData.dll** en la carpeta **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Elija **Desbloquear**.

3. Seleccione **Aplicar**.

4. Seleccione **Aceptar**.


## <a name="create-or-configure-users"></a>Creación o configuración de los usuarios

El paquete **FPSDemoData** requiere seis usuarios mientras que los paquetes **FPSMasterData** requiere un usuario. Consulte el adecuado para su paquete de datos de ejemplo.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Creación o configuración de los usuarios - paquetes de datos de configuración/referencia

El paquete **FPSMasterData** está diseñado para instalación con un usuario llamado Spencer Low con la configuración descrita aquí. Para instalar el paquete correctamente, debe crear (o cambiar temporalmente) usuarios en su entorno para que coincidan con la configuración entrante de datos de ejemplo.

Para crear o configurar usuarios, vaya a **Configuración** > **Seguridad** > **Usuarios**, y realice lo siguiente:

1. Establezca UserFullname=”Spencer Low” con el nombre de usuario “spencerl” (**minúscula**) en los roles de Administrador de proyecto y Director de prácticas.

2. Seleccione el usuario **Spencer Low** y después seleccione **Administrar roles**. Busque y seleccione el rol **Administrador del sistema** y, a continuación seleccione **Aceptar** para conceder derechos completos de administración a Spencer Low. Este paso es necesario para garantizar que los registros de ejemplo se crean con la propiedad del usuario correcto y por tanto rellenar las vistas correctamente.

3. Desde el paquete descargado, necesita actualizar un archivo de asignación de datos con direcciones de correo electrónico del contexto del usuario predeterminado. Para ello, abra **PkgFoldery**, a continuación busque y abra el archivo **ImportUserMapFile.xml** en Bloc de notas (o Visual Studio u otro editor XML). Establezca el campo **DefaultUserToMapTo=** en la dirección de correo electrónico del usuario Spencer Low.

4. Si no está usando Spencer Low con el nombre de usuario **spencerl**, necesita actualizar un archivo adicional. Abra el archivo **DemoDataPreImportConfig.xml** y, a continuación busque la etiqueta **userstocreateandconfigure**. Actualice la etiqueta **\<login\>** con el nombre de usuario del usuario Spencer Low. Para obtener más información, consulte [Notas técnicas](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Creación o configuración de los usuarios - Paquete de datos de demostración

El paquete de datos de demostración requiere seis usuarios. Para que el paquete se instale correctamente, haga lo siguiente:

 1. Cree o cambie temporalmente el nombre de los usuarios existentes para coincidir con la configuración entrante de datos de ejemplo yendo a **Valores** > **Seguridad** > **Usuarios**.
 
    Estos roles son solo necesarios para demostraciones basadas en personas.  
    - Nombre completo del usuario ="David So" como técnico de Field Service   
    - Nombre completo del usuario="Jamie Reding" como distribuidor de Servicio al cliente y Field Service   
    - Nombre completo del usuario="Molly Clark" como administrador de cuentas   
    - Nombre completo del usuario="Spencer Low" como prácticas y jefe de proyecto  
    - Nombre completo del usuario="Veronica Quek" como Miembro del equipo   
    - Nombre completo del usuario="William Contoso"
  
2. Para la importación de datos de demostración, asigne a los seis usuarios anteriores el rol de administrador de modo que los registros de ejemplo se importen correctamente. 

3. Abra **PkgFolder** y, a continuación, busque y abra **ImportUserMapFile.xml**. Actualice los campos **Nuevo=** a las direcciones de correo electrónico de los usuarios correspondientes en el sistema.

   > [!div class="mx-imgBorder"]
   > ![Captura de pantalla de UserMapFile](media/sample-data-7.png)

4. Si el usuario de nombre completo "Spencer Low" tiene otra id. de usuario que **“spencerl”**, necesita actualizar un archivo adicional. Abra **DemoDataPreImportConfig.xml** y busque la etiqueta **userstocreateandconfigure**. Actualice la etiqueta **\<login\>** con el loginId (sensible a mayúsculas y minúsculas). 

5. El calendario del primer usuario (en la etiqueta **userstocreateandconfigure**) se usa para rellenar las horas laborables para todos los recursos reservables en la importación de datos de demostración. Vaya a **Configuración** > **Seguridad** > **Usuarios**, busque al usuario "Spencer Low" y abra la opción de "Horas laborables". Edite las horas laborables existentes seleccionando la opción **Toda la programación semanal periódica de principio a fin**. Asegúrese de que **Las horas laborables se establecen de 8 - 5 p.m. (9 horas), de lunes a viernes y con la zona horaria ajustada a la hora del Pacífico (EE.UU. y Canadá)**. Esto es necesario para asegurarse de que el proyecto y el tablero de programación se muestran como se espera.

**Recomendación:** Considere crear una copia de seguridad de su organización ahora, por si acaso necesita revertir al punto de partida si algo sale mal durante la instalación de los datos de ejemplo. Para obtener más información, vea [Copia de seguridad y restauración de instancias](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Ejecute el Package Deployer

1. Busque y ejecute **PackageDeployer.exe** en la carpeta **v902FPSMasterData** o **PackageDeployer_FPSDemoData**.

2. Acepte los términos y las condiciones

3. En la siguiente ventana:

   a. Seleccionar una implementación tipo **Office 365**.

   b. Use el usuario y la contraseña del usuario administrador del sistema configurados en “Crear o configurar usuarios” (”Spencer Low” con nombre de usuario “spencerl”).

   c. Asegúrese de que **Mostrar la lista de organizaciones disponibles** esté seleccionado.

      > [!div class="mx-imgBorder"]
      > ![Captura de pantalla de la ventana del Package Deployer con la opción "Mostrar la lista de organizaciones disponibles" seleccionada](media/sample-data-2.png)

4. Seleccione la organización donde desea instalar los datos de ejemplo.

5. Seleccione **Siguiente** hasta que vea el diálogo **Configurar datos de demostración**.

   > [!div class="mx-imgBorder"]
   > ![Captura de pantalla de la ventana de estado del instalador de los datos de demostración](media/sample-data-3.png)

6. Antes de continuar, tenga en cuenta que instalar datos de ejemplo puede tardar hasta una hora (normalmente ~10 minutos). Deberá asegurarse de que el equipo permanecerá encendido y conectado a una red durante todo el proceso de instalación, y que la sesión permanece activa.   

7. Cuando esté listo, haga clic en **Siguiente** para iniciar el proceso de instalación de datos de ejemplo. Después de cargar los datos de ejemplo, haga clic en **Finalizar**.

## <a name="verify-the-sample-data-installation"></a>Compruebe la instalación de los datos de ejemplo

Para una comprobación de estado, compruebe que aparecen el número de registros y los tipos de entidades incluidas en escenario ficticio Fabrikam Robotics correctamente.

Una vez que los datos de ejemplo se carguen completamente, inicie sesión como el usuario Spencer Low y confirme lo siguiente:

- Si la aplicación Project Service está instalada, vaya a **Project Service** > **Configuración** > **Listas de precios**. Confirme que existen tasas de facturación y tasas de coste con la divisa adecuada para cada país o región en el conjunto de datos.

- Si la aplicación Project Service está instalada, vaya a **Universal Resource Scheduling** > **Configuración** > **Unidades organizativas**. Confirme que una lista de precios de coste con la divisa adecuada se ha asociado con cada unidad organizativa (salvo entradas de ciudad). Si faltan alguna, busque y asocie la lista de precios de coste adecuada.

- Si la aplicación Field Service está instalada, vaya a **Project Service** > **Configuración** > **Listas de precios**. Confirme que existen tasas de facturación y las tasas de coste. Vaya a **Field Service** > **Configuración** > **Listas de precios** y compruebe que hay tasas de facturación y tasas de coste, con la divisa adecuada para cada país o región en el conjunto de datos.

  > [!div class="mx-imgBorder"]
  > ![Captura de pantalla de listas de precios activos](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Captura de pantalla de unidades organizativas activas](media/sample-data-5.png)

## <a name="technical-notes"></a>Notas técnicas

Consulte a continuación para obtener más detalles técnicos sobre la instalación de estos datos.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Instalación de datos de ejemplo sobre datos existentes (no recomendado)

Si necesita instalar datos de ejemplo sobre un entorno de prueba o demostración de Field Service o Project Service existente que ya tiene datos, deberá suspender los controles previos de seguridad realizados por el instalador.

Para ello, vaya a la carpeta **PkgFolder** para buscar y abrir el archivo **DemoDataPreImportConfig.xml** con Bloc de notas (u otro editor XML).

Busque el valor siguiente y, a continuación cambie el valor de true a false:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Este cambio hace que el instalador omita algunas comprobaciones de seguridad importantes, entre ellas:

- Confirmar que no hay más que un registro activo **Unidad organizativa** y, a continuación cambiar su nombre a **Fabrikam US**.

- Confirmar que no hay más que un registro activo **Plantilla de trabajo**.

- Confirmar que no hay más que un registro activo **Parámetro de proyecto** y, a continuación cambiar el nombre de esa entidad a **Parameters**.

### <a name="configuration-components"></a>Componentes de configuración

Hay varios otros componentes de configuración en este archivo de configuración previo a la importación. Para usuarios técnicos, algunos de estos incluyen:

- **\<RequiredSolutions\>** especifica las instalaciones de la solución requeridas previamente y sus números de versión.

- **\<InstallSampleData\>** controla si se instalan los datos de ejemplo estándar para las aplicaciones.

    - false - omite la instalación de estos datos integrados (que son extraíbles)

    - true - instala los datos integrados simultáneamente con la instalación de los datos de ejemplo de FS y PSA

- **\<PreImportDataCollection\>** especifica las asignaciones de datos de archivo plano y los registros asociados que se importarán por delante de la instalación de los datos de ejemplo principales.

- **\<EntitiesToEnableScheduling\>** especifica qué entidades deben ser habilitadas para reservar en Microsoft Dynamics Scheduling (alias Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** especifica los recursos reservables que se crearán (si no existen aún) antes de que la importación de datos de ejemplo se ejecute. Tenga en cuenta que los recursos reservables de los datos de ejemplo del sistema de origen coinciden con los registros de recursos reservables del sistema de destino en FullName e inicio de sesión de cada recurso. Por tanto, NO es posible cambiar los nombres de este archivo de preconfiguración a menos que primero importe datos de ejemplo en un sistema de destino utilizando estos nombres, luego cambie el nombre de los recursos reservables al nombre que desee junto con los registros de usuarios habilitados y, a continuación exporte los datos de nuevo para importarlos en el sistema de destino final (actualizando las entradas antiguas y nuevas de **ImportUserMapFile.xml** en consecuencia).

- **\<PluginsToDisable\>** especifica complementos de línea de producto muy discretos que es necesario deshabilitar durante la importación de datos de ejemplo y volver a habilitar posteriormente.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Escenario ficticio Fabrikam Robotics

Los paquetes de datos de ejemplo de referencia de Field Service y Project Service instalan la **Solución de datos Fabrikam Manufacturing Master Data (v3.0.0.0)**, junto con aproximadamente 4.000 registros y aproximadamente 40 entidades distintas. Los paquetes separados de datos de ejemplo para Field Service o Project Service contienen un subconjunto de los datos de ejemplo **v902FPSMasterData** de esa aplicación. El paquete **Demo Data** instala la **solución de datos de demostración de Fabrikam Manufacturing (v3.0.0.7)** con aproximadamente 22.000 registros a través de 148 entidades.

La compañía ficticia Fabrikam Robotics es fabricante de robots de línea de montaje de dispositivos electrónico y se conoce por la calidad de sus productos, la innovación y la sólida atención al cliente, incluidos servicios de planeamiento de instalación, implementación y mantenimiento continuo. Fabrikam tiene su sede en Estados Unidos (Fabrikam Estados Unidos)., y tiene operaciones de servicio basadas en proyectos en Francia, India, Reino Unido, y Suiza.

Las operaciones de Field Service se centran en Estados Unidos, sobre todo en el área del gran Seattle. La empresa se centra en sacar provecho de la conectividad de Internet de las Cosas (IoT) para supervisar la efectividad de activos del cliente y para ofrecer servicios proactivos in situ.

A continuación se ofrece un resumen de alto nivel de los datos de ejemplo:

- Elementos de datos de ejemplo comunes (incluidos para ambas aplicaciones)

    - 1 usuario

    - 71 cuentas

    - 137 contactos

    - Diferentes tipos y categorías de transacciones

    - 50 productos con 1 lista de precios de productos

    - 14 listas de precios/costes

    - 31 características (cualificaciones de recursos) en 2 modelos de clasificación con niveles 3 (valores de clasificación)

- Project Service

    - 8 unidades organizativas

    - 6 niveles de uso específicos del rol

    - Más de 2.800 especificaciones para precios de rol

- Field Service

    - 4 zonas de ventas

    - 5 tipos de orden de trabajo

    - 22 activos de cliente

    - 9 tipos de incidentes con un intervalo de características de recurso asociadas (9), servicios (13) y tareas de servicio (13)
   
El paquete **Datos de demostración** instala aproximadamente 179 órdenes de trabajo, 12 proyectos y datos transaccionales asociados. 

### <a name="change-the-work-hours-for-sample-resources"></a>Cambiar las horas laborables para recursos de ejemplo

De forma predeterminada, todos los recursos reservables tienen un calendario de 24 horas laborables.

Si necesita cambiar las horas laborables de los recursos reservables de ejemplo, vaya a **Universal Resource Scheduling** > **Programación** > **Recursos**.

Seleccione un usuario (por ejemplo, Spencer Low) y cambie las horas laborables de Spencer por las horas que desea aplicar a varios usuarios. Vaya a **Universal Resource Scheduling** > **Configuración** > **Plantilla de horas laborables** y edite el registro **Plantilla de trabajo predeterminada**. En el campo **Recurso de plantilla**, seleccione un usuario con las horas laborables que desea aplicar a otros recursos. Vaya **Universal Resource Scheduling** > **Programación** > **Recursos** > .**Recursos reservables activos** Seleccione los recursos que desee cambiar y, a continuación seleccione **Establecer calendario**. En la lista desplegable **Plantilla de trabajo** , seleccione la plantilla **Hora laborable predeterminada** u otra plantilla con el recurso de plantilla correcto. Cuando vuelva al tablero de programación, verá que los recursos ahora tienen horas laborables actualizadas.

> [!div class="mx-imgBorder"]
> ![Captura de pantalla de recursos reservables activos](media/sample-data-6.png)
