---
title: Flows 
sidebar_label: Flows overview
---

A flow is a structure that defines the sequence of a AI-agent conversation with users based on their questions and responses. It consists of a series of [nodes](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes), where each node represents a specific point in the conversation. Nodes can include messages, questions, prompts, actions, or conditions based on user input.

After creating a flow, the first flow you create is considered the [start flow](https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/manage-flows#start-flow-welcome), and the second flow is considered the [fallback flow](https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/manage-flows#fallback-flow). However, when there are multiple flows, you can set any flow as the start or fallback flow.

**Key features of Conversational Flows:**

* **Structured interaction**: Flows provide a structured framework for organizing conversations between users and AI-agents, ensuring a seamless and intuitive user experience.
* **Message sequencing**: Nodes within flows determine the sequence of messages presented to users, allowing for logical progression through the conversation.
* **User input handling**: Flows include nodes to capture and process user inputs, such as text messages, selections, or commands, enabling AI-agents to understand user intents and respond accordingly.
* **Conditional logic**: Flows can adjust dynamically based on user responses using [condition nodes](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/logic-nodes), enabling personalized interactions.
* **AI-agent goal achievement**: Flows guide users through completing specific tasks or achieving objectives, such as placing an order, scheduling an appointment, or seeking information.

**Sample conversational flow**

**Use case**: Ordering South Indian Food from a AI-agent

![](https://i.imgur.com/zwPxgj6.png)

User: Show me the menu<br/>
AI-agent: Please select your Cuisine: South Indian, North Indian<br/>
User: South Indian<br/>
AI-agent: Please select the Item: Idly, Dosa, and Pongal<br/>
User: Idly<br/>
AI-agent: Please enter the quantity<br/>
User: 2<br/>
AI-agent: Thanks for ordering with us<br/>

This flow guides the user through the process of ordering South Indian food from the AI-agent by structuring a series of interactions between the user and the AI-agent.

## Key elements to build a flow

You can use the following elements to build a Conversational flows:

Icon | Options | Descriptions 
-----|---|-------------
| <img src="https://imgur.com/sGJ8plu.png" alt="drawing" width="40%"/> | [Nodes](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes) | Define specific points in the conversation flow
<img src="https://imgur.com/BDYFfE5.png" alt="drawing" width="10%"/> | [Channel filter](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/logic-nodes#2-channel-filter) | Set the active channels where you want the AI-agent deployed
<img src="https://imgur.com/AZ0zthd.png" alt="drawing" width="10%"/> | [Variables](https://docs.yellow.ai/docs/platform_concepts/studio/build/bot-variables) | Store static or dynamic values
<img src="https://imgur.com/yA4l4Mk.png" alt="drawing" width="10%"/> | [Language](https://docs.yellow.ai/docs/platform_concepts/studio/build/localization) | Choose the language(s) your AI-agent needs to support
![](https://imgur.com/15aueyb.png)| [Flow trigger](https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/configureflow) | Triggers the flow based on the selected Intent, Entities, Event, and URL clicks

![](https://imgur.com/Yauehn0.png)

## Flow visualization settings

Once you have manually designed your conversational flow, exported a template, or automated the flows, you can use the following options to visualize the flow:

![](https://imgur.com/2t5ryBl.png)

Icon | Options | Description 
---|-----|------------
 ![](https://imgur.com/bbBFnxu.png) | Zoom in | This options allows you to zoom in on the flow diagram, making the text and elements larger and easier to read.
 ![](https://imgur.com/UbuXaST.png) | Zoom out | This options allows you to zoom out of the flow diagram, making the text and elements smaller and allowing you to see rest of the flow at once.
![](https://imgur.com/in92bBz.png) | Fit view | This option adjusts the zoom level to fit the entire flow diagram within the viewable area, ensuring that the entire flow is visible on the screen
![](https://imgur.com/XShq0SD.png)| Auto layout | Automatically arranges the nodes and connections within the flow diagram in an organized manner. You can also undo the alignment by clicking the *Undo* option.
![](https://imgur.com/n4kCtBU.png) | [Settings](#flow-settings) | This option includes additional settings related to the flow visualization such as Init function, Change category, Mandate words, Precluded words, Disable steps for Go Back functionality, and Channels. For more information, see [Flow settings](#flow-settings).
![](https://imgur.com/0l7QrYH.png)| Minimap | This option displays a overview of the entire flow diagram, allowing you to navigate to different sections of the flow by clicking on the desired section in the minimap.

## Flow settings

You can configure the following flow settings for your flow:

| Field | Description |
| ------ | ---------- |
| Init function | Function that will be executed before going through a flow.|
| Change category | Change the Category of the flow if required. |
| Mandate words | Include the mandatory words that have to be in the user's utterance to trigger this flow.|
| Precluded words | Flow will not be triggered if these words are present in the user utterance.|
| Disable steps for Go Back functionality | If the user response is 'go back' (or related words - configured in tools), this takes them to the previous question. At the flow level, you can disable some steps from which going back should not be allowed.|
| Channels | Flow will trigger only for the selected active channels. |

<img src="https://imgur.com/cxJhFwM.png" alt="drawing" width="90%"/>

## Best practices for creating bot flows

Follow these best practices to ensure your flow meets user expectations and achieves its objectives:

1. **Understand your agent's objectives**: 
     * **Define the purpose**: Understand the scope and purpose of your bot (use case). Clearly outline what types of questions or requests the bot should handle based on your intended use case. For example, answering FAQs, booking services, or providing support.
2. **Start with a clear flow structure**
     * **[Welcome and Fallback flows](https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/manage-flows#configure-start-welcome-and-fallback-flow)**: Set up specific flows to greet users and handle unrecognized inputs.
     * **Entry triggers** – Clearly specify what starts a flow, such as user queries, button clicks, or events.
     * **Use conditional logic**: Use [Condition nodes](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/logic-nodes) to create logical branches that handle multiple scenarios and outcomes.
4. **Manage your flows**: You can update flows, create duplicates for similar use cases, or remove outdated flows as needed.
5. **Enable Live agent assistance**: If the bot cannot resolve a query, use the Raise ticket node transfer the user to a live agent.
6. **Integrate with backend systems**: Include [APIs](https://docs.yellow.ai/docs/platform_concepts/studio/api/add-api), [databases](https://docs.yellow.ai/docs/platform_concepts/studio/database), and third-party integrations if you want to fetch or update data from third-party systems.
7. **Enable multichannel support**: Design the flow to work across multiple channels like web, mobile apps, and social media.
8. **Provide [multi-language support](https://docs.yellow.ai/docs/platform_concepts/studio/build/localization)**: Use the Set Language node to allow your users to interact in their preferred language.








