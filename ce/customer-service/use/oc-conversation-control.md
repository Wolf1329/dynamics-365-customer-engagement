---
title: View the communication panel for conversations
description: Learn what you can do as a representative in the communication panel when you interact with the customer.
ms.date: 07/25/2025
ms.topic: how-to
author: neeranelli
ms.author: nenellim
ms.reviewer: nenellim
ms.custom: bap-template
---

# View the communication panel for conversations

[!INCLUDE[cc-feature-availability-embedded-yes](../../includes/cc-feature-availability-embedded-yes.md)]

The communication panel is where you, as a customer service representative (service representative or representative), interact with your customer. When you sign in to the application, the communication panel is in hidden mode by default. You can view the communication panel only when you accept an incoming conversation to communicate with the customer.

If you want to minimize the communication panel, select **Minimize**. The communication panel is collapsed to a window in the left corner of the Active Conversation form, giving you more screen space.

You can increase or decrease the width of the communication panel for a specific channel by dragging the right edge of the communication panel to the left or right. The resized width of the communication panel is channel specific. For example, if you increase the width of the communication panel for chat, the next time you get a chat conversation, you'll see the resized panel. However, the width remains the same for another channel, such as WhatsApp.
You can resize the communication panel when it is in the expanded mode only.

You can do the following tasks in the communication panel:

- Send quick replies.
- Search for and share knowledge articles with the customer with whom you are interacting.
- Transfer the conversation (work item) to another representative or queue.
- Use the consult option if you need help with resolving the work item.
- Generate a summary of the conversation. More information: [View and share auto-summarized conversations](cs-ai-generated-summary.md)


## Enhance productivity using keyboard commands

The communication panel has options that you can use to perform actions, such as see quick replies, consult, and transfer, and launch notes control. You can also use keyboard commands to perform these actions.

 > [!div class=mx-imgBorder]
 > ![Omnichannel communication panel chat interface.](../media/oceh-conversation-control-chat-interface.png "Omnichannel communication panel chat interface")  

The following table lists the options and the keyboard shortcuts that you can use.
 
| Annotation | Option     | Description                                   | command |
|------|------------------|-----------------------------------------------|----------|
|  1   | Quick replies    | Send templated messages created by you as personal quick replies or quick replies created by your administrator | `/q` |
|  2   | Consult          | View list to consult with other users | `/c` |
|  3   | Transfer         | View list to transfer the request | `/t` and `/tq` |
|  4   | Add to chat      | Is enabled when the second representative accepts a consult request||
|  5   | - Take notes <br>- Link to conversation <br>- Translation | - Take notes specific to conversation <br>- Link the record to this conversation<br> - If translation of messages is enabled, you can turn on or off the translation  ||
|  6   | Customer sentiment | View real-time customer satisfaction levels |  |

## Send quick replies

The communication panel allows you to send predefined messages to a customer with whom you're interacting. These predefined  messages are stored as quick replies.

Use the following options to use quick replies in your conversation:

- Select the **Quick replies** button to retrieve the messages and send them to the customers and or representatives with whom you consult.

- Use a keyboard command to see the list of quick replies. Type the forward slash (/) key and the letter q (**/q**). When you type **/q**, the **Quick replies** panel is displayed.

- Select **View all**. The quick replies are displayed in the right pane. You can select a quick reply in the list to send to the customer. You can also choose a language of your choice and search for the quick replies.

   :::image type="content" source="../media/view-all-quick-replies.png" alt-text="Vew all quick replies option that lets you see quick replies in the right pane.":::

You or the administrator can create the quick replies. You can create personal quick replies if the administrator has enabled the option. Your quick replies are available on the **Personal** tab of the **Quick replies** panel, and those created by the administrator are available on the **All** tab. Use the personal quick replies when you're in a conversation with a customer by doing the following:

