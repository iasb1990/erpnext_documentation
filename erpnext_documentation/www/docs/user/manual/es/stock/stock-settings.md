<!-- add-breadcrumbs -->
# Configuraciones de Existencias

Se pueden establecer configuraciones predeterminadas para las transacciones de existencias desde la página Configuraciones de Existencias.


## 1. Nombre de Producto de acuerdo a

![Stock Settings](/docs/assets/img/stock/stock-settings-1.png)

De forma predeterminada, el nombre del Producto se establece de acuerdo al Código de Producto ingresado. Si se desea que los Productos se nombren de acuerdo con [Nombres en Serie](/docs/user/manual/en/setting-up/settings/naming-series) configurados previamente, seleccionar la opción "Nombres en Serie".


## 2. Configuraciones Predeterminadas

### 2.1 Grupo de Productos Predeterminado
Este será el grupo de productos predeterminado al cual se asignará un nuevo producto. Los Grupos de Productos son últiles para clasificar y configurar propiedades para todo el grupo. Para saber más, visitar la página [Grupo de Productos](/docs/user/manual/en/stock/item-group).

### 2.2 UdM de Existencias Predeterminada
La unidad de medida predeterminada para las existencias es Números, puede ser modificada desde este campo. 

### 2.3 Depósito Predeterminado
Configurar el Depósito predeterminado desde donde se realizan las transacciones de existencias. Este campo será tomado para el Depósito Predeterminado en la función Producto: 
    ![Stock Settings](/docs/assets/img/stock/stock-settings-def.png)

### 2.4 Depósito de Muestras de Reserva 
Este es el Depósito en el cual se almacenan las muestras de reserva. Para saber más visitar [esta página](/docs/user/manual/en/stock/retain-sample-stock).

