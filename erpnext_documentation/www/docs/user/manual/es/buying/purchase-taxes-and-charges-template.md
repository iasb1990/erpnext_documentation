<!-- add-breadcrumbs -->
# Plantilla de Impuestos (Compra)

**Los Impuestos y Gastos de Venta pueden ser aplicados a cualquier producto que se compre.**

La Plantilla de Impuestos y Gastos de Compra es similar a la Plantilla de Impuestos y Gastos de Venta. Las plantillas creadas desde este formulario pueden ser utilizadas en Órdenes de Compra y Facturas de Compra para registros internos.

Si se quiere usar Cuentas Fiscales en la plantilla de impuestos debe configurarse el Tipo de Cuenta como "Fiscal" para esa cuenta particular.

Para acceder a la Plantilla de Impuestos y Gastos ir a: 
> Inicio > Adquisiciones > Configuración > Plantilla de Impuestos y Gastos de Compra

## 1. Como añadir Impuestos/Gastos de Compra a través de una plantilla
Antes de crear una nueva plantilla, es importante saber que ya hay plantillas creadas para muchos de los impuestos comunmente usados.

1. Click en Nuevo
2. Ingresar el nombre del Impuesto.
3. En "tipo", configurar sobre qué va a ser calculado el impuesto y su tasa. Hay cuatro opciones en esta sección según las cuáles el impuesto puede ser calculado.
  1. Real: Sobre el monto del producto
  1. Sobre Total Neto: Sobre el Total Neto de todos los productos.
  1. Sobre el Monto de la Fila Anterior: Esto es para generar gastos compuestos. Por ejemplo, aplicar un impuesto sobre el monto al cual ya se le aplicó otro impuesto en la fila anterior. 
  1. Sobre el Total de la Fila Anterior: Igual que lo explicado anteriormente pero aplicado al total de la factura y no solo al monto de un producto.
4. Seleccionar una cuenta principal que ya tenga las tasas impositivas predeterminadas, o crearla.
5. Si se selecciona aplicar predeterminadamente, se aplicará esta plantilla de forma predeterminada para las nuevas transacciones de Compra.
6. Guardar.
<img class="screenshot" alt="Purchase taxes" src="{{docs_base_url}}/assets/img/buying/purchase-taxes.png">


## 2. Características
### 2.1 Tabla de Impuestos y Gastos de Venta

* **Considerar el Impuesto o Gasto para**: Total - por el total de todos los productos. Valuación - por cada producto. Valuación y total - se aplica el impuesto/gasto a los dos [Ver este artículo](/docs/user/manual/en/accounts/articles/what-is-the-differences-of-total-and-valuation-in-tax-and-charges) para entender la diferencia.
* **Add or Deduct:** Whether you want to add or deduct the tax from the item.

* **Fila de Referencia**: Si el impuesto esta basado en el "Total de la Fila Anterior" se puede seleccionar el número de fila que será usado de base para este cálculo (la configuración predeterminada es la fila anterior).
   <img class="screenshot" alt="Purchase taxes table" src="{{docs_base_url}}/assets/img/buying/purchase-taxes-table.png">

* **¿Está el impuesto incluido en la tarifa básica?**: Si esta casilla está seleccionada, se considerará que el importe del impuesto ya está incluido Precio Impreso/Monto Impreso.
* **Cuenta Principal:** La cuenta bajo la cual se registrará este impuesto. Si se selecciona VAT u otras de las cuentas ya existentes, la tarifa será completada automáticamente. 
* **Centro de Costos:** Si el impuesto/gasto es un ingreso (como envío) o gasto, debe ser contabilizado en relación a un Centro de Costos.
* **Descripción:** Description of the tax (that will be printed in invoices/quotes).
* **Tasa:** La tasa del impuesto, por ejemplo:14 = 14%.
* **Monto:** El monto de impuesto a ser aplicado, por ejemplo: 100.00 = â‚¹100.


### 3. Temas relacionados
1. [Orden de Compra](/docs/user/manual/en/buying/purchase-order)
1. [Configuraciones de Compra](/docs/user/manual/en/buying/buying-settings)

{next}
