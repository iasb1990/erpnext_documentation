<!-- add-breadcrumbs -->
# Error de Existencias en Nota de Envío 

**Pregunta**: Al enviar una Nota de Envío, se recibe un mensaje que dice que las existencias del producto son insuficientes, pero las mismas están disponibles en el Depósito. 

**Respuesta**: Al enviar una Nota de Envío, el nivel de existencias se revisa de acuerdo con la Fecha y Hora de Publicación de la misma. Es posible que haya existencias disponibles del Producto en el Depósito. Pero, si se está creando una Nota de Envío con fecha anterior, y si los productos no estaban disponbiles en el depósito en esa Fecha y Hora de la Nota de Envío, es muy probable que se reciba un mensaje de error respecto a las existencias negativas. Para confirmar esto, referirse al informe de Inventario de Existencias. 

Si este es el caso, se deberá editar la Fecha y Hora de Publicación de la Nota de Envío y asegurarse que es luego de la Fecha y Hora de Publicación del registro de recepción del producto. 