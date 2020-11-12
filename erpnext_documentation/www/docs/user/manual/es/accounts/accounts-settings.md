<!-- add-breadcrumbs -->
# Configuración de cuentas

ERPNext da la posibilidad de configurar y restringir ciertas acciones dentro del módulo de contabilidad.

![Account Settings]({{docs_base_url}}/assets/img/accounts/account-settings.png)

## 1. Cuentas congeladas hasta
Se congelan las transacciones hasta la fecha especificada. Nadie puede crear/modificar entradas contables, salvo el rol seleccionado a continuación.

## 2. Rol que permite definir cuentas congeladas y editar asientos congelados
Los usuarios con este rol tienen permiso para congelar cuentas y crear/modificar entradas contables contra cuentas congeladas.

## 3. Determine Address Tax Category From
[Tax category](/docs/user/manual/en/accounts/tax-category) can be set on Addresses. An address can be Shipping or Billing address. Set which addres to select when applying Tax Category.

## 4. Porcentaje permitido de sobrefacturaión
Porcentaje por el cual se puede sobrefacturar transacciones. Por ejemplo, si el valor de la orden es de $100 por un producto y el porcentaje especificado en este campo es de 10%, entonces está permitido facturar con un precio de $110.

## 5. Controlador de créditos
Aquí se selecciona el rol que tiene permitido crear transacciones que exceden el límite de crédito establecido. El límite de crédito puede determinarse por cliente.

## 6. Comprobar número de factura único por proveedor
Al tildar esta opción no se permitirá la creación de facturas de compra con el mismo 'Factura de proveedor No.'. Esto es útil para evitar entradas duplicadas. 

## 7. Realizar pago mediante asiento contable
Al tildar esta opción, si un usuario realiza un pago desde una factura, el sistema generará un asiento contable en lugar de una entrada de pago.

## 8. Desvinculación de pago en la cancelación de la factura
Al tildar esta opción, el sistema desvinculará el pago contra la factura cancelada. Por defecto, si una entrada de pago es validada, la factura vinculada no puede ser cancelada hasta que la entrada de pago sea igualmente cancelada. Al desvincularse, es posible cancelar y corregir las facturas. Por su parte, los pagos quedan desvinculados y son considerados pagos adelantados.

## 9. Desvinculación de pago adelantado en la cancelación de la orden
Similar a la opción anterior,esta configuración desvincula cualquier pago adelantado hecho sobre ordenes de venta o de compra. 


## 10. Entrada automática de depreciación de bienes
Cuando esta opción está tildada, se creará automáticamente una entrada contable por depreciación de bienes en la primera fecha especificada. Por ejemplo, se puede programar la creación de una entrada de depreciación anual por los próximos 3 o 4 años dependiendo del Number of Depreciations Booked especificado en el master de bienes. Para más detalles, visitar la página [Depreciación de bienes](/docs/user/manual/en/asset/asset-depreciation).

## 11. Permitir centro de costo en entrada de cuenta de balance
Si esta opción está tildada, se podrá etiquetar en la Hoja de balance entradas hechas contra Centro de costos. Por defecto el Centro de costos está sólo disponible para cuentas de ganancia o pérdida.

## 12. Añadir automáticamente Impuestos y cargos desde la Plantilla de impuestos
Habilitando esta opción se completará automáticamente la tabla de Impuestos de las transacciones con los valores correspondientes según la [Plantilla de impuestos](/docs/user/manual/es/accounts/item-tax-template) del Producto seleccionado.

## 13. Traer automáticamente Términos de pago
Habilitar esta configuración hará que se traigan automáticamente los Términos de pago del Proveedor. 

## 14. Ajustes de impresión

![Account Settings]({{docs_base_url}}/assets/img/accounts/account-settings-1.png)

* **Mostrar impuesto inclusivo en la impresión**: Los impuestos aplicados serán mostrados en la vista de impresión.
* **Mostrar cronograma de pago en la impresión**: El cronograma de pagos generado por los [Términos de pago](/docs/user/manual/en/accounts/payment-terms) será visible en la impresión.

## 15. Permitir Tipos de Cambio Obsoletos
Esta opción debería estar destildada si se desea verificar la validez del tipo de cambio en transacciones de exportación. Si no está tildada, el campo Tipo de cambio será de sólo lectura.

Stale Days is the number of days to use when deciding if a Currency Exchange record is stale. This is valid when 'Allow Stale Rates' is **disabled**. So, if the Stale Days is set as 10, stale rates that are 10 days will be allowed. If Allow Stale Rates is enabled, there is no time limit on the age of stale rates.

If stale rates are enabled, the order of fetching is:

* Latest rate from Currency Exchange form
* If no Currency Exchange is found latest rate as per market is fetched automatically

If stale rates are disabled, the order of fetching is:

* Latest rate from Currency Exchange form upto number of days set in 'Stale Days'
* If no Currency Exchange is found Latest rate as per market is fetched automatically


## 16. Use Custom Cash Flow Format
You may choose to use Custom Cash Flow Formats to customize what the Cash Flow report looks like. To know more, [visit this page](/docs/user/manual/en/accounts/articles/how-to-customise-cash-flow-report).