1. Select the quick responses icon ![quick responses icon.](../media/personal-quick-reply-icon.png) at the bottom of your conversation window. The **Quick replies** panel displays the available predefined messages on the **All** and **Personal** tabs.
2. Select the **Personal** tab, and type the number sign (#) in the compose box to list the tags and search for the personal quick replies that are available for your use.
3. Use the **more** option to view the complete text of the quick reply.

    > ![Use personal quick reply.](../media/use-personal-quick-replies.png "Use personal quick reply")

### Search for quick replies and tags

After you type **/q** in the communication panel messaging area, you can continue typing any keywords and if the **Quick replies** library has at least one message associated with the word, it's filtered and displayed to you. You can also use the number (#) sign to search for the predefined messages.

You can type any of the following options in the compose box to search for the messages that are available for your use:

   * Type **/q**, followed by <**keyword**>, to list messages that match the keyword.
   * Type **/q**, followed by the number sign (**#**), to list all tags.
   * Type **/q**, followed by <**tagname**> <**keyword**>, to list quick replies that match the tag and keyword.
   * Type **/q**, followed by <**tagname**>, to list all quick replies that match the tag. Additionally, you can also add another tag after the <**tagname**> for example, type **/q**, followed by <**tagname**> <**tagname**>, to further refine the quick replies matching both the tags.

 > [!div class=mx-imgBorder]
 > ![Type /q and the keyword to filter the replies.](../media/oceh-send-quick-replies-filter.png "Filter replies")  

### Share reconnection link with customers

If the reconnection link is configured by your administrator, you can share the link with customers during the session that they can use to connect back to the chat when they're disconnected for some reason, such as loss of connectivity or restart of their computer. The reconnection link information is available as a quick response.

> [!IMPORTANT]
> You can share the reconnection link only when you don't end the chat session using the **End** button.

## Consult with representative or supervisor

You can consult with other representatives or supervisors using the consult option. You can invite the representative or supervisor by selecting the **Consult** button in the communication panel and choosing from the list of available representatives.

The following events occur when you select the **Consult** button:

- You can search for representatives to consult within the same queue or other queues. Additionally, you can filter them within a queue based on their skills. The application displays the representatives whose skills match the selected criteria in full or partially, along with their name, and current presence status.

   :::image type="content" source="../media/add-to-consult.png" alt-text="Select the people icon to add the secondary representative to the conversation.":::

- Select and invite a representative, and then start a consultation.

- The secondary representative receives a notification for the consult request.

- When the secondary representative accepts the consult request, a separate pane with an option to end opens beside the communication panel for the primary representative. 
 
   :::image type="content" source="../media/consult-primary-agent-view.png" alt-text="View of consult pane for the primary representative.":::

- The secondary representative sees a consultation window on the page with an option to leave. They'll also have a read-only view of the messages exchanged between the primary representative and customer. Consulting on a chat conversation doesn't affect the secondary representative's capacity.
   
- The primary representative can add the secondary representative to the customer conversation by selecting the people icon. The secondary representative can join the customer conversation only after the primary representative selects to add the representative.

Additionally, the following considerations apply:

- You can use the UI buttons to collapse and expand the consult pane. When the primary representative selects the option to take notes, the consult pane is in collapsed mode.
- The primary representative can end the consult or the secondary representative can leave, after which, the secondary representative won't be able to view the interaction between the primary representative and customer.

You can also use a keyboard command to see the list of representatives and or supervisors who are available for consultation. Type the forward slash (/) key and the letter c (**/c**). Type forward slash and the letters cq (**/cq**) to view the list of queues.

> [!Note]
> We recommend that you invite no more than five consulting representatives when conversing with the customer.

After you type **/c** in the communication panel messaging area, you can continue typing the name of the participant and if it's present, the names are filtered and displayed to you.

## Transfer conversations

If your administrator has enabled the [**Transfer to representatives**](../administer/enable-transfer-consult.md) setting in the Copilot Service admin center, the **Representatives** tab appears when you select the transfer icon and you can transfer the conversation to another representative.

In the communication panel, you can transfer the work item to a representative or queue. If operating hours are configured for the queues, you can successfully transfer the conversation to those queues only that are operational at the transfer time.

:::image type="content" source="../media/screenshot-transfer-option.png" alt-text="Use the transfer option to transfer a conversation.":::

> [!NOTE]
> When you transfer a conversation to a queue, the assignment strategy runs to find the best representative in the queue. If the queue doesn't have any representatives, the application automatically sets the status of the conversation to Closed.

After the transfer is complete, the representative who initiated the transfer can't participate in the conversation any more. The primary representative's capacity and presence status are updated accordingly.

Representatives whose presence is set to Busy-DND, Away, or Offline don't appear in the representative list of the transfer pane.

Use the keyboard command to see the list of representatives and/or the supervisor who is available for transfer. Type the forward slash (/) key and the letter t (**/t**).

Use the keyboard command to see the list of queues to transfer the conversation request. Press the forward slash (/) key and the letters T and Q (**/tq**).

**/t** (forward slash, letter t) launches the **Representatives** and **Queues** tabs. Select either tab and then select the representative or the queue from the list to transfer the conversation. The **/t** command keeps the focus on the **Representatives** tab whereas the **/tq** command keeps the focus on the **Queues** tab.

When skill-based routing is enabled, then during the transfer, the **Transfer** panel shows users sorted in the order of matching skills. A check for representative skills isn't done by the app and the conversation can be transferred to any representative irrespective of the skill match.

When a conversation needs to be transferred from one queue to another, the matching criteria that were used in the conversation is reused to find a representative in the new queue. For example, if exact match was used to attach the skills to the conversation, the same criteria is used to find the representative in the new queue.

:::image type="content" source="../media/screenshot-transfer-to-representative.png" alt-text="Screenshot of selecting a representative to transfer the conversation.":::

### Search representatives or queues for transfer of conversation requests

After you type **/t** or **/tq** in the communication panel messaging area, you can continue typing the name of the participant and if it's present, the representative or queues names are filtered and displayed to you.

**/taq** (forward slash, letter t, letter a, letter q) helps you search for the queue in the **Representatives** tab of the transfer window.

## Take notes specific to conversations

Use the notes option to capture information specific to the conversation when you interact with customers. Use the More commands option in the communication panel to launch the notes.

To learn more, see [Take notes specific to conversation](oc-take-notes.md).

## Link to conversations

> [!Note]
> Link to conversation isn't applicable to the embed experience.

When you have a conversation with a customer, you can use the link option that's at the bottom of the conversation control to link the conversation to the case, account, or contact record.

To learn more, see [Search, link, and unlink a record to the conversation](oc-search-link-unlink-record.md).

## Monitor real-time customer satisfaction

As a representative, you can view the real-time customer satisfaction levels on the communication panel. A sentiment icon is displayed at the top of the communication panel based on the previous six customer messages sent to you.

To learn more, see [Monitor real-time customer sentiment](oc-monitor-real-time-customer-sentiment-sessions.md)

## Close or end a conversation

When you select the close button (**X**) to close the communication panel, a confirmation message appears to let you know that the session will end. Select **Close** on the dialog if you want to end the session.

When you select the **End** button, the conversation ends, and the customer receives a message that the service representative has ended the conversation.

:::image type="content" source="../media/conversation-end-close.png" alt-text="Screenshot of the communication chanel with the close and end options.":::

The conversation behavior is dependent on the channel through which it comes. Learn more in [How conversations are handled on close or end](oc-conversation-state.md#how-conversations-are-handled-on-close-or-end).


### Related information

[Monitor real-time customer sentiment](oc-monitor-real-time-customer-sentiment-sessions.md)  
[Introduction to the agent interface](oc-introduction-agent-interface.md)  
[Manage sessions](oc-manage-sessions.md)  
[Manage applications](oc-manage-applications.md)  
[Manage presence status](oc-manage-presence-status.md)  
[View customer information on Active Conversation form](oc-customer-summary.md)  
[Search for and share knowledge articles](../oc-search-knowledge-articles.md)  
[Take notes specific to conversation](oc-take-notes.md)  
[View active conversations for an incoming conversation request](oc-view-customer-summary-incoming-conversation-request.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
