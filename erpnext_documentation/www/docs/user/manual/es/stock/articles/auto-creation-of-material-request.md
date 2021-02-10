<!-- add-breadcrumbs -->
#Creación Automática de Pedido de Material

Para prevernir faltantes de existencias se puede registrar un nivel de pedido. Cuando el nivel de existencias esta por debajo del nivel de pedido, el gerente de compras es notificado y recibe instrucciones para iniciar el proceso de compra para el producto.

En ERPNext, se puede actualizar el Nivel de Pedido y la Cantidad de Pedido en la función Producto. Si el mismo producto tiene un nivel de pedido diferente, también se puede actualizar el nivel y cantidad de pedido en base a depósitos. 

<img alt="reorder level" class="screenshot" src="{{docs_base_url}}/assets/img/articles/reorder-request-1.png">

Con el nivel de pedido , también se puede definir cuáles serán los pasos a seguir. Es decir, si iniciar una nueva compra o transferir desde otro depósito. De acuerdo con lo que se configure en la función Producto, el objetivo será actualizado a su vez en el Pedido de Material.

<img alt="reorder level next action" class="screenshot" src="{{docs_base_url}}/assets/img/articles/reorder-request-2.png">

Cuando las existencias del producto alcanzan el nivel de pedido, se crea automáticamente un Pedido de Material. Se puede habilitar esta función desde: 

`Inventario > Configuración > Configuracion de Inventario`

<img alt="active auto-material request" class="screenshot" src="{{docs_base_url}}/assets/img/articles/reorder-request-3.png">

Se creará un Pedido de Material separado para cada producto. El usuario con el rol de Gerente de Compras recibirá una alerta via mail respecto a estos Pedidos de Materiales. 

Si la creación automática del Pedido de Material falla, el usuario con el rol de Gerente de Compras será informado respecto al mensaje de error. Uno de los mensajes de error más frecuentes es:

**Ocurrió un error para ciertos productos al crear Pedido de Material en base al Nivel de Pedido.**
**Fecha 01-04-2016 no perteneciente a un Año Fiscal.**

Uno de los motivos de error puede ser también el Año Fiscal. Click [aquí](/docs/user/manual/en/accounts/articles/fiscal-year-error.html) para aprender más sobre esto.
<!-- markdown -->