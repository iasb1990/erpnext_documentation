<!-- add-breadcrumbs -->
# Orden de Compra

**Una Orden de Compra es un contrato vinculante con el Proveedor, al cual se le promete comprar una serie de productos bajo ciertas condiciones.**

Es similar a la Orden de Venta pero en vez de enviarla a un sujeto externo, se la mantiene para registros internos. 

> Inicio > Adquisiciones > Compras > Orden de Compra

![Buying Flow](/docs/assets/img/buying/buying_flow_po.png)

## 1. Prerrequisitos
Antes de crear y utilizar una Orden de Compra es aconsejable crear lo siguiente:

* [Proveedor](/docs/user/manual/en/buying/supplier)
* [Producto](/docs/user/manual/en/stock/item)


## 2. Cómo Crear una Orden de Compra

Una Orden de Compra puede crearse automáticamente desde un Pedido de Material o una Cotización de Proveedor.

1. Ir al listado de Orden de Compra y hacer click en Nuevo.
1. Seleccionar el Proveedor, y la fecha en que se requieren los productos
1. En la tabla de productos, seleccionar el producto por código, se puede cambiar el "pedido para fecha" para cada producto. 
1. Configurar la cantidad y el precio será obtenido automáticamente si está configurado en la función Producto. 
1. Configurar Impuestos
1. Guardar y Enviar
    <img class="screenshot" alt="Purchase Order" src="{{docs_base_url}}/assets/img/buying/purchase-order.png">

### 2.1 Configurar Depósitos

* **Configurar Depósito de Destino**: De forma opcional, se puede configurar un Depósito de destino predeterminado a donde se enviarán los Productos comprados. Esto será obtenido en las filas de la tabla de Productos.

### 2.2 Obtener Productos desde Pedidos de Materiales Abiertos
Los Productos pueden ser ingresados en la Orden de Compra automáticamente desde [Pedidos de Materiales](/docs/user/manual/en/stock/material-request) abiertos. Para que esto funcione se deben seguir los siguientes pasos:

