<!-- add-breadcrumbs -->
# Proveedor

**Los Proveedores son empresas o individuos que proveen productos o servicios.**

Para acceder al listado de Proveedor ir a:
> Inicio > Compras > Proveedor > Proveedor

## 1. Creación de un Proveedor
1. Ir al listado de Proveedores y hacer click en Nuevo. 
2. Ingresar un nombre para el proveedor.
4. Seleccionar el grupo de proveedores como Farmaceúticos, Hardware, etc. 
5. Guardar.
    <img class="screenshot" alt="Supplier Master" src="{{docs_base_url}}/assets/img/buying/supplier-master.png">

Las opciones Avisar en Solicitudes de Cotización, Avisar en Ordenes de Compra, Evitar Solicitudes de Cotización y Evitar Ordenes de Compra estarán disponibles una vez que se cree la [Calificación del Proveedor](/docs/user/manual/es/buying/supplier-scorecard) y se realicen transacciones.

## 2. Características 

En transacciones futuras, los campos se completarán automáticamente si se configuran las opciones predeterminadas como: Cuenta Bancaria Predeterminada, Plantilla Predeterminada de Condiciones de Pago, etc. en la sección Proveedor.

### 2.1 Detalles de Impuestos

* **País**: Si el Proveedor es de otro país, se lo puede cambiar aquí.
* **CUIT/CUIL**: Número de Identificación Fiscal del Proveedor.
* **Categoría de impuestos**: Esto está vinculado a [Reglas fiscales](/docs/user/manual/es/accounts/tax-rule). Si se configura aquí una Categoría de impuestos, cuando se seleccione este proveedor, se aplicará la Plantilla de Impuestos (Compra) correspondiente. Esta plantilla está vinculada a las Reglas Fiscales y éstas últimas, a una Categoría de impuestos. La Categoría de impuestos puede utilizarse para agrupar proveedores a los cuáles se aplicarán los mismos impuestos. Por ejemplo: Gobierno, Comercial, etc. 
* **Categoría de Retención de Impuestos**: Al configurar una categoría aquí, la misma será ingresada en la [Factura de Compra](/docs/user/manual/es/accounts/purchase-invoice). Para más información, visitar la página [Categoría de Retención de Impuestos](/docs/user/manual/es/accounts/tax-withholding-category).
* **Deshabilitado**: Deshabilita al Proveedor, el cual no será mostrado en la Lista de Proveedores.
* **Es Transportista**: Si el proveedor está vendiendo servicios de transporte, hacer click en esta casilla. 
* **Es un Proveedor Interno**: Si el proveedor es de una empresa hermana o principal/subsidiaria, hacer click en este campo y seleccionar la empresa que representa.


### 2.2 Permitir la creación de Factura de Compra sin Orden de Compra y Recibo de Compra 

Si la opción "Se requiere Orden de compra para la creación de Facturas y Recibos de compra" o "Se requiere Recibo de compra para la creación de Facturas de compra" están configuradas como "Si", en las [Configuración de Compras](/docs/user/manual/es/buying/buying-settings), esto puede cambiarse para un proveedor en particular tildando "Permitir la creación de facturas de compra sin orden de compra" o "Permitir la creación de facturas de compra sin recibo de compra" en el Proveedor. 

<img class="screenshot" alt="Supplier Master" src="{{docs_base_url}}/assets/img/buying/supplier-po-pr-required.png">

### 2.3 Divisa y Lista de Precios
**Moneda de Facturación**: La moneda del proveedor puede ser diferente que la del comprador. Si se elige un proveedor en Dólares, entonces la moneda será configurada como dólares y se mostrará la tasa de cambio para futuras transacciones de compra.

![Supplier Currency](/docs/assets/img/buying/supplier-currency.gif)

Cada Proveedor puede tener una **Lista de Precios** predeterminada de forma que cada vez que se compre un nuevo producto de este proveedor a precios diferentes, se actualizará la lista de precios asociada a dicho proveedor. Dentro de la lista de precios se encuentra el precio de producto, se pueden ver los precios en Compras > Productos y Precio > Precio de Producto.

Si se selecciona a este proveedor en particular, entonces, en transacciones de compra se obtendrá esta Lista de Precios. 

### 2.4 Límite de Crédito

* **Plantilla de Términos de Pago Predeterminados**: Si se configura aquí una Plantilla de Términos de Pago, la misma será seleccionada automáticamente en futuras transacciones de compra. 
* **Bloquear Proveedor**: Se puede bloquear facturas, pagos o ambos de un proveedor hasta una fecha específica. Elegir el "Tipo de Pausa", si no se selecciona un tipo de pausa, ERPNext lo configurará como "Todos". Cuando un proveedor está bloqueado, su estado será mostrado como "En Pausa". 

    Los tipos de pausa son como se muestra a continuación:
    - Facturas: ERPNext no permitirá que se creen Facturas de Compra u Ordenes de Compra para el proveedor. 
    - Pagos: ERPNext no permitirá que se creen Entradas de Pago para el Proveedor.
    - Todos: ERPNext aplicará ambos tipos de pausa mencionados anteriormente.

    Si no se configura una fecha de finalización, ERPNext tendrá al Proveedor en pausa **indefinidamente**.

