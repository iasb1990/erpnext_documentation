<!-- add-breadcrumbs -->
# Orden de Venta

**Una Orden de Venta es una confirmación de un pedido del cliente.**

Usualmente es un contrato vinculante con el cliente. Una vez que el cliente confirma la Cotización, se puede convertir a la misma en una Orden de Venta.

<img class="screenshot" alt="Make Quotation from Opportunity" src="{{docs_base_url}}/assets/img/selling/selling-flow-so.png">

Para acceder a Orden de Venta ir a:
> Inicio > Comercialización > Ventas > Orden de Venta

## 1. Prerrequisitos
Antes de crear y utilizar una Orden de Venta es aconsejable crear lo siguiente: 

* [Cliente](/docs/user/manual/en/CRM/customer)
* [Producto](/docs/user/manual/en/stock/item)

## 2. Cómo crear una orden de venta
1. Ir al listado de Orden de Venta y hacer click en Nuevo.
1. Seleccionar el Cliente
1. Configurar la "Fecha de Envío" - se aplica a todo el pedido.
1. En Tipo de Orden, se puede establecer si se trata de una Orden de Venta, una Orden de Mantenimiento, o si proviene de una operación online [Carrito de compras](/docs/user/manual/en/website/shopping-cart) en el sitio web. La configuración predeterminada la va a establecer como "Ventas".
1. En la sección "Orden de Compra del Cliente" se puede insertar el número de Orden de Compra u otros detalles que puedan ser útiles como referencia. 
1. Añadir los productos y cantidades a ser enviados en la tabla de productos. Si los precios de los productos ya fueron configurados, el campo Precio se completará automáticamente. Si no, es necesario introducir los precios de los productos manualmente. También se puede modificar la tarifa completada automáticamente en caso de que deban hacerse cambios en su valor. 
1. Hacer click en "Guardar" para guardar un borrador de la Orden de Venta. 
1. Si se hace click en "Enviar", la Orden de Venta será enviada al Sistema. 

### 2.1 Otras formas de crear una Orden de Venta
1. También se puede crear una Orden de Venta desde una Cotización que haya sido enviada haciendo click en el boton "Crear" que se encuentra arriba a la derecha.

  <img class="screenshot" alt="Make Sales Order from Quotation" src="{{docs_base_url}}/assets/img/selling/make-SO-from-quote.png">

1. O se puede crear una nueva Orden de Venta y extraer detalles de una Cotización. 

  <img class="screenshot" alt="Make Sales Order from Quotation" src="{{docs_base_url}}/assets/img/selling/so-from-quote.gif">

Para permitir pautas de precios por clientes, (el "Cliente A" paga $1,00 por el "Producto 1", pero el "Cliente B" paga $1,25 por el mismo producto) hay que hacer click en la caja "Permitir al Usuario Editar Lista de Precios en Transacción" en [Configuración de Venta](/docs/user/manual/en/selling/selling-settings). Esto permite guardar el precio por producto específico para cada cliente cuando se cambia un precio en la Orden de Venta. 

## 3. Características

### 3.1 Moneda y Listado de Precios
Se puede seleccionar la moneda en la cual se arma la cotización u orden de venta. Si se configura un Listado de Precios, los precios de los productos serán obtenidos desde allí. Si se selecciona "Ignorar pautas de tarifas" las  [Pautas de tarifas](/docs/user/manual/en/accounts/pricing-rule) establecidas en Cuentas > Pautas de tarifas, serán ignoradas.

Para saber más sobre Listado de Precios, [click aquí](/docs/user/manual/en/stock/price-lists).

Para saber sobre manejo de transacciones en múltiples monedas, [click aquí](/docs/user/manual/en/accounts/articles/managing-transactions-in-multiple-currency).

