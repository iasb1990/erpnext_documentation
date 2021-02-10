<!-- add-breadcrumbs -->
# Nota de Envío

**Una Nota de Envío se realiza cuando se envía un cargamento desde el Depósito de la Empresa hacia el cliente.**

Normalmente, se envía una copia de la Nota de Envio con el transportista. La Nota de 
Envío contiene la lista de Productos que se envían en el cargamento y actualiza el inventario.
La Nota de Envío es un paso opcional y puede crearse una Factura de Venta directamente desde una Orden de Venta. 

Para acceder al listado de Nota de Envío ir a:
> Inicio > Existencias > Transacciones de Existencias > Nota de Envío

![Delivery Note flow](/docs/assets/img/stock/delivery-note-flow.png)


## 1. Prerrequisitos
Antes de crear y utilizar una Nota de Envío, se recomienda crear lo siguiente:

* [Orden de Venta](/docs/user/manual/en/selling/sales-order)

> Observación: Desde la versión 13 en adelante se introdujeron libros contables inalterables lo cual cambia las reglas de cancelación de entradas de existencias y de registro de transacciones de existencias de fechas anteriores en ERPNext. [Leer más aquí](/docs/user/manual/en/accounts/articles/immutable-ledger-in-erpnext).

## 2. Cómo Crear una Nota de Envío
La creación de Nota de Envío es muy similar al Recibo de Compra. Generalmente se crea desde una Orden de Venta "Enviada" (que todavía no fue enviada al cliente) al hacer click en Crear > Envio.

Para crear una Nota de Envío de forma _manual_ (no recomendado), seguir los siguientes pasos:

1. Ir al listado de Nota de Envío y hacer click en Nuevo.
1. Los detalles del Producto y del cliente pueden ser tomados desde la Orden de Venta haciendo click en "Obtener Productos Desde > Orden de Venta".
1. La UdM y los Precios serán tomados automáticamente.
1. Guardar y Enviar.

    <img class="screenshot" alt="Delivery Note" src="{{docs_base_url}}/assets/img/stock/delivery-note.png">

Para tomar los Productos desde una Orden de Venta, hacer click en Obtener Productos Desde > Orden de Venta. Esto abrirá una ventana emergente donde se pueden buscar Ordenes de Venta y seleccionar una.

Si la Nota de Envío es creada desde la Orden de Venta, se tomará desde allí toda la información respecto a Productos no enviados y otros detalles. 

También se puede editar la fecha y hora de publicación de la Nota de Envío, de forma predeterminada, las mismas se establecerán en el día y la hora en que se crea la Nota de Envío. 


### 2.1 Estados

Estos son los Estados en que puede encontrarse una Orden de Envío:

* **Borrador**: Se guarda un borrador pero todavía no se envía al sistema.
* **Pendiente de Facturación**: Pendiente de facturación a través de una [Factura de Venta](/docs/user/manual/en/accounts/sales-invoice).
* **Completa**: Enviada y con todos los Productos enviados. 
* **Cancelada**: Nota de Envío cancelada.
* **Cerrada**: El fin del Estado Cerrado es administrar el cierre definitivo de la Nota de Envío. Por ejemplo, el Cliente pidió 20 unidades de producto pero se cierra en 15. Por ende las otras 5 unidades no serán enviadas ni facturadas. 

### 2.2 Envios Parciales

Cuando se crea una Nota de Envío desde una Orden de Venta, las cantidades pueden cambiarse. De forma que, si la Orden de Venta contiene 10 Productos a ser enviados, y solo se envía 5 esta semana y los restantes la semana que viene, entonces se puedan crear dos Notas de Envío en dos semanas. 


## 3. Acciones Relacionadas
### 3.1 Detalles de la Orden de Compra del Cliente
Aquí se puede ingresar el número de Orden de Compra del Cliente a fin de tenerla como referencia. 

### 3.2 Dirección y Contacto
* **Dirección de Envio**: La dirección del Cliente a donde serán enviados los Productos. 
* **Persona de Contacto**: Si el cliente es una organización, agregar la Persona de Contacto en este campo. 


[Contactos](/docs/user/manual/en/CRM/contact) y [Direcciones](/docs/user/manual/en/CRM/address) se almacenan por separado para que se puedan adjuntar muchos Contactos o Direcciones al cliente.

