# Producto

**Un Producto es un producto o servicio ofrecido por una empresa**

El término Producto también se aplica a materias primas o componentes de productos que todavía deben ser manufacturados (antes de poder ser vendidos a los clientes). ERPNext permite administrar todo tipo de productos como materias primas, sub-productos, productos finales, variantes de productos y servicios. 

ERPNext esta optimizado para el manejo de ventas y compras a través de productos. Si se ofrecen servicios, se puede crear un Producto por cada servicio que se ofrece. Completar la sección de Producto es muy importante para una implementación exitosa de ERPNext.

Para acceder al listado de Producto ir a:
> Inicio > Inventario > Productos y Precios > Producto

## 1. Prerrequisitos
Antes de crear y utilizar un Producto, se recomienda crear lo siguiente: 

* [Grupo de Productos](/docs/user/manual/en/stock/item-group)
* [Depósito](/docs/user/manual/en/stock/warehouse)
* Se requiere una Unidad de Medida

## 2. Cómo crear un Producto
1. Ir al listado de Producto y hacer click en Nuevo.
2. Ingresar un Código de Producto, el nombre se completará automáticamente con el Código de Producto al hacer click en el campo Nombre de Producto.
3. Seleccionar un Grupo de Productos
4. Ingresar las existencias iniciales y el precio estándar de venta.
5. Guardar.
  ![Producto Guardado](/docs/assets/img/stock/item-saved.png)

