---
title: Unidades organizativas
description: Este tema describe el concepto de unidades organizativas y explica cómo crear y mantener unidades organizativas en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9a8c503dc6286f40c80ed9b7a8a04974ff7e50b4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581397"
---
# <a name="organizational-units-overview"></a>Descripción general de las unidades organizativas

En Microsoft Dynamics 365 Project Operations, una *unidad organizativa* es un grupo o división distinta de una compañía de servicios profesionales que emplea recursos facturables que tienen índices de costes.

Para compañías de servicios profesionales que emplean recursos técnicos en diferentes áreas de práctica o líneas de negocio, el coste para desempeñar un rol puede variar, dependiendo del área de práctica o línea de negocio donde se desempaña el rol. En este escenario, el concepto de unidades organizativas ayuda, al proporcionar una forma de agrupar un conjunto de roles facturables en una división de una compañía que tiene una estructura de costes distinta para esos roles.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>El concepto de unidades organizacionales en Project Operations

En Project Operations, una unidad organizativa tiene una divisa específica y listas de precios de coste específicas.

La divisa de una unidad organizativa es la divisa principal que se usa para el seguimiento de los costes.

Es posible adjuntar una o varias listas de precios de coste a cada unidad organizativa. Project Operations impone las siguientes limitaciones en las listas de precios que pueden adjuntarse a una unidad organizativa:

- Las listas de precios deben estar en la divisa de la unidad organizativa.
- Las listas de precios deben ser listas de precios de coste.

Además, la entidad Recurso incluye un atributo para la unidad organizativa. Cada usuario puede asignarse a una unidad organizativa.

### <a name="roles-of-organizational-units"></a>Roles de las unidades organizativas

La unidad organizativa desempeña dos roles en Project Operations:

- **Unidad de contratación**: unidad organizativa que representa el grupo o la división de la compañía responsable de lograr la venta y administrar la entrega del trabajo y los servicios al cliente. La unidad de contratación se identifica con el campo **Unidad de contratación** en la sección del encabezado de las páginas **Oportunidad**, **Oferta**, **Contrato del proyecto** y **Proyecto**.
- **Unidad de dotación de recursos**: unidad organizativa a la que pertenece o está asignado un recurso. Esta unidad organizativa puede ofrecer sus recursos para determinados roles en declaraciones del trabajo (SOW) y proyectos que son propiedad de la unidad de contratación.

