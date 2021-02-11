<!-- add-breadcrumbs -->

# Informe de Inventario de Existencias

**Un Informe de Inventario de Existencias es un informe detallado que registra todos los movimientos de existencias de una empresa.**

Las transacciones hacia adentro o hacia afuera relacionadas a Fabricación, Compras, Ventas y Transferencias de Existencias son registradas en el Inventario de Existencias que luego se refleja en el Informe de Inventario de Existencias. 

Refleja la cantidad y el valor de las existencias **enviadas, recibidas, o transferidas** junto con los productos en inventario y sus detalles de depósito.

Puede ser referido cuando está habilitado el sistema de **Inventario Permanente**, ya que este informe refleja la historia de todas las transacciones de existencias. Presenta una visión más detallada de las transacciones de existencias.

## Atributos del Informe de Inventario de Existencias

* **Precio de Ingreso**: Refleja el valor real de las existencias, al cuál fueron traídas a inventario. 
Refleja el mismo valor ingresado en el campo *Precio* del documento.

* **Balance de Valor**: Representa el valor total de las existencias remanentes en inventorio. Es el producto de la Tarifa de Valoración y el Cantidad en Balance de un producto. 

* **Tarifa de Valoración**: Se calcula de acuerdo con el método de valoración seleccionado.

Aquí es como el Informe de Inventario de Existencias representa un **Entrada de Inventario** de tipo *Recepción de Material*.

![Stock Ledger Report](/docs/assets/img/stock/stock-ledger.png)

Refleja un producto **Silla** de cantidad *1000 unidades* con un Precio de Ingreso (Precio Básico) de *3000* recibido en el depósito *Tiendas - L* además de calcular la Tarifa de Valoración y el Balance de Valor. 

Se puede hacer click en **Voucher #** para abrir el documento desde donde fue creada esta transacción. 

Los Inventarios de Existencias son generados desde las siguientes transacciones:

-   Factura de Venta, Factura de Compra (con *Actualizar Existencias* habilitado)
-   Nota de Envío
-   Recibo de Compra
-   Entrada de Inventario
-   Conciliación de Inventario

Se pueden añadir campos de los Tipos de Documento previamente mencionados, haciendo click en Menú > Añadir Columna.
