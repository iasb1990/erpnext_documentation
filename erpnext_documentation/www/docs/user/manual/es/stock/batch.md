<!-- add-breadcrumbs -->
# Lote

**La función Lote en ERPNext permite agrupar muchas unidades de un Producto y asignarles un único valor/número/etiqueta llamado Número de Lote.**

Esto se hace de acuerdo al Producto. Si el Producto es en lote, entonces debe mencionarse el número de Lote en cada transacción de existencias. Los números de Lote pueden configurarse de forma manual o automática. Esta función es útil para configurar fechas de vencimiento de muchos Productos o moverlos conjuntamente a diferentes Depósitos.

Para acceder al listado de Número de Lote ir a:
> Inicio > Inventario > Número de Serie y Lote > Lote


## 1. Prerrequisitos
Antes de crear y utilizar un Lote, es recomendable crear lo siguiente:

* [Producto](/docs/user/manual/en/stock/item)
* Habilitar "Tiene Número de Lote" en la Función Producto
    ![Batch No Enabled](/docs/assets/img/stock/batch-no-enabled.png)


## 2. Cómo crear un nuevo Lote

Para configurar un producto como en lote, debe habilitarse el campo "Tiene Número de Lote" en la función Producto. Si no se seleccionó "Crear Nuevo Lote Automáticamente" al crear un producto, se deberán crear los Lotes de forma Manual. 

To create new Batch No. master for an item, go to:

1. Ir al listado de Lote y hacer click en Nuevo.
1. Configurar la ID del Lote.
1. Seleccionar el Producto.
1. Si se realiza cualquier transacción con el producto, no puede configurarse ni desconfigurarse el núermo de lote.
1. Guardar.

Cuando se habilitan los Lotes para un Producto, también estará disponible la opción de [retener muestra de producto](/docs/user/manual/en/stock/retain-sample-stock). 

### 2.1 Creación Automática de Lote
Si se quiere crear un lote automáticamente al crear un Recibo de Compra, se debe habilitar la casilla "Crear Nuevo Lote Automáticamente" en la funcion Producto:

<img class="screenshot" alt="Item Setup for Batches" src="{{docs_base_url}}/assets/img/stock/item_setup_for_batch.png">

## 3. Características
### 3.1 Dividir y Mover Lotes

Al abrir un lote, se verán en la página todas las cantidades que pertenecen a ese lote.

<img class="screenshot" alt="Batch View" src="{{docs_base_url}}/assets/img/stock/batch_view.png">

* Para mover el lote de un Depósito a otro, se puede hacer click en el botón **Mover**.

* También se puede dividir un lote en lotes mas chicos haciendo click en el botón **Dividir**. Esto creará un nuevo Lote en base a este Lote y las cantidades se dividirán entre lotes.

    ![Split Batch](/docs/assets/img/stock/batch_split.png)

* Si se configura la fecha de vencimiento, el Lote mostrará "No Vencido" hasta la fecha de vencimiento, luego de la cuál mostrará un cartel de "Vencido". Si no se configura fecha, el Lote mostrará "No Configurada".

### 3.2 Transacciones de Productos en Lote

Se deberá crear una función de Lote antes de crear un Recibo de Compra.
De esta forma, cada vez que se cree un Recibo de Compra u Orden de Trabajo para un producto en lote, 
primero se deberá crear su Número de Lote, y luego seleccionarlo en la Orden de Compra o Registro de Inventario.

En cada transacción de existencias (Recibo de Compra, Nota de Envío, Factura) con un producto en lote,
se deberá ingresar el Número de Lote del Producto. 

> Observación: En transacciones de existencias, las ID de los Lotes serán filtradas en base al Código de Producto, Depósito,
Fecha de Vencimiento del Lote (comparada con la fecha de Publicación de la transacción) y Cantidad Actual en Depósito.
Al buscar la ID del Lote sin haber ingresado un valor en el campo Depósito, el filtro de Cantidad Actual no será aplicado. 

### 4. Temas Relacionados
1. [Número de Serie](/docs/user/manual/en/stock/serial-no)
1. [Entrada de Existencias Inciales para Productos Seriados y en Lote ](/docs/user/manual/en/stock/articles/opening-stock-balance-entry-for-serialized-and-batch-item)
1. [Administrar Inventario en base a Lotes ](/docs/user/manual/en/stock/articles/managing-batch-wise-inventory)
