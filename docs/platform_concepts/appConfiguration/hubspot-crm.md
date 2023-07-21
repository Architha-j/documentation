---
title : Hubspot CRM
sidebar_label : Hubspot CRM
---

## Scope of Integration

Yellow.ai Integration with Hubspot CRM allows you to seamlessly connect your Hubspot CRM instance with yellow.ai platform. Any customer who has a Hubspot CRM account will be able to connect their Hubspot instance with yellow.ai using OAuth. This connector will make sure you can do actions on your leads (contacts). Using this integration you can create, update, read, delete the leads (contacts) and also you can search for contacts with email and phone number.

## Configuration

Configuring the integration with hubspot CRM is straightforward. Follow the steps defined below
to start integrating:

### 1. Navigate to integration tab

Inside your project, navigate to the Configuration tab and then click on the Integrations
Tab. Search for Hubspot CRM.

<img src="https://i.imgur.com/445XrpL.png" alt="drawing" width="50%"/>


### 2. Connect your hubspot account

Click on **Connect** to see an option of click to **Connect with Hubspot**. After you click that, you will notice that you will be prompted to login to your Hubspot account.

![](https://i.imgur.com/v8CK0KN.gif)


### 3. Add our webhook

   You would need to add our webhook in your hubspot CRM account to receive events which were defined in this integration. The instructions that you have to follow to add our webhook will be available in the hubspot integration card.

<img src="https://i.imgur.com/hzAick6.png" alt="drawing" width="55%"/>

Following the above steps will connect your Hubspot CRM account with yellow.ai platform.

If you have multiple accounts, follow the above mentioned steps to add each of them.

:::note
1. Enter a unique name for each account to easily identify them within the yellow.ai platform. It is recommended to use a name that aligns with its purpose for better usability. 
2. You can add a maximum of 5 merchant accounts.
3. In a two-tier environment, such as bots with only Development/Live environments, you can add account names only in the development mode. Once added and flows have been built, in the Live mode, you can only choose the account names and not edit them.
4. In a three-tier environment, such as bots with Staging/Sandbox/Production modes, in Staging and Sandbox modes, you can add and edit new accounts. However, in Production, only the account details added in Staging will be available. You can only map in the production environment.
:::

##  Events
Following are the events which are currently accommodated in the Integration:

Event | Description
----- | -----------
hubspot-contact-created | You will receive this event to the bot when a new lead(contact) got created in yourhubspot CRM. Based on that event you can confirm the user or you can design your custom flow according to your use case.

<img src="https://i.imgur.com/r6s3N14.png" alt="drawing" width="60%"/>

<img src="https://i.imgur.com/vPqTZBC.png" alt="drawing" width="60%"/>

:::info
If you have added multiple accounts in your platform, enable events for each of those accounts.
:::

## Use-cases

Following are the use-cases which are currently accommodated in the Integration:

:::note
When multiple accounts are added, select the appropriate account for each node, allowing you to leverage the unique functionalities of each account for their intended purposes.
:::

### 1. Simple integration with OAuth

Yellow.ai does not store the client’s credentials and leverages OAuth 2.0 approach for integrating with client’s Hubspot account.
While integrating, yellow.ai navigates the user to the login page of Hubspot, user has to login into his hubspot CRM account and has to provide his consent.


### 2. Do actions with hubspot action nodes

   You can store a new **Lead(Contact)** and save it in your hubspot CRM. You can update,
read, delete the lead(contact) too. Also you can search the leads (contacts) in your crm
with email and phone number.


<img src="https://i.imgur.com/7pjdFH7.png" alt="drawing" width="60%"/>

<img src="https://i.imgur.com/FnrPohB.png" alt="drawing" width="60%"/>



## Supported Version

This integration will work on versions v3 and above.


For more information about action nodes you use here, refer this[doc  
](https://developers.hubspot.com/docs/api/crm/contacts)For more information about webhook events you receive, refer this[doc](https://developers.hubspot.com/docs/api/webhooks)
