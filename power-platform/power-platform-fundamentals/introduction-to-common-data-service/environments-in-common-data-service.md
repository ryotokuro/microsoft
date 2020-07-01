# Environments in Common Data Service

Environments are spaces where you can store and **manage all of your business data, apps and flows on the Power Platform**. This means that all your applications, dependencies and things are all kept in one space \(housed in the environment\). With each environment you have **ONE Common Data Service database** which is the dedicated database for all the business apps and flows.

Environments are **created under the Azure AAD so that users within that Active Directory are the only ones who can access it**. The Azure AAD can therefore be the representation of your organisation, holding users who are your employees, and the apps and services are kept an environment so only your business employees can use them.

Furthermore, your environment is also **geographically bound**. This means that everything within that environment will be created and stored local to your region. As such, when you create a Common Service database for example in Australia East, the **Common Service Database is created in the database centres located in the Australia East region**. So all the connections, flows, Power Apps, Automates are also bound to that region.

![](../../../.gitbook/assets/image%20%281%29.png)

As an illustration, you can see that **Contoso Corp is the Azure Active Directory** that represents your whole corporation. Within the corporation there are different environments which are tied to each region. You have **one environment for the US, one for Canada and one for Australia**. Each of them have their own respective Apps, Flows and Common Data Models and are able to be accessed by everyone within your corporation \(or under the Active Directory\).

