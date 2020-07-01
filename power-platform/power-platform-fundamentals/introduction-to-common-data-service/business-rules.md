# Business Rules

Business rules are conditions that are applied onto your data. The Common Data Service allows you to apply these rules on the data directly, allowing you to **maintain your business logic at the DATA layer instead of the APP layer**. This saves you from having to configure your application with the same rules every time you interact with your data and instead makes it so that whenever you use your data, the **logic is consistent**.

So regardless of however you access the data - whether it be through Power Apps, Power Automate or even through an external API, the rules always apply.

## Uses of business rules

A common example is when your data is **used by different types of Power Apps.**  
For both **Canvas Apps and Model-driven Apps**, you can:

* **Set** fields in an entity
* **Clear** field values
* **Validate** data
* Show **error messages**

**Model-driven Apps** support the use of more complex business rules such as:

* **Showing specific fields**
* **Hiding** fields
* **Enabling** fields
* **Disabling** fields
* **Create business recommendations** based on intelligence from the data

## Example of business rule use

One example of how business rules can be used is by checking if a field `Credit Limit` is greater than $1,000,000 \(`Credit Limit > 1000000?`\). If so, then it changes the `VP Approver` field to be **required**.

This affects how the user interacts with the application just like cases where your password may be required, or your app needs extra permissions, etc.

![](../../../.gitbook/assets/image%20%288%29.png)





