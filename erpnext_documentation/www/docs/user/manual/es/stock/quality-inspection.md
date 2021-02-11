<!-- add-breadcrumbs -->
# Inspección de Calidad

En ERPNext, se puede configurar que los productos entrantes o salientes pasen por Inspecciones
de Calidad.

Para habilitar esta función ir a:
> Inicio > Inventario > Herramientas > Inspección de Calidad

## 1. Prerrequisitos
Antes de crear y utilizar una Inspección de Calidad, se recomienda crear lo siguiente: 

* [Producto](/docs/user/manual/en/stock/item)
* Habilitar los Criterios de Inspección de Calidad en la función Producto: 
    ![Enable Quality Inspection](/docs/assets/img/stock/enable-quality-inspection.png)

## 2. Cómo crear una Nueva Inspección de Calidad

1. Desde un Recibo de Compra/Nota de Envío en la etapa Borrador, ir al campo Inspección de Calidad en la tabla de Productos y hacer click en Crear Nueva Inspección de Calidad.
1. Seleccionar el tipo de inspección, sea Ingreso (Compra), Egreso (Ventas), o En Curso (Fabricación). 
1. Seleccionar el tipo de documento de Referencia, es decir Recibo de Compra, Factura de Compra, Nota de Envío, Factura de Venta o Registro de Inventario. 
1. Seleccionar el Producto y configurar el tamaño de la meustra a ser inspeccionada. Tener en cuenta que solo se tomarán aquellos Productos que tengan habilitados Criterios de Inspección en la función Producto.  
1. Se utilizará la Plantilla de Inspección de Calidad configurada en la función Producto. 
1. Se puede cambiar quién realizará la inspección y tambien añadir quién la verificará. 
1. Puede añadirse cualquier otra Observación respecto a la Inspección. 
1. Guardar y Enviar.

<img class="screenshot" alt="Quality Inspection" src="{{docs_base_url}}/assets/img/stock/quality-inspection.png">

## 3. Temas Relacionados
1. [Recibo de Compra](/docs/user/manual/en/stock/purchase-receipt)
1. [Nota de Envío](/docs/user/manual/en/stock/delivery-note)
1. [Entrada de Inventario](/docs/user/manual/en/stock/stock-entry)
1. [Factura de Venta](/docs/user/manual/en/accounts/sales-invoice)
1. [Factura de Compra](/docs/user/manual/en/accounts/purchase-invoice)