### 2.5 Método de Valoración Predeterminado
FIFO - Primero que Entra Primero que Sale o Valoración por Promedio Móvil para los productos. El método predeterminado es FIFO. Si se selecciona Promedio Móvil, los Productos nuevos serán valuados de acuerdo al método Promedio Móvil. Se puede cambiar esto al crear nuevos Productos en el formulario de Productos. Una vez que se guarda el producto, el Método de Valoración no puede ser modificado. Leer más [aquí](https://frappe.io/blog/erpnext-features/inventory-valuation-method-fifo-vs-moving-average).

## 3. Porcentaje Límite
Este es el porcentaje en el cual se permite recibir o enviar más que la cantidad pedida. Por ejemplo: si se pidieron 100 unidades, el Proveedor manda 120 y el porcentaje es 10%, entonces solo se pueden recibir 110 unidades. De forma predeterminada este campo está configurado en 0. 

## 4. Mostrar Campo de Código de Barras
Un campo para ingresar detalles de Código de Barras para un producto. Si este campo no está seleccionado, no será visible en el formulario de Producto. 

## 5. Convertir Descripción de Producto para Volver a HTML Base 
Generalmente, las descripciones de producto son copie y pegue de un sitio web o un Word/PDF y contienen muchos estilos integrados. Esto estropea la vista de Impresión de las facturas o cotizaciones. 

Para mejorar esto, se puede hacer click en la casilla "Convertir Descripción de Producto para Volver a HTML Base" en la Configuración de Existencias. Esto permitirá que, cuando se guarden los Productos, sus descripciones serán depuradas. 

Se puede deshabilitar esta propiedad si se desea controlar las descripciones, vistas y permitir que se integren HTML.

## 6. Introducir Automáticamente

![Stock Settings](/docs/assets/img/stock/stock-settings-2.png)

### 6.1 Introducir Automáticamente Listados de Precio si están ausentes 
Al habilitar esto, se introducirá automáticamente un Precio de Producto al Listado de Precios de un Producto, al utilizar dicho Producto en su primera transacción. Este precio será tomado del campo "Tarifa" configurado en la primera transacción con el Producto. El Listado de Precios depende de si se está realizando una transacción de Compra o Venta. 

Observar que, el Precio de Producto será introducido automáticamente solo en la primera transacción en caso de que no hubiese sido ingresado con anterioridad.

Si esta casilla está desactivada, el "Precio de Venta Estándar" configurado para el Producto al crearlo será añadido como Precio de Producto.

### 6.2 Configurar Números de Serie Automáticamente de acuerdo a FIFO 
Los Números de Serie para las existencias se configurarán automáticamente de acuerdo con los Productos ingresados en base al sistema: primero que entra, primero que sale. Los Números de Serie serán configurados automáticamente en transacciones como Facturas de Compra/Venta, Notas de Envío, etc. 

## 7. Permitir Existencias Negativas
Esto permitirá que las existencias de productos se muestren en valores negativos. El uso de esta opción depende del caso de uso. Por ejemplo, los asientos de transacciones de existencias son ingresados a fin de semana o fin de mes. En este caso, las existencias negativas deben ser habilitadas para que se puede continuar con los asientos de transacciones de compra/venta.

## 8. Configurar Cantidades en las Transacciones de acuerdo a los Números de Serie
La cantidad de productos será configurada de acuerdo con los números de serie. Por ejemplo, si el usuario ingresó números de serie como A001, A002 y A003, entonces el sistema establecerá que la cantidad de productos en la transacción es 3.

## 9. Pedido de Material Automático

![Stock Settings](/docs/assets/img/stock/stock-settings-3.png)

### 9.1 Generar Pedido de Materiales cuando las existencias alcancen el Nivel de Pedido

Esta opción es útil si se desea asegurar un abastecimiento constante de materias primas/productos para evitar faltantes. 
Un [Pedido de Materiales](/docs/user/manual/en/stock/material-request) se generará automáticamente cuando las existencias alcancen el nivel de pedido establecido en el [formulario de Producto](/docs/user/manual/en/stock/item#34-automatic-reordering).

### 9.2 Notificar por Email al generar un Pedido de Materiales automático 
Se enviará un email al usuario con el rol de "Gerente de Compras" cuando se genere un Pedido de Materiales automático. 

## 10. Configuraciones de Transferencias entre Depósitos

<img class="screenshot" alt="Delivery Note Material Transfer" src="{{docs_base_url}}/assets/img/stock/inter-warehouse.png">

### 10.1 Habilitar depósito de cliente para transferencias de materiales desde Nota de Envío y Factura de Ventas. 

Esta opción resulta útil cuando se debe presentar una transferencia de materiales como Nota de Envío. Por ejemplo, si hay requerimientos estatutarios donde donde deben aplicarse impuestos a cada transferencia de Materiales. Es más facil administrar una situación como esta en una transacción como Nota de Envío, que en Ingreso de Existencias. 

### 10.2 Habilitar depósito de proveedor para transferencias de materiales desde Recibo de Compra y Factura de Compra 

Similar a la opción anterior, esta opción es útil cuando se debe presentar una transferencia de materiales como Recibo de Compra. 

Para saber más respecto a transferencias de materiales entre depósitos a través de Nota de Envío y Factura de Compra por favor ver el siguiente artículo: [Transferencia de Material desde Nota de Envío y Factura de Compra](/docs/user/manual/en/stock/articles/material-transfer-from-delivery-note)

## 11. Congelar Ingresos de Existencias

Pasada esta fecha, el usuario no tendrá permitido realizar registros de existencias.

![Stock Settings](/docs/assets/img/stock/stock-settings-4.png)

* **Existencias Congeladas Hasta**: Una fecha límite hasta la cual las existencias estarán congeladas. 
* **Congelar Existencias de más de [Días]**: Transcurridos una x cantidad de días, las existencias serán congeladas. Esto se calcula en base a la fecha de creación del producto. 
* **Rol con Permiso para Editar las Existencias Congeladas**: El rol seleccionado en este campo, tendrá permiso para editar las existencias congeladas.

## 12. Identificación de Lote
Configuraciones generales para lotes de existencias a ser identificados por [Nombres en Serie](/docs/user/manual/en/setting-up/settings/naming-series). Se puede anular esto en el DocType de Producto.
