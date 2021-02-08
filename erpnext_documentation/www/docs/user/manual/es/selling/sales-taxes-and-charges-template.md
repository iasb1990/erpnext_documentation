<!-- add-breadcrumbs -->
# Plantilla de Impuestos y Gastos

**Los Impuestos y Gastos de Venta pueden ser aplicados a cualquier producto que se venda.**

Las plantillas creadas desde este formulario pueden ser utilizadas en Órdenes de Venta y Facturas de Venta. 

Si se quiere usar Cuentas Fiscales en la plantilla de impuestos debe configurarse el Tipo de Cuenta como "Fiscal" para esa cuenta particular. La forma en que ERPNext configura los impuestos es a través de plantillas. Otros tipos de gastos que puedan 
aplicarse a las facturas (como envío, seguro, etc) también pueden configurarse como impuestos. 

Para saber más respecto a la configuración de impuestos visitar [esta página](/docs/user/manual/en/setting-up/setting-up-taxes).

Para acceder a la Plantilla de Impuestos y Gastos ir a: 
> Inicio > Comercialización > Configuración > Plantilla de Impuestos y Gastos

Para saber más respecto a la configuración de impuestos visitar [esta página](/docs/user/manual/en/setting-up/setting-up-taxes)

## 1. Como añadir Impuestos/Gastos de Venta a través de una plantilla
Antes de crear una nueva plantilla, es importante saber que ya hay plantillas creadas para muchos de los impuestos comunmente usados. 

1. Ir al listado de Plantilla de Impuestos y Gastos y hacer click en Nueva.
2. Ingresar el nombre del Impuesto.
3. En "tipo", configurar sobre qué va a ser calculado el impuesto y su tasa. Hay cinco opciones en esta sección según las cuáles el impuesto puede ser calculado. 
  1. Real: Ingresar el monto del gasto.
  2. Sobre Total Neto: Sobre el Total Neto de todos los productos.
  3. Sobre el Monto de la Fila Anterior: Esto es para generar gastos compuestos. Por ejemplo, aplicar un impuesto sobre el monto al cual ya se le aplicó otro impuesto en la fila anterior.
  4. Sobre el Total de la Fila Anterior: Igual que lo explicado anteriormente pero aplicado al total de la factura y no solo al monto de un producto.
  5. Sobre Cantidad de Producto: El impuesto será calculado como Tasa del Impuesto * Cantidad de Producto. Por ejemplo, si la tasa del impuesto es 2% y el número de productos es 1, entonces la Tarifa del Impuesto será 4, si el número de productos es 5, la Tarifa será 10, y así sucesivamente.
4. Seleccionar una cuenta principal que ya tenga las tasas impositivas predeterminadas, o crearla.
5. Si se selecciona aplicar predeterminadamente, se aplicará esta plantilla de forma predeterminada para las nuevas transacciones de Venta. 
6. Guardar.
  ![Impuestos de Venta](/docs/assets/img/selling/sales-taxes.png)


## 2. Características
### 2.1 Tabla de Impuestos y Gastos de Venta

* **Considerar el Impuesto o Gasto para**: Total - por el total de todos los productos. Valuación - por cada producto. Valuación y total - se aplica el impuesto/gasto a los dos. [Ver este artículo](/docs/user/manual/en/accounts/articles/what-is-the-differences-of-total-and-valuation-in-tax-and-charges) para entender la diferencia.

* **Fila de Referencia #**: Si el impuesto esta basado en el "Total de la Fila Anterior" se puede seleccionar el número de fila que será usado de base para este cálculo (la configuración predeterminada es la fila anterior).
    ![Tabla de Impuestos de Venta](/docs/assets/img/selling/sales-taxes-table.png)

* **¿Está el impuesto incluido en la tarifa básica?**: Si esta casilla está seleccionada, se considerará que el importe del impuesto ya está incluido Precio Impreso/Monto Impreso en la tabla de productos de una transacción. Esto resulta útil cuando se le quiere informar al cliente el precio con impuestos incluidos. Para contabilizar los precios con impuestos incluídos, el sistema calcula el Monto Neto deduciendo el monto de impuesto a aplicar y luego calculando el impuesto sobre el mismo.  
* **Cuenta Principal:** La cuenta bajo la cual se registrará este impuesto. Si se selecciona VAT u otras de las cuentas ya existentes, la tarifa será completada automáticamente. 
* **Centro de Costos:** Si el impuesto/gasto es un ingreso (como envío) o gasto, debe ser contabilizado en relación a un Centro de Costos. 
* **Descripción:** Description of the tax (that will be printed in invoices/quotes).
* **Tasa:** La tasa del impuesto, por ejemplo:14 = 14%.
* **Monto:** El monto de impuesto a ser aplicado, por ejemplo: 100.00 = â‚¹100.

Las tasas impositivas que se defininan en la planitlla serán la tasa común para todos los Productos. Si hay Productos que deban tener diferentes tasas, se puede desactivar la tasa estándar configurando una Plantilla de Impuesto de Producto para el Producto o Grupo de Productos. 

### 3. Temas relacionados
1. [Orden de Venta](/docs/user/manual/en/selling/sales-order)
1. [Configuración de Venta](/docs/user/manual/en/selling/selling-settings)

{next}
