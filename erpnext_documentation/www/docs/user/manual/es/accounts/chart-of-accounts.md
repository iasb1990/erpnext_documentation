<!-- add-breadcrumbs -->
# Plan de cuentas

**El Plan de cuentas es el listado de cuentas de la organización.**

La estructura general del Plan de cuentas está basada en un sistema contable de doble entrada, el cual se ha convertido en un estándar mundial para cuantificar el estado financiero de una compañía.

El Plan de cuentas es un gráfico de árbol que muestra los nombres de las cuentas (y grupos) que una compañía necesita para administrar la contabilidad. ERPNext crea automáticamente un Plan de cuentas básico con cada compañía, el cual puede ser modificado dependiendo de las necesidades y requerimientos legales de cada una de ellas.

Para cada compañía, el Plan de cuentas determina la forma de clasificar las entradas contables, basándose mayormente en requisitos legales (impuestos, conformidad con regulaciones estatales).

![CoA Tree](/docs/assets/img/accounts/chart-of-accounts-tree.png)

El Plan de cuentas ayuda a responder preguntas como:

 * ¿Cuánto vale la organización?
 * ¿Cuánto se debe?
 * ¿Cuál es la ganancia de la empresa? Por lo tanto, ¿cuánto se paga en impuestos?
 * ¿De cuánto son las ventas?
 * ¿Cuales son los gastos?

Para quienes están a cargo de un negocio, es muy importante saber cuán bien le está yendo económicamente.

> **Tip**: If you can’t read a Balance Sheet it's a good opportunity to start learning about this. It will be worth the effort. You can also take the help of your accountant to set up your Chart of Accounts.

Para acceder al Plan de cuentas, ingresar a:
> Inicio > Cuentas > Maestros > Plan de cuentas

## 1. Creación y edición de cuentas
ERPNext cuenta con un Plan de cuentas estándar por defecto. En lugar de crear/modificar cuentas, se puede utilizar el [Importador de Plan de cuentas](/docs/user/manual/en/setting-up/chart-of-accounts-importer). Tener en cuenta que el Plan de cuentas existente será sobrescrito al usar esta herramienta.

1. Ingresar al Plan de cuentas.
 
 Aquí se puede desplegar grupos de cuentas que contienen otras cuentas. Las opciones son "Agregar hijo" a un grupo, "Editar" o "Eliminar" la cuenta.

 <img class="screenshot" alt="Chart of Accounts" src="{{docs_base_url}}/assets/img/accounts/chart-of-accounts-add.gif">

1. La opción de crear una cuenta hija sólo aparece al clickear una cuenta de tipo grupo (carpeta). 
1. Ingresar el nombre para la nueva cuenta.
1. Ingresar un número para la cuenta.
1. Tildar "Es un grupo" si se desea que la cuenta se cree como tal y pueda contener otras cuentas.
1. Determinar el tipo de cuenta. Este dato es importante ya que algunos campos admiten sólo cierto tipo de cuentas.
1. Cambiar la divisa/moneda en caso de que esta cuenta vaya a ser usada para transacciones con determinada moneda. Por defecto se autocompleta este campo con la moneda de la compañía. Para más información, visitar la página [Contabilidad con múltiples divisas](/docs/user/manual/es/accounts/multi-currency-accounting).
1. Click en **Crear**.

Generalmente se deben crear cuentas para:

 * Viajes, salarios, teléfono, etc. dentro de **Egresos**.
 * Impuesto sobre el Valor Añadido (IVA), Impuestos de ventas, Capital, etc. dentro de **Pasivos**.
 * Ventas de productos, ventas de servicios, etc. dentro de **Ingresos**.
 * Inmueble, maquinaria, muebles, etc. dentro de **Activos**.

<img class="screenshot" alt="Chart of Accounts" src="{{docs_base_url}}/assets/img/accounts/chart-of-accounts-1.png">

> Tip: cuentas con divisas diferentes son creadas cuando se reciben o realizan pagos desde o hacia paises con distinta moneda. Por ejemplo, si se encuentra en Argentina y se realiza una transacción con Estados Unidos, se deberán crear cuentas como "Deudores US", "Acreedores US", etc.

Estos son los grupos principales de en plan de cuentas:

