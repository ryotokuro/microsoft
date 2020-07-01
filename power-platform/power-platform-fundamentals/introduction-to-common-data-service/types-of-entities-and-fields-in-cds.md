# Types of Entities and Fields in CDS

![Screenshot of a standard Customer Entity ](../../../.gitbook/assets/image%20%2816%29.png)

## Types of Entities

### Standard

These are entities that are **always created** for **every instance** of the Common Data Service database. So as mentioned before when an instance is generated, a set of standard entities are also set-up so the user can immediately begin to extend on the database and draw relationships. As such, for standard entities you are able to **add more fields to any entity** but you **can only delete fields from custom entities.** 

### Complex

With complex entities, they **contain more complex variable data.** This can be things like:

* Server-side business logic
* Real-time workflows
* Plugins

Complex entities are usually present in things like Dynamics365 apps.

## Fields

Fields are a level below entities - so entities are made up of various fields. These are like the attributes of objects and so they **hold pieces of information within a record** that is kept inside an entity. You can think of **fields as columns in Excel**. It's one data entry which can hold a specific type of data.

**A field also has type**. This means that the **type of data within a field matches the type of the field**. For example, if you have a field that is of `Type: Date` then you can store data like `16-Sep` if your solution requires data for Dates. Similarly, if your solution has **numbers** then you would use a Field that has `Type: Number` in order to store your data.

![Entity example with fields](../../../.gitbook/assets/image%20%2812%29.png)

The number of fields within an entity can vary depending on your situation. It very well range from a single digit to a few hundred. However, if you find yourself exceeding several hundred fields, then it's probably more ideal to think about how to **restructure your database because when you get to that point, there is definitely a more ideal solution.**

With each instance of a Common Data Service Database, you're equipped with standard entities consisting of standard fields right off the bat. It is generally **best practice to utilise the standard entities FIRST before deciding to create new entities**. You can easily rename the entities to fit your solution context - so always utilise the standard entities wherever you can!