### 3.1 Configurar Depósito de Origen
Si se posee el mismo stock de productos en múltiples depósitos, configurar un depósito de origen en esta sección va a ocasionar que todos los productos de la tabla de productos sean extraídos desde ese depósito. Debe haber existencias disponibles en el "Depósito de Origen" que se está seleccionando. Esta opción va a modificar el "Depósito Predeterminado" establecido en la función producto.

### 3.2 Tabla de Productos

* **Fechas de envío para cada producto**: Si hay muchos productos, establecer una fecha de entrega en la primera fila hará que la misma sea copiada a las filas de abajo, si éstas están en blanco. Si no se configuran en su totalidad, hay que configurarlas desde la parte de arriba de la Orden de Venta. 

    Una Orden de Venta muestra el monto facturado, la tasa de valuación, y la ganancia bruta en la tabla de productos cuando se hace click en el triángulo invertido para expandir una fila. 

    También se pueden sumar productos en la tabla de productos escaneando sus códigos de barra si se cuenta con un lector de código de barras. Aprender a usar códigos de barras para rastrear productos [aquí](/docs/user/manual/en/stock/articles/track-items-using-barcode)

* **Depósito de envío**: Este es el depósito desde el cual se extraerán los productos para ser enviados al cliente.

* **Envío directo**: Esta es una situación en la cual no se cuenta con existencias de los productos sino que se los envía directamente al cliente desde el distribuidor. Para permitir un envío directo para un producto hacer click en la caja "Proveedor envía a cliente". Al hacer esto, la opción Depósito de Envío desaparecerá. Elegir al proveedor en el campo "Proveedores". 

    Además, si se crea una Orden de Compra desde esta Orden de Venta, se creará para el proveedor seleccionado y solo para los productos válidos para envío directo. 

* **Planificación**: Para saber respecto a los campos de planificación [click aquí](/docs/user/manual/en/stock/projected-quantity).

