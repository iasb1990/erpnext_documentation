<!-- add-breadcrumbs -->
# Grupo de Proveedores
**El Grupo de Proveedores es un conjunto de proveedores que son similares en algun sentido.**

Un proveedor puede distinguirse de un contratista o subcontratista, quien  
por lo general realiza un aporte especializado a los producto. Un proveedor es también conocido como 
vendedor. Hay distintos tipos de proveedores de acuerdo con los bienes y
productos que proveen.

ERPNext permite crear categorías personalizadas de proveedores. Estas 
categorias son conocidas como Grupos de Proveedores. Por ejemplo, si se cuenta principalmente con 
empresas farmacéuticas y distribuidores FMCG, se pueden crear 
nuevos Grupos de Proveedores y nomenclarlos de forma acorde.

Para acceder a Grupos de Proveedores ir a:
> Inicio > Adquisiciones > Proveedor > Grupo de Proveedores

## 1. Prerrequisitos
Antes de crear y utilizar un Grupo de Proveedores, es aconsejable crear lo siguiente: 

* [Proveedor](/docs/user/manual/en/buying/supplier)

## 2. Cómo Crear un Grupo de Proveedores
1. Ir al listado de Grupo de Proveedores y hacer click en Nuevo
1. Escribir un nombre para la nueva Categoría de Proveedores
1. Se puede configurar un Grupo de Proveedores Principal para este Grupo de Proveedores. 
1. Hacer click en la casilla Es Grupo lo convertirá en un Grupo de Proveedores Principal.
1. Tambien se puede asignar una Plantilla de Condiciones de Pago predeterminada al Grupo de Proveedores. Esto resulta últil en caso de que, por ejemplo, todos los proveedores de hardware pidan la mitad del pago al generar la orden de venta y la otra mitad luego del envío. 
1. Guardar.

<img class="screenshot" alt="Supplier Group" src="{{docs_base_url}}/assets/img/buying/supplier-group.png">

Se puede clasificar a los proveedores dentro de un rango de opciones disponibles en ERPNext.
Seleccionar dentro de una serie de opciones como Distribuidor, Electrónico, Hardware, Local, Farmacéutico, Materias Primas, Servicios, etc. Clasificar a los proveedores en diferentes tipologías facilita la contabilidad y los pagos. 

## 3. Árbol de Grupo de Proveedores

También se puede construir un Grupo de Proveedores en forma de jerárquica de Árbol, de
forma similar al Plan de Cuentas.

Para ver la estructura de Árbol, hacer click en **Árbol** en la barra lateral. Para volver a la vista de lista seleccionar: **Menu > Ver Lista**.

<img class="screenshot" alt="Supplier Group" src="{{docs_base_url}}/assets/img/buying/supplier-group-tree.png">

Con los nuevos [Permisos de Usuario](/docs/user/manual/en/setting-up/users-and-permissions)
pueden aplicarse permisos basados en jerarquias. 
Esto quiere decir que, si un usuario tiene permitdo ver el nodo principal del Grupo de Proveedores,
el/ella califican para ver los nodos secundarios de ese nodo principal. 

Por ejemplo, en la imagen mostrada anteriormente, digamos que el permiso es aplicado or example, 
para un usuario para ver el documento "Distribuidor". Por ende, el usuario tambien tiene permiso para
ver sus nodos secundarios como "Distribuidor de Libros", "Distribuidor Electrónico", etc. 

### 4. Temas Relacionados
1. [Proveedor](/docs/user/manual/en/buying/supplier)

{next}
