<!-- add-breadcrumbs -->
# Entrada de Existencias Inciales para Productos Seriados y en Lote 

Para aquellos Productos que cuentan con Número de Serie y Número de Lote, la entrada de existencias iniciales debe ser realizada a través de una actualización via Ingreso de Existencias. [Click aquí para aprender como se administra el inventario seriado en ERPNext](/docs/user/manual/en/stock/serial-no.html).

**Pregunta:** ¿Por qué la entrada de Existencias Iniciales no puede ser actualizada a través de una Conciliación de Inventario en el caso de productos seriados y en lote?

En ERPNext, el nivel de existencias para un producto seriado se calcula en base a la cuenta de los Números de Serie existentes para ese producto. Por ende, al menos que se creen Números de Serie para el producto seriado, su nivel de existencias no será actualizado. En la Herramienta de Conciliación de Stock, solo se pueden actualizar las existencias iniciales para un producto, pero no los Números de Serie y de Lote. 

### Balance Inicial para el producto seriado

A continuación se detallan los pasos para crear una entrada de balance inicial de existencias para el producto Seriado y en Lote. 

#### Paso 1: Nuevo Ingreso de Existencias

> Existencias > Ingreso de Existencias > Nuevo

#### Paso 2: Seleccionar el objetivo

El Objetivo del Ingreso de Existencias debería ser establecido como `Recepción de Material`.

#### Paso 3: Actualizar fecha de publicación

La Fecha de Publicación debería ser la fecha en que se desea actualizar el balance inicial para un producto. 

#### Paso 4: Actualizar Almacén Objetivo

El Almacén Obetivo sera aquel en que se actualizará el balance inicial del producto. 

#### Paso 5: Seleccionar productos

Seleccionar productos para los cuales es actualizado el balance inicial. 

#### Paso 6: Actualizar Cantidad Inicial

Para el producto seriado, actualizar cantidad a la cantidad de Números de Serie que haya. 

Para el producto seriado, mencionar Números de Serie equivalentes a su Cantidad. O, si los Números de Serie están configurados para ser creado en base a un Prefijo, no es necesario mencionarlos manualmente. Click [aquí](/docs/user/manual/en/stock/articles/serial-no-naming.html) para aprender más respecto a nombrar con Números de Serie. 

Para un producto en lote, proveer la ID del Lote en el cual se actualizará el balance inicial. Preparar la función lote y actualizarla para el producto en Lote. Para crear nuevo Lote ir a: 

> Existencias > Configuración > Lote > Nuevo

[Click aquí para aprender más respecto a cómo se administra el inventario en base a Lotes en ERPNext.](/docs/user/manual/en/stock/articles/managing-batch-wise-inventory.html)

#### Paso 7: Actualizar la Valuación del Producto

Actualizar la valuación del producto, la cuál será por unidad de producto. Si diferentes unidades del mismo producto tienen distintas valuaciones, las mismas deben ser actualizadas en una fila diferente, con Valuaciones diferentes.

#### Paso 8: Cuenta de Diferencia

Al tratarse de un sistema de inventario continuo, se crea una entrada contable por cada transacción de existencias. El sistema contable de doble entrada requiere que el Total de Débitos coincida con el Total de Créditos en una entrada. Al enviar el Ingreso de Existencias, el sistema debita la cuenta Depósito por el valor total de productos. Para balancear esto, se utiliza una cuenta temporal como Cuenta de Diferencia. 

<img alt="Difference Account" class="screenshot" src="{{docs_base_url}}/assets/img/articles/difference-account-1.png">

#### Paso 9: Guardar y Enviar Ingreso de Existencias

Al enviar un Ingreso de Existencias, se realizará una publicación del inventario de existencias, y el balance inicial será actualizado para los productos en la Fecha de Publicación dada.

<!-- markdown -->
