<!-- add-breadcrumbs -->
# Voucher de Costo en Destino

**Costo en Destino es el costo final total que requiere un producto para llegar hasta la puerta del comprador.**

El Costo en Destino incluye los costos originales del producto, todos los gastos de envío, derechos de aduana, impuestos, seguros, costos de conversión de monedas, etc. Puede que todos estos componentes no se apliquen en cada envío, pero los costos relevantes deben ser considerados como parte del costo en destino.

> **¿Qué es Costo en Destino?**

> Para entender mejor el costo en destino, tomemos un ejemplo de nuestra vida diaria. Necesitamos un lavarropa para nuestra casa. Antes de comprar, realizamos averiguaciones para encontrar el mejor precio. En este proceso, podemos encontrar un mejor precio en un negocio que se encuentra lejos de casa. Sin embargo, si vamos a comprar en ese negocio, tambien debemos considerar el costo de envío. El costo total, con envío incluido, puede ser mayor al que conseguimos en un negocio más cercano. En ese caso, elegiremos comprar en el negocio más cercano, ya que el costo en destino del producto será más barato. 

De forma similar, al hacer negocios, es crucial identificar el costo en destino para un Producto, debido a que ayuda a decidir el costo de venta de ese producto e impacta en las ganancias de la empresa. Por ende, todos los gastos de costo en destino deberían ser incluidos en la tarifa de valoración del Producto.

De acuerdo con un estudio realizado por [Third-Party Logistics](http://www.3plstudy.com/), solo un 45% de los encuestados utilizan el Costo en Destino minuciosamente. Los principales motivos para no utilizar el Costo en Destino son: falta de información necesaria (49%), falta de herramientas adecuadas (48%), tiempo insuficiente (31%), y desconocimiento respecto a cómo aplicar costo en destino (27%).

Para acceder al listado de Voucher de Costo en Destino ir a:
> Inicio > Inventario > Herramientas > Voucher de Costo en Destino

## 1. Prerrequisitos
Antes de crear y utilizar un Voucher de Costo en Destino, se recomienda crear lo siguiente: 

* [Recibo de Compra](/docs/user/manual/en/stock/purchase-receipt)

    O

* [Factura de Compra](/docs/user/manual/en/accounts/purchase-invoice)


## 2. Cómo Crear un Voucher de Costo en Destino

1. Ir al listado de Voucher de Costo en Destino y hacer click en Nuevo.
1. Seleccionar el tipo de Documento Comprobante, sea Factura de Compra o Recibo. Se pueden seleccionar muchos documentos. 
1. Seleccionar la Factura o Recibo específico. El nombre del proveedor y el Total General se obtendrán automáticamente. 
1. Hacer click en el botón Obtener Productos desde Recibo de Compra para tomar los detalles de producto desde la Factura o Recibo de Compra. 
1. Seleccionar si la Distribución de Costos se hará de acuerdo con cantidad o Monto. 
1. Ingresar la Cuenta de Gastos y el Monto para los Costos Adicionales en la tabla de Impuestos y Gastos. El monto se distribuirá de forma equitativa de acuerdo con la cantidad o monto, según lo que se seleccionó anteriormente.  
1. Guardar y Enviar.

    <img class="screenshot" alt="Landed Cost Voucher" src="{{docs_base_url}}/assets/img/stock/landed-cost-voucher.png">


En el documento se pueden seleccionar muchas Facturas/Recibos de compra y obtener todos los productos desde esos Recibos de Compra. Luego se deben ingresar los gastos aplicables, en la tabla de "Impuestos y Gastos". Se puede borrar fácilmente un producto, si los gastos adicionales no se aplican al mismo. 

Los gastos sumados son distribuidos de forma proporcional entre todos los productos, de acuerdo con el monto o cantidad. Si se seleccionó en base al monto, el Producto con el mayor valor recibirá una mayor proporción de los gastos. En el caso de cantidad, el Producto con mayor cantidad recibirá la mayoría de los gastos, y los otros Productos recibirán montos menores. Esto se muestra en la siguiente captura de pantalla. 

<img class="screenshot" alt="Landed Cost Voucher" src="{{docs_base_url}}/assets/img/stock/landed-cost-distribution.png">

## 3. Acciones Relacionadas
### 3.1 Añadir Costo en Destino al Recibo de Compra

En ERPNext, al crear el Recibo de Compra (PR), se pueden sumar gastos relacionados al costo en destino en la tabla de "Impuestos y Gastos". Esos gastos deberían ser ingresados como "Total y Valoración" o "Valoración", en el campo "Tomar Impuesto o Gasto para". Aquellos gastos que son pagaderos al mismo Proveedor del cuál se obtienen los productos deberían ser catalogados como "Total y Valoración". En cambio, si los gastos son a pagar a un tercero, deberían ser catalogados como "Valoración". Al enviar el Recibo de Compra, el sistema calculará el costo en destino de todos los productos, teniendo en cuenta esos gastos. El costo en destino será considerado al calcular la Tarifa de Valoración del producto (de acuerdo con los métodos FIFO o Promedio Móvil). 

Pero, en realidad, al crear un Recibo de Compra puede que no conozcamos todos los gastos que se aplicarán para el costo en destino. El transportista puede enviar su factura luego de 1 mes, pero no tiene sentido esperar tanto para generar el Recibo de Compra. Las empresas que importan productos o partes, pagan grandes montos en Derechos Aduaneros. Y, generalmente, la factura del Departamento de Aduana llega despúes de un tiempo. Es en estos casos en que el Voucher de Costo en Destino es de gran utilidad, ya que permite añadir esos gastos adicionales en una fecha posterior y actualizar el costo en destino de los productos comprados. 

### 3.2 ¿Qué sucede al enviar?

1. Se recalcula la Tarifa de Valoración de los productos de acuerdo con el nuevo costo en destino. 

3. Si se utiliza "Inventario Permanente", el sistema realizará registros contables generales para corregir el balance de Existencias Disponibles. Debitará (aumentará) la "cuenta depósito" correspondiente y acreeditará (disminuirá) la **Cuenta de Gastos** mencionada en la tabla de Impuestos y Gastos. Si los productos ya fueron enviados, el Costo de Productos Vendidos (CoGS) ya ha sido registrado de acuerdo con la tarifa de valoración anterior. Es decir, que se volverán a publicar los registros contables generales para todos los registros futuros de productos asociados, para corregir el valor CoGS..

### 4. Temas Relacionados
1. [Viaje de Entrega](/docs/user/manual/en/stock/delivery-trip)
1. [Recibo de Compra](/docs/user/manual/en/stock/purchase-receipt)
