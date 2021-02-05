# Cupón de Descuento

**El Cupón de Descuento permite a un cliente acceder a descuentos en productos adquiridos a través del carrito de compras.**

¡Todos aman los descuentos! Por ende es una buena estrategia hacer cupones que los ofrezcan. Para alentar a los Clientes a comprar desde el sitio web, la función de cupón de descuento es interesante.

Hay revendedores u otros sitios que generan potenciales clientes para el sitio web ERPNext de otra empresa. 

Cuando el cliente potencial viene a realizar una compra desde otro sitio o desde campañas de e-mail hacia el sitio web de ERPNext se puede:
	
	a) Rastrear desde que afiliado o Socio Comercial proviene el cliente potencial [código de referencia]
	(/docs/user/manual/en/selling/sales-partner)

	b) Otorgar descuentos (de acuerdo con la Pautas de Tarifas) sobre la totalidad de la compra, es decir, cupón de descuento

Para acceder al listado de Cupón de Descuento ir a:

> Inicio > Contabilidad > Cupón de Descuento


## 1. Prerrequisitos

1. La función de Cupón de Descuento debe ser activada desde la Configuración del Carrito de Compras:

	> Inicio > Configuración > Configuración del Carrito de Compras

	<img class="screenshot" alt="Shopping Cart Settings to enable Coupon Code" src="{{docs_base_url}}/assets/img/selling/coupon-code-shoppingcart-settings.png">

2. Crear una Pauta de Tarifa activando la función **Cupón de Descuento**.

## 2. Cómo crear un Cupón de Descuento

1. Ir al listado Cupón de Descuento y hacer click en Nuevo.
2. Ingresar el **Nombre del Cupón**, por ejemplo "AHORRAR 20"
3. Al seleccionar el **Tipo de Cupón**, se puede elegir entre Promocional o Tarjeta de Regalo.
   	
	Promocional es para promover un plan general.
   	
	Tarjeta de regalo es para generar cupones de descuento de forma aleatoria y distriburilos a clientes o usuarios específicos. 
   
4. El **Cupón de Descuento** es un código en mayúsculas, único y de solo lectura que es generado de acuerdo al Tipo de Cupón y al Nombre del Cupón. 
	
	Para Tipo de Cupón,
	
	a) *Promocional* , elimina todos los espacios y toma hasta los primeros 8 caracteres, por ejemplo, AHORRA20
	
	b) *Tarjeta de regalo* , genera un código aleatorio de 11 dígitos, por ejemplo, AP48K7CT9LP

    Puede ser utilizado en la página del carrito de compras, antes de realizar el pedido, para acceder al descuento. 
  
4. Seleccionar la [Pauta de Tarifa](/docs/user/manual/en/accounts/pricing-rule)  activando la función **cupón de descuento**. 

5.Hacer click en Guardar.

	<img class="screenshot" alt="Coupon Code Doctype" src="{{docs_base_url}}/assets/img/selling/coupon-code.png">

## 3. Características

### 3.1 Validez y utilización

1. **Válido Desde-Hasta** - validez del cupón
2. **Uso Máximo** - Para limitar el uso del código de descuento
3. **Uso** - El conteo de Uso se incrementará en 1 por cada Orden de Venta que se envíe utilizando el cupón de descuento.
4. **Descripción del Cupón de Descuento** - puede ser utilizada al crear la plantilla de email a fin de informar a los potenciales clientes sobre el cupón de descuento y el sistema. 

	<img class="screenshot" alt="Pricing Rule Coupon Code Based" src="{{docs_base_url}}/assets/img/selling/coupon-code-pricing-rule.png">



### 3.2 El Cupón de Descuento puede ser aplicado de dos maneras

1. A través de una URL, a fin de que sea más simple para el usuario su utilización, el cupón de descuento será tomado automáticamente desde el parámetro ("cc") de la URL e insertado en el cuadro de texto Aplicar Descuento.

	http://xyz.erpnext.com/products/golden-ring?cc=SAVE5

2. Aplicar el cupón explícitamente en la página del carrito de compras completando los datos del cupón y haciendo click en "Aplicar Cupón de Descuento", como se muestra más abajo 

	<img class="screenshot" alt="Shopping Cart Apply CouponCode" src="{{docs_base_url}}/assets/img/selling/coupon-code-pricing-rule.png">

Si el cupón de descuento es aplicado de forma exitosa, el precio se actualizará automáticamente.


### 4. Temas relacionados

1. [Carrito de Compras](/docs/user/manual/en/website/shopping-cart)
2. [Pautas de Tarifas](/docs/user/manual/en/accounts/pricing-rule)