![Unidades de contratación y unidades de dotación de recursos.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Preguntas frecuentes sobre unidades organizativas

A continuación se muestran algunas de las preguntas más frecuentes acerca de las unidades organizativas.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>¿Cómo se relaciona la entidad Unidad organizativa en Project Operations con la entidad Organización que ya existe en Dynamics 365?

La entidad Organización de Dynamics 365 representa el nombre de una instancia global de Dynamics 365. Este nombre suele ser el nombre de la empresa global.

La entidad Unidad organizativa representa un grupo o una división de la empresa global. Este grupo o división cuenta con un conjunto de roles y una lista de precios de coste para dichos roles. Estos roles y esta lista de precios no son iguales que los de otros grupos o divisiones de la empresa.

Al instalar Project Operations se crea una unidad organizativa predeterminada en función de la organización. Todos los recursos existentes se asignan a la unidad organizativa predeterminada. Si se importan nuevos recursos o usuarios de Active Directory en Dynamics 365, el proceso de importación de usuarios los asigna a la unidad organizativa predeterminada en Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>¿Qué diferencias hay entre la entidad Unidad organizativa y la entidad Unidad de negocio?

En Dynamics 365, la entidad Unidad de negocio es una construcción de seguridad. La asociación de un usuario a una unidad de negocio determina las entidades y los registros de entidad a los que el usuario tiene acceso. También determina los permisos (Crear, Leer, Escribir, Eliminar, Anexar, Anexar a, Asignar o Compartir) que el usuario tiene sobre dichos registros de entidad.

La entidad Unidad organizativa representa un grupo o una división de una compañía que tiene distintos índices de costes para los empleados que tiene asignados. La asociación de un recurso a una unidad organizativa determina el coste del recurso para la involucración del proyecto.

Al implementar Dynamics 365, optimice la autorización de seguridad de la jerarquía de unidades de negocio y la asignación de usuarios a las unidades de negocio. Asigne a la misma unidad negocio todos los usuarios que deben tener acceso al mismo conjunto de registros. La unidad organizativa no tiene ningún efecto en el acceso o la autorización de seguridad.

**Ejemplo que muestra una diferencia potencial en el modelado de unidades organizativas y unidades de negocio**

Contoso, Ltd. cuenta con una próspera área de prácticas de tecnología de Microsoft. Antonio y Elena son desarrolladores de C\#; sin embargo, Elena se encuentra en Estados Unidos, mientras que Antonio está en India. La mayoría de las involucraciones de proyectos requieren recursos de Contoso India y de Contoso Estados Unidos, y Prakash y Tricia necesitan el mismo nivel de acceso de seguridad a los proyectos de esta área de prácticas. Sin embargo, hay una diferencia importante entre el coste de los desarrolladores de Contoso India y el coste de los desarrolladores de Contoso Estados Unidos.

A continuación se describe una forma óptima de diseñar este escenario con Dynamics 365 y Project Operations.

1. Cree el área de prácticas de tecnología de Microsoft como una unidad de negocio y asocie a Antonio y Elena a dicha unidad. De esta forma, se ayuda a asegurarse de que ambos empleados tienen el mismo nivel de acceso de seguridad a cualquier proyecto de dicha área de prácticas. Ambos podrán comprobar el progreso e informar del tiempo, los gastos, el uso de materiales y las actualizaciones de tareas.
2. Cree dos unidades organizativas para asegurarse de que el coste del proyecto se vea correctamente reflejado.
3. Asocie a Tricia con Contoso US y a Prakash con Contoso India.
4. Asigne listas de precios de coste adecuadas a ambas unidades organizativas. De esta forma, ayuda a asegurarse de que los costes que se graban en el proyecto de Prakash y Tricia reflejen de manera precisa la diferencia de costes entre Contoso US y Contoso India.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>¿Están relacionadas las unidades organizativas con las zonas de ventas en Dynamics 365?

No hay ninguna asociación ni relación entre las zonas de ventas y las unidades organizativas. Una zona de ventas suele ser un área geográfica en la que se producen las ventas. Una lista de precios de ventas se puede asociar a cada zona de ventas.

Una unidad organizativa es una división o agrupación interna de la compañía que realiza un seguimiento de los costes de un conjunto de roles que realiza ventas a otras divisiones o clientes externos.

**Ejemplo que muestra una diferencia potencial en el modelado de unidades organizativas y territorios de ventas**

Contoso, Ltd. tiene dos centros de desarrollo: Contoso Estados Unidos y Contoso India. El coste de los recursos difiere grandemente entre estos dos centros de desarrollo. Contoso vende sus servicios de tecnología de la información (TI) en muchos mercados internacionales, como, por ejemplo, América Latina, Norteamérica, Asia Pacífico, Europa y Oriente Medio. Los índices de facturación de los mismos roles de proyecto pueden variar enormemente en estos mercados. Contoso Estados Unidos y Contoso India deben configurarse como unidades organizativas, y cada unidad organizativa debe tener su propia lista de precios de coste. Asia Pacífico, América Latina, Norteamérica, Europa Occidental y Oriente Medio deben configurarse como zonas de ventas y cada zona de ventas debe tener su propia lista de precios de ventas.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>¿Por qué hay restricciones en la asociación de listas de precios a las unidades organizativas?

Los precios de ventas suelen ser únicos para las áreas geográficas o los mercados en los que se venden los servicios. Las divisiones internas de una compañía no suelen tener precios de ventas propios para el mismo tipo de servicios. Sin embargo, las divisiones internas tienen distintos costes de bienes vendidos (COGS) en función de los conocimientos de las personas que emplean y las condiciones de trabajo de la región en las que operan. Puesto que las unidades organizativas se modelan como divisiones internas de una compañía, solo pueden tener listas de precios de coste.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>¿Por qué no es posible asociar las listas de precios de ventas con unidades organizativas?

En Project Operations, las listas de precios de ventas se pueden asociar a clientes y zonas de ventas. Las entidades transaccionales, como, por ejemplo, Oportunidad, Oferta, Contrato de proyecto y Proyecto, utilizan las listas de precios de ventas que unidas a la cuenta de un cliente o zona de ventas para determinar los índices de facturación y los posibles ingresos de la involucración en el proyecto.

Las listas de precios de coste se asocian a las unidades organizativas. Las entidades transaccionales, como Oportunidad, Oferta, Contrato de proyecto y Proyecto, utilizan las listas de precios de coste que están unidas a la unidad de contratación para determinar los costes de una involucración en el proyecto.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>¿Son jerárquicas las unidades organizativas en Project Operations?

No. En la versión actual de Project Operations, las unidades organizativas no son jerárquicas. Por tanto, puede realizar las siguientes tareas:

- Configurar un patrón para introducir precios de coste predeterminados que trascienden a la jerarquía.
- Informar de ingresos o costes que están acumulados en diferentes niveles de la jerarquía de la unidad organizativa.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Somos una gran empresa multinacional que tiene una jerarquía compleja, de varios niveles de centros de costes, divisiones y oficinas de facturación. ¿Cómo podemos optimizar el uso del concepto de unidades organizativas en la versión actual de Project Operations?

Cuando se tiene una jerarquía compleja de centros de costes, divisiones, oficinas de facturación, etc., configure los nodos hoja de la jerarquía como unidades organizativas distintas.

El ejemplo siguiente muestra una jerarquía típica.

**Contoso India**

- Práctica de SAP

    - Consultores técnicos
    - Consultores técnicos

- Práctica de tecnología de Microsoft

    - Consultores técnicos
    - Consultores funcionales

**Contoso US**

- Práctica de SAP

    - Consultores técnicos
    - Consultores funcionales

- Práctica de tecnología de Microsoft

    - Consultores técnicos
    - Consultores técnicos

Si su jerarquía se parece a este ejemplo, debe configurarla como lista plana, tal y como se muestra aquí:

- Contoso India - Práctica de SAP - Consultores técnicos
- Contoso India - Práctica de SAP - Consultores funcionales
- Contoso India - Práctica de tecnología de Microsoft -Consultores funcionales
- Contoso India - Práctica de tecnología de Microsoft -Consultores funcionales
- Contoso Estados Unidos - Práctica de SAP - Consultores técnicos
- Contoso Estados Unidos - Práctica de SAP - Consultores funcionales
- Contoso Estados Unidos - Práctica de tecnología de Microsoft - Consultores técnicos
- Contoso Estados Unidos - Práctica de tecnología de Microsoft - Consultores funcionales

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Somos una pequeña compañía de servicios profesionales que opera como una única división. ¿Cómo podemos optimizar el uso del concepto de unidades organizativas en la versión actual de Project Operations?

Si su compañía opera como una única unidad con una lista de precios de coste, no tiene que configurar ninguna unidad organizativa. La instalación de Project Operations crea una unidad organizativa predeterminada con el mismo nombre que el de la organización. De manera predeterminada, todos los usuarios se asignan a esta unidad organizativa. Siempre que el sistema requiere que se seleccione una unidad organizativa, esta unidad organizativa es la que se selecciona de forma predeterminada.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Cuando se crea un proyecto a partir de una línea de contrato de proyecto u oferta, la unidad de contratación predeterminada procede del contrato del proyecto o la oferta. ¿Cuál es la unidad de contratación predeterminada si se crea un proyecto antes de las entidades de ventas, como, Oferta o Contrato de proyecto?

Cuando se crea un proyecto por su cuenta, la unidad de contratación predeterminada del proyecto se basa en el usuario que lo crea. Dicho usuario es también el jefe de proyecto predeterminado. Si el proyecto se asigna a una entidad de ventas, como, por ejemplo, una oferta o un contrato de proyecto, la unidad de contratación del proyecto se basa en su lugar en la entidad de ventas. En este caso, es posible que se vuelvan a calcular las estimaciones de proyecto, ya que la lista de precios de coste se usa para calcular los cambios de estimación de costes si se cambia la unidad de contratación. La lista de precios de ventas se usa para calcular las estimaciones de ventas que se cambiarán para mantenerlas sincronizadas con la lista de precios del proyecto de la oferta.

Los campos **Unidad de contratación** y **Divisa** del proyecto están bloqueados y no se pueden editar porque deben estar sincronizados con los valores de la entidad de ventas (contrato de proyecto u oferta) a la que está asignado el proyecto.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Crear y mantener unidades organizativas en Project Operations

Para crear una unidad organizativa en Project Operations, siga estos pasos.

1. Vaya a **Configuración \> Unidades organizativas**.
2. Seleccione **Nuevo**.
3. En el área **General**, en el campo **Nombre**, escriba un nombre para la unidad organizativa. Luego configure los otros campos según sea necesario.
4. Seleccione **Guardar** para crear el registro, de forma que pueda seguir editándolo.
5. En **Listas de precio de coste**, seleccione el signo más (**+**) para agregar una lista de precios. Solo puede agregar listas de precios que tengan aquí el contexto **Coste**.
6. En el campo **Nombre**, seleccione el botón **Buscar** y seleccione una lista de precios que desee poner a disposición de la unidad organizativa. Siga agregando listas de precios según se requiera.
7. Cuando haya terminado de agregar listas de precios, seleccione **Guardar** en la esquina inferior derecha de la página.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