### 3.3 Moneda y Listado de Precios
En esta sección se puede configurar la moneda en la cual se enviará la Nota de Envío. Esto generalmente se obtiene, si fue configurado, de la Orden de Venta. Si se configura un Listado de Precios, los precios de los productos serán tomados de allí. Si se selecciona "Ignorar pautas de tarifas", las Pautas de tarifas establecidas en Cuentas > Pautas de tarifas, serán ignoradas.

Para saber más sobre Listado de Precios, [click aquí](/docs/user/manual/en/stock/price-lists).

Para saber respecto a administrar transacciones en distintas monedas, [click aquí](/docs/user/manual/en/accounts/articles/managing-transactions-in-multiple-currency).

### 3.4 Depósitos

* **Configurar Depósito de Origen**: Desde aquí provendrán los Productos a ser enviados al Cliente. 
* **Depósito Destino**: En un escenario de ventas típico, el Producto existe en el Depósito y llega al Cliente. Sin embargo, si se desea retener existencias de muestra, se debe ingresar un Depósito en este campo. 

### 3.5 Tabla de Productos
* **Código de Barra**: Se puede rastrear Productos utilizando [Códigos de Barra](/docs/user/manual/en/stock/articles/track-items-using-barcode).

* El Código de Producto, el nombre, descripción, Imagen y Fabricante serán obtenidos desde la [función Producto](/docs/user/manual/en/stock/item).

* **Escanear Código de Barra**: Se pueden añadir Productos a la tabla de Productos al escanear sus códigos de barra si se cuenta con un lector de código de barra. Para aprender a rastrearlos click [aquí](/docs/user/manual/en/stock/articles/track-items-using-barcode)

* **Descuento y Margen**: Se pueden aplicar descuentos sobre productos individuales en forma de porcentaje  o el monto total del Producto. Leer [Applicar Descuento](/docs/user/manual/en/selling/articles/applying-discount) para más detalles.

* **Precio**: El Precio será tomado desde el [Listado de Precios](/docs/user/manual/en/stock/price-lists), si se hubiere configurado ahí, y se calculará el Monto total.
* 
* **Plantilla de Impuesto de Producto**: Se puede configurar una Plantilla de Impuesto de Producto para aplicar un Impuesto específico a este Producto en particular. Para saber más, visitar [esta página](/docs/user/manual/en/accounts/item-tax-template).

* Si hubiesen sido configurados allí, los Detalles de Peso del Producto por unidad y Peso en UdM serán tomados de la función Producto.

* **Depósito y Referencia**: Se muestra el Depósito desde el cual se envían los Productos al Cliente. A su vez, si la Nota de Envío se creó de la siguiente forma "Orden de Venta > Nota de Envío", también se mostrará la Orden de Venta. 

* **Número de Serie y Número de Lote**: Si el Producto es seriado o está en lotes, se deberá introducir el [Número de Serie](/docs/user/manual/en/stock/serial-no) y [Número de Lote](/docs/user/manual/en/stock/batch) en la tabla de Productos. Se pueden ingresar múltiples Números de Serie en un sola fila (cada uno en una línea distinta) y se deberá ingresar tantas veces el Número de Serie como la cantidad de producto a comprar/vender. 

    Se mostrarán la "Cantidad Disponible en el Depósito de Origen", la "Cantidad de Lote Disponible en el Depósito de Origen" y la "Cantidad Instalada". Para saber más respecto a instalación, visitar la página [Nota de Instalación](/docs/user/manual/en/stock/installation-note).

    **Observación**: El Producto debe estar seriado o en lote para que estas características funcionen. Si el Producto esta seriado, aparecerá una ventana emergente donde se pueden ingresar los Números de Serie. 

* La Cuenta de Gastos es la cuenta desde la cuál se debitará el monto. Si se selecciona "Permitir Valoración 0", se permitirá enviar la Nota de Envío inclusive si la Valoración del Producto es 0. Esto puede ser porque se trate de una muestra de un producto o por un acuerdo con el Proveedor.  

* Las Dimensiones Contables ayudan a identificar cada transaccion con diferentes Dimensiones sin la necesidad de crear nuevos Centros de Costos. Para esto, primero se deben crear las Dimensiones Contables, para saber más, visitar [esta página](/docs/user/manual/en/accounts/accounting-dimensions).

