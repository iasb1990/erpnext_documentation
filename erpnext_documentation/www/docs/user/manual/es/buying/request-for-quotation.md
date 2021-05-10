<!-- add-breadcrumbs -->
# Solicitud de Cotización

**Un Pedido de Cotización es un deocumento que envía una empresa a uno o más proveedores pidiendo una cotización para determinados productos.**

![Buying Flow](/docs/assets/img/buying/buying_flow_rfq.png)

Para acceder a Pedido de Cotización ir a:
> Inicio > Adquisiciones > Compras > Pedido de Cotización

## 1. Prerrequisitos
Antes de crear y utilizar un Pedido de Cotización, es aconsejable crear lo siguiente:

* [Proveedor](/docs/user/manual/en/buying/supplier)
* [Producto](/docs/user/manual/en/stock/item)

## 2. Como Crear un Pedido de Cotización
1. Ir al listado de Pedido de Cotización y hacer click en Nuevo.
2. Ingresar la Fecha
3. Elegir el proveedor al cuál se enviará el Pedido de Cotización.
4. En la siguiente tabla, ingresar los productos, la cantidad y el depósito de destino a donde se enviarán los productos.
1. El Depósito puede dejarse en blanco si el campo "Mantener Existencias" esta deshabilitado para el producto.
5. Guardar y Enviar.

Un Pedido de Cotización también puede crearse desde un Pedido de Material enviado. Una vez que se crea el Pedido de Cotización, se puede imprimir y enviar el PDF que tendrá todos los detalles relevantes para el Pedido de Cotización y recibir la respuesta via mail. También se puede recibir la respuesta (Cotización del Proveedor) desde el mismo ERPNext, ver sección _3.1 Cotización de Proveedor por Usuario_. Sin embargo, si se trata de una gran cantidad de productos, el proveedor puede estar más cómodo con una planilla de Excel, etc. 

## 3. Características

### 3.1 Obtener Productos Desde
Los productos en la tabla de productos pueden ser obtenidos desde otros documentos. Las opciones son: Pedido de Material, Oportunidad y Posible Proveedor. 

* **Pedido de Material**: Los Productos se obtendrán desde un Pedido de Material enviado que se seleccione. Un Pedido de Material puede buscarse con algunas palabras y también puede seleccionarse un rango de fechas para filtrar los Pedidos de Materiales. 

* **Oportunidad**: Los Productos pueden obtenerse desde una Oportunidad guardada. Aquí también puede seleccionarse un rango de fechas. 

* **Posible Proveedor**: Seleccionar un Posible Proveedor. Entonces, si ya se tiene algún Pedido de Material realizado para este proveedor, los productos se obtendrán de allí. 

### 3.2 Botón Obtener Proveedores
En vez de ingresar los proveedores en la tabla de forma manual, también se puede obtenerlos utilizando este botón. Cuando se hace click en el botón Obtener Proveedores, se verá un campo "Obtener Proveedores A Través De". Hay dos opciones para obtener proveedores: por etiquetas o por grupos. 

* **A Través de Etiquetas**: Ir a "Categoría de Etiqueta" a través de la barra de búsqueda. Primeramente se deben haber creado y asignado las etiquetas al DocType del Proveedor en el módulo de Adquisiciones. Luego se puede seleccionar por Etiqueta y obtener un proveedor. Al hacer click en Agregar "Todos los Proveedores", se obtendrán los proveedores que coincidan con las etiquetas seleccionadas. 

* **A Través de Grupos**: Seleccionar "Grupo de Proveedores" y elegir el grupo de proveedores desde el cual se desea añadir proveedores. Por ejemplo, si se selecciona Hardware, todos los proveedores de hardware serán añadidos, de forma tal que se pueda recibir una cotización de todos ellos. 

En la tabla de Proveedores, al expandir una fila usando el triángulo invertido, se verá la opción "Descargar PDF" la cuál abrirá un PDF del Pedido de Cotización. 

### 3.3 Mensaje para el Proveedor
Ingresar en este campo cualquier mensaje adicional para el Proveedor. Este campo puede ser completado automáticamente utilizando una "Plantilla de Mail". El campo para seleccionar una Plantilla de Mail está justo por encima de Mensaje para el Proveedor. 

### 3.4 Bases y Condiciones

En operaciones de Compra/Venta puede haber ciertas bases y condiciones que rigen la forma en que el proveedor vende bienes o servicios al cliente. Se pueden aplicar las Bases y Condiciones a las transacciones y éstas aparecerán en el documento impreso. Para saber más respecto a Bases y Condiciones, [click aquí](/docs/user/manual/en/setting-up/print/terms-and-conditions)

### 3.5 Configuración de Impresión
#### Papel membretado
Se pueden imprimir los pedidos de cotización/orden de compra en papel con el membrete de la empresa. Saber más [aquí](/docs/user/manual/en/setting-up/print/letter-head).

"Agrupar productos iguales", agrupará los productos iguales que se hayan sumado muchas veces a la tabla de Producto. Esto puede verse al imprimir.

