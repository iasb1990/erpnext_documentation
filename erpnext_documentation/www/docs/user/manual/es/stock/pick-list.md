# Lista de Selección de Productos

**Una Lista de Selección de Productos es un documento que indica qué productos deben ser quitados del inventario para completar órdenes.**

Ésto resulta especialmente útil para empresas con grandes cantidades de inventario, volúmenes de orden o clientes comprando muchas unidad de mantenimiento de existencias (SKU).
La Lista de Selección de Productos selecciona el Depósito donde un Producto está disponible en términos FIFO (Primero que ingresa, primero que sale)
La Selección del Depósito para un producto en lote es diferente. En el caso de productos en lote, se selecciona el Depósito en el cual el lote está más cerca de la fecha de vencimiento. 

Para acceder al listado de Lista de Selección de Productos ir a:

> Inicio > Inventario > Transacciones de Inventario > Lista de Selección de Productos

## 1. Prerrequisitos

Antes de crear y utilizar una Lista de Selección de Productos, se recomienda crear lo siguiente: 

- [Producto](/docs/user/manual/en/stock/item)
- [Depósito](/docs/user/manual/en/stock/warehouse)

## 2. Cómo Crear un Lista de Selección de Productos

1. Ir al listado de Lista de Selección de Productos y hacer click en Nuevo.
 <img class='screenshot' alt='Unsaved Pick List' src='{{docs_base_url}}/assets/img/stock/pick-list-unsaved-doc.png'>

1. Configurar la Empresa
1. Seleccionar el Objetivo de la Lista de Selección de Productos. Nos encontraremos con estas opciones en el campo Objetivo:  

   - **Envío:** Esta opción permitirá añadir Productos desde una Orden de Venta para enviar. Luego de enviar la Lista de Selección de Productos, puede crearse una nueva Nota de Envío desde el Depósito del cual se seleccionaron los productos. 

   - **Transferencia de Material para su Fabricación:** Esto permitirá seleccionar una Orden de Trabajo desde la cual se presentarán las materias primas para elegir. Se puede seleccionar el número de productos finales para los cuales se eligen las materias primas. Luego de elegir las cantidades se puede crear un Registro de Inventario para los productos seleccionados, es decir, materias primas.

   - **Transferencia de Material:** Esto permitirá seleccionar un Pedido de Materiales para el cual se desea elegir productos. Luego de realizada la selección, se puede crear un Registro de Inventario para los productos elegidos. 

1. Añadir el Producto y la cantidad que se quiere seleccionar en la tabla de Ubicación de Productos. Hacer click en **Obtener Ubicaciones de Productos** para obtener el Depósito y otros detalles para cada Producto. 

1. **Depósito Principal:** Si se selecciona un Depósito principal, solo los Depósitos que se encuentran dentro del mismo serán sugeridos. 

1. **Obtener Ubicación de Productos:** Una vez que se eligieron los productos, se puede hacer click en el botón **Obtener Ubicación de Productos** para poder seleccionar el Depósito para cada producto. Como el Depósito será obtenido de forma automática si se elige un Producto desde cualquier documento de referencia, este botón puede resultar útil para añadir manualmente Productos adicionales o cambiar la cantidad de productos Existentes en la tabla de Ubicación de Productos.  

1. **Ubicación de Productos:** Este campo tendrá toda la información respecto a la ubicación del producto (Depósito), Número de Serie para productos seriados y número de lote para productos en lote. 
 <img class='screenshot' alt='Item Locations' src='{{docs_base_url}}/assets/img/stock/pick-list-item-locations.png'>

 Si los productos poseen Números de Serie, la fila de Productos se verá de la siguiente forma:
 <img class='screenshot' alt='Item Location Detail' src='{{docs_base_url}}/assets/img/stock/pick-list-item-location-detail.png'>

1. Guardar y Enviar.
 <img class='screenshot' alt='Submitted Pick List' src='{{docs_base_url}}/assets/img/stock/pick-list-submitted-doc.png'>

### 2.1 Crear Lista de Selección de Productos desde Orden de Venta

