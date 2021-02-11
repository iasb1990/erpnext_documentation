<!-- add-breadcrumbs -->
# Administrar Productos Finales Rechazados

Puede suceder que algunos productos manufacturados no pases las pruebas de calidad y sean rechazados.

El proceso de fabricación estándar en ERPNext no cubre la administración de productos rechazados. Por ende se deberían crear entradas de productos finales tanto para los productos aceptados como para los rechazados. Con esto, los productos rechazados serán recibidos también en el depósito de productos finales. 

Para mover los productos rechazados desde ese depósito, se debería crear una entrada de Transferencia de Material. Debajo se encuentran los pasos para crear dicha entrada.

#### Paso 1: Nuevo Ingreso de Existencia

> Existencias > Documentos > Ingreso de Existencia > Nuevo

#### Paso 2: Finalidad

Finalidad = Transferencia de Material

#### Paso 3: Depósito

Depósito de Origen = Depósito de Productos Finales
Depósito Objetivo = Depósito de Productos Rechazados

#### Paso 4: Productos

Seleccionar los productos que no hayan pasado la prueba de calidad e ingresar el total de productos rechazados en el campo Cantidad. 

#### Paso 5: Enviar el Ingreso de Existencias

Al Guardar y Enviar el Ingreso de Existencias, las existencias de productos rechazados serán movidas desde el Depósito de Productos Finales hacia el Depósito de Productos Rechazados. 


<!-- markdown -->