* **Salto de Página** creará un salto de página justo antes de este producto al imprimir.

### 3.6 Registrar Inspecciones de Calidad
Si para algunos Productos es obligatorio registrar Operaciones de Calidad (si esto fue establecido en la función Producto), se deberá actualizar el campo "Inspección de Calidad". El sistema solo permitirá enviar el Recibo de Compra si se actualiza 
la "Inspección de Calidad".

Luego de habilitar los Criterios de Inspección para Ventas en el [Formulario de Productos](/docs/user/manual/en/stock/item#216-inspection-criteria) y de adjuntar allí una Plantilla de Inspección de Calidad, las Inspecciones de Calidad pueden ser registradas en Notas de Envío. 

### 3.7 Impuestos y Gastos
Los Impuestos y Gastos serán tomados desde la [Orden de Venta](/docs/user/manual/en/buying/purchase-order).

Visitar la página de [Plantilla de Impuestos y Gastos de Compra](/docs/user/manual/en/selling/sales-taxes-and-charges-template) para saber más de impuestos.

El total de gastos e impuestos será mostrado debajo de la tabla. 

Para añadir impuestos de forma automática a través de una Categoría Impositiva, visitar [esta página](/docs/user/manual/en/accounts/tax-category).

Asegurarse de anotar correctamente todos los impuestos en la tabla de Impuestos y Gastos para una valoración precisa.

#### Pauta de Envío
Una Pauta de Envío ayuda a determinar el costo de enviar un producto. El costo tenderá a aumentar a medida que la distancia de envío sea mayor. Para saber más, vistar la sección [Pauta de Envío](/docs/user/manual/en/selling/shipping-rule) page.

### 3.8 Descuentos Adicionales
En esta sección puede configurarse cualquier descuento adicional a aplicar a toda la orden. Este descuento puede basarse en el Importe Total, es decir, luego de impuestos y gastos, o en el Total Neto, es decir, antes de impuestos y gastos. El descuento adicional puede ser aplicado como porcentaje o monto. 
Leer [Aplicar Descuento](/docs/user/manual/en/selling/articles/applying-discount) para más detalles.

### 3.9 Bases y Condiciones
En operaciones de Compra/Venta puede haber ciertas bases y condiciones que rigen la forma en que el proveedor vende bienes o servicios al cliente. Se pueden aplicar las Bases y Condiciones a las transacciones y éstas aparecerán en el documento impreso. Para saber más respecto a Bases y Condiciones, [click aquí](/docs/user/manual/en/setting-up/print/terms-and-conditions)

### 3.10 Información de Transportista

Si se terceriza el transporte de los Bienes hacia su lugar de envío, los detalles del transportista pueden ser agregados. Esto no es lo mismo que [envío directo](/docs/user/manual/en/selling/articles/drop-shipping).

* **Transportista**: El Proveedor que va a llevar el Producto al Cliente. La función Transportista debería estar habilitada en la función Proveedor para poder seleccionar el [Proveedor](/docs/user/manual/en/buying/supplier) aquí.
* **Conductor**: Se puede añadir aquí el conductor que manejará el medio de transporte. 

![Delivery Note Transport](/docs/assets/img/stock/delivery-note-transport.png)

Pueden registrarse los siguientes detalles:

* Distancia en kilómetros
* Método de transporte, es decir, ruta, aire, tren o barco. 


### 3.11 Más Información

La Nota de Envío puede relacionarse a lo siguiente a fines de contar con información más completa: 

* [Proyecto](/docs/user/manual/en/projects/project)
* [Campaña](/docs/user/manual/en/CRM/campaign)
* [Cliente Potencial](/docs/user/manual/en/CRM/lead_source)

### 3.11 Configuración de Impresión

#### Papel membretado
Se pueden imprimir las Notas de Envío en papel con el membrete de la empresa. Saber más [aquí](/docs/user/manual/en/setting-up/print/letter-head).

"Agrupar productos iguales", agrupará los productos iguales que se hayan sumado muchas veces a la tabla de Producto. Esto puede verse al imprimir. 

#### Encabezados de Impresión
Los encabezados de las Notas de Envío pueden ser modificados al imprimir el documento. Se puede hacer esto seleccionando **Encabezado de Impresión**. Para crear nuevos Encabezados de Impresión ir a: Inicio > Configuraciones > Impresión > Encabezados de Impresión. Leer máse [aquí](/docs/user/manual/en/setting-up/print/print-headings).

Hay opciones adicionales para poder imprimir la Nota de Envío sin el monto, esto puede ser útil cuando el Producto tiene un valor muy alto. También, al imprimir, se pueden agrupar los Productos iguales en una fila. 

### 3.12 Estado
Aquí se muestran el estado del documento y el porcentaje de instalación. Cualquier instrucción adicional para el envío puede ser ingresada en este campo. 

### 3.13 Comisión

Si la venta fue realizada a través de algún Socio Comercial, aquí se pueden añadir aquí los detalles de su comisión. Esto generalmente se toma desde la Orden de Venta.

### 3.14 Equipo de Ventas
**Vendedores:** ERPNext permite añadir a todos los vendedores que hayan trabajado en esta venta.

Esto generalmente se toma desde la Orden de Venta, por ejemplo: 

<img class="screenshot" alt="Sales Team in Sales Order" src="{{docs_base_url}}/assets/img/selling/so-sales-team.png">

### 3.15 Enviar Paquetes o Productos con Paquete de Productos

Si se está enviando Productos que son parte de un [Paquete de Productos](/docs/user/manual/en/selling/product-bundle), ERPNext creará automáticamente una tabla de Lista de Empaque basada en los sub productos de ese Producto. 

Si los Productos son seriados, entonces para el tipo de Productos del Paquete de Productos hay que 
actualizar el Número de Serie en la tabla de "Lista de Empaque". 

### 3.16 Packing Items into Cases, for Container Shipment

Si se está realizando el envío a través de distintas cajas o por peso, se puede utilizar una Nota 
de Embalaje para dividir la Nota de Envío en unidades más pequeñas. Para saber más respecto Nota de Embalaje visitar [esta página](/docs/user/manual/en/stock/packing-slip).


Se pueden crear muchas Notas de Embalaje desde una Nota de Envío y ERPNext se
asegurará que las cantidades en la Nota de Embalaje no excedan las cantidades
en la Nota de Envío. Tener en cuenta que se puede crear una Nota de Embalaje desde una Nota de Envío solo cuando la Nota de Envío está en etapa de Borrador. 

### 3.17 Luego de Enviar

Cuando la Nota de Envio es enviada, se creará un registro en el Inventario de Existencias para cada Producto y se actualizará el inventario. 
La Cantidad Pendiente en la Orden de Venta es actualizada (si se aplica).

El Tablero mostrará las siguientes opciones: 

* [Nota de Instalación](/docs/user/manual/en/stock/installation-note)
* [Devolución de Venta](/docs/user/manual/en/stock/sales-return)
* [Viaje de Envío](/docs/user/manual/en/stock/delivery-trip)
* [Facturas de Venta](/docs/user/manual/en/accounts/sales-invoice)

![Delivery Note after submit](/docs/assets/img/stock/delivery-note-submit.png)

> Consejo: Para deshabilitar la creación de Notas de Envío sin Órdenes de Venta: 

### 3.18 Devolución de Orden de Venta
Una vez enviada la Orden de Venta utilizando una Nota de Envío, se puede crear una devolución en caso de que el [Cliente](/docs/user/manual/en/CRM/customer) devuelva el Producto. Para saber más visitar la página [Devoluciones de Venta](/docs/user/manual/en/stock/sales-return).

### 3.19 Saltear Nota de Envío

Si no se quiere crear una Nota de Envío luego de realizada una Orden de Venta, y se desea pasar directamente a una Factura de Venta, habilitar esta opción en [Configuraciones de Venta](/docs/user/manual/en/selling/selling-settings#32-delivery-note-required).


### 4. Temas Relacionados
1. [Depósito](/docs/user/manual/en/stock/warehouse)
1. [Error de Existencias en Nota de Envío](/docs/user/manual/en/stock/articles/delivery-note-stock-error)
1. [Transferencia de Material Desde Nota de Envío y Recibo de Compra](/docs/user/manual/en/stock/articles/material-transfer-from-delivery-note)
1. [Nota de Instalación](/docs/user/manual/en/stock/installation-note)
1. [Viaje de Envío](/docs/user/manual/en/stock/delivery-trip)