<!-- add-breadcrumbs -->
#Entrada para Volver a Embalar

La entrada para Volver a Embalar se crea para aquellos productos comprados al por mayor que deben ser embalados en paquetes mas chicos. Por ejemplo, un producto comprado en toneladas puede volver a embalarse en kilos.

Observaciones:
1. El producto comprado y el que es reembalado tendrán Códigos de Producto diferentes. 
2. La entrada para Volver a Embalar puede ser realizada con o sin Lista de Materiales.

En una entrada para Volver a Embalar, puede haber uno o mas productos a ser reembalados. Veamos la situación detallada más abajo para entender mejor. 

Asumamos que estamos comprando cajas de pintura en aerosol de un color específico (Verde, Azul, etc). Y luego se vuelve a empaquetar para crear paquetes que contengan múltiples colores de pintura en aerosol (Azul-Verde, Verde-Amarillo, etc.).

#### 1. Nuevo Ingreso de Existencias

`Existencias > Documentos > Ingreso de Existencias > Nuevo Ingreso de Existencias

#### 2. Ingresar Productos

Seleccionar el Objetivo como "Entrada para Volver a Embalar"

Para materias primas o insumos, solo se proveerá el Depósito de Origen. 

Para productos reembalados, solo estará disponible el Depósito Objetivo. Se deberá proveer valuación para los productos reembalados.  

<img alt="Repack Entry" class="screenshot" src="{{docs_base_url}}/assets/img/articles/repack-1.png">

Actualizar Cantidad para todos los Productos seleccionados

#### 3. Enviar Ingreso de Existencias

Al enviar el Ingreso de Existencias, se reducirán las existencias del insumo desde el Depósito de Origen y se añadirán las existencias del producto reembalado al Depósito Objetivo. 

<img alt="Repack Stock Entry" class="screenshot" src="{{docs_base_url}}/assets/img/articles/repack-2.png">

<!-- markdown --> 