<!-- add-breadcrumbs -->
# Pedido de Materiales

**Un Pedido de Materiales es un documento simple que identifica el requerimiento de un cierto conjunto de Productos (productos o servicios) por un motivo en particular.**

Un Pedido de Material puede tener los siguientes objetivos:

* **Compra**: Si el material pedido debe ser comprado.
* **Transferencia de Material**: Si el material pedido debe ser pasado de un Depósito a otro. 
* **Material Distribuido**: Si el material pedido debe ser Distribuido para algún objetivo como fabricación.
* **Fabricación:** Si el material pedido debe ser producido.
* **Provisto por un Cliente**: Si el material pedido será provisto por un Cliente. Para saber más respecto a esto visitar la página [Productos Provisto por un Cliente](/docs/user/manual/en/manufacturing/articles/customer-provided-items).

<img class="screenshot" alt="Material Request" src="{{docs_base_url}}/assets/img/buying/material-request-flowchart.png">

Para acceder al listado de Pedido de Material ir a:
> Inicio > Existencias > Transacciones de Existencias > Pedido de Materiales

## 1. Cómo Crear un Pedido de Materiales
1. Ir al listado de Pedido de Materiales y hacer click en Nuevo.
2. Ingresar el campo Pedido para Fecha
3. Seleccionar uno de los objetivos mencionados anteriormente.
4. Se pueden tomar Productos desde Listas de Materiales, Órdenes de Venta o Paquetes de Productos. 
  ![MR fetch from](/docs/assets/img/stock/mr-fetch-from.png)
5. Seleccionar el Producto y configurar la cantidad.
6. Seleccionar el Depósito para el cual los productos son pedidos.
7. En esta tabla, se puede cambiar el Pedido para Fecha para Productos individuales.
8. Guardar y Enviar.

### 1.1 Formas alternativas de crear un Pedido de Materiales
Un Pedido de Materiales puede generarse automáticamente:

* Desde una [Orden de Venta](/docs/user/manual/en/selling/sales-order).
* Cuando la Cantidad Proyectada de un Producto en Almacen (Depósito) alcanza un nivel particular.
* Desde el [Plan de Producción](/docs/user/manual/en/manufacturing/production-plan) para planificar las actividades de fabricación.

Si los Productos son de inventario, también se debe mencionar el Depósito a donde se espera que los mismos sean enviados. Esto ayuda a controlar la [Cantidad Proyectada](/docs/user/manual/en/stock/projected-quantity) para este Producto.

> Información: El Pedido de Materiales no es obligatorio. Es ideal si se cuenta con compras
centralizadas, para poder recolectar esta información de varias oficinas.

### 1.2 Estados

Los estados en que puede encontrarse un Pedido de Material son:

* **Borrador**: Un borrador está guardado pero todavía no fue enviado al sistema.
* **Enviado**: El documento es enviado al sistema.
* **Suspendido**: Si no se requieren más materiales, el Pedido de Material puede ser suspendido. 
* **Cancelado**: Los materiales no son necesarios y, por ende, se cancela el pedido.
* **Pendiente**: La Compra/Fabricación está pendiente para completar el Pedido de Material. 
* **Parcialmente Pedido**: Órdenes de Compra para algunos Productos del Pedido de Materiales fueron hechas y otras están pendientes.
* **Pedido**: Todos los Productos en el Pedido de Materiales fueron pedidos a través de Órdenes de Compra.
* **Distribuídos**: Los materiales son distribuídos utilizando el asiento Distribución de Existencias de Material. 
* **Transferido**: Los materiales requeridos son transferidos de un Depósito a otro utilizando Ingreso de Existencias. 
* **Recibido**: Los materiales fueron pedidos y recibidos en el Depósito utilizando un Recibo de Compra. 

## 2. Características
### 2.1 Tabla de Productos
* **Código de Barra**: Se puede rastrear Productos utilizando [códigos de barra](/docs/user/manual/en/stock/articles/track-items-using-barcode).

* El Código de Producto, el nombre, descripción, Imagen y Fabricante serán obtenidos desde la función Producto.

* **Escanear Código de Barra**: Se pueden añadir Productos a la tabla de Productos al escanear sus códigos de barra si se cuenta con un lector de código de barra. Para aprender a rastrearlos click [aquí](/docs/user/manual/en/stock/articles/track-items-using-barcode)

* La UdM, el Factor de Conversión, y el Monto serán obtenidos. Se cambia el Depósito para el cuál se realiza el pedido de material. 

* Detalles contables como la Cuenta de GAstos y Dimensiones Contables pueden ser configurados para los Productos. 

* Salto de Página creará un salto de página justo antes de este producto al imprimir.

### 2.2 Configurar Depósitos
* **Configurar Depósitos**: De forma opcional, se puede configurar el Depósito a donde llegarán los Productos pedidos. Esto será incluido en el campo "Para Depósito" en las filas de la tabla de Productos. 

### 2.3 Más Información
En el campo "Pedido Desde", se puede configurar una Referencia desde la cual se generó el Pedido de Material. 

### 2.4 Detalles de Impresión
#### Papel membretado
Se pueden imprimir los Pedidos de Materiales en papel con el membrete de la empresa. [Click aquí](/docs/user/manual/en/setting-up/print/letter-head) para saber más.

#### Encabezados de Impresión
Los encabezados de los Recibos de Compra pueden ser modificados al imprimir el documento. Se puede hacer esto seleccionando **Encabezado de Impresión**. Para crear nuevos Encabezados de Impresión ir a: Inicio > Configuraciones > Impresión > Encabezados de Impresión. Leer más [aquí](/docs/user/manual/en/setting-up/print/print-headings).

### 2.5 Bases y Condiciones
En operaciones de Compra/Venta puede haber ciertas bases y condiciones que rigen la forma en que el proveedor vende bienes o servicios al cliente. Se pueden aplicar las Bases y Condiciones a las transacciones y éstas aparecerán en el documento impreso. Para saber más respecto a Bases y Condiciones, [click aquí](/docs/user/manual/en/setting-up/print/terms-and-conditions)

### 2.6 Luego de Enviar
Se pueden crear los siguientes documentos:

* [Pedido de Cotización](/docs/user/manual/en/buying/request-for-quotation)
* [Orden de Compra](/docs/user/manual/en/buying/purchase-order)
* [Cotización de Proveedor](/docs/user/manual/en/buying/supplier-quotation)

<img class="screenshot" alt="Material Request" src="{{docs_base_url}}/assets/img/stock/material-request.png">


### 2.7 Generar Pedido de Materiales Automáticamente

Los Pedidos de Materiales pueden ser generados automáticamente al habilitar la configuración en [Configuraciones de Existencias](/docs/user/manual/en/stock/stock-settings#9-automatic-material-request) y establecer el nivel en el [Formulario de Producto](/docs/user/manual/en/stock/item#34-automatic-reordering). Cuando el nivel de existencias caiga por debajo de una cierta cantidad, al configurar un pedido automático, se generará automáticamente un pedido de materiales para el Producto.

## 3. Temas Relacionados
1. [Producto](/docs/user/manual/en/stock/item)
1. [Creación Automática de Pedido de Materiales](/docs/user/manual/en/stock/articles/auto-creation-of-material-request)
1. [Lista de Selección](/docs/user/manual/en/stock/pick-list#23-create-pick-list-from-material-request)
1. [Pedido de Cotización](/docs/user/manual/en/buying/request-for-quotation)
1. [Orden de Compra](/docs/user/manual/en/buying/purchase-order)
1. [Cotización de Proveedor](/docs/user/manual/en/buying/supplier-quotation)
