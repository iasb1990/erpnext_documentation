<!-- add-breadcrumbs -->
# Unidad de Medida (UdM)

**Una UdM es una unidad que se utiliza para medir los Productos.**

Hay muchas UdM creadas de forma predeterminada en ERPNext. Sin embargo, pueden añadirse más de acuerdo con las necesidades del negocio que las utilice.  
En las UdM hay una opción "Debe ser Número Entero". Si esta casilla está habilitada, no se pueden utilizar fracciones en esta UdM. Para saber más respecto a fracciones y UdMs ver [esta página](/docs/user/manual/en/stock/articles/managing-fractions-in-uom).

La lista UdM en sí misma solo guarda el nombre. Las tasas de conversión son almacenadas en un documento llamado "Factor de Conversión de UdM". Si se suman nuevas UdMs y se piensa utilizarlas en transacciones donde deberán convertirse en otras UdMs, es aconsejable que se las añada a esta lista.

Por ejemplo, aquí 1 Kilo es aproximadamente 2,2 Libras y el factor de conversión exacto es almacenado: 

![UoM conversion factor](/docs/assets/img/stock/uom_convert.png)
