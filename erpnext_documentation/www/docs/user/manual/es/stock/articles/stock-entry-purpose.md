<!-- add-breadcrumbs -->
#Objetivo de Registro de Inventario

Un Registro de Innventario es una transacción de existencias, la cual puede ser utilizada con muchos objetivos. A continuación, aprenderemos más sobre Objetivos de Regitro de Inventario.

#### 1.Objetivo: Envío de Material

El registro de Envío de Material se utiliza para enviar producto/os desde un depósito. Al enviar el Envío de Material, las exsitencias de ese producto serán deducidas del Depósito de Origen.

El Envío de Material generalmente se realiza para productos consumibles de bajo valor como por ejemplo material de oficina, etc. También puede crearse un Envío de Material para conciliar el inventario de productos seriados y en lote. 

<img alt="Material Issue" class="screenshot" src="{{docs_base_url}}/assets/img/articles/stock-entry-issue.png">

#### 2.Objetivo: Recepción de Material

El registro de Recepción de Material se crea para ingresar existencias de producto/s a un depósito. Este tipo de registro de inventario puede ser creado para actualizar el balance inicial de productos seriados o en lote. También sirve para ingresar productos comprados sin Orden de Compra. 

Con fines de valoración de inventario, la Valoración del Producto se convierte en un campo obligatorio en el registro de Recepción de Material. 

<img alt="Material Receipt" class="screenshot" src="{{docs_base_url}}/assets/img/articles/stock-entry-receipt.png">

#### 3. Objetivo: Transferencia de Material

El registro de Transferencia de Material se crea para Transferencias de Materiales entre depósitos.

<img alt="Material Transfer" class="screenshot" src="{{docs_base_url}}/assets/img/articles/stock-entry-transfer.png">

#### 4.Objetivo: Transferencia de Material para Fabricación

En el proceso de fabricación, las materias primas son enviadas desde los almacenes hacia el departamento de producción (generalmente Depósitos de Trabajo en Curso). Esta Transferencia de Material se crea desde una Orden de Trabajo. Los Productos en este registro con tomados desde la Lista de Materiales para el Producto, de acuerdo con lo seleccionado en la Orden de Trabajo. 

<img alt="Transfer for Manufacture" class="screenshot" src="{{docs_base_url}}/assets/img/articles/stock-entry-manufacture-transfer.gif">

#### 4.Objetivo: Fabricación

La Fabricación es creada desde una Orden de Trabajo. En este registro, tanto las materias primas como el producto a producir son tomados desde la Lista de Materiales seleccionada en la Orden de Trabajo. Para las materias primas solo se menciona el Depósito de Origen (por lo general Depósito de Trabajo en Curso). Para el producto a ser fabricado solo se actualiza el depósito de destino, de acuerdo a lo configurado en la Orden de Trabajo. Al enviar, las existencias de materias primas son quitadas del Depósito de Origen, lo cual indica que las mismas fueron consumidas en el proceso de fabricación. El Producto fabricado es añadido al Depósito de Destino, señalando la finalización del ciclo de producción.  

<img alt="Manufacture" class="screenshot" src="{{docs_base_url}}/assets/img/articles/stock-entry-manufacture.gif">

#### 5.Objetivo: Re Embalar

El Registro de Re Embalar se crea cuando se compran productos al por mayor y luego se vuelven a embalar en paquetes más pequeños.[Ver esta página para saber más respecto a Registro Re Embalar](/docs/user/manual/en/stock/articles/repack-entry.html)

#### 6.Objetivo: Subcontrato

Una transacción de subcontratación implica una transferencia de materias primas hacia el depósito del subcontratado. Esto requiere ingresar un depósito para el subcontratado. Los registros de Subcontrato transfieren existencias desde el depósito de la empresa hacia el depósito del subcontratado. [Ver esta página para saber más respecto a Subcontratación](/docs/user/manual/en/manufacturing/subcontracting.html).

<img alt="Subcontract" class="screenshot" src="{{docs_base_url}}/assets/img/articles/stock-entry-subcontract.gif">

<!-- markdown -->
