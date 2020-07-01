# Understanding relationships using Entities

In order to design an elegant and efficient solution, the general strategy is to **structure your database in sections, by grouping up your data into different containers \(or entities\)**. This allows you to establish a common relationship between different pieces of information in your solution and lets you more easily track important entities and create metrics based on your data.

## Sales Solution Example

Let's look at trying to build a sales solution as an example to illustrate how structuring our data properly can help a business operate more effectively.

In order to build a system to manage sales orders there are a few things we need:

* **A list of products**
  * The current inventory count \(stock\) of each product
  * The price of each product 
* **Customer information**
  * Name of customer
  * Customer identification number
  * Customer contact number
  * Address of customer
  * Credit rating of customer 
* **Sales Invoices**
  * Data of sale
  * Invoice reference number
  * Salesperson
  * Customer information \(as above\)
  * line item 
* **Line item \(unique item identifier\)**
  * References the item
  * Provides cost and price of item at the time of sale
  * Decreases quantity of item based on number sold

Here you can see a natural sort of grouping occurs when talking about the system. Where you have different categories of things within the system \(these are our entities\). It would be impractical if we were to try and shove all of these different things into one entity, messing up the structure of our database. Instead, we can create entities based off these four groups being:

* Products
* Customers
* Invoices
* Line Items

Creating an entity for each of these can thereby result in a much **cleaner solution that we can scale out if necessary**. This helps us out with reducing chances of having **duplicate data** because we can now easily lookup things in our database before adding anything new. Moreover, by making it easier to get things from our solution, it helps with generating reports quickly since all the functionality we need to interact with our data is set out nicely.

## Relational Entities

**Entities that relate to one another hold a relational connection.** We can define these relationships as either being:

1. **One-to-one** relationship
2. **Many-to-many** relationship

A one-to-one relationship is simply a normal **hierarchial relationship** where we have a **parent-child** arrangement. In the example above, the **invoices contain a line item on them**. As such, we can say that the `Parent: Invoice` and the `Child: Line Item`. This relationship means that with our invoices, we can have zero, one or many children one each invoice, but you generally won't have a line item without the invoice existing first \(i.e. need parent to have a child\).

## Parent \(Keys\) and Child \(Foreign\)

Parents have a **unique identifier** that we call **Keys**. An example of this being used would be the Invoice entity containing a unique invoice number. This value is **stored in the Parent record as a 'Key'** and also stored in the **Child record** as a **'Foreign Key'**.

![Visual representation of Parent-Child relationship using keys](../../../.gitbook/assets/image%20%2821%29.png)

Having the data set up in this manner enables us to **do filtering easily**. If we want to get the **children nodes of the** `Parent: Invoice` then we simply search for entities that **contain a Foreign Key which matches the Key of the Parent**.

