<!-- add-breadcrumbs -->
# Vendedores en Operaciones de Venta

En ERPNext, la función de Vendedores se configura en un [esquema de árbol](/docs/user/manual/en/setting-up/articles/managing-tree-structure-masters.html). Los Vendedores pueden ser seleccionados en todas las operaciones de venta.

Los Vendedores también pueden actualizarse en la función de Clientes. Al seleccionar un cliente en las transacciones, los Vendedores actualizados en el Cliente serán tomados para las operaciones de venta.

<img class="screenshot" alt="Sales Person Customer" src="{{docs_base_url}}/assets/img/articles/sales-person-transaction-1.png">

#### Contribución del Vendedor

Si dos o más vendedores están trabajando de forma conjunta en una orden, debe establecerse la contribución (%) de cada uno.

<img class="screenshot" alt="Sales Person Order" src="{{docs_base_url}}/assets/img/articles/sales-person-transaction-2.png">

Al guardar la transacción, de acuerdo al Total Neto y la Contribución (%) se calculará la`Contribución al Total Neto` para cada Vendedor.

<div class=well> El total de % de Contribución para todos los Vendedores debe ser del 100%. Si se selecciona solo un Vendedor, entonces el % de Contribución será 100%.</div>

#### Informe de Transacciones del Vendedor

Para ver este informe ir a:

`Comercialización > Informes Principales > Resumen de Transacciones del Vendedor

Este informe puede generarse basado en Orden de Venta, Nota de Envío y Factura de Venta. Mostrará el monto toal de venta realizado por un empleado. 

<img class="screenshot" alt="Sales Person Report" src="{{docs_base_url}}/assets/img/articles/sales-person-transaction-3.png">

#### Comisión del Vendedor

ERPNext solo muestra el total de venta realizado por un Vendedor. Si se le ofrece comisión a dicho Vendedor debería añadirse a los Vendedores como Socios Comerciales en ERPNext. Para Socios Comerciales se puede definir la Comisión (%). Al seleccionar Socios Comerciales en Operaciones de Venta, de acuerdo al Total Neto, también se calcula el Monto de la Comisión. Se pueden ver los informes de comisión de Socios Comerciales en:

`Cuentas > Informes Principales > Comisiones de Socios Comerciales