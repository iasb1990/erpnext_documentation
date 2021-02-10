<!-- add-breadcrumbs -->
# Contabilidad de Existencias en Inventario

El valor del inventario disponible es tratado como un Activo corriente en el [Plan de Cuentas](/docs/user/manual/en/accounts/chart-of-accounts) de la empresa. Para preparar un Balance General, se deben realizar los asientos contables para esos activos. Generalmente hay dos métodos para contabilizar el inventario.  

## 1. Inventario Automático/Permanente

En este proceso, para cada transacción de existencias, el sistema realiza 
asientos contables a fin de sincronizar el balance de existencias y el balance contable. Esta es la 
configuración predeterminada para cuentas nuevas en ERPNext. De forma predeterminada, el Inventario Permanente está habilitado en la [Empresa](/docs/user/manual/en/setting-up/company-setup#23-stock-settings).

Cuando se compran y reciben productos, esos productos son registrados en los activos de la empresa
(existencias disponibles). Cuando se venden y envían esos productos, se registra
un gasto (Costo de Bienes Vendidos) igual al costo de entrega de los bienes. 
Luego de cada transacción de existencias, se crean registros en el Libro Mayor. Como resultado
de lo anterior, el valor de la Cuenta de Inventario siempre coincide con el balance de las cuentas relevantes. 
Esto ayuda a mejorar la exactitud del balance general y del Estado de
resultados.

Para ver asientos contables para una transacción de existencias en particular,
[click aquí]

### 1.2 Ventajas del Inventario Permanente

El Inventario Permanente facilita la administración de los valores de activos y gastos(/docs/user/manual/en/stock/perpetual-inventory) de la empresa, manteniendo un alto nivel de precisión. Los balances de existencias siempre estarán sincronizados con los balances de cuentas relevantes, de esa forma no es necesario realizar asientos manuales periódicos para balancearlas. 

En el caso de nuevas transacciones de existencias con fechas anteriores o cancelaciones/enmiendas de transacciones existentes, todas las futuras entradas al Inventario de Existencias y al Libro Mayor serán recalculadas para 
todos los productos de esa transacción. Lo mismo se aplica 
si se añaden costos a los Recibos de Compra enviados, a través 
del Voucher de Costo de Envío. 

> Observación: El Inventario Permanente depende exclusivamente de la valuación del producto. 
Por ende, es necesario tener cuidado al introducir las valuaciones en cualquier transacción 
de ingreso de existencias, como Recibo de Compra, Recibo de Material o 
Fabricación/Productos que cambian su empaquetado.

* * *

## 2. Inventario Periódico

En este método, los asientos contables deben ser creados en forma manual a fin de sincronizar el balance de existencias con el de las cuentas relevantes. El sistema no crea
asientos contables de forma automática para activos al realizar compras de material 
o ventas. 

En un ejericio contable, cuando se compran y reciben productos, se registra un gasto 
en el sistema contable. Luego, se venden y envían algunos de estos productos.

Al final de un ejercicio contable, el valor total de productos a ser vendidos 
debe estar registrado como activo de la empresa, normalmente conocido como existencias disponibles. 

La diferencia entre el valor de los productos que esperan ser vendidos y 
el valor de las existencias disponibles de períodos anteriores puede ser positiva o negativa. Si 
es positiva, este valor se elimina de gastos (Costo de Bienes Vendidos) y se 
agrega a activos (existencias disponibles). Si es negativa, se realiza el
asiento inverso. 

Este proceso completo se denomina **Inventario Periódico**.

Si ya se posee un usuario que se encuentra utilizando Inventario Periódico y desea utilizar Inventario 
Permanente, se deben seguir [algunos pasos](/docs/user/manual/en/stock/articles/migrate-to-perpetual-inventory) para realizar el cambio. 

### 3. Temas relacionados
1. [Inventario Permanente](/docs/user/manual/en/stock/perpetual-inventory)
1. [Cambiar a Inventario Permanente](/docs/user/manual/en/stock/articles/migrate-to-perpetual-inventory)