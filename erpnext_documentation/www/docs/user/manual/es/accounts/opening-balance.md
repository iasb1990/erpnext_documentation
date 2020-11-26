<!-- add-breadcrumbs -->
# Apertura de cuentas

**La Apertura de cuentas es el balance realizado al inicio del período contable tomando como base el cierre del período anterior o cuando la compañía recién está comenzando.**

Esto también aplica al arrancar una nueva compañía por lo que los balances realizados fuera de ERPNext deberían ser importados previamente.

## 1. Introducción

Si la compañía es nueva, se tendrán algunos balances para importar. Sin embargo, si se está migrando desde otro sistema es posible que haya una cantidad considerable de información para importar.

Se recomienda comenzar a usar ERPNext para contabilizar desde un nuevo año fiscal; pero se puede comenzar en cualquier momento. Para establecer las cuentas se necesitará la siguiente información para el día en el que se comience a usar ERPNext:

### Activos
1. Activos de stock (stock en mano).
1. Activos fijos como muebles, computadoras, etc.
1. Cuentas a cobrar, por ejemplo, facturas impagas que fueron enviadas al Cliente.
1. Activos corrientes como balances bancarios, efectivo en mano, depósitos, etc.

### Pasivos
1. Cuentas de Capital como el capital de accionistas (o dueños)
1. Pasivos corrientes como préstamos, pago de salarios, etc.
1. Cuentas a pagar, por ejemplo, facturas impagas que fueron enviadas por los Proveedores


Si se estaba utilizando algún otro software contable, se deberán **cerrar** los estados financieros en ese sistema primero. El cierre de los balances debería ser trasladado como una apertura de cuentas en ERPNext. Antes de hacer esto, es importante asegurarse de que el [Plan de cuentas](/docs/user/manual/es/accounts/chart-of-accounts) posee todas las cuentas requeridas.

Los asientos de apertura se pueden crear usando la Herramienta de Apertura de Creación de Facturas de ERPNext.

> Los asientos de apertura son solo para cuentas de Hoja de balance, no para cuentas de pérdida y ganancia.

## 2. Apertura de cuentas de Activo

2.1 [Activos fijos](/docs/user/manual/es/accounts/opening-balance/fixed_assets)

2.2 [Activos de stock](/docs/user/manual/es/stock/opening-stock)

2.3 [Cuentas a cobrar](/docs/user/manual/es/accounts/opening-balance/accounts_receivable)

2.4 [Activos corrientes](/docs/user/manual/es/accounts/opening-balance/current_assets)

## 3. Apertura de cuentas de Pasivo

3.1 [Cuentas de Capital](/docs/user/manual/es/accounts/opening-balance/capital_accounts)

3.2 [Pasivos corrientes](/docs/user/manual/es/accounts/opening-balance/current_liabilities)

3.3 [Cuentas a pagar](/docs/user/manual/es/accounts/opening-balance/accounts_payable)

## 4. Verificación de la apertura de cuentas

Una vez que los activos y pasivos fueron importados, el balance de la cuenta de **Apertura temporaria** debería ser cero.

## 5. Paso a paso


### 6. Temas relacionados
1. [Plan de cuentas](/docs/user/manual/es/accounts/chart-of-accounts)
1. [Asiento contable](/docs/user/manual/es/accounts/journal-entry)
1. [Entrada de pago](/docs/user/manual/es/accounts/payment-entry)
1. [Conciliación de pagos](/docs/user/manual/es/accounts/payment-reconciliation)

{next}
