<!-- add-breadcrumbs -->
# Devoluciones de Venta

**Un Producto vendido que se devuelve es conocido como Devolución de Venta.**

Que bienes vendidos sean devueltos es algo que sucede comunmente en los negocios. Pueden ser devueltos por el cliente debido a cuestiones de calidad, no entrega en fecha acordada o cualquier otra razón. 

## 1. Prerrequisitos
Antes de crear y utilizar una Devolución de Venta, se aconseja crear lo siguiente: 

* [Producto](/docs/user/manual/en/stock/item)
* [Factura de Venta](/docs/user/manual/en/accounts/sales-invoice)
    
    O

    [Nota de Entrega](/docs/user/manual/en/stock/delivery-note)

## 2. Cómo Crear una Devolución de Venta

1. Primero abrir la Nota de Entrega/Factura de Venta original, desde la cual el Cliente devolvió los Productos.

    <img class="screenshot" alt="Original Delivery Note" src="{{docs_base_url}}/assets/img/stock/sales-return-original-delivery-note.png">

1. Luego, hacer click en "Crear > Devolución de Venta", lo cuál abrirá una nueva Nota de Entrega con el campo "Es Devolución" seleccionado, los Productos, Precio e impuestos tendrán números negativos.

    <img class="screenshot" alt="Return Against Delivery Note" src="{{docs_base_url}}/assets/img/stock/sales-return-against-delivery-note.png">

1. También se puede crear el registro de devolución desde la Factura de Ventas original, para devolver los productos junto con una nota de crédito, hacer click en la opción "Actualizar Existencias" en Factura de Ventas de Devolución. 

    <img class="screenshot" alt="Return Against Sales Invoice" src="{{docs_base_url}}/assets/img/stock/sales-return-against-sales-invoice.png">

1. Al enviar la Nota de Entrega/Factura de Venta de Devolución, el sistema aumentará las existencias en el Depósito mencionado. Para mantener una correcta valoración del inventario, el balance de existencias subirá de acuerdo con el precio de compra original de los productos devueltos.

    <img class="screenshot" alt="Return Stock Ledger" src="{{docs_base_url}}/assets/img/stock/sales-return-stock-ledger.png">

1. En caso de una Factura de Venta de Devolución, la cuenta del Cliente será acreditada y las cuentas de ingresos e impuestos serán debitadas, como se muestra en el Libro Contable.

    <img class="screenshot" alt="Return Stock Ledger" src="{{docs_base_url}}/assets/img/stock/sales-return-general-ledger.png">

Si se encuentra habilitado el Inventario Permanente, el sistema también realizará registros en la cuenta depósito para sincronizar el balance de la cuenta depósito con el balance de la Cuenta de Inventario.  

## 3. Temas Relacionados
1. [Devolución de Compra](/docs/user/manual/en/stock/purchase-return)
1. [Inventario Permanente](/docs/user/manual/en/stock/perpetual-inventory)
