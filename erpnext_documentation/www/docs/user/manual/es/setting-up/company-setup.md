<!-- add-breadcrumbs -->
# Compañía

**Una compañía es una entidad legal conformada por un grupo de personas con el objetivo de llevar adelante una iniciativa comercial o industrial.**

En ERPNext, la primera compañia es creada junto con la cuenta de ERPNext. Por cada compañía, se puede determinar una actividad principal como manfactura, ventas minoristas o servicios, entre otros.

Si se tiene más de una compañía, es posible crearlas desde:

> Inicio > Cuentas > Compañía

## 1. Cómo crear una nueva compañía
1. Ir al listado de Compañías, hacer click en Nuevo.
1. Ingresar el nombre, abreviación y divisa/modena predeterminada de la compañía.
1. Guardar.

La abreviación de la compañía es generada automáticamente, por ejemplo, FT para Frappe Technologies. Esta abreviación ayuda a diferenciar cuentas, centros de costo, plantillas de impuestos, almacenes, etc. de una compañía de los de otra. 

También es posible asignar un logo y una descripción a cada compañía.

![Company Master](/docs/assets/img/setup/company-master.png)

### 1.1 Estructura multi-compañía

Es posible que se tenga un grupo de compañías, algunas más grandes que otras, que son parte de una compañía mayor.

En ERPNext, la estructura de compañías puede ser paralela (compañías hermanas), compañías padre-hija o una combinación de ambas.

Una compañía padre es una organización mayor que cuenta con una o más compañías hijas. Una compañía hija es subsidiaria de la compañía padre.

La vista de árbol de compañías muestra la estructura general de las compañias creadas.

<img class="screenshot" alt="Company Tree" src="{{docs_base_url}}/assets/img/accounts/company-tree.png">

Una vez conformado el árbol de compañías, ERPNext validará si las cuentas de las compañías hijas coinciden con las de la compañía padre. Todas las cuentas pueden combinarse en un Plan de cuentas consolidado.

### 1.2 Otras opciones en la creación de compañías

* **Dominio**: es la actividad principal de la compañia. Ej: manufactura, servicios, etc.
* **Es un grupo**: si está tildado, se creará como compañía padre.
* **Empresa matriz**: si es una compañía hija, se deberá seleccionar en este campo la compañía a la cual pertenece. Una vez seleccionada, el Plan de cuentas de la nueva compañía se creará tomando como modelo la compañía padre.

### 1.3 Plan de cuentas
Por cada compañía, se mantiene un Plan de cuentas independiente. Esto permite separar la contabilidad de cada compañía cumpliendo con los requisitos legales. También es posible importar Planes de cuentas mediante el [Importador de Planes de cuentas](/docs/user/manual/en/setting-up/chart-of-accounts-importer).

<img class="screenshot" alt="Company Chart of Accounts" src="{{docs_base_url}}/assets/img/accounts/company-coa.png">

ERPNext posee Planes de cuentas disponibles para ciertos países. Cuando se crea una nueva compañía, se puede seleccionar generar el Plan de cuentas de una de las siguientes formas:

* Plan de cuentas estándar
* Basado en el Plan de cuentas de una compañía existente

<img class="screenshot" alt="Company Chart of Accounts" src="{{docs_base_url}}/assets/img/accounts/company-coa-2.png">

Nótese que, si se seleccionó una compañía padre, el Plan de cuentas será creado en base al de esa compañía.

### 1.4 Predeterminados
En la compañía se puede especificar una gran cantidad de valores por defecto para otros documentos y cuentas. Estas configuraciones por defecto son de gran ayuda en las entradas rápidas de transacciones contables, donde el valor para la cuenta será tomado de la compañía (si ese campo está definido). Tan pronto como la compañía es creada, se crea un Plan de cuentas y Centro de costos de forma automática.

The following defaults can be set for a company:

* Default Finance Book
* Default Letter Head
* Default Holiday List
* Standard Working Hours
* Default Terms and Conditions
* Country
* Tax ID
* Date of Establishment

## 2. Features
### 2.1 Monthly Sales Target
Set the monthly sales target number in the company currency, for example, $10,000. Total monthly sales will be visible once transactions are made. To know more [click here](/docs/user/manual/en/setting-up/setting-company-sales-goal).

### 2.2 Account Settings
Some of the following accounts will be set by default when you create a new company, others can be created. The accounts can be seen in the [Chart of Accounts](/docs/user/manual/en/accounts/chart-of-accounts). These values can be changed later on if needed.

