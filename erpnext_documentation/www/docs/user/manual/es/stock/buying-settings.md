<!-- add-breadcrumbs -->
# Configuraciones de Compra

Las Configuraciones de Compra es donde se pueden definir las propiedades que luego serán aplicadas a las transacciones del módulo de Compra.
Se pueden encontrar las Configuraciones de compra en:
> Inicio > Adquisiciones > Configuraciones > Configuraciones de Compra

![Buying Settings]({{docs_base_url}}/assets/img/buying/buying-settings.png)

Veamos las opciones disponibles que pueden ser configuradas:

## 1. Proveedor
### 1.1 Denominación de Proveedores

Cuando un proveedor es guardado, el sistema genera una identificación única o nombre para ese Proveedor la cual podrá ser utilizada para hacer referencia al mismo en distintas transacciones de Compra. 

Si no está configurado de otra forma, ERPNext utiliza el Nombre del Proveedor como el nombre único. Si se quiere identificar a los Proveedores utilizando nombres como SUPP-00001, SUPP-00002, u otras series pautadas, seleccionar el valor de Nomenclatura de Proveedor De Acuerdo a cómo "Nombres en Serie".

Se puede definir o seleccionar el patrón de Series de Nombres desde: **Configuraciones > Información > Nombres en Serie**

[Click aquí](/docs/user/manual/en/setting-up/settings/naming-series) para saber más respecto a definir Nombres en Serie. 

### 1.2 Grupo de Proveedores Predeterminado

Configurar lo que debería ser el valor predeterminado de Grupo de Proveedores al crear un nuevo Proveedor. Por ejemplo, si la mayoría de los proveedores son de hardware, se puede establecer el valor predeterminado como "Hardware". 

## 2. Compras
### 2.1 Lista de Precios predeterminada

Configurar la Lista de Precios Predeterminada, la cual se usará al crear una nueva Transacción de Compra, el valor predeterminado es "Compra Estándar". Los precios de los productos serán obtenidos de esta Lista de Precios. Se puede modificar la "Lista de Precios" utilizando la flecha en la parte inferior derecha del campo para cambiar la moneda y el país. 

### 2.2 Se requiere Orden de Compra

Si esta opción está configurada como "Si", ERPNext no permitirá crear una Factura de Compra o Recibo de Compra sin crear primero una Orden de Compra. Si se generan transacciones al por menor, donde el pedido sucede fuera de  línea, entonces la Orden de Compra puede saltearse. Si se están aceptando Productos de muestra, se puede crear directamente un Recibo de Compra para recibir los Productos en el Depósito.  

Esta configuración puede ser anulada para un proveedor en particular al habilitar la casilla "Permitir la Creación de Factura de Compra sin Orden de Compra", en la función proveedor. 

<img alt="Purchase Order Required" class="screenshot" src="{{docs_base_url}}/assets/img/buying/po-required.png">

### 2.3 Se requiere Recibo de Compra

Si esta opción está configurada como "Si",ERPNext no permitirá crear Factura de Compra sin primero crear un Recibo de Compra. En caso de que el Producto en transacción sea un servicio, no requerirá un recibo, se puede crear una Factura directamente.  

Esta configuración puede ser anulada para un proveedor en particular al habilitar la casilla "Permitir la Creación de Factura de Compra sin Recibo de Compra", en la función proveedor. 

<img alt="Purchase Receipt Required" class="screenshot" src="{{docs_base_url}}/assets/img/buying/pr-required.png">

### 2.4 Mantener Mismo Precio A Lo Largo del Ciclo de Compras 

Si esto está seleccionado, ERPNext no permitirá cambiar el precio de un Producto en una Factura de Compra o Recibo de Compra creado desde una Orden de Compra, es decir, mantendrá el mismo precio a lo largo del ciclo de compras. Si existe la posibilidad de que el precio del Producto pueda cambiar, se debe deshabilitar esta opción.

## 3. Permitir que el Producto sea Añadido Muchas Veces

Cuando esta casilla está deshabilitada, un producto no puede ser añadido muchas veces en la misma Orden de Compra. Sin embargo, se puede cambiar la cantidad. Esta es una casilla de verificación para prevenir compras accidentales del mismo producto. Puede ser habilitada para usos específicos donde hay muchas fuentes para el mismo material, por ejemplo, en fabricación. 

### 4. Temas Relacionados
1. [Grupo de Proveedores](/docs/user/manual/en/buying/supplier-group)

{next}