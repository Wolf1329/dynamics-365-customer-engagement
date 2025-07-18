---
title: Assignment methods for queues
description: Learn about the different assignment methods for queues and how you can use them in unified routing.
ms.date: 07/18/2025
ms.topic: conceptual
author: neeranelli
ms.author: nenellim
ms.reviewer: nenellim
ms.collection:
ms.custom: bap-template
searchScope:
- D365-App-customerservicehub
- D365-Entity-queueitem
- D365-UI-*
- Customer Engagement
- Dynamics 365
- Customer Service
---

# Assignment methods in unified routing

[!INCLUDE[cc-feature-availability-embedded-yes](../../includes/cc-feature-availability-embedded-yes.md)]

Use assignment methods to determine how to assign work items. You can use the out-of-the-box assignment methods or build custom assignment rules by configuring the prioritization rules and assignment rulesets.

## How automated assignment works

The auto assignment process in unified routing matches incoming work items with the best-suited customer service representatives (service representative or representative) based on the configured assignment rules. This continuous process consists of multiple assignment cycles and a default block size of work items.

Each cycle picks up the top unassigned work items in the applicable default block size and attempts to match each work item with an appropriate representative. Work items that aren't assigned to representatives because of their unavailability or because no matching skill was found are routed back to the queue. The next assignment cycle picks up the next block of the top-priority items that includes new work items.

When eligible representatives aren't found for the work items, the assignment cycle keeps retrying to assign the top number of default sized block items as applicable for the channel.

For digital messaging and voice, the default block size is 100 work items of top priority.

For the records channel,
- The work items prioritized per queue are 10,000 
- The work items processed for assignment are 2,000 by default

