<!-- add-breadcrumbs -->
# Cantidad Proyectada

**La Cantidad Proyectada es el nivel de exitencias que se predice para un Producto en particular de acuerdo con los niveles actuales de existencias y otros requerimientos.**

Es la cantidad de inventario bruto que incluye oferta y demanda en el pasado, que es
realizado como parte del proceso de planificación.

El inventario proyectado es utilizado por el sistema de planificacion para monitorear el punto
de pedido y la cantidad. La Cantidad proyectada es utilizada por el motor
de planificación para monitorear los niveles de existencias mínimas. Estos niveles son 
mantenidos para satisfacer demandas inesperadas. 

Tener un control preciso del inventario proyectado es crucial para determinar
faltantes y calcular la cantidad de pedido adecuada. 

<img class="screenshot" alt="Projected Quantity" src="{{docs_base_url}}/assets/img/stock/projected_quantity.png">

La fórmula para calcular la cantidad proyectada es como se muestra a continuación:

*Cantidad Proyectada = Cantidad Actual + Cantidad Planeada + Cantidad Requerida + Cantidad Pedida - Cantidad Reservada - Cantidad Reservada para Producción - Cantidad Reservada para Subcontratación*

* **Cantidad Real**: Cantidad disponible en el Depósito. Estas son las existencias físicas reales que se tienen. 
* **Cantidad Planeada**: Cantidad para la cual se ha armado una Orden de Trabajo pero esta pendiente de Fabricación. 
* **Cantidad Requerida**: Cantidad Requerida a través de un [Pedido de Material](/docs/user/manual/en/stock/material-request). Se añade al enviar el Pedido de Material y se quita cuando se crea una Orden de Compra/Orden de Trabajo/Registro de Existencias desde la misma de acuerdo con el tipo de Pedido de Material. 
* **Cantidad Pedida**: Cantidad pedida para Compra ([Orden de Compra](/docs/user/manual/en/buying/purchase-order)), pero no recibida a través de un [Recibo de Compra](/docs/user/manual/en/stock/purchase-receipt) o una [Factura de Compra](/docs/user/manual/en/accounts/purchase-invoice). 
* **Cantidad Reservada**: Cantidad pedida para venta por el Cliente ([Orden de Venta](/docs/user/manual/en/selling/sales-order)), pero no enviada (a través de una [Nota de Entrega](/docs/user/manual/en/stock/delivery-note)). Esta cantidad aumenta cuando se envía una Orden de Venta y disminuye cuando se crea y envía una Nota de Entrega o Factura de Compra desde esa Orden de Venta.
* **Cantidad Reservada para Producción**: Las materias primas son reservadas cuando se envía una [Orden de Trabajo](/docs/user/manual/en/manufacturing/work-order) y se reducen cuando las materias primas son transferidas al depósito de Trabajo en Curso a través de un Registro de Inventario.
* **Cantidad Reservada para Subcontratación**: Materias primas reervadas cuando se envía una Orden de Compra de subcontratación. Cuando las materias primas son transferidas al Depósito del Proveedor a través de un Registro de Inventario, esta cantidad de reduce. Para saber más respecto a subcontratación [click aquí](/docs/user/manual/en/manufacturing/subcontracting).

#### Temas Relacionados
1. [Depósito](/docs/user/manual/en/stock/warehouse)
1. [Pedido de Material](/docs/user/manual/en/stock/material-request)
