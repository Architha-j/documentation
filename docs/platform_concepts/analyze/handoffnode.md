---
title: Topic Analysis for Third party ticketing tools 
sidebar_label: For 3rd party ticketing tools
---



:::note 

In this article, we refer to any applications other than Yellow.ai, such as third-party ticketing systems and support CRMs, as third-party apps.
:::



## Containment rate for 3rd party apps 


Containment rate refers to the number of conversations handled solely by the  without agent intervention. There are two types of such chat transfers:

1. **Active handover**
    - In Yellow Inbox, chat is transferred to an agent with the event `agent-transfer`.
    - 3rd Party Inbox: AI-agent is paused, and chat is handed over to an agent with the event configured at the AI-agent-level.  

2. **Passive handover**
    - **Schedule callback**: AI-agent schedules a callback by collecting user details.
    - **Email**: AI-agent creates an email ticket.
    - **Ticket in 3rd Party System/Trigger Event**: AI-agent creates a support ticket in another system or triggers a custom event.


## Offling ticket handling using Chat handoff node 

### Current limitation 

Yellow Inbox transfer are tracked with the `agent-transfer` event. But while using 3rd Party Inbox, the transfer depends on AI-agent-level configuration but that **is not currently trackable**.

### Suggested solution

With **Bot Developer** access, you can configure the **Chat Handoff** node. This node is typically connected to the node used to raise a ticket in a third-party system. When this node is encountered, the `agent-session` event is tracked in the **User Engagement Session Table**. This setup enables tracking of the number of sessions that end with a passive handoff to third-party ticketing systems.

![chat handoff](https://imgur.com/ix6sMpU.png)

![image](https://imgur.com/CvniYAF.png)

In the example below, a successful action after raising a ticket in Zendesk connects to the Chat Handoff node. When a passive or offline ticket is created in Zendesk, agents respond via email, call, or other channels. Meanwhile, this handoff is tracked. The Chat Handoff node acts as an identifier for agent transfers, enabling you to track the containment rate effectively.

![example](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcsCC_H9djVb0DBv3R2mmRlu3MaPocs-mOtzxyBiTN61wnlFRsUSrFsGbJgir3VnEn7flwiTgzCjlkJ4K4JnC7IJ7CkJ--5dd5QH3KB2oGDDMjdr95mXAtaiEQrj2RupK6Lv3B2I_5tMuKE-zOzytyee-Q-?key=doHOJQMEdYvKlVOmPCYX8w)

:::info

**Chat Handoff** node is enabled by default for all customers using Analyze.

:::


------------


## Analyze transcripts in third-party apps

Offline tickets in third-party ticketing tools are created under the following conditions:
* Inbox (Yellow.ai or third-party) is accessed outside business hours, when agents are unavailable.
* The inbox is not utilized, and only offline tickets are generated.

These interactions occur across various channels, including call, email, web chat, and SMS. However, transcripts from third-party ticketing tools are not accessible on the platform. As a result, only interactions between users and AI agents are available for analysis, limiting insights from agent-user conversations managed through third-party systems. To address this, transcripts from third-party ticketing tools will be imported, analyzed, and displayed along with insights in the Yellow.ai's Analyze module.

**Flow**

Yellow.ai workflow:
* AI agent responds to user inquiries.
* Live agent takes over, pausing the AI agent.
* AI agent resumes after the live agent can no longer respond.

Third-party workflow:
* AI agent responds to user inquiries.
* An offline ticket is created, while the AI agent remains active.
* The chat continues with the AI agent, running in parallel with offline ticket management, with no defined session end time.

Once a handover to the third-party tool occurs, ticket details are received. Upon ticket closure (with no specific time constraint), the ticket is analyzed, and both the **transcript** and **insights** are displayed in the Analyze module.

----------

Offline ticket messages sent to Yellow.ai's backend won't initiate processes (such as, ticket closure and fetching chat transcripts) automatically. To enable this, you need to create an automation rule in your Freshdesk (or other third-party ticketing app) and configure a webhook. This webhook can be set up using Yellow.ai's **Integration** module.


## Configure Freshdesk webhook

### Set up Freshdesk webhook

Follow these steps to enable automations and set up a webhook: 

1. **Log in to your Freshdesk account**: Use your credentials to log in to your Freshdesk account.
2. **Go to admin settings**: Click on Admin in the left-hand sidebar to open the configuration options.
3. **Open the automation section**: In the Workflows section of the admin settings, click on Automations to access workflow and trigger management options.
4. **Select Ticket Updates**: Under the automations tab, choose **Ticket Updates** to create rules for ticket-related updates.
5. **Define webhook trigger conditions**: Specify the conditions for the webhook trigger. Add the required criteria to ensure the webhook activates under the appropriate circumstances.
    ![image](https://imgur.com/EJQDhEC.png)
6. **Action settings**: Add the action settings as below.
    ![image](https://imgur.com/uWwm48Q.png)


:::info
Webhook URL for the connected account can be fetched from **Yellow.ai > Integration > Your third-party tool > Weebhook URL** beside the account name.
    ![image](https://imgur.com/GLJbBRc.png)
:::

### Enable Freshdesk events on Yellow.ai’s platform  

1. **Go to automation**: Open Yellow’s platform and navigate to **Automation** from the sidebar.  
2. **Access events**: In the automation settings, go to **Events** and select **Integrations**.  
3. **Activate the Freshdesk event**: Locate the **freshdesk-ticket-updated** event and activate it for the connected Freshdesk account.  
    ![image](https://imgur.com/7TlMBkU.png)


Once configured, you can see the analysis generated on the Analyse module for the chats happening on the third-party apps. 

![image](https://imgur.com/sRRhxb7.png)
![image](https://imgur.com/V3Cd0lt.png)
![image](https://imgur.com/ndfgeSV.png)

## Configure Webhook and Trigger to track tickets in Zendesk

To receive notifications for ticket updates within Zendesk's offline ticketing system, you can set up webhook and trigger.

### Create a Webhook

To configure a webhook for receiving ticket update notifications, follow these steps:

1. Log in to your Zendesk account.

2. Go to **Admin Center** by clicking the **Admin icon** in the sidebar.

3. Navigate to **Apps** > **Integrations** > **Webhooks**.

4. Click on **Create Webhook**.

5. In **Name** field, enter the name of your webhook.

6. In **Endpoint URL**, provide the URL where you want to receive the notifications.

8. In **Request** method, select POST.

9. In **Request** format, choose JSON.

10. Click **Create** to save the webhook.

  ![](https://i.imgur.com/f4ZpJGw.png)

### Create a Trigger

To notify the webhook when a ticket is updated, set up a trigger:

1. Go to **Admin center** by clicking the **Admin icon** in the sidebar.

2. Navigate to **Objects and rules** > **Triggers**.

3. Click on **Add trigger**.

4. In trigger details, enter a **Name** of the trigger.

5. In **Conditions**, define when the trigger should activate (example, when a ticket is updated).

6. In **Actions**, set the action to notify the webhook you created.

   ![](https://imgur.com/akjkijx.png)