Learn more in [best practices to manage queues](unified-routing-best-practices.md#manage-queues).

## How unified routing prioritizes work items

Unified routing prioritizes work within individual queues and across queues. Prioritization within a queue can be of the following types:

- First-in-first-out is the default prioritization logic applicable for the out-of-box assignment methods and [custom assignment methods](configure-assignment-rules.md) that have no prioritization rules.
- Custom prioritization that can be defined with a custom assignment method.

The oldest conversation or work item in the queue is assigned first. For asynchronous messaging channels such as persistent chat, WhatsApp, and Facebook, the oldest conversation is determined based on the last interaction time. For example, if the first contact on WhatsApp for a customer is on Monday, and the initial problem is resolved by Tuesday but the conversation isn't closed, it goes into the [waiting state](../use/oc-conversation-state.md). If the same customer comes back on Thursday afternoon with a new question while new customers are waiting in the queue since Thursday morning, the returning customer is prioritized only after the customers who are waiting since Thursday morning.

For record queues, the first-in-first-out assignment method is based on the time the record was routed, which is when the associated live work item is created. Learn more in [Understand how unified routing affects queue items and live work items for routed records](../develop/unified-routing-impact-on-apis.md).

If you want to prioritize assignment based on conversation creation time, you can use custom prioritization rules.

When service representatives are subscribed to multiple queues, you can use the [Queue priority](queues-omnichannel.md#configure-queue-prioritization) field of the queue to prioritize work across queues. Work from the higher priority queues is assigned first over lower priority queues. Queues can also be given the same priority. In such a case:
- If they have the default first-in-first-out ordering, the oldest item across all these queues is assigned first.
- If they have custom prioritization rules, then the queues are ordered alphabetically based on the queue names to determine the highest priority work. 

If you have configured queues based on both out-of-the-box assignment methods and custom prioritization rules, the queues with out-of-the-box assignment methods are prioritized first followed by the queues based on custom prioritization rules.

For example, lets look at a setup with the following four queues, all with priority defined as 1:

- **VIP Support and Premium Support**: Default first-in-first-out prioritization
- **Order Support and Invoice Inquiries**: Custom prioritization rules

For a representative who is subscribed to all the four queues, they receive the oldest item from the VIP Support and Premium support queues. If these two queues don't have eligible items for the representative, work from the Invoice Inquiries queue is assigned next followed by the work from the Order Support queue. 

> [!NOTE]
> We recommend that you assign distinct queue priorities to queues with custom prioritization rules. Even if the queues have the same prioritization ruleset, they're considered to be distinct.

## Types of assignment methods

The assignment methods available out of the box are explained in the sections that follow.

### Highest capacity

The system assigns a work item to a service representative with the highest available capacity. The selected representative has the skills that are identified during the classification stage and presence that matches one of the allowed presences in the workstream. If more than one representative is available with the same capacity, the work item is assigned based on the round-robin order.

If you want to use skill-based routing, the "exact match" and "closest match" options are available.

- If you set **Default skill matching algorithm** in the workstream as **Exact Match**, then the system filters representatives using exact skill match, allowed presence for the workstream, capacity requirements, and orders the filtered representatives by available capacity.

- If you set **Default skill matching algorithm** in the workstream as **Closest Match**, the system filters representatives based on the presence allowed for the workstream and capacity requirements. The system then orders the filtered representatives by closest match and not available capacity. Learn more in [Closest match](set-up-skill-based-routing.md#closest-match).

If you need to distribute work fairly among representatives, then you should consider switching to a round robin assignment strategy.

> [!NOTE]
> When you modify a rating model, the ongoing conversations or open work items that have skills with the rating model continue to have the existing rating. Sometimes, this might result in no representatives who match the assignment criteria.

### Advanced round robin

The system assigns a work item to the representative who matches the criteria for skills, presence, and capacity. The initial order is based on when a user is added to the queue. Then, the order is updated based on assignments. Similar to how work items are assigned in the highest capacity method, in round robin assignment, the work items are prioritized as mentioned at [How unified routing prioritizes work items](#how-unified-routing-prioritizes-work-items).

The ordering for round robin assignment is maintained queue-wise. Some representatives can be a part of multiple queues. Therefore, depending on the representative's last assignment timestamp in a queue, the representatives might be assigned back-to-back or concurrent work items but from different queues.
In scenarios when multiple representatives match the work item requirement, and there's a tie in the "order by", like, multiple matched representatives with the same available capacity, the system resolves the assignment using round robin based on the earliest time of the last assignment.

For example, three representatives, Lesa, Alicia, and Alan, are available with the coffee refund skill and can handle up to three chats at a time. Their last assignment time stamps are 10:30 AM, 10:35 AM, and 10:37 AM, respectively. A work item about a coffee refund arrives in the queue at 10:40 AM. With the order by set to "profile-based available capacity", all the representatives at 10:40 AM have the same available capacity of 2 each. To break the tie between the representatives, the system uses round robin. Therefore, the incoming chat is assigned to Lesa because her last assignment was the earliest at 10:30 AM. Later at 10:45 AM, if another coffee refund work item comes in, the system assigns it to Alicia. This is also based on the round robin order of assignment between Alicia and Alan because their available capacities are 2 each and Alicia had an earlier assignment than Alan at 10:35 AM.

### Least active

The system assigns a work item to the representative who is least active among all the representatives in voice and messaging queues and who matches the required skills, presence, and capacity.

The assignment method uses "the time since last capacity is released for a voice or messaging conversation" and the [**Block capacity for wrap-up**](create-workstreams.md#configure-work-distribution) setting configured in the workstream to determine the least-active representative and routes the next incoming call to them.

Let's see how it works with the following examples.

**Scenario 1**

Oscar Ward and Victoria Burke are two service representatives with the same skills. Oscar works on the **Members Messaging** queue, while Victoria works on **Members Messaging** and **Returns Voice** queues.

- **Number of conversations with Oscar**: 1 chat
- **Number of conversations with Victoria**: 1 call and 1 chat

At 1:00 PM, a new chat conversation arrives.

Because Oscar has fewer concurrent conversations than Victoria, the new chat is assigned to Oscar.

**Scenario 2**

Maya and Hailey are two service representatives with the same skills. Maya works on the **Orders Messaging** queue, while Hailey works on **Orders Messaging** and **Delivery Voice** queues. 

Let's assume that Hailey is working on a call and chat at the same time while Maya is engaged in two chat conversations.

Maya completes one of the chats at 1:55 PM, and Hailey completes the chat at 2:00 PM. A new chat conversation arrives at 2:05 PM.

- **Number of conversations with Hailey**: 1 call
- **Number of conversations with Maya**: 1 chat

Because both Maya and Hailey have the same concurrent assignments, the least active assignment strategy considers the last capacity release time across both voice and messaging queues.

Maya is determined to be least active compared to Hailey and therefore, the new chat is assigned to Maya.

Routing to the least-active representative assignment strategy helps in a balanced distribution of work items across representatives, and results in higher representative efficiency and improved customer satisfaction.

You can also build a [custom report](model-customize-reports.md) to track a representative's "last capacity release time" and understand the assignment distribution across representatives. The data about the representative's last capacity release time is available in the "msdyn_agentchannelstate" Dataverse entity.

> [!IMPORTANT]
>
> The least-active assignment method is available for the voice and messaging channels only and is the default selection when you create a voice queue.
>
> This feature is intended to help customer service managers or supervisors enhance their team’s performance and improve customer satisfaction. This feature is not intended for use in making—and should not be used to make—decisions that affect the employment of an employee or group of employees, including compensation, rewards, seniority, or other rights or entitlements. Customers are solely responsible for using Dynamics 365, this feature, and any associated feature or service in compliance with all applicable laws, including laws relating to accessing individual employee analytics and monitoring, recording, and storing communications with end users. This also includes adequately notifying end users that their communications with representatives may be monitored, recorded, or stored and, as required by applicable laws, obtaining consent from end users before using the feature with them. Customers are also encouraged to have a mechanism in place to inform their representatives that their communications with end users may be monitored, recorded, or stored.

### Create new

You can also create a custom assignment method to suit your business needs. The system lets you create and use your own rulesets and rules to configure priority, severity, and capacity for choosing the queues to which work items need to be routed. You can create the following rulesets:

- **Prioritization rulesets**: Lets you define the order in which the work items are assigned to representatives when they're available to take more work.
- **Assignment rulesets**: Represent a set of conditions that are used to select representatives and use an order by option to sort the matching representatives.
  
> [!IMPORTANT]
>
> - You must configure presence, capacity, and skill-matching rules in the custom assignment method because the default settings defined for the workstream won't be used in custom assignment method.
> - The out-of-the-box assignment strategies don't consider the representative operating hours. You must write a custom assignment method by using the "is_working" operator in the rule definition.

### Assignment cycle

Assignment cycle is the prioritization of work items, their selection, and their assignment to the best-suited representative based on the assignment rules. Unified routing optimizes the assignment cycles across the multiple queues in the organization for best performance.

The assignment cycle starts with one of the following triggers:

- Arrival of a new work item in the queue.
- Change to representative presence.
- Updates to representative capacity: If capacity is updated at runtime, then change in capacity triggers assignment. If capacity is updated manually, the change doesn't trigger assignment. 
- Addition of a representative to the queue.
- Periodic trigger every five minutes for record type of work item.

## How prioritization rulesets work

A prioritization ruleset is an ordered list of prioritization rules. Every prioritization rule represents a priority bucket within the queue. In a prioritization rule, you can specify a set of conditions and order by attributes. During evaluation, the prioritization rules are run in the order they're listed. For the first prioritization rule, the work items in the queue that match its conditions are put in the same priority bucket. In the priority bucket, the items are further sorted by the order specified in the prioritization rule. The second rule runs on the rest of the items in the queue, to identify the next priority bucket, and sorts the bucket by the **Order by** attribute until all rules are evaluated.

You can create one prioritization ruleset only per queue.

As an example, consider the prioritization ruleset as seen in the following screenshot with four rules.

:::image type="content" source="../media/ur-prioritization-scenario.png" alt-text="Screenshot of a prioritization scenario.":::

- During any assignment cycle, this prioritization ruleset runs, and the rules within the ruleset run in the order they're listed.

- The first rule, "High priority and premium," finds all work items in the queue where the associated case priority is "High" and the case category is "Premium". The system creates the top priority bucket with those work items and sorts them in the "First in and first out" manner as specified in the **Order by** attribute. The first work item to be assigned from the queue is the oldest item in this bucket.

- The next priority bucket is the work items where case category is "Premium". The work items with "Premium" case category and "High" priority have already been put in top bucket as per the preceding rule, so this rule only considers other work items with "Premium" case priority. The **Order by** attribute in this case also is "First in and first out".

- The next priority bucket consists of work items where case priority is high and they haven't been bucketed already. Here the work items are ordered by their "First Response By" field in the ascending order—that is, the work items that require the first response at the earliest are prioritized first.

Some important points about prioritization rules are as follows:

- You can create only one prioritization ruleset per queue.
- Prioritization rules are run during every assignment cycle. If you change any attributes of the work item, such as the priority of the case, that change is considered during the next assignment cycle.
- By default, the queue is sorted on a "first in and first out" manner. If you don't create a prioritization rule, then the oldest work item is assigned first.
- In normal scenarios, when a sufficient number of representatives are available to take up the work items, the processing period is a couple of seconds only. The representatives are assigned work items in the priority order. However, if work items pile up because of fewer eligible representatives, and then a representative becomes available during the processing period, the representative is offered the next work item according to the priority order. This strategy might create a perception that the highest priority item wasn't assigned; especially after some top-priority items are attempted for assignment and yet remain in the queue.
- The work items that don't match the criteria of any of the prioritization rulesets are kept in the last priority bucket, and are ordered by "first in first out".
- Prioritization rules are skipped for affinity work items and such work items are assigned before other work items in the queue. Learn more about affinity in [Representative affinity](create-workstreams.md#representative-affinity).

## How assignment rulesets work

The assignment ruleset is an ordered list of assignment rules. Each assignment rule represents a set of conditions that is used to determine the representatives to select and an order-by field to sort the matching representatives. At runtime, the assignment rule with the top order is evaluated first. The representatives are matched as per the conditions specified in the rule. If more than one matching representative exists, they're sorted by the order by field, and the top representative is assigned the work. If no representatives are matched, then the next assignment rule in the ruleset is evaluated. This method can be thought of as a gradual relaxation of constraints in the assignment, such that first, the strictest criteria are applied, and then the conditions are reduced so that the best representative is found. If no matching representatives are found, then the work item remains in the queue.

In the assignment rule, the system user attributes are matched with the requirement of the work item. When you select static match, the condition is formed on the System User entity attribute and static values. When you select dynamic match, the conditions on the left are based on the system user root entity and the conditions on the right are based on the conversation root entity. You can drill down to two levels on the conversation root entity to form the rule conditions. An assignment rule with the dynamic match and static match is as follows.

:::image type="content" source="../media/assignment-rule-root-entity.png" alt-text="Screenshot of an assignment rule with dynamic match and static match conditions.":::

### Components of an assignment rule

The assignment rules are composed of the following items:

- **Order**: Specifies the order in which the assignment rule is evaluated in a ruleset. The lower-order rules are run first. If any rule results in matching a user, then the next set of rules isn't evaluated.
- **Name**: The unique rule name.
- **Condition**: The expressions that are evaluated to match the users with the attributes of incoming work. The conditions have three parts:
  - **User attribute**: Properties of the users that can be used for comparing the user with the incoming work. The user attributes can be one of the following:
    - **Select attributes on the System User table.**
    - **Presence Status**: Maintained by the unified routing service based on user workloads and manual selection.
    - **Capacity**: Maintained by the unified routing service based on user workloads and manual selection.
    - **User skills**: Represents the skills associated with the user that can be used for doing skill-based assignment.
    - **Calendar Schedule**: Schedule of the user as represented in the user service scheduling calendars.
    - **Bot attributes**: Can be used only when you have configured bots as users and want to do some comparisons on them.
  - **Operators**: Define the comparison relationship between the User attribute and incoming work item attributes. 

      Unified routing filters the attribute-specific operators for you to choose from. Some special operators that are available for the attribute types are as follows.
    
      |Attribute type|Operator|Definition|
      |--------------|--------|----------|
      |Presence Status| Equals, Does not equal, Contains data, Does not contain data| Use an operator to find representatives who have matching presence status as specified in the work item. |
      |Capacity|Equals, Does not equal, Contains data, Does not contain data|Use an operator to compare if the representative has enough capacity to work on the specified items. <br>**Note**: The system implicitly performs capacity profile check in custom assignment but for unit-based capacity, you need to specify the conditions.|
      |User skills|Exact match|Use an operator to find representatives who have all the skills which the incoming work item requires.|
      |User skills|Custom match|Use the operator to find representatives whose skills match at runtime based on the selected lookup attribute on the work item.|
      |Calendar schedule|Is working|Use this operator to find representatives who are working as per their service scheduling calendars. Automated assignment considers the representative calendar schedule only and doesn't consider the operating hours defined for the queues.|
  
  - **Value**: The user attributes are compared against this value to find the right representative. The value can be static, such as Address 1: County equals "USA". The value can also be dynamic, so that you can compare the user attribute dynamically with the values on the work item. In dynamic values, you can select any attribute on the work item or related records. For example, the following condition finds users whose country/region is the same as that of the customer associated with the case.
  
     :::image type="content" source="../media/dynamic-value-match.png" alt-text="Screenshot of a sample dynamic match.":::

    For some operators, values aren't required. They can be conditions, such as "Contains data," "Does not contain data," and "Calendar schedule: is working."

    For user skills, the values are predefined for the operators. Learn more in [Set up skill-based routing](set-up-skill-based-routing.md).

- **Order by**: If multiple representatives match the conditions in a rule, you can use the "Order by" clause to find the best-suited one. You can specify the following order by clauses:

  - **Ordering Attributes**:

    - **Least active**: Is available for voice and messaging queues only. The work item is routed to the least active representative who matches the required skills, presence, and capacity. Learn more in the [Types of assignment methods](#types-of-assignment-methods) section.
    - Round robin
    - Unit-based available capacity
    - Profile-based available capacity
    - Proficiency
    - Skill count

  - **User Attributes**: These attributes are defined on the system user entity.

A sample assignment rule is explained in the following scenario with a screenshot.

:::image type="content" source="../media/ur-sample-assign-scenario.png" alt-text="Sample assignment method.":::

The first condition specifies the "user skills" on which the operator is an exact match. Then the user attributes are evaluated. The different user attributes are specified with operators, and values for each attribute, such as the **Presence status** attribute, should be equal to "Available" or "Busy". On the right of the operator, you can specify the value that you want the attribute to be matched against. The values can be "static," such as "presence status equals Available or Busy". If you specify "dynamic," the condition is matched at runtime based on the expression you specify. For example, if you specify "Preferred Customer Type Equals Conversation.Contact.Membership Level," the "preferred customer type" of every representative is matched against the dynamically calculated membership level of the customer associated with the chat.

Dynamic match reduces the effort of having to write and maintain multiple static rules for each permutation and combination of the possible value.

### Limits on offering a work item repeatedly to a representative

Representatives can accept or decline work items that come through automatic assignment. Both [rejection](enable-agent-reject-notifications.md) and [allowing the notification to time out](manage-missed-notifications.md) are considered as declining the work item. If a representative declines a work item by either method, their priority for that conversation is reduced during the next assignment attempt. The representative might be reconsidered for the same work item up to three times or the specified limit in following scenarios:
- If the representative is uniquely qualified for the declined conversation and meets the capacity and presence requirements.
- If all other eligible representatives also decline.

If the representative declines the same work item three times or reaches the configured limit, the representative is no longer considered for auto assignment of that particular work item. The system then attempts to assign the declined work item to other eligible representatives in the queue. The representatives can still manually pick the work item.

For example, representative Serena Davis rejects a chat from customer Ana Bowman twice and the assignment notification times out in the third attempt. The system considers it as three declines and auto assignment won't offer the same chat to Serena Davis again. But the system offers the chat from Ana Bowman to other eligible representatives. Also, Serena Davis is considered for other incoming conversations except the declined chat from Ana Bowman.

> [!NOTE]
> If all matching representatives decline the work item because representative availability is low or the work requires a very specific skill and proficiency, the work remains in the queue. Similarly, if 100 representatives decline a particular work item, auto assignment won't consider the work item in further assignment cycles. It can be manually assigned by supervisors or can be picked up by other representatives including those who rejected it.

You can update the default limit of three declines to a value between one and five based on your org requirement. The limit is applicable to all channels in the org.

You can make an OData call as follows to check the limit for your organization.

`<org-url>/api/data/v9.0/msdyn_omnichannelconfigurations?$select=msdyn_number_of_declines_allowed`

If this OData call returns the null value, it means that the decline limit is set to a default value of 3.

You can update the OData call as follows to modify the limit.

`var data = { "msdyn_number_of_declines_allowed": 3 } // update the record Xrm.WebApi.updateRecord("msdyn_omnichannelconfiguration", "d4d91600-6f21-467b-81fe-6757a2791fa1", data).then( function success(result) { console.log("Omnichannel Configuration updated"); // perform operations on record update }, function (error) { console.log(error.message); // handle error conditions } );`

### Related information

[Configure assignment methods and rules](configure-assignment-rules.md)  
[FAQ about unified routing in Customer Service, Omnichannel for Customer Service](unified-routing-faqs.md)  
[Conversation diagnostics](configure-conversation-diagnostics.md)  
[Create workstreams](create-workstreams.md)  
[Create queues](queues-omnichannel.md)  
[Set up unified routing for records](set-up-record-routing.md)  
[Set up skill-based routing for unified routing](set-up-skill-based-routing.md)  
