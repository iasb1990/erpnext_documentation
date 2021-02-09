<!-- add-breadcrumbs -->
# Cotización de Proveedor

**Una Cotización de Proveedor es un documento de un potencial proveedor donde se especifica el costo de bienes o servicios que proveerán en un período específico.**

Una Cotización de Proveedor también puede contener Condiciones de Venta, Condiciones de Pago y Garantías. La aceptación de la cotización por parte del comprador puede ser considerada como un acuerdo vinculante para ambas partes.

![Buying Flow](/docs/assets/img/buying/buying_flow_sq.png)

Para acceder a la Cotización de Proveedor ir a:
> Inicio > Adquisiciones > Compras > Cotización de Proveedor

## 1. Prerrequisitos
Antes de crear y utilizar una Cotización de Proveedor, es recomendable crear lo siguiente:

* [Proveedor](/docs/user/manual/en/buying/supplier)
* [Producto](/docs/user/manual/en/stock/item)

## 2. Cómo Crear una Cotización de Proveedor

### 2.1 Cotización de Proveedor desde Pedido de Material

Se puede crear una Cotización de Proveedor desde un Pedido de Material
![Supplier Quotation from Material Receipt]({{docs_base_url}}/assets/img/buying/supplier-quotation-from-mr.png)

O:

Una Cotización de Proveedor puede crearse desde la [Función Proveedor](/docs/user/manual/en/buying/supplier).

O:

El proveedor puede enviar la cotización a través de ERPNext. Para saber más de esto, visitar la [Página de Pedido de Cotización](/docs/user/manual/en/buying/request-for-quotation#4-creating-a-supplier-quotation-after-rfq).

### 2.2 Crear una Cotización de Proveedor de forma manual
1. También se puede crear una Cotización de Proveedor directamente desde:

    **Adquisiciones > Compras > Cotización de Proveedor > Nueva**.
1. Seleccionar el Proveedor que envió la cotización 
1. La Dirección y el Contacto serán obtenidos si fueron configurados en la función proveedor. 
1. Ingresar el Código de Producto, seleccionar la cantidad. Si se configuró un precio de Compra Estándar para el producto en la sección [Precio de Producto](/docs/user/manual/en/stock/item-price), el mismo será obtenido.
    <img class="screenshot" alt="Supplier Quotation" src="{{docs_base_url}}/assets/img/buying/supplier-quotation.png">

Si se cuenta con muchos Proveedores que proveen el mismo Producto, generalmente 
se envía un [Pedido de Cotización](/docs/user/manual/en/buying/request-for-quotation) a varios Proveedores. En
muchos casos, en especial si se cuenta con compra centralizada, es recomendable registrar todas las cotizaciones de forma que: 

  * Se puedan comprar precios fácilmente en el futuro.
  * Controlar si todos los Proveedores tuvieron la oportunidad de cotizar. 

Las Cotizaciones de Proveedores no siempre sirven para la mayoría de los negocios pequeños. Se recomienda
siempre evaluar el costo de recolectar información con el valor que realmente provee. 
Como recomendación, solo se puede hacer esto para productos de alto valor. 

## 3. Características
### 3.1 Impuestos y Gastos
Si el Proveedor va a cobrar gastos o impuestos adicionales como gastos de envío o de seguro, los mismos pueden ser añadidos aquí. Esto ayudará a registrar los costos con más facilidad y precisión. A su vez, si algunos de estos gastos aumentan el valor del producto, también habrá que mencionarlos en la tabla de Impuestos. También se pueden usar plantillas para los impuestos. Para mas información respecto a confiugración de impuestos ver la página [Plantilla de Impuestos y Gastos de Compra](/docs/user/manual/en/buying/purchase-taxes-and-charges-template).

### 3.2 Más
Hay campos para Categoría Fiscal, Pauta de Envío, Plantilla de Impuestos y Gastos de Compra, Descuento, Bases y Condiciones, Configuraciones de Impresión. Se pueden llenar estos campos para tener un registro interno. Visitar la página [Cotización](/docs/user/manual/en/selling/quotation) para saber más respecto a estas secciones. Tener en cuenta que los detalles que se completen aquí como Pauta de Envío, Impuestos, Descuento, Bases y Condiciones, etc, son del proveedor y pueden ser registrados para un seguimiento preciso. 

Observaciones:

- Si fue configurada, la Categoría Fiscal será tomada desde la función proveedor 
- Configuraciones de Impresión es para realizar cambios a la impresión de la cotización de proveedor
- Las Bases y Condiciones establecidas aquí son del proveedor
- La cotización de proveedor puede ser vinculada a pedidos de material utilizando el botón "Vincular a pedido de material". 

### 3.3 Luego de Enviar
Luego de enviar la Cotización de Proveedor pueden crearse los siguientes documentos: 

* Orden de Compra - Una Orden de Compra si se está de acuerdo con la cotización del proveedor. 
* Cotización - Una cotización al cliente.
* Repetir Automáticamente - Repetir Automáticamente la cotización del proveedor en intervalos específicos. 

### 4. Temas Relacionados
1. [Proveedor](/docs/user/manual/en/buying/supplier)
1. [Grupo de Proveedores](/docs/user/manual/en/buying/supplier-group)
1. [Orden de Compra](/docs/user/manual/en/buying/purchase-order)
1. [Pedido de Cotización](/docs/user/manual/en/buying/request-for-quotation)

{next}