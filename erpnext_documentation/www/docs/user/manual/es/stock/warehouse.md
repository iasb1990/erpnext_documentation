<!-- add-breadcrumbs -->
# Almacén

**Un Almacén es un edificio comercial para almacenar bienes. Los Almacenes son 
utilizados por fabricantes, importadores, exportadores, mayoristas, empresas de transporte,
aduanas, etc.**

Por lo general son edificios grandes y simples en zonas industriales de 
ciudades, y pueblos. Por lo general poseen muelles de carga para cargar y descargar 
bienes de los camiones.

La terminología de 'Almacén' en ERPNext es un poco más amplia y quizás puede ser considerada como "lugares de almacenamiento". Se pueden crear también sub-almacenes que pueden ser una estantería dentro de la locación real. 

Esto podría convertirse en un Árbol bastante detallado como el siguiente:

*Almacén > Sala > Fila > Estante > Recipiente*

Para acceder al listado de Almacén ir a:
> Inicio > Existencias > Configuración > Almacén

## 1. Cómo crear un Almacén
1. Ir al listado de Almacén y hacer click en Nuevo.
2. Ingresar un nombre para el Almacén.
3. Configurar/revisar el Almacén Principal. Si se selecciona "Es Grupo" se pueden crear sub-almacenes bajo este grupo de Almacenes. 
4. Guardar. 

Los Almacén son guardados con la respectiva abreviatura de la Empresa. Esto permite identificar
a simple vista a que empresa pertenece cada Almacén. 

### 1.1 Opciones Adicionales al crear un Almacén
**Cuenta**: Configurar una cuenta predeterminada para todas las transacciones con este Almacén. Configurar esta cuenta mostrará las transacciones desde este Almacén en los Libros Contables. 
**Tipo de Almacén**: Se puede crear un Tipo de Almacén para clasificar Almacenes. Por ejemplo pueden marcarse: Almacén de Proveedor, Almacén de Existencias, Almacén de Materias Primas, Salas, etc. Esta clasificación es útil para generar informes o en ciertas transacciones de existencias.  

#### Dirección y Contacto
Se pueden añadir distintos tipos de direcciones para el Almacén como por ejemplo de Facturación, de Envío, entre otras. También se puede añadir un contacto, como por ejemplo el Administrador del Almacén.

![Warehouse](/docs/assets/img/stock/warehouse.png)

### 1.2 Luego de Guardar
Luego de guardar un Almacén, aparecerán las siguientes opciones: 

* **Balance de Existencias**: Esto abrirá el informe de Balance de Existencias para ver la cantidad, valuación, balance, etc. 
* **Contabilidad General**: Esto abrirá la Contabilidad General para ver las transacciones contables. 
* **De No Grupo a Grupo**: Si el Almacén se definió como No Grupo, es decir, no puede contener otros Almacenes en su interior, este botón permitirá que es Almacén se convierta en Grupo de Almacenes.

## 2. Características

### 2.1 Vista en Árbol
Se puede cambiar a Vista de Árbol lo cuál mostrará todos los grupos y Almacenes Secundarios. 

<img class="screenshot" alt="Warehouse" src="{{docs_base_url}}/assets/img/stock/warehouse-tree.png">

### 2.2 Cuenta de Almacén
En ERPNext, si se habilita el [Inventario Permanente](/docs/user/manual/en/stock/perpetual-inventory), cada Almacén debe pertenecer a una empresa específica para mantener 
el balance de existencias ordenado por empresas. Para hacr esto, cada Almacén debería estar relacionado con una 
Cuenta en el Gráfico de Cuentas (del mismo nombre que el Almacén). Esta cuenta captura el equivalente monetario de los bienes o materiales guardados en ese almacén en particular. 

Si se cuenta con un Árbol de Almacenes más detallado, entonces es recomendable relacionar las sub-locaciones (sala, fila, estante, etc.) a la cuenta del Almacén (el Almacén principal de ese Árbol) debido a que la mayoría de las situaciones no requieren contabilizar el valor 
de existencias por cada Estante o Recipiente. Por ejemplo, si se tiene un Almacén A, con una sala, las filas son B,C, etc, entonces hay que realcionar B y C a la cuenta de A.

> Consejo: ERPNext mantiene balances de existencias para cada combinación específica de Producto y Almacén. 
Por ende, se puede obtener el balance de existencias para cualquier Producto específico en un Almacén determinado para cualquier fecha. 

### 3. Temas relacionados
1. [Motivo de Ingreso de Existencias](/docs/user/manual/en/stock/articles/stock-entry-purpose)
1. [Informe de Nivel de Existencias](/docs/user/manual/en/stock/stock-level-report)
