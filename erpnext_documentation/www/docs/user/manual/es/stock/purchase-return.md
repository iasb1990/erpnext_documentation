<!-- add-breadcrumbs -->
# Devolución de Compra

**Un Producto comprado que se devuelve es conocido como Devolución de Compra.**

Con la función de Devolución de Compra, se puede devolver productos al 
Proveedor. Esto puede suceder por un número de razones como productos defectuosos,
problemas de calidad, comprador que no necesita los productos, etc.

## 1. Prerrequisitos
Antes de crear y utilizar una Devolución de Compra, se aconseja crear lo siguiente: 

* [Producto](/docs/user/manual/en/stock/item)
* [Factura de Compra](/docs/user/manual/en/accounts/purchase-invoice)
    
    O

    [Recibo de Compra](/docs/user/manual/en/stock/purchase-receipt)


## 2. Cómo Crear una Devolución de Compra
1. Primero abrir el Recibo de Compra original, desde el cual el Proveedor envió los Productos.

    <img class="screenshot" alt="Original Purchase Receipt" src="{{docs_base_url}}/assets/img/stock/purchase-return-original-purchase-receipt.png">

1. Luego, hacer click en "Crear > Devolución", lo cuál abrirá un nuevo Recibo de Compra con el campo "Es Devolución" seleccionado, los Productos, Precio e impuestos tendrán números negativos.

    <img class="screenshot" alt="Return Against Purchase Receipt" src="{{docs_base_url}}/assets/img/stock/purchase-return-against-purchase-receipt.png">

1. Al enviar la Devolución de Compra, el sistema disminuirá las existencias en el Depósito mencionado. Para mantener una correcta valoración del inventario, el balance de existencias subirá de acuerdo con el precio de compra original de los productos devueltos.

    <img class="screenshot" alt="Return Stock Ledger" src="{{docs_base_url}}/assets/img/stock/purchase-return-stock-ledger.png">

1. En el Libro Contalbe, la cuenta Existencias Diponibles se acreditará y la cuenta de Existencias Recibidas pero No Facturadas será debitada. 

    <img class="screenshot" alt="Return Stock Ledger" src="{{docs_base_url}}/assets/img/stock/purchase-return-general-ledger.png">

Si se encuentra habilitado el Inventario Permanente, el sistema también realizará registros en la cuenta depósito para sincronizar el balance de la cuenta depósito con el balance de la Cuenta de Inventario.

### 3. Temas Relacionados
1. [Devolución de Venta](/docs/user/manual/en/stock/sales-return)
1. [Inventario Permanente](/docs/user/manual/en/stock/perpetual-inventory)