1. Seleccionar un Proveedor en la Orden de Compra.
1. Configurar el Proveedor predeterminado en el formulario de Producto en el campo [Configuraciones Predetermidas de Producto](/docs/user/manual/en/stock/item#39-item-defaults).
1. El [Pedido de Material](/docs/user/manual/en/stock/material-request) debe ser de tipo "Compra".
1. Hacer click en el botón **Obtener Productos desde Pedidos de Material Abiertos** debajo del nombre del Proveedor. En ese momento aparecerá un diálogo con Pedidos de Materiales con Productos para los cuales el Proveedor predeerminado es el mismo que el seleccionado en la Orden de Compra. Al seleccionar el Pedido de Material y hacer click en **Obtener Productos**, los mismos serán tomados desde el Pedido de Material. 
<img class="screenshot" alt="Get Items from Open Material Requests" src="{{docs_base_url}}/assets/img/buying/get-items-from-open-mr.png">

> **Observación:** El botón **Obtener Productos desde Pedidos de Material Abiertos** es visible siempre y cuando la tabla de Productos esté vacía. 

## 3. Características

### 3.1 Dirección y Contacto

* **Seleccionar Dirección de Proveedor**: La Dirección de Facturación del Proveedor.
* **Seleccionar Dirección de Envío**: La dirección de envío del Proveedor desde la cuál estará enviando los productos. 
* Dirección, Dirección de Envío, Contacto, Mail de Contacto serán obtenidas si se guardan en la función Proveedor.


### 3.2 Moneda y Listado de Precios
Se puede seleccionar la moneda en la cual se almacenará la orden de compra. Si se configura un Listado de Precios, los precios de los productos serán obtenidos desde allí. Si se selecciona "Ignorar pautas de tarifas" las Pautas de tarifas configuradas en Cuentas > Pautas de tarifas, serán ignoradas.

Para saber más sobre Listado de Precios, [click aquí](/docs/user/manual/en/stock/price-lists).

Para saber sobre manejo de transacciones en múltiples monedas, [click aquí](/docs/user/manual/en/accounts/articles/managing-transactions-in-multiple-currency).

### 3.3 Subcontratar o "Proveer Materias Primas". 

Configurar la opción "Proveer Materias Primas" es útil para subcontrataciones donde se provee las materias primas para fabricar un producto. Para saber más, visitar la [Página de Subcontratación](/docs/user/manual/en/manufacturing/subcontracting).

### 3.4 Tabla de Productos

* **Escanear Código de Barra**: Se pueden añadir Productos a la tabla de Productos al escanear sus códigos de barra si se cuenta con un lector de código de barra. Para aprender a rastrearlos click [aquí](/docs/user/manual/en/stock/articles/track-items-using-barcode)

* **Cantidad y Precio**: Al seleccionar el código de Producto, se obtendrán su nombre, descripción y UdM. El "Factor de Conversión UdM" se configurará de forma predeterminada en 1, se puede cambiar dependiendo de la UdM recibida del venedor, leer más en la próxima sección. 

    La 'Tarifa de Lista de Precio' será obtenida si se configura una tarifa de Compra Estándar. "Última Tarifa de Compra" muestra el precio del producto de la última Orden de Compra. Si fue configurado, el Precio se obtendrá desde la función producto. Se puede adjuntar una Plantilla de Impuestos de Producto para aplicar una tasa impositiva específica al producto. 

* **Pesos de Producto** se obtendrá si fue configurado en la función Producto, sino, se debe ingresar de forma manual. 

* **Depósito**: El depósito a donde se entregarán los productos; será completado automáticamente si fue configurado en el campo "Configurar Depósito de Destino" en la Orden de Compra. A través de Pedido Abierto, puede vincularse un Pedido Abierto, para saber más [click aquí](/docs/user/manual/en/selling/blanket-order). También pueden vincularse un 'Proyecto' y una Lista de Materiales para rastrear su progreso. 

* "Cantidad de acuerdo a la UdM predeterminada" mostrará las existencias actuales de acuerdo con la UdM configurada en la función Producto. La "Cantidad recibida"se acualizará cuando los productos sean facturados. 

* **Detalles Contables**: Esta sección se completa de forma automática para una Orden de compra. La "Cuenta de Gastos" es aquella contra la cual se factura la Orden de Compra y el Centro de Costo es la cuenta a la cual se carga la Orden de Compra.

Fecha "Requerido Para" en cada Producto: Si se esperan envíos por partes, el Proveedor sabrá cuanta cantidad enviar en cada fecha. Esto ayudará a prevenir un sobre abastecimiento. También ayudará a controlar que tanto cumple el Proveedor los plazos. 

**Permitir Tarifa de Valoración 0**: Haciendo click en "Permitir Tarifa de Valoración 0" permitirá enviar el Recibo de Compra incluso si el valor del Producto es 0. Esto puede darse porque se trata de un producto de muestra o a un acuerdo con el Proveedor. T

### 3.6 Materias Primas Proveidas
Esta sección aparece cuando el campo "Proveer Materias Primas" se configura como "Si". Esta sección muestra una tabla con los Productos a ser proveidos al Proveedor para el proceso de subcontratación. 

* **Configurar Depósito de Reserva**: Al [Subcontratar](/docs/user/manual/en/manufacturing/subcontracting), las materias primas pueden ser reservadas en un Depósito separado. Al seleccionar el Depósito de Reserva aquí, el mismo se insertará en las filas de Productos de la lista de Materias Primas Proveídas.

#### Tabla de Materias Primas Proveídas

* **Cantidad Pedida**: El número de Productos requerido para completar la subcontratación de la forma especificada en la [Lista de Materiales](/docs/user/manual/en/manufacturing/bill-of-materials).
* **Cantidad Proveida**: Esto se actualizará cuando se creen los Registros de Inventario para transferir materiales al Depósito del Proveedor desde el Depósito de Reserva utilizando el botón **Transferir**.
    ![Subcontract Transfer Material](/docs/assets/img/buying/subcontract-transfer-materials.gif)

### 3.7 Conversión de UdM de Compra y UdM de Inventario

En la Orden de Compra, se puede cambiar la UdM de acuerdo con los requerimientos de inventario.

Por ejemplo, si se compró la materia prima en grandes cantidades con una UdM - Cajas, y se desea convertirla en UdM - Unidades, se puede realizar esto al crear la Orden de Compra. 

1. Configurar la UdM como unidades en la función producto. Tener en cuenta que la UdM configurada en la función Producto es la UdM de inventario. 

2. En la Orden de Compra mencionar la UdM como Caja. (Debido a que el material va a llegar en Cajas)

3. En la sección Depósito y Referencia, la UdM será obtenida automáticamente y será Unidades (desde el formulario de Producto):

 <img class="screenshot" alt="Purchase Order - UOM" src="{{docs_base_url}}/assets/img/buying/purchase-order-uom.png">

4. Mencionar el factor de conversión de UdM. Por ejemplo, (1); si una caja tiene 1 kilo. 

5. Tener en cuenta que la cantidad de existencias será actualizada de acuerdo con lo anterior. 

 <img class="screenshot" alt="Purchase Order - UOM" src="{{docs_base_url}}/assets/img/buying/po-stock-uom.png">

### 3.8 Impuestos y Gastos

Si el Proveedor va a cobrar gastos o impuestos adicionales como 
gastos de envío o de seguro, los mismos pueden ser añadidos aquí. Esto ayudará 
a registrar los costos con más facilidad y precisión. A su vez, si algunos de estos gastos aumentan el valor
del producto, también habrá que mencionarlos en la tabla de Impuestos. 

Visitar la página de [Plantilla de Impuestos y Gastos de Compra](/docs/user/manual/en/buying/purchase-taxes-and-charges-template) para saber más respecto a impuestos.

El total de impuestos y gastos se verá debajo de la tabla.

Para añadir impuestos de forma automática a través de una Categoría Impositiva, visitar [esta página](/docs/user/manual/en/accounts/tax-category).

Para lograr una valuación precisa, es necesario asegurarse de ingresar todos los impuestos y gastos correctamente en la Tabla de Impuestos y Gastos. 

#### Pauta de Envío
Una Pauta de Envío ayuda a determinar el costo de enviar un producto. El costo tenderá a aumentar a medida que la distancia de envío sea mayor. Para saber más, vistar la sección [Pauta de Envío](/docs/user/manual/en/selling/shipping-rule).

<img class="screenshot" alt="Purchase Order Taxes" src="{{docs_base_url}}/assets/img/buying/po-taxes.png">

Por ejemplo, se compran Productos que valen X y se venden por 1.3X. Por ende 
el Cliente paga 1.3 veces el impuesto que el vendedor paga al Proveedor. Como ya se pagó impuestos al Proveedor
por X, lo que se debe al Estado es solo 0.3 de impuestos. 

Esto puede ser rastreado fácilmente en ERPNext, ya que, cada impuesto principal es también una Cuenta. 
Idealmente, se deben crear dos Cuentas para cada tipo de VAT que se pague y colecte,
“VAT-X de Compra” (activo) y “VAT-X de Venta” (pasivo), o algo similar que cumpla
la misma función.

### 3.9 Descuentos Adicionales
Además de ofrecer descuentos por producto, esta sección permite sumar un descuento al total de la cotización. Este descuento puede ser aplicado al importe total, es decir, con impuestos incluidos, o al importe neto, es decir, sin incluir impuestos y otros gastos. El descuento adicional puede aplicarse como monto o porcentaje. 

Para más detalles leer, [Aplicar descuento](/docs/user/manual/en/selling/articles/applying-discount).

### 3.10 Condiciones de Pago
A veces el pago no se realiza en una sola cuota. Dependiendo del acuerdo, la mitad puede abonarse antes del envío y la otra mitad al recibir los productos o servicios. En esta sección, se puede añadir una plantilla de Condiciones de Pago o insertar los mismos de forma manual. 

Para saber más respecto a Condiciones de Pago,  [click aquí](/docs/user/manual/en/accounts/payment-terms).

### 3.11 Bases y Condiciones
En operaciones de Compra/Venta puede haber ciertas bases y condiciones que rigen la forma en que el proveedor vende bienes o servicios al cliente. Se pueden aplicar las Bases y Condiciones a las transacciones y éstas aparecerán en el documento impreso. Para saber más respecto a Bases y Condiciones, [click aquí](/docs/user/manual/en/setting-up/print/terms-and-conditions)

### 3.12 Configuración de Impresión
#### Papel membretado
Se pueden imprimir los pedidos de cotización/orden de compra en papel con el membrete de la empresa. Saber más [aquí](/docs/user/manual/en/setting-up/print/letter-head).

"Agrupar productos iguales", agrupará los productos iguales que se hayan sumado muchas veces a la tabla de Producto. Esto puede verse al imprimir.

#### Encabezados de Impresión
Los títulos de los documentos pueden ser modificados. Leer más [aquí](/docs/user/manual/en/setting-up/print/print-headings).

El Descuento Adicional del vendedor, los Términos de Pago, las Bases y Condiciones pueden registrarse en la Orden de Compra.

### 3.13 Más Información
Esta sección muestra el estado de la Orden de Compra, porcentaje de productos recibidos y porcentaje de productos facturados. Si es una Orden entre Empresas, la Orden de Venta puede ser vinculada aquí. 

### 3.14 Luego de Enviar
Una vez que se "Envía" la Orden de Compra, se pueden generar acciones como estas:

* Se puede Añadir, Actualizar y Borrar Productos en la Orden de Compra haciendo click en el botón **Actualizar Productos**. De cualquier forma, no se puede borrar productos que ya hayan sido recibidos.

* Estado: Luego de enviada se puede mantener una Orden de Compra o Cerrarla. 

* Crear: De una Orden de Compra enviada, se puede crear lo siguiente: 

    * [Recibo de Compra](/docs/user/manual/en/stock/purchase-receipt) - Un recibo que indica que se recibieron los Productos.
    * [Factuar de Compra](/docs/user/manual/en/accounts/purchase-invoice) - Una factura para la Orden de Compra.
    * [Registro de Pago](/docs/user/manual/en/accounts/payment-entry) - Un registro de pago que indica que el pago de la orden de compra ha sido realizado. 
    * [Registro Contable](/docs/user/manual/en/accounts/journal-entry) - Se crea un Asiento en el Libro Mayor.

    ![Purchase Order post submitting](/docs/assets/img/buying/po-after-submit.png)

### 4. Temas Relacionados
1. [Pedido de Cotización](/docs/user/manual/en/buying/request-for-quotation)
1. [Plantilla de Impuestos y Gastos de Compra](/docs/user/manual/en/buying/purchase-taxes-and-charges-template)
1. [Comprar en Diferentes Unidades](/docs/user/manual/en/buying/articles/purchasing-in-different-unit)
1. [Enmendar Orden de Compra luego de Envío](/docs/user/manual/en/buying/articles/amending-purchase-order-after-submit)

{next}