## 2. Tipos de cuentas
A grandes rasgos las cuentas se clasifican en ingresos, egresos (gastos), activos y pasivos.

### 2.1 Cuentas de la Hoja de balance

Las cuentas de la Hoja de balance son "Aplicación de fondos (Activos)" y "Fuentes de fondos (Pasivos)", lo cual representa el valor neto de la compañia en un momento determinado.
Cuando se inicia o finaliza un período financiero, la suma de los Activos debe ser igual a la suma de los asivos.

> **Una nota de contabilidad**: si uno es nuevo en el tema, se puede llegar a preguntar "¿cómo pueden ser los Activos iguales a los Pasivos? Eso significaría que la compañía no posee nada." Bueno, eso es correcto. Toda la "inversión" hecha en la compañía para comprar activos (como terreno, mebles, máquinas) es realizada por los dueños. Los dueños son una "obligación" de la compañía ya que las ganancias les pertenencen.

> Si una empresa estuviera por cerrar, se necesitaría vender todos los activos y pagar todas las obligaciones (incluyendo ganancias) a los dueños, dejando la compañía en sí con nada.

Todas las cuentas dentro de la Hoja de balance representan un activo que espropiedad de la compañía como "Cuenta bancaria", "Terreno e inmueble", "Muebles" o un pasivo (fondos que la compañía la debe a otros) como "Aporte de los propietarios", "Deuda" etc.

Dos cuentas especiales para tener en consideración son Cuentas por cobrar (dinero que se espera recibir de los Clientes) y Cuentas por pagar (dinero que se debe pagar a los Proveedores) dentro de Activos y Pasivos respectivamente.


### 2.2 Cuentas de pérdida y ganancia

Pérdida y ganancia es el grupo de cuentas dentro de "Ingresos" y "Egresos" que representa las transacciones contables de un determinado período.

A diferencia de las cuentas de la Hoja de balance, las cuentas de pérdida y ganancia no representan el valor neto (activos), sino más bien la cantidad de dinero gastado y obtenido por servicios al cliente durante cierto período. Por lo tanto, el inicio y al final del año fiscal, pasan a ser cero.

En ERPNext es sencillo llevar la cuenta de las pérdidas y ganancias gracias al reporte de Estado de pérdidas y ganancias.

![Profit and Loss Report]({{docs_base_url}}/assets/img/accounts/profit_n_loss_report_1.png)


Nótese que, en el primer día del año no se has registrado pérdidas o ganancias; pero de cualquier forma hay activos, por lo que las cuentas de la hoja de balance nunca vuelven a cero al inicio o final del período.

### 2.3 Grupos y cuentas

Existen dos tipos principales de cuentas en ERPNext: grupos y cuentas. Los grupos pueden tener subgrupos y cuentas dentro de ellos; mientras que las cuentas son nodos hoja del Plan de cuentas y no pueden contener otras.

Las transacciones contables sólo pueden realizarse contra cuentas (no grupos).

> Info: The term "Ledger" means a page in an accounting book where entries are
made. There is usually one ledger for each account (like a Customer or a
Supplier).

> Note: An Account “Ledger” is also sometimes called as Account “Head”.

<img class="screenshot" alt="Chart of Accounts" src="{{docs_base_url}}/assets/img/accounts/chart-of-accounts-2.png">


### 2.4 Otros tipos de cuentas

En ERPNext, también es posible especificar más información al crear una nueva cuenta, con el objetivo de poder situarla en un escenario como una "Cuenta bancaria" o una "Cuenta de impuestos" sin afectar la estructura del plan de cuentas.

Explicación de los tipos de cuentas:

