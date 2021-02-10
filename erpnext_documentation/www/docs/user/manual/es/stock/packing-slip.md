<!-- add-breadcrumbs -->
# Nota de Embalaje

**Una nota de embalaje es un documento que enumera los productos que se encuentran en un envío.**

Por lo general se la adjunta a los bienes enviados.

Desde una Nota de Envío pueden crearse muchas Notas de Embalaje. Esto es útil cuando el envío está empaquetado en cajas diferentes. Cada caja puede tener el peso y número de Productos que contiene. Por ejemplo, si se envían 20 sillas en 4 cajas, cada caja contiene 5 sillas con diferentes Notas de Embalaje para cada caja. 

Para acceder al listado de Nota de Embalaje ir a::
> Inicio > Inventario > Herramientas > Nota de Embalaje

> Observación: Para crear Notas de Embalaje desde una Nota de Envio, la Nota de Envío debe estar en etapa de Borrador.  

## 1. Prerrequisitos
Antes de crear y utilizar una Nota de Embalaje se recomienda crear primero lo siguiente:

* [Nota de Entrega](/docs/user/manual/en/stock/delivery-note)


## 2. Cómo crear una nueva Nota de Embalaje
Por lo general, las Notas de Embalaje se crean desde una Nota de Envío cuando la misma se encuentra en estado de Borrador, sin embargo, si se desea crear una Nota de Embalaje de forma manual, seguir los pasos explicados a continuación. 

1. Ir al listado de Nota de Embalaje y hacer click en Nueva.
1. Seleccionar la Nota de Envío.
1. Ingresar el Número de Paquete de esta Nota de Embalaje.
1. Hacer click en el botón Obtener Productos para ingresar los Productos y Cantidades en la tabla de Productos.
1. Guardar.

La mayoría de estos detalles se obtendrán automáticamente si se genera la Nota de Embalaje desde una Nota de Envío.

<img class="screenshot" alt="Packing Slip" src="{{docs_base_url}}/assets/img/stock/packing-slip.png">


### 2.1 Opciones Adicionales al Crear una Nota de Embalaje
**Número de Paquete**: Si hay muchos paquetes del mismo tipo en el envío entonces conviene configurar los Números de Paquete Desde y Hasta. Por ejemplo, los números de paquete del 1 al 5 en una Nota de Embalaje, luego los números de paquete del 6 al 10 y así sucesivamente.  Esto se verá al imprimir la Nota de Embalaje. Tener en cuenta que esto sólo funcionará si el Envío contiene toda esa cantidad de Productos.

## 3. Características

### 3.1 Tabla de Productos

* Si es un Producto en Lote, es necesario seleccionar el Número de Lote.
* La Cantidad, Unidad de Medida, Peso Neto y Peso en UdM se obtendrán de la Nota de Envío.
* Salto de Página creará un salto de página justo antes de este producto al imprimir.

### 3.2 Detalles de peso del paquete

Estos detalles se verán al imprimir la Nota de Embalaje.

**Peso Neto**: Se calcula como la suma del peso de todos los Productos en la tabla.

**Peso Bruto**: Este es el peso final total, incluye el peso de los materiales de embalaje utilizados. 

**Peso Bruto UdM**: Aquí puede configurarse una UdM para el peso final del producto.

### 3.3 Papel membretado
Se puede imprimir la Nota de Embalaje en papel con el membrete de la empresa. Saber más [aquí](/docs/user/manual/en/setting-up/print/letter-head).


### 4. Temas Relacionados
1. [Inspección de Calidad](/docs/user/manual/en/stock/quality-inspection)
1. [Nota de Entrega](/docs/user/manual/en/stock/delivery-note)
