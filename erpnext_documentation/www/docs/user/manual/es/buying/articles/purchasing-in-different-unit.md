<!-- add-breadcrumbs -->
#Comprar en Unidades de Medida (UdM) Diferentes

Cada producto tiene su propia Unidad de Medida (UdM) de almacenamiento asociada. Por ejemplo, la UdM de lapiceras puede ser Unidades y la arena puede ser guardada en kilos. Sin embargo, cuando realizamos un pedido a un Proveedor, la UdM de un producto puede cambiar. Por ejemplo, podemos pedirle al Proveedor 1 kit/caja de Lapiceras, o, un camión de arena. Al crear la transacciónd e compra, se puede cambiar la UdM de Compra para un producto. 

### Situación:

El Producto "Lapicera" se almacena en Unidades pero se compra en Cajas. De esta forma, realizaremos una Orden de Compra por Lapiceras en Caja. 

#### Paso 1: Editar la UdM en la Orden de Compra

En la Orden de Compra se verán dos campos UdM.

- UdM
- UdM de Almacenamiento

En ambos campos, la UdM de un producto será obtenida de forma preestablecida. Se deberá editar el campo UdM, y seleccionar UdM de Compra (en este caso, la Caja). Actualizar la UdM de Compra mas que nada sirve de referencia al proveedor. En el formato de impresión se verá la cantidad de producto en la UdM de Compra. 

<img alt="Item Purchase UoM" class="screenshot" src="{{docs_base_url}}/assets/img/articles/editing-uom-in-po.gif">

#### Step 2: Actualizar los Factores de Conversión

Si se reciben 20 unidades de Lapiceras en una Caja, el Factor de Conversión será 20.

<img alt="Item Conversion Factor" class="screenshot" src="{{docs_base_url}}/assets/img/articles/po-conversion-factor.png">

De acuerdo con la Cantidad y el Factor de Conversión, se calculará la cantidad en la UdM de Inventario. Si se compra solo una Caja, entocnes la cantidad en UdM de inventario será configurada como 20.

<img alt="Purchase Qty in Default UoM" class="screenshot" src="{{docs_base_url}}/assets/img/articles/po-qty-in-stock-uom.png">

### Actualización del Inventario de Existencias

Sin respetar la UdM de Compra seleccionada, la actualización del inventario de existencias se realizará en la UdM predeterminada de un producto. Por ende, es importante que el factor de conversión sea ingresado correctamente al comprar productos en diferentes UdM. 

<img alt="Print Format in Purchase UoM" class="screenshot" src="{{docs_base_url}}/assets/img/articles/po-stock-uom-ledger.png">

### Configurar Factor de Conversión de un Producto

En la función Producto, dentro de la sección Compra, se pueden ennumerar todas las UdM de compra posibles para un producto, junto con su respectivo Factor de Conversión UdM. 

<img alt="Purchase UoM master" class="screenshot" src="{{docs_base_url}}/assets/img/articles/item-purchase-uom-conversion.png">

<!-- markdown -->