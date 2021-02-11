<!-- add-breadcrumbs -->
# Permitir Sobre Facturación/Envío

Al crear una Nota de Envío, el sistema valida si la cantidad de producto es la misma que en la Orden de Venta. Si la cantidad de producto aumentó, se recibirá un mensaje de validación de sobre-envío o recepción. 

En el caso de ventas, si se quiere enviar más productos que los mencionados en la Orden de Venta, se debe actualizar el campo "Permitir sobre envío o recepción hasta este porcentaje" en la función Producto.

<img alt="Itemised Limit Percentage" class="screenshot" src="{{docs_base_url}}/assets/img/articles/limit-1.png">

Al crear una factura, también se valida el precio del producto de acuerdo con la transacción precedente como Orden de Venta. Esto también aplica al crear Recibo de Compra o Factura de Compra desde Orden de Compra. Al actualizar el campo "Permitir sobre envío o recepción hasta este porcentaje" éste se aplicará a todas las transacciones de compra y venta. 

Por ejemplo, si se pidieron 100 unidades de un producto, y si el porcentaje de sobre recepción es 50, entonces se podrá hacer un Recibo de Compra de hasta 150 unidades. 

El valor global para "Permitir sobre envío o recepción hasta este porcentaje" se actualiza desde las Configuraciones de Inventario. El valor actualizado aquí será aplicable para todos los productos. 

1. Ir a `Inventario > Configuración > Configuraciones de Inventario`

2. Configurar `Porcentaje Límite`.

3. Guardar Configuraciones de Inventario.

<img alt="Item wise Allowance percentage" class="screenshot" src="{{docs_base_url}}/assets/img/articles/limit-2.png">


<!-- markdown -->