#### Encabezados de Impresión
Los títulos de los documentos pueden ser modificados. Leer más [aquí](/docs/user/manual/en/setting-up/print/print-headings).

### 3.6 Más

**Botón de Vínculo con Pedido de Material**: Este botón vincula el Pedido de Cotización con cualquier Pedido de Material. Los productos deberían ser los mismos en el Pedido de Cotización y en el Pedido de Material.

![Link to Material Request]({{docs_base_url}}/assets/img/buying/link-to-material-request.png)

Ahora, cuando se guarde el Pedido de Cotización, se podrá ver en el Tablero que está vinculado al Pedido de Material. 
Si hay muchos Pedidos de Material con los mismos productos, entonces el vínculo se creará con el Pedido de Material más nuevo. 

## 4. Crear una Cotización de Proveedor luego de un Pedido de Cotización. 
Luego de crear un Pedido de Cotización, hay dos formas de generar una Cotización de Proveedor desde el Pedido de Cotización. 

### 4.1 Cotización de Proveedor por Usuario

1. Abrir Pedido de Cotización y hacer click en **Cotización de Proveedor > Crear**.

    ![Supplier Quotation from RFQ]({{docs_base_url}}/assets/img/buying/make-supplier-quotation-from-rfq.png)

2. Seleccionar el Proveedor, y hacer click en el proveedor nuevamente. En esta página hacer click en el + que se encuentra al lado de "Cotización de Proveedor". Se abrirá una nueva página de Cotización de Proveedor, el usuario debe ingresar la cantidad, el precio y enviarla.

    ![Supplier Quotation from Supplier]({{docs_base_url}}/assets/img/buying/supplier-quotation-from-sup.png)
    
### 4.2 Cotización de Proveedor por Proveedor

1. Si se crea un [Contacto](/docs/user/manual/en/CRM/contact) para el Proveedor y se asocia a una dirección de mail, los detalles de Contacto y la dirección de correo electrónico serán obtenidas al seleccionar el Proveedor. Crear un Contacto y mail si todavía no se encuentran presentes. 

2. Hacer click en el botón "Enviar Mail al Proveedor".

    **Si la cuenta de Proveedor no está presente**: El sistema creará una cuenta de Proveedor y enviará los detalles al Proveedor. El proveedor deberá hacer click en el link (Actualización de Contraseña) presente en el mail. Luego de actualizar la contraseña, el Proveedor puede acceder a su portal con el formulario de Pedido de Cotización. El Proveedor será creado como Usuario de Sitio Web. 

    ![Supplier email if account not present]({{docs_base_url}}/assets/img/buying/supplier-password-update-link.png)

    
    **Si la cuenta de Proveedor está presente**: El sistema le enviará el link de Pedido de Cotización al Proveedor, el mismo tendrá que ingresar utilizando sus credenciales para ver el formulario de Pedido de Cotización en el portal. 

    ![Supplier email if account present]({{docs_base_url}}/assets/img/buying/send-rfq-link.png)

3. De cualquier forma, cuando el Proveedor ingresa, se le mostrará la siguiente pantalla. Desde aquí pueden enviar la cotización:

    ![Supplier Quotation Screen]({{docs_base_url}}/assets/img/buying/rfq-supplier-quotation.png)

    El proveedor debe ingresar el monto y las notas (términos de pago) en el formulario y hacer click en enviar. en la sección de Cotización, estarán visibles las cotizaciones anteriores. 

4. Al enviar, el sistema creará la Cotización de Proveedor (en modo borrador) contra el proveedor. El usuario debe revisar la Cotización de Proveedor y enviarla. Cuando todos los Productos del Pedido de Cotización hayan sido cotizados por un Proveedor, el estado de la cotización será actualizado a "Recibido" en la tabla de "Pedido de Cotización" del Proveedor. 

    ![RFQ status after supplier quote]({{docs_base_url}}/assets/img/buying/rfq-supplier-quoted.png)

## 5. Sin Cotización del Proveedor

Si un Proveedor indica que no enviará una cotización para los productos, esto puede señalarse en el documento de Pedido de Cotización haciendo click en la casilla "Sin Cotización" luego de que el Pedido de Cotización haya sido enviado. La casilla de Sin Cotización puede ser vista al expandir la fila de un Proveedor haciendo click en el triángulo invertido del lado derecho. 

![No Quote from Supplier]({{docs_base_url}}/assets/img/buying/no-quote-supplier.png)

Para saber respecto a crear una Cotización de Proveedor hacer [click aquí](/docs/user/manual/en/buying/supplier-quotation).


### 6. Temas Relacionados
1. [Orden de Compra](/docs/user/manual/en/buying/purchase-order)
1. [Proveedor](/docs/user/manual/en/buying/supplier)
1. [Cotización del Proveedor](/docs/user/manual/en/buying/supplier-quotation)
1. [Cotización](/docs/user/manual/en/selling/quotation)
1. [Pedido de Material](/docs/user/manual/en/stock/material-request)

{next}
