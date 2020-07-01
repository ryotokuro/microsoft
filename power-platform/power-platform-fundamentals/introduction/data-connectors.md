# Data Connectors

The reason why the Power Platform thrives is because it can **connect to a myriad of external services** and **leverage data from a multitude of sources**. This is made possible through the **bridging data to different apps and workflows** \(also known as data connectors\).

{% hint style="info" %}
**Note**  
_Premium_ and _custom_ connectors require a **paid plan to use**
{% endhint %}

## Different Data Sources

The first and foremost thing that is important to understand is the **types of data sources** that these connectors are providing connections to. The two types of data sources can be categorised as **tabular data** and **function-based** data.

### Tabular Data

Tabular data sources _look like Excel_. The **data is assorted in rows and columns** and have associations based on the **format of the table**. Since tabular data is set up in a **structured matter**, it is very easy for products such as **Power Apps to interpret and display that data**. For example, using the association of headings, Power Apps can take tabular data sources to **automatically create galleries, forms** and other controls based on the information.

Additionally, if editing the data source is supported, you can **add, edit and delete rows of data from Power Apps directly**. Some examples of tabular data sources are: Microsoft Sharepoint, Common Data Service and SQL Server.

### Function-based Data

Function-based sources by definition **allow you to use functions to act on the data provided by the source**. The data that this source provides provides **additional functionality** on top of tabular data \(extending on the uses of tabular data\). Such extensive actions that function-based data provides are things like:

* Sending an email
* Updating permissions
* Setting a calendar event

To illustrate this, an example would be if a data source provided a set of **email address as the data**. This can be enacted on by using **functionality to send mail to these addresses** making it **function-based data**. For permissions you can take a list of settings and for calendar events you might have location data, date/time, attendees, etc.

So **function-based data has a lot more options and opportunities with the data.** Looking at the examples of functional-based data sources \(Office 365 Users,  Project Online, Azure Blob Storage\), **you can picture what you might be able to do with the data**. For user data, you can set permissions, interact with the users and much more just by having that information. A relevant example with **Azure Blob Storage** \(a popular type of storage\), I find that a lot of websites store their videos in blobs \(like Microsoft Stream\) and retrieve that data from the source \(Azure server\) to display on their website.

## Connectors

As mentioned before, connectors **bridge data sources with your app, workflow or dashboard**. For emphasis, the Power Platform provides over 275 connectors to common data sources that people use frequently.

To distinguish connectors, the Power Platform offers two different types: **Standard** and **Premium connectors**. Standard connectors are typically for sources developed by Microsoft and available to the public or freeware while premium pertains to more third-party platforms or options that have a paid plan \(like SQL\).

| Standard | Premium |
| :--- | :--- |
| SharePoint | MailChimp |
| Outlook | SurveyMonkey |
| YouTube | SQL Server |

### Triggers & Actions

What makes connectors and data sources so powerful is the ability to act upon the data - deemed **Triggers & Actions** on the Power Platform. Once you have established a data source and configured a connector to that source, your next move can be a **Trigger** or an **Action**.

{% hint style="info" %}
**Triggers** are **only used in Power Automate**

**Actions** are used in **both Power Automate** and **Power Apps**
{% endhint %}

#### Triggers

Triggers which are **only used for Power Automate** are **used to signify when a flow is to begin** \(flow being the logical process\). Triggers can be **activated by some condition;** which could be **time-based**; going off at 8am everyday ****or **set off by an event occuring**; like receiving an email or creating a record in a table. Te thing that is fundamentally important about triggers is that a trigger is required in order to initiate a workflow \(spawned in Power Automate\).

#### Actions

Actions on the other hand **can be used in both Power Automate and Power Apps**. An action can **occur by being intentionally set off by a user**, or from the **signal from a trigger \(after a certain condition is met\)** - and set off the interaction of functions on data. It is therefore through **Actions that this interaction occurs** - such as **sending an email, or adding to your data source**.

{% hint style="info" %}
As such, you can consider **Actions to be the actual response** that occurs which effects change in your system. Whereas **Triggers are the driving signal** that gets "triggered" once a certain condition is met. The fundamental behaviuor is that with _Triggers_, no event actually happens - but it can set off an Action \(or flow\) to occur.
{% endhint %}

##  Custom Connectors

Now although there are 275 out-of-the-box connectors that the Power Platform provides, perhaps you still need a connector that fits your specific use case. Something that interfaces properly with your data model. To meet that need, Microsoft also provides the option of building your own custom connector - to tailor the requirements of your connection between the app, workflow or device to your data source.

By using a **custom connector, you're then able to utilise external third party interfaces for things that aren't supported natively**. A common example of this is public available APIs or even custom APIs which are hosted through Azure. Having this option to extend functionality the way you like it covers all the bases you'll need, as connectors can securely bridge your system to send information to and from the API.

The way that this works simply, is that the connector can utilise the functions for API communication available in Power Apps or Automate, and on the other end, it uses the functions in the API service to retrieve and send the data required. This makes connectors highly accessible and can be used across different Power Platform apps and services.

