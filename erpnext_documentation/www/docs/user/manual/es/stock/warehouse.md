<!-- add-breadcrumbs -->
# Depósito

**Un depósito es un edificio comercial para almacenar bienes. Los Depósitos son 
utilizados por fabricantes, importadores, exportadores, mayoristas, empresas de transporte,
aduanas, etc.**

Por lo general son edificios grandes y simples en zonas industriales de 
ciudades, y pueblos. Por lo general poseen muelles de carga para cargar y descargar 
bienes de los camiones.

La terminología de 'Depósito' en ERPNext es un poco más amplia y quizás puede ser considerada como "lugares de almacenamiento". Se pueden crear también sub-Depósitos que pueden ser una estantería dentro de la locación real. 

Esto podría convertirse en un Árbol bastante detallado como el siguiente:

*Depósito > Sala > Fila > Estante > Recipiente*

Para acceder al listado de Depósito ir a:
> Inicio > Existencias > Configuración > Depósito

## 1. Cómo crear un Depósito
1. Ir al listado de Depósito y hacer click en Nuevo.
2. Ingresar un nombre para el Depósito.
3. Configurar/revisar el Depósito Principal. Si se selecciona "Es Grupo" se pueden crear sub-depósitos bajo este grupo de Depósitos. 
4. Guardar. 

Los Depósitos son guardados con la respectiva abreviatura de la Empresa. Esto permite identificar
a simple vista a que empresa pertenece cada Depósito. 

### 1.1 Opciones Adicionales al crear un Depósito
**Cuenta**: Configurar una cuenta predeterminada para todas las transacciones con este Depósito. Configurar esta cuenta mostrará las transacciones desde este Depósito en los Libros Contables. 
**Tipo de Depósito**: Se puede crear un Tipo de Depósito para clasificar Depósitos. Por ejemplo pueden marcarse: Depósito de Proveedor, Depósito de Existencias, Depósito de Materias Primas, Salas, etc. Esta clasificación es útil para generar informes o en ciertas transacciones de existencias.  

#### Dirección y Contacto
Se pueden añadir distintos tipos de direcciones para el Depósito como por ejemplo de Facturación, de Envío, entre otras. También se puede añadir un contacto, como por ejemplo el Administrador del Depósito.

![Warehouse](/docs/assets/img/stock/warehouse.png)

### 1.2 Luego de Guardar
Luego de guardar un Depósito, aparecerán las siguientes opciones: 

* **Balance de Existencias**: Esto abrirá el informe de Balance de Existencias para ver la cantidad, valuación, balance, etc. 
* **Contabilidad General**: Esto abrirá la Contabilidad General para ver las transacciones contables. 
* **De No Grupo a Grupo**: Si el Depósito se definió como No Grupo, es decir, no puede contener otros Depósitos en su interior, este botón permitirá que es Depósito se convierta en Grupo de Depósitos.

## 2. Características

### 2.1 Vista en Árbol
Se puede cambiar a Vista de Árbol lo cuál mostrará todos los grupos y Depósitos Secundarios. 

<img class="screenshot" alt="Warehouse" src="{{docs_base_url}}/assets/img/stock/warehouse-tree.png">

### 2.2 Cuenta de Depósito
En ERPNext, si se habilita el [Inventario Permanente](/docs/user/manual/en/stock/perpetual-inventory), cada Depósito debe pertenecer a una empresa específica para mantener 
el balance de existencias ordenado por empresas. Para hacr esto, cada Depósito debería estar relacionado con una 
Cuenta en el Gráfico de Cuentas (del mismo nombre que el Depósito). Esta cuenta captura el equivalente monetario de los bienes o materiales guardados en ese depósito en particular. 

Si se cuenta con un Árbol de Depósitos más detallado, entonces es recomendable relacionar las sub-locaciones (sala, fila, estante, etc.) a la cuenta del Depósito (el Depósito principal de ese Árbol) debido a que la mayoría de las situaciones no requieren contabilizar el valor 
de existencias por cada Estante o Recipiente. Por ejemplo, si se tiene un Depósito A, con una sala, las filas son B,C, etc, entonces hay que realcionar B y C a la cuenta de A.

> Consejo: ERPNext mantiene balances de existencias para cada combinación específica de Producto y Depósito. 
Por ende, se puede obtener el balance de existencias para cualquier Producto específico en un Depósito determinado para cualquier fecha. 

### 3. Temas relacionados
1. [Motivo de Ingreso de Existencias](/docs/user/manual/en/stock/articles/stock-entry-purpose)
1. [Informe de Nivel de Existencias](/docs/user/manual/en/stock/stock-level-report)