* **Accumulated Depreciation**: To store the total accumulated depreciation information of the Company Assets. Accumulated depreciation appears on the balance sheet.
* **Asset Received But Not Billed**: A temporary liability account which holds the value of Asset received but not billed yet.
* **Bank**: The account type under which bank accounts will be created. There must be at least one group account of type "Bank" in the CoA.
* **Cash**: The account type under which cash account will be created. There must be at least one group account of type "Cash" in the CoA.
* **Chargeable**: Additional charges applied to Items can be stored in accounts of this type. For example, "Freight and Forwarding Charges".
* **Capital Work in Progress**: Current charges when creating Fixed Assets are stored in CWIP accounts. For example, construction costs when constructing a building. In ERPNext Assets are booked against CWIP accounts when they are not yet being used. 
* **Cost of Goods Sold**: An account under this type is used to book the accumulated total of all costs incurred while manufacturing/purchasing a product or service, sold by a Company.
* **Depreciation**: The expense account to book the depreciation of the fixed assets. This appears on the Income statement.
* **Equity**: These type of accounts represent transactions with people that own the business, i.e. the shareholders/owners.
* **Expenses Included In Asset Valuation**: The account to book the expenses (apart from the direct material costs of Assets) included in the landed cost of an Asset.
* **Expenses Included In Valuation**: The account to book the expenses (apart from direct material costs) included in the landed cost of an item/product, used in Perpetual Inventory.
* **Fixed Asset**: The account to maintain the costs of fixed assets.
* **Income Account**: This type of accounts represents any source of income or revenue booked for the Company.
* **Payable**: The account type represents the amount owed by a company to its creditors (Suppliers).
* **Receivable**: The account type represents the amount owed to a company by its debtors (Customers).
* **Round Off**: In many Invoices there can be some [rounding off](/docs/user/manual/en/accounts/articles/round-off-account-validation) in the final amount. For accurate tracking, those amounts can be booked to accounts of this type.
* **Stock**: The account group under which [Warehouse accounts](/docs/user/manual/en/accounts/articles/round-off-account-validation) will be created. 
* **Stock Adjustment**: An expense account to book any adjustment entry of stock/inventory. Generally comes at the same level of Cost of Goods Sold.
* **Stock Received But Not Billed**: A temporary liability account which holds the value of stock received but not billed yet and used in Perpetual Inventory.
* **Tax**: All tax accounts like VAT, TDS, GST, etc. come under this type.
* **Temporary**: A Temporary account is useful for balancing incomes, expenses and nullifying them when shifting to ERPNext mid-year with outstanding accounting entries.

> **Note**: When making Payment Entries, the default bank account will be fetched in the following order if set:
    
>       * Company form
>       * Mode of Payment default account
>       * Customer/Supplier default bank account
>       * Select manually in Payment Entry

### 2.5 Financial statements
Financial statements for your company are easily viewable in ERPNext. You can view financial statements
such as Balance Sheet, Profit and Loss statement, and Cash flow statement.

An Example of various financial statement are given below:

1. Cash Flow Report:
 <img class="screenshot" alt="Cash Flow Report" src="{{docs_base_url}}/assets/img/accounts/cash_flow_report.png">

1. Profit and Loss Report:
 <img class="screenshot" alt="Profit and Loss Report" src="{{docs_base_url}}/assets/img/accounts/profit_n_loss_report.png">
 
1. Balance Sheet Report:
 <img class="screenshot" alt="Balance Sheet Report" src="{{docs_base_url}}/assets/img/accounts/balance_sheet_report.png">

### 2.6 Account Number
A standard Chart of Accounts is organized according to a numerical system. Each major category will begin with a certain number, and then the sub-categories within that major category will all begin with the same number. For example, if assets are classified by numbers starting with the digit 1000, then cash accounts might be labeled 1100, bank accounts might be labeled 1200, accounts receivable might be labeled 1300, and so on. A gap between account numbers is generally maintained for adding accounts in the future.

You can assign a number while creating an account from Chart of Accounts page. You can also edit a number from account record, by clicking **Update Account Name / Number** button. On updating account number, the system renames the account name automatically to embed the number in the account name.

![Account Number]({{docs_base_url}}/assets/img/accounts/acc-no.png)

## 3. Video

<div>
 <div class="embed-container">
 <iframe src='https://www.youtube.com/embed//AcfMCT7wLLo' frameborder='0' allowfullscreen>
 </iframe>
 </div>
</div>

### 4. Related Topics
1. [Opening Balance](/docs/user/manual/en/accounts/opening-balance)
1. [Accounts Settings](/docs/user/manual/en/accounts/accounts-settings)
1. [Journal Entry](/docs/user/manual/en/accounts/journal-entry)
1. [Inter Company Journal Entry](/docs/user/manual/en/accounts/inter-company-journal-entry)
1. [Accounting Reports](/docs/user/manual/en/accounts/accounting-reports)
1. [Multi Currency Accounting](/docs/user/manual/en/accounts/multi-currency-accounting)
