# Configuración de Ventas

La Configuración de Ventas es donde se pueden definir las propiedades y validaciones que luego serán aplicadas a las transacciones involucradas en el ciclo de ventas.

Veamos las opciones disponibles dentro de la Configuración de Ventas en ERPNext.

<img class="screenshot" alt="Selling Settings" src="{{docs_base_url}}/assets/img/selling/selling-settings.png">

Para acceder a la Configuración de Ventas ir a:
> Inicio > Comercialización > Configuraciones > Configuración de Ventas

## 1. Nomenclatura
### 1.1 Denominación de clientes

Cuando un cliente es guardado, se genera una identificación única para ese cliente.

La configuración predeterminada genera esa identificación utilizando el Nombre del Cliente. Si, en cambio, se prefiere guardar un cliente utilizando una nomenclatura hay que seleccionar, en el campo Nomenclatura de Cliente, establecer valor como "Nomenclatura". De esa forma, los clientes se verían así - "CUST00001, CUST00002, CUST00003...", etc.

Se puede configurar una Nomenclatura de clientes desde:

**Configuración > Datos > Nomenclatura**

### 1.2 Denominación de Campañas

Al igual que para los clientes, se puede configurar la nomenclatura para las Campañas. De forma predeterminada, la campaña se guardará bajo el Nombre de Campaña. 

## 2. Configuración predeterminada
### 2.1 Grupo de clientes y territorio predeterminados

Seleccionar un Grupo de Clientes predeterminado que será actualizado automáticamente al crear un nuevo Cliente. 

Las Cotizaciones pueden ser creadas tanto para Clientes como para Potenciales Clientes. Cuando una Cotización realizada a un Potencial Cliente se convierte en Orden de Venta, el sistema intenta convertir a ese Potencial Cliente en Cliente. Al crear un Cliente en la base de datos, los valores para Grupo de Clientes y Territorio son tomados de la Configuración de Ventas. Si no se encuentran valores predeterminados para Grupo de Clientes o Territorio, se recibirá un mensaje de validación que solicitará el mencionado Grupo de Clientes o Territorio. También es posible convertir un Potencial Cliente en Cliente de forma manual. 

### 2.2 Lista de Precios predeterminada

La Lista de Precios establecida en este campo será utilizada de forma automática en el campo de Lista de Precios de las transacciones de venta como Cotización, Orden de Venta, Nota de Envío, y Factura de Venta. 

### 2.3 Cerrar Oportunidad transcurrida determinada cantidad de días

Si hay muchas Oportunidades con un estado distinto a Abierto, las mismas serán cerradas automáticamente luego de transcurridos los días establecidos en este campo.

### 2.4 Validez predeterminada de la cotización

Las cotizaciones realizadas para los clientes solo son válidas durante una cierta cantidad de días. En la Cotización se puede actualizar de forma manual la Fecha de Validez. De forma predeterminada, la misma será establecida en 30 días desde la fecha de realización de la Cotización. Se puede cambiar esa cantidad de días en este campo de acuerdo a las características del negocio. 

## 3. Configuración de requisitos
### 3.1 Se requiere Orden de Venta

Si se desea que sea obligatoria la creación de una Orden de Ventas antes de crear una Factura de Ventas, hay que establecer el parámetro "Se requiere Orden de Venta" como "Si". De forma predeterminada este campo estará en "No". 

Esta configuración puede ser cambiada para un cliente en particular haciendo click en la caja "Permitir Crear Factura de Venta sin Orden de Venta" en el perfil del cliente. 

<img alt="Sales Order Required" class="screenshot" src="{{docs_base_url}}/assets/img/selling/so-required.png">

### 3.2 Se requiere Nota de Envío

Para que sea obligatoria la creación de una Nota de Envío antes de generar la Factura de Venta este campo debería configurarse en "Si". De forma preestablecida se encontrará en "No". 

Esta configuración puede ser cambiada para un cliente en particular haciendo click en la caja "Permitir Crear Factura de Venta sin Nota de Envío" en el perfil del cliente.

<img alt="Delivery Note Required" class="screenshot" src="{{docs_base_url}}/assets/img/selling/dn-required.png">

### 3.3 Frecuencia de Actualización de Ventas
Esta es la frecuencia con la cual se actualizarán el avance de los proyectos y los detalles de las transacciones de una empresa. De forma predeterminada, esta actualización se dará con Cada Transacción, sin embargo, si la frecuencia de transacciones es muy alta, también se puede configurar la actualización para que se realice de forma Diaria o Mensual. 

## 4. Otras configuraciones
### 4.1 Mantener las tarifas a lo largo del Ciclo de Ventas

El sistema de forma predeterminada validará el mismo precio de producto a lo largo del ciclo de ventas (Orden de Venta -> Nota de Envío -> Factura de Venta). Si se espera que el precio del producto varie dentro del mismo ciclo, debiendo evitar que suceda la validación mencionada anteriormente, esta caja debe estar sin clickear. 

### 4.2 Permitir al usuario editar el Precio del Producto

La tabla de productos en las transacciones de venta contiene un campo llamado Listado de Precios. Este campo esta configurado de forma preestablecida para no permitir ediciones en todas las transacciones de venta. Esto es para asegurar que el precio de un producto será obtenido del registro de Precio de Producto y que el usuario no pueda editarlo. 

Si resulta necesario editar el Precio de Producto obtenido del Listado de Precios, esta casilla debería estar sin clickear.

### 4.3 Permitir que un Producto sea añadido mas de una vez en una transacción
Este es un campo de validación que impide que un producto sea añadido más de una vez en una transacción cuando se encuentra sin clickear. En algunos casos esto puede resultar necesario, por ende, si es así, hacer click en esta casilla de verificación. 

### 4.4 Permitir más de una Orden de Venta proveniente de una sola Orden de Compra 
Al crear una Orden de Venta, se puede actualizar el Número y la Fecha de la Orden de Compra recibida del cliente. Se podrá crear solo una Orden de Venta por cada Número y Fecha. Sin embargo, si se desea permitir la creación de múltiples Órdenes de Venta por cada Número de Orden de Compra, hacer click en la casilla "Permitir más de una Orden de Venta proveniente de una sola Orden de Compra". 

### 4.5 Validar el Precio de Venta del Producto en relación a su Precio de Compra o Valuación. 
Al realizar una venta es importante saber que no esta incurriendo en pérdidas. Al validar este campo, el Precio de Venta del Producto será comparado con su precio de compra o valuación. Si el precio de venta del producto es menor que el precio de compra se recibirá un aviso si la casilla de verificación está seleccionada.

### 4.6 No Mostrar la Identificación Fiscal del Cliente en las Transacciones de Venta
Debido a las reglamentaciones, la mayoría de los clientes poseen una Identificación Fiscal única. A su vez, la misma debe ser utilizada en las transacciones de venta. Sin embargo, si no se desea utilizar esta función, se puede deshabilitar al hacer click en esta casilla. 

{siguiente}