1. Ir a una [Orden de Venta](/docs/user/manual/en/selling/sales-order).
1. Hacer click en el botón **Crear** en la parte superior derecha del formulario y luego hacer click en la opción **Lista de Selección de Productos**.
1. Una vez que se elige Lista de Selección de Productos, toda la información requerida para la Lista de Selección de Productos será obtenida desde la Orden de Venta. 
1. Se debería poder ver la Tabla de Ubicación de Productos con los Depósitos seleccionados para cada Producto. 
1. Guardar este documento, el cual podrá ser utilizado para seleccionar existencias por la persona que realiza esta actividad. 
1. Enviar el documento una vez que se finalizó la selección de productos y que las cantidades seleccionadas de producto fueron actualizadas en el documento. 

**Consejo:** Se puede crear una Lista de Selección de Productos para muchas Órdenes de Venta del mismo Cliente. Hacer click en Obtener Productos y seleccionar la Orden de Venta. 

> **Observación:**
>
> - La Lista de Selección de Productos solo puede ser creada para Órdenes de Venta que tienen Productos pendientes de envío.
> - Una **Nota de Envío** puede ser creada solo si la Lista de Selección de Productos es enviada.

### 2.2 Crear Lista de Selección de Productos desde Orden de Trabajo

1. Ir a una [Orden de Trabajo](/docs/user/manual/en/manufacturing/work-order).
1. Hacer click en el botón **Crear Lista de Selección de Productos**.
1. Se verá el cuadro de diálogo pidiendo la cantidad de Productos Finales. Este es un campo requerido para calcular la cantidad de materias primas necesarias para fabricar la cantidad ingresada de Productos Finales. 
<img class='screenshot' alt='Dialog For qty' src='{{docs_base_url}}/assets/img/stock/pick-list-dialog-for-qty.png'>

1. Se debería poder ver la tabla de Ubicación de Productos con el Depósito seleccionado para cada materia prima. 
1. Guadar este documento el cual luego podrá ser remitido a la persona que seleccionará los productos. 
1. Enviar el documento una vez que se terminó de seleccionar los productos y el producto seleccionado se haya actualizado correctamente en el documento. 

> **Observaciones:**
>
> - La Lista de Selección de Productos solo puede ser creada para Órdenes de Trabajo que se encuentran en el estado de "No Iniciadas" o "En Curso".
> - Un **Registro de Inventario** puede crearse solo luego de que la Lista de Selección de Productos fue enviada. 

### 2.3 Crear Lista de Selección de Productos desde Pedido de Material

1. Ir a [Pedido de Material](/docs/user/manual/en/stock/material-request).
1. Hacer click en el botón **Crear** y luego click en la opción **Lista de Selección de Productos**.
1. Se debería poder ver la tabla de Ubicación de Productos con el Depósito seleccionado para cada producto en el Pedido de Material.
1. Guadar este documento el cual luego podrá ser remitido a la persona que seleccionará los productos. 
1. Enviar el documento una vez que se terminó de seleccionar los productos y el producto seleccionado se haya actualizado correctamente en el documento.

> **Observaciones:**
>
> - Solo los Pedidos de Material de tipo "Transferencia de Material" pueden ser utilizados para crear Listas de Productos. 
> - Un **Registro de Inventario** de tipo "Transferencia de Material" puede ser creado luego de que la Lista de Selección de Productos haya sido enviada. 

## 3. Características

### 3.1. Actualizar Inventario Actual

Si una Lista de Selección de Productos está desactualizada, puede haber un cambio en la disponibilidad de existencias para el momento en que se crea una Nota de Envío o Registro de Inventario desde la misma. Hacer click en **Actualizar Inventario Actual**, actualizará las cantidades y depósitos en la tabla de Ubicaciones de Productos.

> **Observaciones:** Este botón es visible siempre y cuando no haya Notas de Envío o Registros de Inventario creados desde esa Lista de Selección de Productos. 

## 4. Temas Relacionados

1. [Orden de Venta](/docs/user/manual/en/selling/sales-order)
1. [Orden de Trabajo](/docs/user/manual/en/manufacturing/work-order)
1. [Pedido de Material](/docs/user/manual/en/stock/material-request)