### 2.1 Propiedades del Producto

  * **Nombre del Producto:** Es el nombre real del producto o servicio. 
  
  * **Código del Producto:** El Código de Producto es una forma simple de identificar el Producto. Si hay pocos Productos, se recomienda que el Código de Producto y el Nombre sean el mismo. De esta forma los nuevos usuarios pueden reconocer y actualizar más facilmente los detalles de Productos en todas las transacciones. En caso de haber muchos productos con nombres largos y listas de cientos de productos, es aconsejable codificarlos. Para entender cómo codificar productos [Codificación de Productos](/docs/user/manual/en/stock/articles/item-codification). También se puede generar un Código de Producto en base a un [Número de serie](/docs/user/manual/en/setting-up/settings/naming-series) activando esta función en [Configuraciones de Existencias](/docs/user/manual/en/stock/stock-settings#1-item-naming-by).
  
  * **Grupo de Productos:** El Grupo de Productos se utiliza para clasificar un producto de acuerdo a diferentes criterios como productos, materias primas, servicios, sub-productos, bienes de consumo o todos los grupos de productos. Crear un Grupo de Productos predeterminado en el listado de Grupo de Productos en Configuración > Grupo de Productos y preseleccionar la opción mientras se completan los detalles del Nuevo Producto en  [Grupo de Productos](/docs/user/manual/en/stock/item-group). Los Grupos de Productos pueden ser sub-productos, materias primas, etc o también pueden basarse en lo que necesite el negocio. 
  
  * **Unidad de Medida predeterminada:** Estaa es la unidad de medida predeterminada que se utilizará para el producto. Puede ser unidades, kilos, metros, etc. Se pueden almacenar todas las Unidades de Medidas que necesite un producto en Configuración> Datos Principales > UDM. Estas pueden ser pre seleccionadas al completar el Nuevo Producto utilizando el signo % para que aparezca una ventana emergente con el listado de UDM. Para más detalles, visitar la página [UdM](/docs/user/manual/en/stock/uom).

### 2.2 Opciones al crear un Producto
* **Desactivar**: Si se desactiva un Producto, este no podrá ser seleccionado en ninguna transacción.

* **Permitir Producto Alternativo*: A veces, al fabricar un producto final, puede suceder que algunos materiales específicos no estén disponibles. Si se habilita esta opción, se puede crear y seleccionar un producto alternativo del listado de Productos Alternativos. Para saber más, visitar la página [Producto Alternativo](/docs/user/manual/en/manufacturing/item-alternative) page.

* **Mantener Existencias:** Si se mantienen existencias de este Producto en el Inventario, ERPNext realizará una entrada en el Inventario de Existencias para cada transacción de este producto. Asegurarse de no seleccionar esta opción cuando se crea un Producto sin Existencias (fabricación contra pedido/contruir) o un servicio.

* **Incluir Producto en Fabricación**: Esto es para materias primas que serán utilizadas para crear productos finales. Si el Producto es un servicio adicional como "lavado" que será usado en la Lista de Materiales, deshabilitar esta opción. 

* **Valoración**: Hay dos opciones para valuar las existencias de productos. FIFO (Primero que ingresa - Primero que sale) y Promedio Móvil. Para entender en detalles esta seccion ir a [Valoración, FIFO y Promedio Móvil](/docs/user/manual/en/stock/articles/item-valuation-fifo-and-moving-average).

* **Precio de Venta Estándar**: Al *crear* un Producto, ingresar un valor en este campo creará automáticamente un [Precio de Producto](/docs/user/manual/en/stock/item-price) en la base de datos. Ingresar un valor luego de que el Producto ha sido guardadó no funcionará. En este caso, el Precio de Producto será creado desde cualquier transacción con el producto. Es el valor al cual se venderá el producto. Será obtenido de las Órdenes de Venta y Facturas de Venta. 

* **Es Activo Fijo**: Hacer click en esta casilla de verificación si este producto es un Activo de la empresa. Ver el [Módulo de Activos](/docs/user/manual/en/asset) para saber más. 

* **Crear Automáticamente Activos en Compra**: Si un Producto es un Activo de la Empresa, hacer click en esta casilla si se desea crear un activo automáticamente al comprar este producto durante el [Ciclo de Compra](/docs/user/manual/en/buying/purchase-order). Para saber más ver la [Página de Activos](/docs/user/manual/en/asset/asset).

* **Porcentaje de Tolerancia**: Esta opción sólo estará disponible luego de crear y guardar el Producto. Este el porcentaje en el cuál se permitirá sobre facturar y sobre entregar este Producto. Si no es configurado, se seleccionará desde [Configuraciones de Existencias](/docs/user/manual/en/stock/stock-settings#3-limit-percent).

* **Subir una Imagen**: Para subir una imagen al ícono que aparecerá en todas las transacciones, guardar el formulario completado parcialmente. Luego de guardar el archivo, aparecerá el botón "Cambiar" en el ícono de Imagen. Hacer click allí, luego hacer click en Subir y cargar la imagen.  

Para India:

* **HSN/SAC**: El Sistema Armonizado de Nomenclatura (HSN) y el Código de Servicio Contable (SAC) para GST. Estos números son definidos por el gobierno y distintos productos caen bajo distintos códigos. Los nuevos códigos HSN pueden ser añadidos sino están presentes en el listado.  
* **No está clasificada o está exenta**: Para un Producto que está bajo el régimen GST, pero no se le aplican impuestos. Por ejemplo: Cereales.
* **No es GST**: Para un Producto que no está incluído en el régimen. Por ejemplo: petróleo.

## 3. Características

### 3.1 Marca y Descripción

* **Marca**: Si hay más de una marca, guardarlas en Comercialización > Marca y preseleccionarlas cuando se completa un Nuevo Producto.
* **Descripción**: Descripción del Producto. De forma predeterminada se tomará el Código de Producto.
  ![Marca y Descripción del Producto](/docs/assets/img/stock/item-brand-description.png)

### 3.2 Código de Barras

Pueden guardarse códigos de barra en los Productos para escanearlos y agregarlos con facilidad a las transacciones. En la tabla de Códigos de Barra se puede agregar el [código de barra escaneable](/docs/user/manual/en/stock/articles/track-items-using-barcode) de un producto. En ERPNext hay dos tipos de Código de Barra:

* **EAN**: El Número de Artículo Europeo, compuesto por 13 dígitos. El EAN es de uso internacional y es reconocido por la mayoria de los Sistemas TPV.
* **UPC**: El Código Universal de Producto es un número compuesto por 12 dígitos. El UPC generalmente se usa solo en Estados Unidos y Canadá. 

### 3.3 Inventario

* **Duración de un Producto en Días**: Esto es para un producto [Lote](/docs/user/manual/en/stock/batch). El número de días luego de los cuáles el lote de productos será inutilizable. Por ejemplo, medicamentos. 
* **Fin de Vida Útil**: Para un solo Producto, la fecha luego de la cuál será completamente inutilizable. Es decir, no podrá usarse en transacciones y manufacturas. Por ejemplo, se utilizarán cristales de plástico para fabricar productos durante 5 años, luego de los cuáles se querrá utilizar gotas de plástico. 
* **Garantía**: Para poder rastrear un período de garantía es necesario que el producto sea seriado. Cuando el Producto es entregado, la fecha de entrega y la de período de vencimiento se guarda en la sección de Número de Serie. A través de esa sección se puede rastrear el estado de la garantía. 

  El período de garantía es un período de tiempo en el cuál el producto comprado puede ser devuelto o cambiado. 

  <img class="screenshot" alt="Item Warranty" src="{{docs_base_url}}/assets/img/stock/item-inventory.png">

* **Peso UdM**: La Unidad de Medida para el Producto. Puede ser unidades, Kilos, etc. La UdM que se use internamente puede diferir de la UdM de compra. 
* **Peso por Unidad**: El peso real de cada unidad del producto. Ejemplo: 1 kilo de galletas o 10 galletas por paquete. 
* **Tipo de Pedido de Material Predeterminado**: Cuando se cree un nuevo Pedido de Material, el campo establecido aquí será seleccionado de forma predeterminada en el Pedido de Material. Esto también es conocido como "pedido".
* **Método de Valoración**: Seleccionar el Método de Valoración sea FIFO o Promedio Móvil. Para saber más sobre Métodos de Valoración [click aquí](/docs/user/manual/en/stock/articles/item-valuation-fifo-and-moving-average).

### 3.4 Pedido Automático
Cuando las existencias de un producto caen por debajo de una cierta cantidad se puede configurar un pedido automático en la sección "Pedido Automático". Esto debe ser habilitado en las [Configuraciones de Existencias](/docs/user/manual/en/stock/stock-settings#9-automatic-material-request). Esta función creará un [Pedido de Materiales](/docs/user/manual/en/stock/material-request) para el producto. El usuario que posea el rol de Administrador de Compras y Administrador de Existencias será **notificado** cuando se cree el Pedido de Material. 

* **Revisar en (grupo)**: En que grupo de depósitos se revisará la cantidad del producto. 
* **Pedir para**: Para que depósito se hace el pedido de producto. 
* **Nivel de Pedido**: Cuando el producto llegue a esta cantidad, se dispara el pedido. El nivel de pedido puede ser determinado en base al tiempo de espera y el promedio de consumo diario. Por ejemplo, se puede establecer el nivel de pedido de una placa madre en 10. Cuando haya solo 10 placas madres en existencia, el sistema creará un Pedido de Material automáticamente en tu cuenta de ERPNext. 
* **Cantidad a pedir**: El número de unidades a pedir de forma tal que la suma del costo de pedido y los costos de mantenimiento estén en su mínimo. La cantidad a pedir está basada en el "Pedido Mínimo" especificado por el proveedor y otros factores.

  Por ejemplo, si el nivel de pedido es de 100 productos, la cantidad a pedir no necesariamente tiene que ser 100 productos. La cantidad a pedir puede ser mayor o igual al nivel de pedido. Puede depender del tiempo de espera, descuento, transporte y promedio de consumo diario. 

* **Tipo de Pedido de Material**: El tipo de [Pedido de Material](/docs/user/manual/en/stock/material-request) con el cual se pedirán los productos. Esto depende de si se compra el Producto, se lo fabrica o se lo transfiere entre Depósitos. 

  <img alt="Item Reorder" class="screenshot" src="{{docs_base_url}}/assets/img/stock/item-reorder.png">

> **Observación**: El Pedido de Material se creará a las 12 de la noche dependiendo del nivel de pedido establecido. 

### 3.5 Unidades de Medida Múltiples
Se puede contar con distintas Unidades de Medidas para un mismo Producto. Si la UdM de venta predeterminada es unidades pero se recibe la mercadería en kilos, se pueden establecer UdM adicionales con su respectivo factor de conversión. Por ejemplo, 500 unidades de destornilladores = 1 kilo; entonces es necesario seleccionar kilo/litro como UdM y configurar el factor de conversión como 500. Para saber más respecto a vender en diferentes UdM, visitar [esta página](/docs/user/manual/en/selling/articles/Selling-in-different-UOM).

### 3.6 Número de serie

Utilizando Números de Serie se pueden rastrear las garantías y las devoluciones. En caso de que un proveedor retire un Producto individual, el sistema de números ayuda a rastrear ese Producto individual. El sistema numérico también administra las fechas de vencimiento.

Tener en cuenta que si se vende productos de a miles, y si los mismos son muy pequeños, como lapiceras o gomas de borrar, no es necesario seriarlos. 

En ERPNext, se deberá mencionar los Números de Serie en algunas entradas contables. Si el producto no es un bien de consumo durable, si no tiene garantía ni posibilidades de ser devuelto, es bueno evitar asignar números de serie. 

<img alt="Serial No modal" class="screenshot" src="{{docs_base_url}}/assets/img/stock/serial_no_modal.gif">

### 3.7 Lotes

Un grupo de productos puede ser fabricado en lotes. Esto es util para movilizar el lote y asociar una fecha de vencimiento a cierto lote. 

* **Posee Número de Lote**: Si se hace click en esta casilla de verificación se mostrarán opciones como número de lote, fecha de vencimiento, y conservar muestra de existencias. No se puede activar esta opción si hay alguna transacción pre existente para este Producto. Si esta opción esta desactivada, se deberá ingresar manualmente los números de serie para cada transacción. 

* **Numero de Serie de Lote**: Prefijo que será aplicado a los números de lote. Si se configura 5x1SCR, entonces el primer lote será nombrado como  5x1SCR00001 en la primera transacción/fabricación.

* **Crear Nuevo Lote Automáticamente**: Si el número de lote no se menciona en las transacciones, entonces será automáticamente creado siguiendo un formato como este AAAA.00001. Si se prefiere crear los números de lote de un producto de forma manual, entonces dejar este campo en blanco. Esta configuración inactiva lo establecido en la Configuración de Existencias bajo el campo "Prefijo de Series de Nomenclatura". Los números de lote pueden configurarse praa ser generados automáticamente si se fabrican los productos o para ingresarlos manualmente si los mismos provienen de un fabricante externo. 

* **Tiene fecha de vencimiento**: Si se hace click en esta casilla, el número de lote será creado de acuerdo a la fecha de vencimiento. Las mismas pueden ser configuradas en la función "Lote". 

* **Conservar Muestra**: A fin de conservar un mínimo número de existencias de un producto en forma de muestra. Para hacer esto se debe configurar un Depósito de Conservación de Muestras en la Configuración de Existencias. Para saber mas, [click aquí](/docs/user/manual/en/stock/retain-sample-stock).

* **Tiene Número de Serie**: Esto es similar al Número de Lote, será creado cuando se realicen transacciones o manufacturas. Si se configuran los números de serie como AA, entonces un número como AA00001 será creado en la primera transacción.

> Consejo: Al ingresar el Código de Producto en la tabla de Productos, si la tabla requiere detalles de inventario, entonces dependiendo de si el producto es seriado o posee lote, se puede ingresar el número de lote o serie de forma inmediata cuando aparezca la ventana emergente.

<img alt="Batch No modal" class="screenshot" src="{{docs_base_url}}/assets/img/stock/batch_no_modal.png">

> **Observación**: Una vez que se marca un producto como seriado, en lotes o, ninguno de los dos, no se puede cambiar esto luego de haber realizado un Ingreso de Existencias. 

Para saber más visitar la página [Conciliación de Inventario](/docs/user/manual/en/stock/stock-reconciliation).

### 3.8 Variantes
Una Variante de Producto es una versión diferente del Producto. Para saber más respecto a la adminsitración de variantes ver [Variantes de Producto](/docs/user/manual/en/stock/item-variants).

### 3.9 Configuración Predeterminada del Producto

En esta sección se pueden definir configuraciones predeterminadas relacionadas a un producto para todas sus transacciones en toda la empresa. 

* **Depósito Predeterminado:** Este es el Depósito que será seleccionado automáticamente en las transacciones para este Producto. 
* **Lista de Precios Predeterminada:** Tanto de venta como de compra. De la misma forma, se pueden configurar las cuentas predeterminadas de compra y venta. 
* **Proveedor**: Si se configura un proveedor predeterminado, el mismo será seleccionado para nuevas transacciones de compra. 
* **Cuenta de Gastos Predeterminada:** Es la cuenta de la cuál será debitado el costo del Producto. 
* **Cuenta de Ingresos Predeterminada:** Es la cuenta en la cuál se acreditará el ingreso generado por vender el Producto. 
* **Centro de Costos Predeterminado:** Es utilizado para rastrear los gastos para este Producto.

  ![Item defaults](/docs/assets/img/stock/item-defaults.png)

> Consejo: Se pueden añadir más filas para múltiples empresas.

### 3.10 Compra, detalles de reposición

* **Unidad de Medida de Compra Predeterminada**: La UdM predeterminada que será usada en las transacciones de compra. 
* **Pedido Mínimo**: La cantidad mínima requerida para transacciones de compra como Órdenes de Compra. Si esto se configura, el sistema no permitirá avanzar en la operación de compra si la cantidad de producto pedida es menor que la establecida en este campo. 
* **Existencias adecuadas**: Las “Existencias Adecuadas” son utilizadas en el informe "Nivel de pedido recomendado basado en Productos". De acuerdo con las Existencias Adecuadas, el consumo diario promedio y el tiempo de espera, el sistema sugiere el Nivel de Pedido de un producto.

  Nivel de Pedido = Existencias Adecuadas + (Consumo Diario Promedio * Tiempo de Espera)
* **Precio de la Última Compra**: Aquí se mostrará el precio al cual se compró por última vez un producto utilizando una [Factura de Venta](/docs/user/manual/en/accounts/purchase-invoice).
* **Es Producto de Compra:** Si esta casilla no está clickeada, no se podrá usar este producto en operaciones de compra.
* **Es Producto recibido de Cliente:** Clickear esta casilla si el producto es provisto por un cliente y recibido a través de **Ingreso de Existencias > Recibo de Materiales**. Si esta casilla esta seleccionada, el campo de **Cliente** es obligatorio como el Cliente predeterminado para **Pedido de Materiales**. Para saber más, visitar[esta página](/docs/user/manual/en/manufacturing/articles/customer-provided-items).
* **Tiempo de espera en días:** El tiempo de espera en días es el número de días que transcurren entre el pedido de producto y su llegada al Depósito.

  <img class="screenshot" alt="Purchase details" src="{{docs_base_url}}/assets/img/stock/item-purchase-details.png">

### 3.11 Detalles de Proveedor

* **Envío a Cargo del Proveedor (Envío Directo)**: Si el producto será enviado directamente desde el proveedor al cliente hacer click en esta casilla. Leer más [aquí](/docs/user/manual/en/selling/articles/drop-shipping).
* **Código de Proveedores:** Código de Rastreo del Producto definido por el Proveedor. En las transacciones de Compra al selecccionar un Producto, también se obtendrá el Número de Pieza del Proveedor para referencia del mismo. Para leer más sobre esto click [aquí](/docs/user/manual/en/buying/articles/maintaining-suppliers-part-no-in-item).

  ![Detalles del Proveedor del Producto](/docs/assets/img/stock/item-supplier.png)

### 3.12 Detalles de Comercio Exterior
Si se está obteniendo el producto de otro país, se pueden incluir los detalles en esta sección. 

* **País de Origen**: El país desde donde se obtiene el producto. 
* **Número de arancel aduanero**: Se puede crear un número de arancel aduanero con una descripción y utilizarlo como referencia y para compartir con organizaciones aduaneras. Más adelante puede ser usado en las Notas de Envío.  

### 3.13 Detalles de Venta

* **Unidad de Medida de Venta Predeterminada**: La UdM predeterminada que será utilizada en las transacciones de venta.
* **Descuento Máximo (%)**: Se puede definir el % máximo de descuento que puede aplicarse a un producto. Por ejemplo: si se configura un 20%, no puede venderse el mencionado producto con un descuento mayor al 20%.
* **Es Producto de Venta**: Si esta casilla no está seleccionada, no se podrá utilizar el producto en operaciones de venta. 

  ![Item Sales Details](/docs/assets/img/stock/item-sales.png)

### 3.14 Ingreso Diferido y Gasto Diferido
Se puede permitir un ingreso o gasto diferido para el producto. Una vez que se hace click en esta casilla, se verán las opciones para configurar la Cuenta de Gastos Diferidos y el número de meses a través de los cuales el ingreso/gasto es distribuido. 

Por ejemplo, tomemos una membresía anual de un gimnasio, se paga por adelantado pero el servicio se otorga durante todo el año. Para el dueño de gimnasio es un ingreso diferido y para el cliente, un gasto diferido. 

  ![Deferred Revenue](/docs/assets/img/stock/deferred-revenue.png)

Ver las páginas respecto a [Ingreso Diferido](/docs/user/manual/en/accounts/deferred-revenue) for more details.

### 3.15 Detalles del cliente

El Cliente puede identificar un Produto con un Código de Producto diferente. Esto es similar al [Código de Proveedor ](/docs/user/manual/en/stock/item#311-supplier-details). 

* **Nombre del Cliente**: Seleccionar el cliente.
* **Grupo de Clientes**: Este campo será tomado de acuerdo al Cliente seleccionado en el campo anterior. 
* **Código de Referencia:** Un cliente puede identificar este producto con un número distinto. Se puede rastrear el Código de Producto asignado por el Cliente a este producto. Cuando se crea una Orden de Venta, se mostrará el Código de Referencia del Cliente para este Producto. 

### 3.16 Impuesto del Producto

Esta configuración solo es necesaria si un Producto en particular tiene una tasa de impuesto diferente a la definida en la cuenta estándar de impuestos. 

Se deberá crear una nueva "Plantilla de Impuesto de Producto" o elegir una existente. Por ejemplo, si se tiene una Cuenta de impuesto, "VAT 14%" y este Producto en particular está eximido de ese impuesto, entonces se selecciona "VAT 14%" en la primera columna y se configura "0" como tasa impositiva en la segunda columna. Para más detalles, visitar la página de [Plantilla de Impuesto de Producto](/docs/user/manual/en/accounts/item-tax-template). 

![Plantilla de Impuesto de Producto](/docs/assets/img/stock/item-tax-template.png)

También se puede configurar un [Categoría impositiva](/docs/user/manual/en/accounts/tax-category) para este producto.


### 3.17 Criterios de Inspección

* **Inspección Requerida antes de la Compra**: Si es obligatoria la realización de una inspección antes de que el producto sea comprado, es decir, antes de generar el Recibo de Compra, seleccionar esta casilla. 
* **Inspección Requerida antes de la Entrega**: Si en el momento de la entrega del producto por parte del Proveedor es obligatorio realizar una inspección, seleccionar esta casilla. Es decir, antes de crear la Nota de Envío.  
* **Plantilla de Calidad de Inspección**: Si se prepara una Inspección de Calidad para el Producto, se actualizará automáticamente esta plantilla de criterios en la tabla de Inspección de Calidad de la Inspección de Calidad. Ejemplos de estos criterios son: Peso, Largo, Terminación, etc.
La Inspección de Calidad puede hacerse con Vista Rápida y no es necesario ir a una página diferente para actualizar los detalles de la inspección en ERPNext.

Para saber más respecto a Inspección de Calidad, [click aquí](/docs/user/manual/en/stock/quality-inspection).

### 3.18 Fabricación

* **Lista de Materiales Predeterminada**: La [Lista de Materiales](/docs/user/manual/en/manufacturing/bill-of-materials) predeterminada que se utiliza para fabricar este Producto.
* **Proveer Materias Primas para la Compra**:  Si se está tercerizando a un vendedor, se puede elegir proveerlos con las materias primas para fabricar el producto utilizando la Lista de Materiales predeterminada. 
* **Fabricante:** Seleccionar el Fabricante que fabrica este producto. 
* **Número de Pieza del Fabricante:** Ingresar el número de pieza que el fabricante le asignó a este producto. 

  ![Item Manufacturing](/docs/assets/img/stock/item-manufacturing.png)

* Los detalles del fabricante solo aparecerán luego de haber creado un "Fabricante de Producto" desde el panel y seleccionado ese registro como predeterminado. Aquí añadir detalles para:
  * Código de Producto
  * Ingresar el nombre del Fabricante
  * Ingresar el Número de Pieza que el Fabricante utiliza para identificar este producto
  * Seleccionar "Es Predeterminado" para mostrar el fabricante y número de pieza en el registro del Producto. 

  ![Item Manufacturer](/docs/assets/img/stock/item-manufacturer.png)

### 3.19  Sitio Web

* **Mostrar en Sitio Web**: Seleccionar si se quiere mostrar este Producto en el Sitio Web. Una vez que se selecciona esta opción, aparecerán opciones adicionales para configurar el producto en el sitio web. Para ver el producto en el sitio web hacer click en el link "Ver en Sitio Web" arriba a la izquierda justo por encima de la imagen del producto. Visitar el [Módulo de Sitio Web](/docs/user/manual/en/website) para saber más.

  <img class="screenshot" alt="Manufaturing details" src="{{docs_base_url}}/assets/img/stock/item-manufacturing-website.png">

* **Peso**: Los Productos de mayor peso serán mostrados primero en el sitio web. El límite para el número que se puede ingresar aquí es muy alto. 

* **Diapositivas**: Una presentación de diapositivas puede mostrarse en la parte superior de la página. Visitar la página [Página de Inicio](/docs/user/manual/en/website/homepage) en el Módulo de Sitio Web para saber más. 
* **Imagen**: Se puede adjuntar una imagen en vez de una presentación de diapositivas.
* **Depósito del Sitio Web**: Seleccionar un depósito existente o crear uno nuevo para transacciones en el Sitio Web. Este Depósito será diferente de los Depósitos fuera de línea. Las existencias para cualquier transacción en línea serán deducidas de los Depósitos configurados como Depósitos de Sitio Web. 
* **Grupos de Productos del Sitio Web**: En esta tabla se pueden seleccionar [Grupos de Productos](/docs/user/manual/en/stock/item-group) existentes o crear nuevos para clasificar productos en el sitio web.
* **Configurar Etiquetas Meta**: Las etiquetas Meta ayudan con las estrategias de SEO. Ver [Página Web](/docs/user/manual/en/website/web-page) para saber cómo utilizarlas.

Visitar [Fabricación](/docs/user/manual/en/manufacturing) y [Sitio Web](/docs/user/manual/en/website) para entender estos temas en detalle. 

### 3.20 Especificaciones de Sito Web
Esta sección es para configurar otros detalles del Producto

* **Copiar de Grupo de Productos:** Los detalles de "Especificaciones del Sitio Web" serán obtenidos de la configuración de un Grupo de Productos específico configurado en la sección anterior (2.17).
* **Especificaciones del Sitio Web**: La etiqueta y su descripción para el producto. Por ejemplo: "Garantía: 1 año".
* **Descripción de Sitio Web**: Esto aparecerá en la página del producto.
* **Contenido del sitio Web**: (*Introducido en la versión v12*) Se pueden crear diseños adiciones, etc. Utilizar Bootstrap 4 para mostrar en la página del producto. 

### 3.21 Detalles de publicación en Hub

Hub es un mercado gratuito en línea donde los Clientes y Proveedores pueden realizar transacciones. Si ambas partes están en ERPNext, las transacciones se dan de forma fluida. Se puede visitar the hub en: https://hubmarket.org.

* **Publicar en Hub**: Elegir si se desea publicar el producto en https://hubmarket.org/. Es un mercado gratuito. Si el proveedor/cliente también está en ERPNext, las transacciones se darán fluidamente. Por ejemplo, al crear una Orden de Compra, una Orden de Venta será creada para el Proveedor. 
* **Depósito Hub**: Este es un Depósito separado donde guardar las existencias para las transacciones realizadas en hub.
* **Sincronizar con Hub**: Sincronizar el producto y otros detalles con hub cuando se realizan transacciones.

## 4. Video

<div>
  <div class='embed-container'>
    <iframe src='https://www.youtube.com/embed/FcOsV-e8ymE?end=192' frameborder='0' allowfullscreen>
    </iframe>
  </div>
</div>

### 5. Temas relacionados
1. [Precio de Producto](/docs/user/manual/en/stock/item-price)
2. [Codificación de Producto](/docs/user/manual/en/stock/articles/item-codification)
3. [Variantes de Producto](/docs/user/manual/en/stock/item-variants)
4. [Grupo de Productos](/docs/user/manual/en/stock/item-group)
5. [Atributos de Producto](/docs/user/manual/en/stock/item-attribute)
6. [Valoración, FIFO y Promedio Móvil](/docs/user/manual/en/stock/articles//item-valuation-fifo-and-moving-average)
7. [Métodos de Valoración de Productos y Transacciones](/docs/user/manual/en/stock/articles/item-valuation-transactions)
8. [Campo "Mantener Existencias" Congelado en la Función Producto](/docs/user/manual/en/stock/articles/maintain-stock-field-frozen-in-item-master)
9. [Administrar Productos Finales Rechazados](/docs/user/manual/en/stock/articles/managing-rejected-finished-goods-items)
10. [Devolver Productos Rechazados](/docs/user/manual/en/stock/articles/return-rejected-item)
11. [Rastrear Productos utilizando Código de Barras](/docs/user/manual/en/stock/articles/track-items-using-barcode)
12. [Crear Amortización para Producto](/docs/user/manual/en/stock/articles/creating-depreciation-for-item)
13. [Nombrar usando Número de Serie](/docs/user/manual/en/stock/articles/serial-no-naming)
14. [Entrada de Existencias Inciales para Productos Seriados y en Lote ](/docs/user/manual/en/stock/articles/opening-stock-balance-entry-for-serialized-and-batch-item)
15. [Número de Serie](/docs/user/manual/en/stock/serial-no)
16. [Nombrar usando número de serie](/docs/user/manual/en/stock/articles/serial-no-naming)
