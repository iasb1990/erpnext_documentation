<!-- add-breadcrumbs -->
# Envío Triangulado

El **Envío Directo** es una técnica de administración de la cadena de suministro en la cual el vendedor no mantiene existencias de los productos. En cambio, transfiere los pedidos de los clientes y los detalles de envío al fabricante, a otro vendedor o a un mayorista, quien se encarga de enviar directamente los bienes al cliente. 

En ERPNext, se puede administrar el Envío Directo creando una Orden de Compra desde la Orden de Venta. 

> Comercialización > Documentos > Orden de Venta > Orden de Compra

#### Configurar en la Función Producto

Configurar **_Envío a Cargo del Proveedor (Envío Directo)_** y **_Proveedor Predeterminado_** en la Sección Producto.

<img class="screenshot" alt="Setup Item Master" src="{{docs_base_url}}/assets/img/selling/setup-drop-ship-on-item-master.png">

#### Configurar en Orden de Venta
Si el Envío Directo fue configurado en la sección del Producto, entonces en la Orden de Venta de ese producto, se establecerá automáticamente la configuración **Proveedor Envía al Cliente** y el **Proveedor** encargado de tal envío. 

Se puede configurar el Envío Directo para el Producto desde la Orden de Venta. Ir a la sección **Envío Directo**, configurar **Proveedor Envía al Cliente** y seleccional el **Proveedor** al cual se le enviará la Orden de Compra. 

<img class="screenshot" alt="Setup Drop Shipping on Sales Order Item" src="{{docs_base_url}}/assets/img/selling/setup-drop-ship-on-sales-order-item.png">

#### Crear Orden de Compra
Luego de enviar la Orden de Venta, crear la Orden de Compra. 

<img class="screenshot" alt="Setup Drop Shipping on Sales Order Item" src="{{docs_base_url}}/assets/img/selling/drop-ship-sales-order.png">

Desde Orden de Venta, todos los Productos que tengan seleccionada la casilla **Proveedor Envía al Cliente**  o **Proveedor** (coincidente con el proveedor seleccionado en la ventana emergente Para Proveedor) mencionado, serán llevados a la Orden de Compra.

Automáticamente se configurará el Cliente, su Dirección y la persona de Contacto. 

Luego de enviar la Orden de Venta, para actualizar el estado de envío, utiizar el botón **Marcar como Entregado** en la Orden de Compra. De esa forma se actualizará el porcentaje de envío y la cantidad enviada en la Orden de Venta. 

<img class="screenshot" alt="Purchase Order for Drop Shipping" src="{{docs_base_url}}/assets/img/selling/drop-ship-purchase-order.png">

<span style="color:#18B52D">**_Cerrar_**</span>, es una nueva función introducida en **Orden de Compra** y **Orden de Venta**, a fin de cerrar o marcar el cumplimiento.

<img class="screenshot" alt="Close Sales Order" src="{{docs_base_url}}/assets/img/selling/close-sales-order.png">

### Envío Directo en Formato de Impresión
Se puede notificar a los Proveedores enviándoles un mail luego de enviar la Orden de Compra adjuntando el Envío Directo en formato de impresión. 

<img class="screenshot" alt="Drop Dhip Print Format" src="{{docs_base_url}}/assets/img/selling/drop-ship-print-format.png">


{next}    