Los otros campos de la tabla de productos son similares a lo explicado en [Cotización](/docs/user/manual/en/selling/quotation#23-the-items-table).

### 3.3 Lista de envío

Está asociada a los [Paquetes de productos](/docs/user/manual/en/selling/product-bundle) y solo aparece cuando la transacción involucra un paquete de productos. 

La tabla de "Lista de Envío" se actualizará de forma automática cuando se guarde la Orden de Venta. Si algún producto es un Paquete de Productos, entonces la "Lista de Envío" va a estar compuesta por el listado detallado de los productos.

Se deberá seleccionar un Depósito de envío incluso para un producto perteneciente a un paquete de productos, este Depósito luego será actualizado en los productos de la Lista de Envío. Se puede cambiar el depósito, el número de serie y lote en los productos de la lista de envío en el caso de que los productos dentro del paquete de productos provengan de distintos depósitos. .

Una Lista de Envío tiene la siguiente apariencia:

<img class="screenshot" alt="Packing List" src="{{docs_base_url}}/assets/img/selling/so-packing-list.png">

### 3.4 Impuestos y gastos adicionales
Para sumar impuestos a la Cotización se puede seleccionar una [Plantilla de Impuestos y Otros Gastos](/docs/user/manual/en/selling/sales-taxes-and-charges-template) o añadir los impuestos de forma manual en la tabla de Impuestos y Otros Gastos.

El total de impuestos y gastos se verá al final de la tabla. Haciendo click en Detalle de Impuestos se pueden ver todos los componentes y montos. 

<img class="screenshot" alt="Taxes in Quotation" src="{{docs_base_url}}/assets/img/selling/sales-order-taxes.png">

#### Pauta de Envío
Una Pauta de Envío ayuda a determinar el costo de enviar un producto. El costo tenderá a aumentar a medida que la distancia de envío sea mayor. Para saber más, vistar la sección [Pauta de Envío](/docs/user/manual/en/selling/shipping-rule).

Si se selecciona una Categoría de Impuestos, la plantilla y la tabla de impuestos se completarán automáticamente. Para saber mas visitar [esta página](/docs/user/manual/en/accounts/tax-category).

### 3.5 Descuentos Adicionales
Además de ofrecer descuentos por producto, esta sección permite sumar un descuento al total de la cotización. Este descuento puede ser aplicado al importe total, es decir, con impuestos incluidos, o al importe neto, es decir, sin incluir impuestos y otros gastos. El descuento adicional puede aplicarse como monto o porcentaje. 

Para más detalles, leer  [Aplicar descuento](/docs/user/manual/en/selling/articles/applying-discount).

### 3.6 Condiciones de Pago
A veces el pago no se realiza en una sola cuota. Dependiendo del acuerdo, la mitad puede abonarse antes del envío y la otra mitad al recibir los productos o servicios. En esta sección, se puede añadir una plantilla de Condiciones de Pago o insertar las mismas de forma manual. 

Para saber más respecto a Condiciones de Pago, [click aquí](/docs/user/manual/en/accounts/payment-terms).

### 3.7 Bases y Condiciones
En operaciones de Compra/Venta puede haber ciertas bases y condiciones que rigen la forma en que el proveedor vende bienes o servicios al cliente. Se pueden aplicar las Bases y Condiciones a las transacciones y éstas aparecerán en el documento impreso. Para saber más respecto a Bases y Condiciones, [click aquí](/docs/user/manual/en/setting-up/print/terms-and-conditions)

### 3.8 Configuración de Impresión
#### Papel membretado
Las cotizaciones u órdenes de venta pueden ser impresas en papel con el membrete de la empresa. Leer más [aquí](/docs/user/manual/en/setting-up/print/letter-head).

"Agrupar productos" sirve para agrupar productos iguales que hayan sido añadidos más de una vez en la tabla de productos. Esto se puede ver al imprimir. 

#### Encabezados de Impresión
Las Cotizaciones también pueden ser denominadas "Factura Proforma" o "Propuesta".
Esto puede hacerse seleccionando **Encabezados de Impresión**. Para crear nuevos encabezados ir a: Inicio > Configuración > Impresión > Encabezados de Impresión. Leer más [aquí](/docs/user/manual/en/setting-up/print/print-headings).

### 3.9 Más información
* **Campaña::** Una campaña de ventas puede ser asociada a la cotización. Un grupo de cotizaciones puede ser parte de una campaña de ventas
* **Fuente:** Si la cotización es para un potencial cliente, sus datos pueden obtenerse desde la Fuente de Potenciales Clientes tanto desde una campaña, un proveedor, exhibición, etc. Si se quiere cotizar a un cliente actual, seleccionar Cliente Actual.
* **Pedidos de Empresas Vinculadas**: Si dos empresas son parte de la misma organización o tienen una relación principal-secundaria, se puede asociar una Orden de Compra a esta Orden de Venta. Leer más sobre facturación entre empresas vinculadas  [aquí](/docs/user/manual/en/accounts/inter-company-invoices).
* **Proyecto**: Si la Orden de Venta es parte de un Proyecto se puede asociar en esta sección y por ende, el progreso del Proyecto será actualizado.

### 3.10 Estado de Facturación y Envío

* **Estado**: El estado de la Orden de Ventas, puede ser Borrador, en Espera, a Entregar y Facturar, a Facturar, a Entregar, Completa, Cancelada o Cerrada. 
* **Porcentaje de Monto Facturado y Entregado**: El porcentaje del monto facturado y los productos entregados de la Orden de Venta. 

### 3.11 Comisión
Si la venta se dio a través de un Socio Comercial, se pueden sumar los detalles de su comisión aquí. Se ingresa la tasa de comisión y su montó se verá debajo. 

### 3.12 Equipo de Ventas
**Vendedores:** ERPNext permite añadir a todos los vendedores que hayan trabajado en este trato. Se puede cambiar el porcentaje de contribución de los vendedores y calcular cuantos incentivos se ganaron con este trato. 

<img class="screenshot" alt="Sales Team in Sales Order" src="{{docs_base_url}}/assets/img/selling/so-sales-team.png">

### 3.13 Sección de Repetición Automática
Repetir automáticamente Ordenes de Venta es como una suscripción. Seleccionar una fecha de inicio y de fin de la repetición automática. Seleccionar la Repetición Automática creada. Para saber más sobre repeticiones automáticas [click aquí](/docs/user/manual/en/automation/auto-repeat).

### 3.14 Luego de Enviar
La Orden de Venta es una transacción "Enviable". Acciones posteriores (como confeccionar una Orden de Entrega) solo podrán ejecutarse luego de "Enviar" la Orden de Venta.

Una vez que se "Envía" la Orden de Venta, se pueden realizar las siguientes acciones desde la misma: 

* Se pueden Agregar, Actualizar y Borrar productos de la Orden de Venta haciendo click en el botón **Actualizar Productos**. Sin embargo, no se pueden borrar productos que ya fueron entregados o que tienen ordenes de trabajo asignadas.

* Estado: Luego de enviada, se puede mantener la Orden de Venta o Cerrarla.

* Crear: Se puede crear lo siguiente desde una Orden de Venta enviada:

    * Nota de Envío - Para registrar un envío. También se puede hacer una Nota de Envío para productos seleccionados de acuerdo a la fecha de envío.
    * Orden de Trabajo - Iniciar una Orden de Trabajo con las materias primas. 
    * Factura de Venta - Facturar la Orden
    * Pedido de Material - Pedir materiales de los cuales ya no haya existencias. 
    * Pedido de Materias Primas - Pedir las materias primas necesarias para la manufactura.
    * Proyecto - Crear un proyecto basado en la Orden de Venta.
    * Suscripción - Repetir de forma automática una Orden de Venta, es decir, realizar una suscripción. .
    * Solicitar Pago - Solicitar el Pago de la Orden. 
    * Recibo - Registrar pago de la Orden de Venta. 

Estas acciones también pueden verse en la parte de arriba del Panel. También se puede realizar un asiento contable en el Libro Diario, basada en la Orden de Venta, desde el panel. 

<img class="screenshot" alt="Actions from Submitted Sales Order" src="{{docs_base_url}}/assets/img/selling/submit-so.png">

### 3.15 Orden de Venta con Tipo de Orden "Mantenimiento" 
Cuando el "Tipo de Orden" de la Orden de Venta es "Mantenimiento" es necesario seguir estos pasos: 

1. Ingresar Moneda, Listado de Precios y detalles de Productos. 
2. Mencionar impuestos y otra información.
3. Guardar y enviar el formulario.
4. Una vez que el formulario fue enviado, el botón Crear dará las siguientes opciones que son específicas a la Orden de Venta de tipo mantenimiento. 

    i) Visita de Mantenimiento ii) Cronograma de Mantenimiento.

  ![Orden de Venta de Tipo Mantenimiento](/docs/assets/img/selling/so-maintenance.png)

> **Nota 1:**
Al clickear en el botón Acción y seleccionar "Visita de Mantenimiento" se puede llenar el formulario de visita de forma directa. Los detalles de la Orden de Venta serán obtenidos directamente.

> **Nota 2:**
Al hacer click en el botón Acción y seleccionar "Cronograma de Mantenimiento" se pueden completar los detalles del cronograma. Los detalles de la Orden de Venta serán obtenidos directamente. 

> **Nota 3:**
Al hacer click en el botón "Factura" se puede realizar una Factura por los 
servicios. Los detalles de la Orden de Venta serán obtenidos directamente. 

### 4. Temas relacionados
1. [Cotización](/docs/user/manual/en/selling/quotation)
1. [Cerrar Orden de Venta](/docs/user/manual/en/selling/articles/close-sales-order)
1. [Enmendar Orden de Venta luego de ser enviada](/docs/user/manual/en/selling/articles/amending-sales-order-after-submit)
1. [Lista de Selección de Productos](/docs/user/manual/en/stock/pick-list#21-create-pick-list-from-sales-order)

{siguiente}
