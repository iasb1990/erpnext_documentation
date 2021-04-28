<!-- add-breadcrumbs -->
# Corregir Orden de Venta luego de ser validada
La Tarifa y la Cantidad de una Orden de Venta puede ser enmendada luego de haber sido enviada utilizando el botón `Actualizar Productos`.

<img alt="Update Items" class="screenshot" src="{{docs_base_url}}/assets/img/articles/so-update-items.png">

Para actualizar la Tarifa y la Cantidad en una Orden de Venta Enviada, hacer click en el botón `Actualizar Productos`. Al hacer eso aparecerá una ventana de diálogo que permitirá realizar el cambio. 

<img alt="Update Items" class="screenshot" src="{{docs_base_url}}/assets/img/articles/so-update-items-rate-and-qty.gif">

Tener en cuenta las siguientes validaciones y posibilidades de aplicación: 

- La Función de Actualización revisa si la Orden de Venta posee Nota de Envío y Factura de Venta.
- La Cantidad solo puede ser actualizada para Órdenes de Venta que no han sido enviadas o que cuentan con una Nota de Envío Parcial. Para Órdenes de Venta con Notas de Envío completas, la cantidad no puede actualizarse. 
- La Tarifa puede actualizarse para Órdenes de Venta que aún no han sido facturadas o que han sido parcialmente facturadas. Para Órdenes de Venta con Factura de Venta enviada, no puede ser actualizada. 