* Default Bank Account
* Default Cash Account
* Default Receivable Account
* Round Off Account
* Round Off Cost Center
* Write Off Account
* Discount Allowed Account
* Discount Received Account
* Exchange Gain / Loss Account
* Unrealized Exchange Gain/Loss Account
* Default Payable Account
* Default Employee Advance Account
* Default Cost of Goods Sold Account
* Default Income Account
* Default Deferred Revenue Account
* Default Deferred Expense Account
* Default Payroll Payable Account
* Default Expense Claim Payable Account
* Default Cost Center
* Credit Limit
* Default Payment Terms Template

### 2.3 Stock Settings
Perpetual Inventory feature would lead to Stock transactions impacting the company's books of accounts. Know more [here](/docs/user/manual/en/stock/perpetual-inventory). It is enabled by default.

* Default Inventory Account
* Stock Adjustment Account
* Stock Received But Not Billed
* Expenses Included In Valuation

    ![Stock Settings in Company](/docs/assets/img/setup/company-stock-settings.png)

### 2.4 Fixed Asset Depreciation Settings
For managing fixed assets in a company, the following accounts are needed. Most of them will be created by default. They can be seen in the [Chart of Accounts](/docs/user/manual/en/accounts/chart-of-accounts).

* Accumulated Depreciation Account
* Depreciation Expense Account
* Series for Asset Depreciation Entry (Journal Entry)
* Expenses Included In Asset Valuation
* Gain/Loss Account on Asset Disposal
* Asset Depreciation Cost Center
* Capital Work In Progress Account
* Asset Received But Not Billed

    ![Fixed Asset Depreciation](/docs/assets/img/setup/company-asset-depreciation.png)

### 2.5 HRA Settings

Set the default Component for the following Salary Components.

> For the Indian user, setting the default value in this section will help in Employee Tax Declaration calculations, especially for HRA exemption amount.

* Basic Component
* HRA Component
* Arrear Component

### 2.6 Bank Remittance Settings

*Only for India.*

Using the Payment Order feature (in Accounts), you can give a single document of transfer for multiple bank transfers. Updating value in the following fields will help you generate Bank Remittance in a format which can be accepted and can be also uploaded on the bank's portal.

Payment order allows a user to combine several payment entries/payment requests into a single document. Bank Remittance allows a user to send **that** single document to the bank as text format, this text format can be manually uploaded to Kotak bank payments platform.

Client Code and Product Code are codes given by the bank to you. This is required to be added in the text file as per the format specified by Kotak bank.


### 2.7 Budget
Exception Budget Approver Role: The role selected here can bypass the set budget to approve expenses.

### 2.8 Company Info
For reference, the following details of your company can be saved in ERPNext:

* Date of Incorporation
* Phone No
* Fax
* Email
* Website
* Address
* Registration Details

> Note: When setting the address here, it is important to tick the 'Is Your Company Address' checkbox.

![Company Address](/docs/assets/img/setup/company-address.png)

**For India**, different addresses can be added with different GSTIN numbers if the company has multiple locations. For example, if your company has offices in Mumbai, Delhi, and Bangalore, you'll have to add different addresses with different GSTIN numbers.

On saving a company, the following details/actions will be visible in the dashboard:
![Company after Save](/docs/assets/img/setup/company-after-save.png)

**Registration Details**: Here you can save various tax/cheque/bank number for reference.

### 2.9 Deleting all Company Transactions
You can delete all transactions (Orders, Invoices) of a Company. *Use with caution*, transactions once deleted cannot be recovered.

#### Requirements

* The User has to be a System Manager
* The User has to be the creator of the Company

#### Steps
1. Click on the **Delete Company Transactions** button
1. Verify your password
1. Enter Company name for confirmation
    ![Company after Save](/docs/assets/img/setup/company-delete-transactions.png)

And you're done. The master data like Item, Account, Employee, BOM etc. will remain as it is.

#### What is affected?

* Sales/Purchase Orders/Invoices Receipts/Notes will be deleted
* The monthly sales and sales history will be cleared
* All notifications will be cleared
* Lead Addresses to which the Company is linked will be deleted
* All communications linked to the Company will be deleted
* All naming series will be reset
* Stock Entries linked to a Warehouse of this Company will be deleted

### 3. Related Topics
1. [Setting Up Taxes](/docs/user/manual/en/setting-up/setting-up-taxes)
1. [System Settings](/docs/user/manual/en/setting-up/settings/system-settings)
1. [Charts Of Accounts Importer](/docs/user/manual/en/setting-up/chart-of-accounts-importer)
1. [Users and Permissions](/docs/user/manual/en/setting-up/users-and-permissions)
1. [Adding Users](/docs/user/manual/en/setting-up/users-and-permissions/adding-users)
1. [Letter Head](/docs/user/manual/en/setting-up/print/letter-head)
1. [Email Account](/docs/user/manual/en/setting-up/email/email-account)
1. [Administrator](/docs/user/manual/en/setting-up/users-and-permissions/administrator)
