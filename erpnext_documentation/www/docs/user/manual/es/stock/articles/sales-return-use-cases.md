# Administración de Devoluciones de Venta

En el caso de una Devolución de Venta, los ajustes pertinentes relacionados a las existencias y la contabilidad pueden manejarse de muchas formas. Veamos que sucede con las existencias y cuentas, de acuerdo a los ajustes de la Devolución de Venta. 

### Devolución sin Pago

Si un cliente pide la devolución incluso antes de haber procesado el pago, entonces se puede: 

1. Cancelar la Factura de Venta
2. Crear una Devolución de Venta contra la Nota de Envío.

Si las leyes estatutarias no permiten cancelar Facturas de Venta, también se puede crear una Nota de Crédito en base a la Factura de Venta. 

### Factura de Venta Paga - Ajuste vía Nota de Crédito 

Este es un escenario en el cual el cliente compró un producto para el cuál fue enviada una Factura de Venta y, a la vez, pagó. 

1. Crear una Nota de Crédito en base a la Factura de Venta.
2. En la Factura de Venta, seleccionar el campo "Está pago". Asegurarse de que la Cuenta de Pago/Método de Pago está seleccionado en la tabla correspondiente. 
3. Si se desea también devolver productos a través de la Factura de Venta, seleccionar el campo "Actualizar Existencias". 
4. Guardar y Enviar Nota de Crédito.

<img class="screenshot" alt="Create Shareholder" src="/docs/assets/img/stock/sales-return-against-payment.png">

De acuerdo a esta entrada, los productos vendidos serán aceptados nuevamente en el Depósito. Además, el pago recibido del cliente será revertido. 

Luego de la creación de la Nota de Crédito, el Saldo Pendiente de Facturas de Venta se volverá negativo. Esto permitirá luego ajustar esta Factura de Venta (de balance negativo) contra futuras Facturas de Venta pendientes. 

### Factura de Venta impaga -  Nota de Crédito

En el caso de una Devolución de Venta donde el cliente no procesó el pago, se puede simplemente crear una Nota de Crédito. En la creación de la misma, el el balance pendiente de la Factura de Venta se volverá negativo. 

Para ajustar las existencias, se puede crear una Devolución de Ventas contra la Nota de Envío, o, en la Nota de Crédito misma, seleccionar el campo "Actualizar Existencias".