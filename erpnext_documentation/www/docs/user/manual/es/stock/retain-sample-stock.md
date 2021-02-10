<!-- add-breadcrumbs -->
# Retener Muestra de Producto

**Una Muestra de Producto es un lote de cualquier Producto guardado en caso de que debiera realizarse algún análisis posteriormente.**

El Producto para el cual se crea una muestra de producto puede ser materia prima, material de empaque, o productos finales. 

## 1. Prerrequisitos
Antes de utilizar muestras de productos, se recomienda crear lo siguiente: 

* [Producto](/docs/user/manual/en/stock/item)
* [Lote](/docs/user/manual/en/stock/batch)
* [Depósito](/docs/user/manual/en/stock/warehouse)

## 1. Como Configurar el Depósito de Retención de Muestras en Configuraciones de Inventario

Se recomienda crear un nuevo Depósito, de forma separada, para retener muestras y no utilizarlo en producción.

<img class="screenshot" alt="Sample Retention Warehouse" src="{{docs_base_url}}/assets/img/stock/sample-warehouse.png">

### 1.2 Permitir Retención de Muestras en la Función Producto
La Retención de Muestra se basa en los Lotes, por lo cual, primero debe habilitarse la función Tiene Número de Lote. Luego hacer click en Retener Muestra y configurar el número máximo de muestras para un lote.  

<img class="screenshot" alt="Retain Sample" src="{{docs_base_url}}/assets/img/stock/retain-sample.png">

### 1.3 Realizar Registro de Inventario

* Cuando se crea un [Registro de Inventario](/docs/user/manual/en/stock/stock-entry) con el objetivo de Recepción de Material, puede configurarse la Cantidad de Muestras para aquellos productos que tengan la opción de Retención de Muestra habilitada. Se debe seleccionar el Número de lote para el Producto/Productos. La cantidad de Muestra no puede ser mayor al Máximo configurado en la Función Producto.  

    <img class="screenshot" alt="Retain Sample" src="{{docs_base_url}}/assets/img/stock/material-receipt-sample.png">

* Al enviar este Registro de Inventario, estará disponible el botón "Realizar Registro de Retención de Inventario" para realizar otro Registro de Inventario  para la transferencia de los productos de muestra del lote mencionado al depósito de retención de muestras configurado en Configuraciones de Inventario.

    ![Sample Retention Button](/docs/assets/img/stock/sample-retention-button.png)

* Hacer click en este botón llevará a la generación de un nuevo Registro de Inventario de tipo "Transferencia de Material". Este registro transfiere la muestra retenida desde el Depósito de Destino (Almacenes) al Depósito de Retención de Muestras. Este registro tendrá toda la información, verificar y hacer click en Enviar. 

    <img class="screenshot" alt="Retain Sample" src="{{docs_base_url}}/assets/img/stock/material-transfer-sample.png">

### 2. Temas Relacionados
1. [Depósito](/docs/user/manual/en/stock/warehouse)