### 2.5 Cuentas de Pago Predeterminadas
Ingresar la cuenta predeterminada desde la cual se pagarán las facturas de este proveedor. Sumar más filas para más empresas, se puede seleccionar solo una cuenta por empresa. 

Se puede **integrar** a un proveedor con una cuenta. Para todos los Proveedores, la cuenta "Acreedor" está configurada como la cuenta de pago predeterminada. Cuando se crea una Factura de Compra, el pago hacia el proveedor se registra contra la cuenta "Acreedores".

Si se desea configurar la cuenta de pago para el Proveedor, primero se debe crear esa cuenta en el Plan de Cuentas, y luego seleccionar esa Cuenta de Pago en la función Proveedor.

<img class="screenshot" alt="Supplier Master" src="{{docs_base_url}}/assets/img/buying/supplier-payable-account.png">

Si no se desea configurar la cuenta de pago, y operar con la cuenta predeterminada "Acreedores", entonces no se deben actualizar los valores en la tabla de Cuentas Predeterminadas de Proveedor. 

> Consejo: La Cuenta de Pago Predeterminada está configurada en la función Empresa. Si se desea configurar otra cuenta predeterminada que no sea la Cuenta Acreedores, ir a la función Empresa y configurar esa cuenta como "Cuenta de Pago Predeterminada". 

Dependiendo del [plan](https://erpnext.com/pricing), se podrán ingresar muchas empresas en la cuenta ERPNext. Un Proveedor puede ser utilizado en muchas empresas. En este caso se deberá seleccionar una Cuenta de Pago para el Proveedor de acuerdo a la empresa en la tabla "Cuentas de Pago Predeterminadas", es decir, sumar muchsa filas.  

### 2.6 Más Información
En esta sección, se puede ingresar el sitio web del proveedor y cualquier otro detalle adicional acerca del mismo. Si se congela un proveedor usando la opción "Está Congelado", los registros contables para el mismo serán congelados. En este caso, el único usuario cuyos registros podrán pasar por encima la restricción, es aquel con el "Rol con Permiso a Configurar Cuentas Congeladas y Editar Registros Congelados" en Contabilidad > Configuraciones > Configuraciones Contables. Esto resulta útil cuando el nombre del proveedor o los detalles del banco deben ser enmendados.

* **Idioma de Impresión**: El idioma en el cuál se imprime el documento.

### 2.7 Dirección y Contacto
En ERPNext Los Contactos y Direcciones son almacenados de forma separada a fin de poder crear muchos Contactos y Direcciones para un Proveedor. Una vez que el Proveedor es guardado, aparecerá la opción para crear Contacto y Dirección para ese Proveedor.  

<img class="screenshot" alt="Supplier Master" src="{{docs_base_url}}/assets/img/buying/supplier-new-address-contact.png">

> Consejo: al seleccionar un Proveedor en una transacción, serán traídos los datos del contecto vinculado al mismo que tenga tildada la opción "Es el contacto principal".

### 2.8 Luego de Guardar
Una vez completados todos los detalles necesarios, guardar el documento. Luego de guardar, aparecerán en el Tablero opciones para crear lo siguiente: 

* **Pedido de Cotización**: Un Pedido de Cotización para este proveedor.
* **Cotización de Proveedor**: Cualquier cotización que el proveedor haya enviado y haya sido enviada al sistema. 
* **Orden de Compra**: Órdenes de Compra que se hayan hecho para este proveedor. 
* **Recibo de Compra**: Recibos de Compra entregados por este proveedor y que se han guardado en el sistema. 
* **Factura de Compra**: Facturas de Compra que se han emitido para este proveedor
* **Registro de Pago**: Registros de Pago para las Facturas de Compra hechas a este proveedor.
* **Normas de Pago**: Cualquier Norma de Pago vinculada con este proveedor. Ver la sección _2.2 Moneda y Listado de Precios_ para entender mejor su funcionamiento.

![Supplier Save](/docs/assets/img/buying/supplier-save.png)

Al hacer click en el botón Ver, se pueden ver directamente el Libro Contable o las Cuentas por Pagar para este proveedor. 

Hay un botón para "Enviar Recordatorio de Actualización GST" al proveedor. Pero primero se debe haber configurado una [cuenta de mail](/docs/user/manual/en/setting-up/email/email-account) predeterminada.


### 3. Temas Relacionados
1. [Cotización de Proveedor](/docs/user/manual/en/buying/supplier-quotation)
1. [Sistema de Puntuación de Proveedores](/docs/user/manual/en/buying/supplier-scorecard)
1. [Mantener el Código de Producto del Proveedor en la Función Producto](/docs/user/manual/en/buying/articles/maintaining-suppliers-part-no-in-item)

{next}
