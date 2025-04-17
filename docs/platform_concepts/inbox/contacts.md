---
title: Contacts (send proactive notifications)
sidebar_label : Contacts 
---

:::note
Contacts is currently undergoing a revamp. During this time, there may be temporary issues and disruptions in its functionality. We apologize for any inconvenience caused.
:::

<!--
In this article, you will learn: 
1. [What are proactive notifications?](#defination)
2. [How to create new contacts in the inbox?](#1)
3. [How to send notifications to the contacts?](#2)
4. [How to followup with the tickets created for proactive notifications](#3)

------
-->


#### <a name="defination"></a>  **Proactive notifications**

The support process is a reactive process that takes place when a customer faces an issue and reaches out to the brand for resolution, through their website (or other configured channels). A live agent is connected to a customer and their issues are resolved. 
This proactive notification is an outbound reach out where the agents or the businesses, reach out to the customers (using our **Contacts** feature) to identify issues, problems, and opportunities to maintain relationships (especially in the case of B2B scenarios), to introduce new products/provide product updates, to personally address their queries, etc. This personalization and proactiveness provide:
- A better experience for the end users. 
- Increased customer loyalty.
- Increased potential sales.

:::note 
* This feature is available only for the WhatsApp channel.   
* To extend this to other channels, contact our [support team](mailto:support@yellow.ai)
:::

## <a name="1"></a> 1. Create a new contact 

Follow the steps below to create a new contact:  

1. Log in to the yellow.ai platform. Open **Inbox** > **Contacts**. 

![](https://i.imgur.com/n9Sgfrq.png)

2. If you want to send notifications to a new contact, you can add a new contact by clicking **+Create contact**.  

![](https://i.imgur.com/EyUiBa0.png)  

3. Enter the contact details: 
	- Name, email address, and Phone number with the correct country code (+91 for India). 
	- Upload a contact image (if required). 
4. Click **Create**. 
5. This page will contain all the contacts created in Inbox, use the search bar to find a particular contact by entering the details. 

![](https://i.imgur.com/Za2s5v6.png)



## <a name="2"></a>  2. Send proactive notification to a contact 



Follow the steps below to send a notification to any particular contact:  

1. Search for the required contact and click on the contact name. 
2. Click **Send message**. 

![](https://i.imgur.com/KocHhhp.png)

3. Select the **From** contact number (WhatsApp business number) from which this notification will be sent. For more details on WhatsApp channel, click [here](https://docs.yellow.ai/docs/platform_concepts/channelConfiguration/whatsapp-configuration). 
4. Select the **To** contact number. Click **Next**. 


<img src="https://i.imgur.com/aTNnnoI.png" alt="drawing" width="40%"/>

:::note
If there is an active chat [In Assigned, Queued, Open status] existing for the customer to whom you are trying to reach, you cannot send another proactive notification.
![](https://i.imgur.com/ZRAJhLL.png)
:::

5. Select the template. Click **Next**. 
	- Use the search bar to find the required template. 
	- Hover on a template, to preview it. 

<img src="https://i.imgur.com/NyoAjdh.png" alt="drawing" width="40%"/>

6. You can attach media/ variables/ dynamic content and click **Next**. 

<img src="https://i.imgur.com/91jzw4O.png" alt="drawing" width="70%"/>

7. Add the following details and click **Create ticket and send**: 
	- Select the **Priority**.
	- Select **Assignee** from the drop-down to assign this ticket to an inbox agent. 
	- Add a **Description**. 

<img src="https://i.imgur.com/VxFCRYN.png" alt="drawing" width="40%"/>

8. A ticket will be created and assigned to the agent. These details will be visible on the **Timeline** tab.

<img src="https://i.imgur.com/oUb3kba.png" alt="drawing" width="50%"/>


:::note
- Ticket creation through the contacts tab will take 1-2 minutes to process because Inbox verifies that the user number entered is valid or invalid before creating a ticket. Once the message is sent it will not get updated automatically, you must refresh the page to update ticket status. 

	- **Verification message**  
		<img src="https://i.imgur.com/gK1uMBF.png" alt="drawing" width="50%"/>  

	- **Failure message**  
		<img src="https://i.imgur.com/tbit8zO.png" alt="drawing" width="50%"/>  

	- **Success message**  
		<img src="https://i.imgur.com/EQfLVEv.png" alt="drawing" width="50%"/>  


:::


9. All the tickets sent to a respective contact will be listed under the **Tickets** tab. 

![](https://i.imgur.com/psNPElO.png)


## <a name="3"></a> 3. Chat with the contact 

Follow the steps below to follow up with the contact after the notification is sent:
   
1. Once the number is verified, the ticket is created and a notification is sent to the contact, you can view it on the **Chats** tab.
2. On [chats](https://docs.yellow.ai/docs/platform_concepts/inbox/chats/getstartedwithlivechat), ticket details, and the chat screen will be open (to the assigned inbox agent). 
	- Depending on the agent to whom the ticket is assigned, tickets will be visible on the My Chats tab.
	- Admins can see this chat on the Active chats tab. 


<img src="https://i.imgur.com/RB5TnXj.png" alt="drawing" width="100%"/>

3. When the contact responds to the notification, the Chat restriction is lifted and the agents can have a free-flow conversation. 

:::note
As per [WhatsApp guidelines](https://docs.yellow.ai/docs/platform_concepts/inbox/chats/reinitiatewachats), live agents cannot have a free flowing conversation with the customers up until they respond back to the proactive template message sent by the agents. Once the customer responds, the 24hr session rule is lifted and agents can handhold the customer to resolution. 
:::

