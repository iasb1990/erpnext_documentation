<!-- add-breadcrumbs -->
#Administrar Inventario en base a Lotes 

Un conjunto de productos que comparte las mismas propiedades y aributos puede agruparse en un solo Lote. Por ejemplo, los productos farmacéuticos son de lote, de forma tal que su fecha de fabricación y de vencimiento pueden rastrearse conjuntamente. 

Para mantener lotes de un producto determinado es necesario configurar el campo "Tiene Número de Lote" como "Si" en la Función Producto.   

<img alt="Batch Item" class="screenshot" src="{{docs_base_url}}/assets/img/articles/batchwise-stock-1.png">

Se puede crear un nuevo Lote desde:

`Existencias > Documentos > Lote > Nuevo

Para aprender más respecto a lotes click [aquí.](/docs/user/manual/en/stock/batch.html)

Para el Producto en Lote es obligatorio actualizar el Número de Lote en las transacciones de existencias (Recibo de Compra y Nota de Envío).

#### Recibo de Compra

Al crear un Recibo de Compra, se debe crear un nuevo Lote o seleccionar uno existente de la función Lote. Un lote puede ser asociado con un Producto en Lote. 

<img alt="Batch in Purchase Receipt" class="screenshot" src="{{docs_base_url}}/assets/img/articles/batchwise-stock-2.png">

#### Nota de Envío

Definir el Lote en la tabla de Productos de la Nota de Envío. Si un producto en Lote es añadido dentro de un Paquete de Productos, se puede también actualizar su Número de Lote en la Lista de Envío. 

<img alt="Batch in Delivery Note" class="screenshot" src="{{docs_base_url}}/assets/img/articles/batchwise-stock-3.png">

#### Informe de Inventario en Base a Lotes

Para ver el informe de inventario en base a lotes ir a: 

Existencias > Informes Generales > Historia de Inventarios en Base a Lotes

<img alt="Batchwise Stock Balance" class="screenshot" src="{{docs_base_url}}/assets/img/articles/batchwise-stock-4.png">

<div class="embed-container">
    <iframe src="https://www.youtube.com/embed/J0QKl7ABPKM?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen>
    </iframe>
</div>

{next}