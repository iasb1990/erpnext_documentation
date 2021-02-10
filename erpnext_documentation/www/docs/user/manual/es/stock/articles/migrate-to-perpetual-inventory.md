<!-- add-breadcrumbs -->
# Cambiar a Inventario Permanente

La Valuación de Inventario Permanente se encuentra activado en el sistema de forma predeterminada. 

Para los usuarios que actualmente estén utilizando sistemas de valuación de inventario periódicas y deseen cambiar a sistemas de valuación de inventario permanente, seguir los pasos explicados a continuación. 

### 1. Cómo cambiar a Inventario permanente

1. Para activar el Inventario Permanente, hay que asegurarse que la Cuenta de Existencias Disponibles está sincronizada con el valor de las existencias reales que se encuentran en el Depósito. Para sincronizarla se debe crear un asiento en el libro diario, por la diferencia que exista, con la cuenta de gastos (generalmente utilizada en Factura de Compra) como contrapartida . 

  Por ejemplo, cuando el inventario permanente está desactivado, se debe tener a la cuenta de Gastos (Costo de los Bienes Vendidos) registrada a través de las Facturas de Compra. Al activar el inventario permanente, se debe crear un asiento en el libro diario para mover el valor de las existencias desde la cuenta de gastos hacia la de existencias disponibles. 

  Cr. Cuenta de Gastos ......... XXX
  
  Dr. Cuenta de Existencias Disponibles ... XXX

  También puede funcionar al revés si se selecciona la cuenta de existencias disponibles en la Factura de Compra. 

2. Antes de habilitar el Inventario Permanente, asegurarse que las Cuentas de Existencias están vinculadas al Depósito existente. La cuenta de existencias para un Depósito puede ser configurada en tres niveles.

  * En la función Depósito
  * En la sección Depósito Principal
  * Cuenta Predeterminada de Existencias Disponibles en la configuración de Empresa, si sólo se mantiene una cuenta de Existencias Disponibles para todos los Depósitos.
  * 
3. Asiento de Libro Diario para actualizar la cuenta de Existencias Recibidas pero no Facturadas.

  La cuenta "Existencias Recibidas pero no Facturadas" es una cuenta de ajuste que refleja el valor de las existencias para las cuáles se emitió Recibo de Compra pero todavía no se emitió Factura de Compra. Debería crearse un asiento en el libro diario para actualizar el valor de Recibos de compra pendientes de Facturación en la cuenta "Existencias Recibidas pero no Facturadas".

  Para saber el valor de las existencias recibidas pero no facturadas, puede utilizarse el informe "Productos Recibidos Pendientes de Facturación" en el módulo de Cuentas. .

  Crear un asiento en el Libro Diario de la siguiente forma para actualizar el valor en la cuenta Existencias Recibidas pero no Facturadas.

  Cr. Existencias Recibidas pero no Facturadas ........... XXX
  
  Dr. Cuenta de Gastos .................. XXX

4. Configurar las siguientes cuentas predeterminadas para cada Empresa 

  * Existencias Recibidas pero no Facturadas
  * Cuenta de Ajuste de Existencias
  * Gastos Incluídos en Valuación
  * Centro de Costos
  * Activar Inventario Permanente

5. Ir a: **Inicio > Contabilidad > Empresa**
    
    <img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-1.png">

#### 2. Temas relacionados
1. [Contabilidad de Inventario de Existencias](/docs/user/manual/en/stock/accounting-of-inventory-stock)
1. [Inventario Permanente](/docs/user/manual/en/stock/perpetual-inventory)