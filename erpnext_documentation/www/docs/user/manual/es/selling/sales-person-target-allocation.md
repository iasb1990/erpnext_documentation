<!-- add-breadcrumbs -->
# Asignación de Objetivos a Vendedores

**Es la asignación de los Vendedores a un producto o territorio.**

Además de administrar a los Vendedores, ERPNext también permite asignar objetivos a Vendedores de acuerdo con Grupos de Productos y Territorio. De acuerdo al objetivo asignado y a las ventas efectivamente realizadas por el Vendedor, se obtiene el Informe de Cumplimiento de Objetivo para el Vendedor. 

## 1. Vendedor- Asignación de Objetivos por Grupo de Productos 

### 1.1 Abrir la Ventana de Vendedor 

Para asignar un objetivo se debe abrir el perfil del Vendedor. 

**Comercialización > Socios Comerciales y Territorio > Vendedor > Editar**

### 1.2 Asignación de Objetivo por Grupo de Productos

En el perfil de Vendedor, se encuentra una tabla denominada Objetivo del Vendedor. 

<img class="screenshot" alt="Sales person target" src="{{docs_base_url}}/assets/img/selling/sales-person-target-item-group.png">

En esta tabla se debe seleccionar Grupo de Productos, Año Fiscal, Cantidad Objetivo, Monto Objetivo, y Distribución de Objetivo.  

Se puede asignar objetivos en monto, cantidad o ambos. El Grupo de Productos puede dejarse en blanco. En este caso, el sistema calculará el objetivo de acuerdo con Todos los Grupos de Productos. 

**Distribución de Objetivo**

Se puede distribuir el objetivo en meses. En este caso, es necesario crear una nueva distribución mensual, se puede ver esta opción haciendo click en el campo Distribución de Objetivo en la Tabla de Objetivo. Por ejemplo, un objetivo de venta de 1000 unidades para el primer cuatrimestre del año fiscal 2019-2020 como se muestra en la captura de pantalla anterior.

<img class="screenshot" alt="Target Distribution" src="{{docs_base_url}}/assets/img/selling/sales-person-target-distribution.png">

### 1.3 Informe - Cumplimiento de Objetivos del Vendedor por Grupo de Productos

Para ver este informe ir a: 

**Comercialización > Otros Informes > Cumplimiento de Objetivos del Vendedor por Grupo de Productos**

Este informe mostrará la diferencia entre el objetivo del vendedor y su desempeño. Este informe esta basado en el Informe de Órdenes de Venta. 

En este informe, el objetivo asignado al Vendedor era una cantidad de aproximadamente 83 unidades en un mes, el Vendedor alcanzó 80 en el momento en que se ve el informe, por ende la diferencia es de 3, como se muestra a continuación. 

<img class="screenshot" alt="Target Item Group" src="{{docs_base_url}}/assets/img/selling/sales-person-item-group-report.png">

**Observación:** Para que el informe refleje los detalles correctamente, es necesario relacionar al Vendedor con una Orden de Venta en la sección Equipo de Ventas de la Orden de Venta. A su vez, la misma debe haber sido enviada. 

---

## 2. Vendedor - Asignación de Objetivo por Territorio 

Para asignar a un Vendedor objetivos de acuerdo a un Territorio, es necesario seleccionar al Vendedor en la función Territorio. Este Vendedor es ingresado allí solo para tener la referencia. Los detalles del Vendedor no se actualizarán en el Informe de Cumplimiento de Objetivos por Territorio.

### 2.1 Ir a la función Territorio

**Comercialización > Configuración > Territorio > (Editar territorio específico)**

En el Territorio seleccionado, se encontrará un campo para elegir al Administrador del Territorio. Este campo esta relacionado a la función "Vendedor". 

<img class="screenshot" alt="Sales Person Territory Manager" src="{{docs_base_url}}/assets/img/selling/sales-person-territory-manager.png">

### 2.2 Asignar objetivo

La Asignación de Objetivo en la función Territorio es Similar a la de Vendedor. Se pueden seguir los mismos pasos explicados en la sección  _1.2 Asignación de Objetivo por Grupo de Productos_ para especificar el objetivo en la función Territorio. 

### 2.3 Informe - Cumplimiento de Objetivos en Territorio de acuerdo a Grupo de Productos 

Este informe mostrará la diferencia entre el objetivo y el desempeño de las Ventas en un territorio específico. Este informe se basa en el infome de Orden de Venta. Aunque se puede seleccionar un Vendedor en la función Territorio, sus detalles no serán incluidos en el informe. 

**Observación** el territorio del Cliente/Clientes debe estar bien configurado para que el infome funcione. Por ejemplo, en la captura de pantalla mostrada a continuación, el objetivo era de aproximadamente 8 unidades y se llegó a 5, con lo cual la diferencia es de 3. 

<img class="screenshot" alt="Sales Person Territory Report" src="{{docs_base_url}}/assets/img/selling/sales-person-territory-report.png">

---

## 3. Distribución de Objetivo

Para crear una nueva Distribución Mensual ir a: 
**Contabilidad > Distribución Mensual**

Los documentos de Distribución de Objetivo permiten dividir el objetivo asignado a lo largo de varios meses. Si los productos y servicios son de temporada, se puede distribuir el objetivo de venta acorde a la misma. Por ejemplo, si se trata de la venta de paraguas, el objetivo asignado en la época de monzones será más alto que el de otros meses. 

<img class="screenshot" alt="Target Distribution" src="{{docs_base_url}}/assets/img/selling/target-distribution.png">

Se puede utilizar la Distribución Mensual al asignar objetivos a Vendedores y Territorio.

### 4. Temas relacionados
1. [Vendedores en Operaciones de Venta](/docs/user/manual/en/selling/articles/sales-persons-in-the-sales-transactions)
1. [Utilizando Vendedores en transacciones](/docs/user/manual/en/selling/articles/sales-persons-in-the-sales-transactions)

{siguiente}
