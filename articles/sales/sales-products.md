---
title: Productos
description: En este tema se proporciona información sobre el catálogo de productos que puede utilizar para ofrecer información a los clientes sobre los productos y los precios que ofrece su organización.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 30633a7445baaf99af5be5c88e35b24824022b93
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121284"
---
# <a name="products"></a>Productos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Los productos son la espina dorsal de su negocio. El catálogo de productos de Dynamics 365 Sales Professional es una recopilación de productos y la información sobre precios. Haga que resulte más fácil a los representantes de ventas incrementar las ventas mediante la creación rápida de un catálogo de productos.

## <a name="add-a-product"></a>Agregar un producto

1.  Compruebe que tiene el rol de Administrador del sistema o Administrador de Sales Professional para poder agregar productos en Dynamics 365 Sales Professional.
2.  En el mapa del sitio, en **Configuración**, seleccione **Productos**.
3.  Seleccione **Agregar producto** y complete la siguiente información:

    -  **Nombre**
    -  **Id. del producto**
    -  **Principal**: Seleccione una familia de productos principal para el producto. Si está creando un producto secundario en una familia de productos, el nombre de la familia de productos principal se rellena aquí. Esto no se puede cambiar después de guarda el registro.
    -  **Válida desde**/**Válida hasta**: Defina el período para el que es válido el producto seleccionando las fechas **Válida desde** y **Válida hasta**.
    -  **Unidad de venta**: Seleccione una unidad de venta. Una unidad de venta es una colección de diferentes unidades en las que se vende un producto y define cómo los artículos individuales se agrupan en las cantidades de mayor tamaño. Por ejemplo, si agrega semillas como producto, es posible que haya creado una unidad de venta llamada "Semillas" y haya definido su unidad principal como "paquete".
    -  **Unidad predeterminada**: Seleccione la unidad más común en la que el producto se pondrá a la venta. Las unidades son las cantidades o las medidas en las que vende sus productos. Por ejemplo, si está agregando semillas como producto, puede venderlas en paquetes, en cajas o en palets. Cada una de estos se convierte en una unidad del producto. Si las semillas se venden sobre todo en paquetes, selecciónelo como unidad.
    -  **Lista de precios predeterminada**: Si es un producto nuevo, este campo es de solo lectura. Para poder seleccionar una lista de precios predeterminada, debe completar todos los campos requeridos y luego guardar el registro. Aunque no se requiere una lista de precios predeterminada, una vez que se guarda el registro del producto, es una buena idea establecer una lista de precios predeterminada para cada producto. Después, si un registro de cliente no contiene una lista de precios, Sales puede usar la lista de precios predeterminada para generar ofertas, pedidos y facturas.
    -  **Decimales admitidos**: Escriba un número entero comprendido entre 0 y 5. Si el producto no se puede dividir en fracciones, escriba 0. La precisión del campo **Cantidad** en el registro del producto de la oferta, del pedido o de la factura se valida en comparación con el valor en este campo si el producto no tiene una lista de precios asociada.
    -  **Asunto**: Asocie este producto a un asunto. Puede usar asuntos para clasificar los productos y filtrar los informes.

4.  Seleccione **Guardar**.
5.  En la pestaña **Detalles adicionales**, en la sección **Elementos de lista de precios**, seleccione **Más comandos** y después seleccione **Agregar nuevo elemento de lista de precios**.
7.  En la pestaña **Detalles adicionales**, en la sección **Relación de productos**, seleccione el icono **Más comandos** y después seleccione **Agregar nueva relación de producto.**
8.  En el formulario **Nuevo relación de producto**, introduzca los siguientes detalles y, en la barra de comandos, seleccione **Guardar y cerrar**:

    -   **Productos relacionado**: Seleccione un producto que desee agregar como producto relacionado al registro del producto en el que está trabajando.
    -   **Tipo de relación de ventas**: Seleccione si desea agregar al producto como incremento de ventas, venta cruzada, accesorio o producto sustituto.
    -   **Dirección**: Seleccione si la relación entre los productos será unidireccional o bidireccional. Al seleccionar Unidireccional, el producto que seleccione en **Producto relacionado** aparecerá como recomendación para el producto existente, pero no viceversa.

9.  En el formulario de producto, seleccione **Guardar**.

## <a name="import-products"></a>Importar productos

Puede usar plantillas de importación para incluir datos en masa del producto en Dynamics 365 Sales.

## <a name="revise-a-product"></a>Revisar un producto

Mantenga el inventario de productos actualizado revisando rápidamente las propiedades de los productos que necesite, y republicando la información para que los agentes de ventas puedan consultar los últimos cambios en el inventario.

1.  Compruebe que tiene asignado uno de los siguientes roles de seguridad o permisos equivalente: Administrador del sistema, Personalizador del sistema, Jefe de ventas, Vicepresidente de ventas, Vicepresidente de marketing o Director general.
2.  En el mapa del sitio, seleccione **Productos**.
3.  Abra un producto activo que desee cambiar y, en la barra de comandos, seleccione **Revisar**.
4.  En el cuadro de diálogo **Confirmar Revisar**, seleccione **Confirmar**. Esto cambiará el estado del producto a **En revisión**.
5.  Cuando termine de realizar cambios, en la barra de comandos, seleccione **Publicar**.

    > [!TIP]
    > Para revertir los cambios y continuar con la última versión activa del producto, seleccione **Revertir**. Esto cambia el estado del producto de nuevo a **Activo**.

## <a name="clone-a-product"></a>Clonar un producto 

Cuando cree un nuevo producto, ahorre tiempo clonando uno existente. Esto crea una copia del registro original con todos los detalles excepto el nombre y la identificación

1.  Compruebe que tiene asignado uno de los siguientes roles de seguridad o permisos equivalente: Administrador del sistema, Personalizador del sistema, Jefe de ventas, Vicepresidente de ventas, Vicepresidente de marketing o Director general.
2.  En el mapa del sitio, seleccione **Productos**.
3.  Seleccione un registro de producto que desea clonar y, en la barra de comandos, seleccione **Clonar**. Aparece un cuadro de diálogo de confirmación.
4.  Seleccione **Confirmar**.

Un nuevo registro del producto se abre con los mismos detalles que el original excepto el nombre y la identificación

## <a name="retire-a-product"></a>Retirar un producto 

Si la organización ya no vende un producto, retírelo de modo que el producto ya no está disponible para los agentes de ventas.

1.  Compruebe que tiene el rol de Administrador del sistema o Administrador de Sales Professional o permisos equivalentes.
2.  En el mapa del sitio, seleccione **Productos**.
3.  Abra un producto activo que desee retirar y, en la barra de comandos, seleccione **Retirar**.
4.  En el cuadro de diálogo **Confirmar Retirar**, seleccione **Confirmar**.


## <a name="delete-a-product"></a>Eliminar un producto

Para detener la venta de un producto, elimínelo.

> [!IMPORTANT]
> No puede recuperar los registros eliminados.

1.  Compruebe que tiene el rol de Administrador del sistema o Administrador de Sales Professional o permisos equivalentes.
2.  En el mapa del sitio, seleccione **Productos**.
3.  Seleccione un registro de producto que desea eliminar y, en la barra de comandos, seleccione **Eliminar**.
4.  En el cuadro de diálogo **Confirmar eliminación**, seleccione **Continuar**.
 
 ## <a name="quantity-factors-for-products"></a>Factores de cantidad para productos

Los factores de cantidad respaldan la venta de productos basados ​​en suscripción. Para productos basados ​​en suscripción, la cantidad en la línea de oferta o contrato del proyecto se expresa como el número de meses de usuario.

Por lo general, el precio del software de suscripción se almacena en el catálogo como el precio por usuario por mes. Sin embargo, puede utilizar otras descripciones de tiempo en su lugar. Durante el proceso de venta, el precio en la línea de oferta suele ser el precio por usuario, por mes que negoció y descontó el agente de ventas de TI. Cada operación tiene un número diferente de usuarios y un número diferente de meses de suscripción. La cantidad que se utiliza para calcular la cantidad de la línea de oferta es un producto de la cantidad de usuarios y la cantidad de meses de suscripción.

Los factores de cantidad dependen de los atributos del producto. Cuando configura propiedades específicas para un producto, puede marcar un subconjunto de esas propiedades, o todas las propiedades, como factores de cantidad.

El sistema valida que solo las propiedades numéricas o las propiedades del producto que tienen un tipo de datos numéricos se marcan como factores de cantidad. Cuando un producto para el que se configuran los factores de cantidad se agrega a una línea de oferta, el campo **Cantidad** en la línea de oferta se convierte en un campo de solo lectura. Después de introducir valores para las propiedades del producto que son factores de cantidad, se calcula la cantidad de la línea de oferta.

Por ejemplo, si existen las siguientes propiedades: 

- **Número de usuarios**: el número de usuarios 
- **Número de meses**: el número de meses de suscripción
- **SKU de producto** 

Las propiedades **Número de usuarios** y **Número de meses** se pueden marcar como factores de cantidad editando las propiedades de la línea de productos. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]