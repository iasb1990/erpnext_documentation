<!-- add-breadcrumbs -->
# Transferencia de Material desde Nota de Envío y Factura de Compra 


En ERPNext, se puede crear una entrada de Transferencia de Material desde un documento de [Ingreso de Existencias](/docs/user/manual/en/stock/stock-entry.html). Sin embargo, hay algunos escenarios en la Transferencia de Materiales donde debe ser presentada como Nota de Envío y Recibo de Compra. 

## Transferencia de Material desde Nota de Envío

### Situaciones

1. Uno de los ejemplos es cuando se transfiere un Material desde un almacen hacia un sitio de proyecto, sin embargo, debe presentárselo como Nota de Envío al cliente. 

2. A su vez, hay requerimientos estatutarios donde se debe aplicar impuestos a cada transferencia de Material. Esta situación es más fácil administrar en una transacción como Nota de Envío que como Ingreso de Existencias. 

Considerando estas situaciones, es que sumó la posibilidad de Transferencia de Material a las Notas de Envío. A continuación se encuentran los pasos a seguir para utilizar Nota de Envío para crear una entrada de Transferencia de Material.  

### Pasos

#### Habilitar Depósito de Cliente

El documento Nota de Envío tiene un campo escondido denominado Depósito de Cliente. Se puede habilitar desde [Configuración de Existencias](/docs/user/manual/en/stock/stock-settings.md) al activar "Permitir Transferencia de Material desde Nota de Envío y Factura de Ventas". 

<img class="screenshot" alt="Delivery Note Material Transfer" src="{{docs_base_url}}/assets/img/stock/customer-warehouse.png">

### Seleccionar Depósitos

Al crear una Nota de Envío para Transferencia de Material, seleccionar Depósito de origen para un producto en el campo Depósito Origen.

En el campo Depósito de Cliente, seleccionar el Depósito al cual el Material va a ser transferido o elegir un depósito objetivo. 

<img class="screenshot" alt="Delivery Note Material Transfer" src="{{docs_base_url}}/assets/img/stock/customer-warehouse-2.png">

Al enviar una Nota de Envío, las existencias del producto serán deducidas desde el "Depósito Origen" y sumadas al "Depósito de Cliente". 

## Transferencia de Material desde Recibo de Compra

### Situaciones

Hay algunos requerimientos estatutarios donde donde deben aplicarse impuestos a cada transferencia de Material. Es por eso que es más facil administrar una situación como esta en una transacción como Recibo de Compra que en Ingreso de Existencias, debido a que no pueden aplicarse impuestos a Ingresos de Existencias. 

A continuación se encuentran los pasos para utilizar un Recibo de Compra para crear una entrada de Transferencia de Material. 

### Pasos

#### Habilitar Depósito de Proveedor

Similar al Depósito de Cliente mencionado más arriba, el primer paso es habilitar el Depósito de Proveedor desde [Configuraciones de Existencias](/docs/user/manual/en/stock/stock-settings.md) como fue mostrado anteriormente. 

<img class="screenshot" alt="Delivery Note Material Transfer" src="{{docs_base_url}}/assets/img/stock/supplier-warehouse-enable.png">

### Seleccionar Depósitos

Al crear un Recibo de Compra para una Transferencia de Material seleccionar, para un producto, el depósito objetivo en el campo Depósito Aceptado. 

En el Depósito del Proveedor, seleccionar un Depósito desde donde será transferido el material.

<img class="screenshot" alt="Delivery Note Material Transfer" src="{{docs_base_url}}/assets/img/stock/supplier-warehouse.png">

Al enviar el Recibo de Compra, las existencias del producto se descontarán del "Depósito del Proveedor" y se sumarán al "Depósito Aceptado". 
