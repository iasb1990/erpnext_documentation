<!-- add-breadcrumbs -->
# Enmendar Orden de Compra luego de Envío
Luego de haber sido enviada la Orden de Compra, el Precio y la Cantidad establecidos en la misma, pueden ser enmendados utilizando el botón "Actualizar Productos". 

<img alt="Update Items" class="screenshot" src="{{docs_base_url}}/assets/img/articles/po-update-items.png">

Para Actualizar Precio y Cantidad en una Orden de Compra Enviada, hacer click en el botón "Actualizar Producto". Aparecerá una ventana emergente que permitirá realizar el cambio. 

<img alt="Update Items" class="screenshot" src="{{docs_base_url}}/assets/img/articles/po-update-items-rate-and-qty.gif">

Por favor, tener en cuenta la siguientes validaciones y casos de uso: 

- Las Funciones de Actualización controlan si la Orden de Compra tiene Recibo de Compra y Factura de Compra. 
- La Cantidad puede ser actualizada para una Orden de Compra no recibida o parcialmente recibida. No puede actualizarse para Orden de Compra con un Recibo de Compra completo. 
- El Precio puede actualizarse para Órdenes de Compra no facturadas o parcialmente facturadas. No puede actualizarse para Órdenes de Compra con una Factura de Compra ya enviada. 
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTk3Njc0ODYzXX0=
-->