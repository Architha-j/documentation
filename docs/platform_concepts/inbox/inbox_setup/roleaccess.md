---
title: Inbox access available to Inbox roles(Agent/Supervisor/Admin)
sidebar_label : Inbox role access explained
---

 
> Based on the permission you want to provide, you can add **Inbox Admin/Agent/Supervisor** roles by following [these steps](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox_setup/supportagents).

Following features are available for Inbox Admin/Supervisor/Agent roles :



| Module | Inbox Agent |  Inbox Supervisor   | Inbox Admin | 
| -------- | -------- | --- | -------- | 
| **Live chats**     ||||
|Chats assigned to the current agent|:heavy_check_mark:|  :heavy_check_mark: |  :heavy_check_mark:    |
|Chats raised in a particular group <br/>(with a Supervisor assigned to that group)|:x:| :heavy_check_mark: | :heavy_check_mark:|
|Chats raised in all groups|:x:|:x:| :heavy_check_mark:|  |
|**All the Inbox Settings**|:x:|:x:|:heavy_check_mark:||
|**Email tickets**||
|Creating a manual ticket|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark: |
|Tickets assigned to the current agent|:heavy_check_mark:|:x:|:heavy_check_mark: |
|Tickets raised in a particular group|:heavy_check_mark:|:x:|:heavy_check_mark:|
|Tickets raised in all groups|:x:|:x:|:heavy_check_mark:|
|**Knowledge Base**||||
|Reading articles [Published]|:heavy_check_mark:|  :heavy_check_mark: |  :heavy_check_mark:    |
|Create, Edit & Delete articles|:x:|:heavy_check_mark: |:heavy_check_mark: |
|Publish, Unpublish articles|:x:|:heavy_check_mark:|:heavy_check_mark:||
|**Monitor & Analytics**||||
|Chats & tickets data assigned to current agents|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|
|Chats, Tickets & Agents data for a particular group|:x:|:heavy_check_mark:|:heavy_check_mark:||
|All chats, tickets & agents performance data|:x:|:x:|:heavy_check_mark:|
|**Contacts**||||
|Create, Read, Update, and Delete contacts|:x:|:heavy_check_mark:|:heavy_check_mark:| 


:::note

**Agent permissions**:

In both Chat and Email tickets, agents will not have the ability to:
* Update ticket details of other agents or unassigned tickets.
* Send messages on other agents or unassigned tickets.
* Transfer tickets assigned to other agents or unassigned tickets to other agents.
* Assign tickets that are either assigned to other agents or unassigned.
* Perform any other ticket-related updates on tickets not assigned to them or unassigned tickets.

**Group supervisor permissions**:

In both Chat and Email tickets, agents with Group Supervisor access can:
* Update ticket details for tickets within their supervision group.
* Send messages on tickets within their supervision group.
* Transfer and assign tickets within their supervision group.
* Manage unassigned tickets that belong to their supervision group.

:::
