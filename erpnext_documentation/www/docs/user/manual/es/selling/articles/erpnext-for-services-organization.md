<!-- add-breadcrumbs -->
# ERPNext para Empresas de Servicios

**Pregunta:** ERPNext parece diseñada para vendedores y fabricantes, pero ¿Puede ERPNext ser utilizada por empresas que ofrecen servicios?

**Respuesta:**

Alrededor del 30% de clientes de ERPNext son compañías dedicadas al sector servicios. Estas son empresas abocadas al desarrollo de software, servicios de certificación, consultores individuales y mucho mas. Nosotros mismos, al encontrarnos dentro del sector servicios utilizamos ERPNext para administrar nuestras ventas, contabilidad, asistencia y operaciones de Recursos Humanos. En el siguiente video mostramos como ERPNext utiliza ERPNext.

<iframe width="640" height="360" src="//www.youtube.com/embed/b6r7WxJMfFA" frameborder="0" allowfullscreen=""></iframe>

### Configuración Principal

La configuración para una empresa de Servicios difiere de la pensada para Productos. Las empresas de servicios no mantienen existencias de Productos y, por ende, no cuentan con Depósitos. 

Para crear un Producto (sin existencias) Servicio en la función Producto es necesario deshabilitar el campo "Mantener Existencias". 

<img alt="Service Item" class="screenshot"  src="{{docs_base_url}}/assets/img/articles/services-1.png">

Al crear una Orden de Venta para servicios seleccionar Tipo de Orden como **Mantenimiento**. La Orden de Venta de Tipo Mantenimiento requiere menos detalles comparada con las relacionadas a productos en existencia como la Nota de Envío, depósito de producto, etc. 

Las empresas de Servicios también pueden añadir productos en existencia para registrar sus activos fijos como computadoras, muebles y otros equipos de oficina. 

### Esconder Funciones Innecesarias

Como muchos módulos del estilo de Fabricación y Existencias no serán necesarios para las empresas de servicios, esos pueden ser escondidos desde: 

> Configuración > Permisos > Mostrar/Ocultar Módulos

Los Módulos cuyas casillas se encuentren sin seleccionar, serán escondidos de todos los Usuarios.

#### Configuración de Funciones

Dentro del formulario, hay muchos campos que solo resultan necesarios para empresas dedicadas a la venta y manufactura. Estos campos pueden esconderse para las empresas de servicios. La Configuración de Funciones es una herramienta donde se pueden habilitar/deshabilitar funciones específicas. Si una función está deshabilitada, entonces los campos relacionados con la misma serán escondidos de todos los formularios. Por ejemplo, si se desactiva la función Número de Serie, entonces el campo Numero de Serie será escondido tanto en la sección Producto como en todas las transacciones de compra y venta. 

[Para saber más respecto a la Configuración de Funciones, click aquí.](/docs/user/manual/en/customize-erpnext/hiding-modules-and-features).

#### Permisos

ERPNext es un sistema controlado por permisos. Los usuarios acceden al sistema de acuerdo con los permisos que les son asignados. Entonces, si a un usuario no se le asigna un Rol relacionado al módulo de Existencias y Manufactura, el mismo será escondido de ese Usuario. [Click aquí para saber más sobre administración de permisos.](/docs/user/manual/en/setting-up/users-and-permissions.html).


<!-- markdown -->
