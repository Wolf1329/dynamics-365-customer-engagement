---
title: Implement a custom scenario for smart assist agent
description: Use this topic to learn how to enable similar case suggestions and use custom actions to build your custom smart assist agents.
ms.date: 04/29/2025
ms.topic: reference
author: neeranelli
ms.author: nenellim
ms.reviewer: nenellim
---

# Implement a custom scenario for smart assist agent

[!INCLUDE[cc-rebrand-bot-agent](../../includes/cc-rebrand-bot-agent.md)]

This topic provides information on how you can enable similar case suggestions in your smart assist AI agent.

## Prerequisites

> [!IMPORTANT]
> Read the topic [Build a smart assist agent](smart-assist-bot.md) for information on how to get started with building a custom smart assist agent. 

- You need to have an understanding on how to create an agent using [Azure Bot Service](/azure/bot-service/abs-quickstart?view=azure-bot-service-4.0&preserve-view=true). When you register your agent with Azure Bot Service, you obtain `Microsoft App ID` and `Client secret` which you need to update the `appsettings.json` file in the agent.
- Create a Language Understanding (LUIS) app by following the instructions mentioned in [Add natural language understanding to your agent](/azure/bot-service/bot-builder-howto-v4-luis?tabs=csharp&view=azure-bot-service-4.0&preserve-view=true). See the section [Retrieve application information from the LUIS.ai portal](/azure/bot-service/bot-builder-howto-v4-luis?tabs=csharp&view=azure-bot-service-4.0&preserve-view=true#retrieve-application-information-from-the-luisai-portal) for information on how to retrieve the values you need to setup the agent.

## Scenario: Similar case suggestion

This scenario enables you to suggest similar cases with open case action button. The customer service representative (service representative or representative) is presented with a list of similar cases as a recommendation. The representative clicks on the case that they finds most similar and relevant, and then goes to the case note and looks at the resolution in note. The representative suggests the same resolution to the customer over chat.

### Generate intent to interpret the context of the conversation

It is necessary analyze the conversation and understand its context before recommending an action to the representative. Use [Language Understanding (LUIS)](https://luis.ai) to find the intent of the ongoing conversation. Here is an example on how you can create a LUIS app to find intent from a given text: [Quickstart: Use prebuilt Home automation app](/azure/cognitive-services/luis/luis-get-started-create-app).

You can create intents for each issue type or topic that you want to address for incoming requests from customers or the most common topics being discussed.  

For the example scenario of similar case recommendations for "printer noise" issue, create an intent with the same name and add 10-15 examples like "printer noise, loud noise from printer, printer makes grinding noise, loud click noise, and loud sound". The LUIS app then needs to be trained for this intent.  

### Author adaptive cards to display recommendations in the smart assist UI

[Adaptive cards](https://adaptivecards.io) is an open-source standard that helps apps and services exchange rich snippets of native UI. The smart assist agent interprets the conversation context in real-time and provides recommendations to the representatives.

### Custom actions for implementing custom functionalities

Custom actions can help you implement custom functionalities in your smart assist agent.

The steps for enabling the similar case scenario are as follows:

1. **Set up Similarity Rules**

Setup similarity rule by following the steps 1 to 7 in mentioned here: [Create a new similarity rule to view similar cases](../administer/suggest-similar-cases-for-a-case.md#create-a-new-similarity-rule-to-view-similar-cases).
 
2. **Turn Relevance search ON**

Turn on Relevance Search in the administrator section. Learn more in [Enable a field for exact matching of similar cases](../administer/suggest-similar-cases-for-a-case.md#enable-a-field-for-exact-matching-of-similar-cases). 
  
3. **Similar cases API**

Similar cases can be fetched using the `GetSimilarRecords` function. But before you execute the Web API query with this function, make sure that you set up similarity rules. More information: [Use advanced similarity rules to view similar case suggestions](../administer/suggest-similar-cases-for-a-case.md). Also, make sure to enable **Relevance Search** in the administrator section to ensure that similarity rules work in the expected manner. Also, in the **Match Field** section add a few criteria such as case title and case type.

**Request**

```http
GET [Organization URI]/api/data/v9.1/GetSimilarRecords(Id=@Id,Filter=@Filter,ReturnFields=@ReturnFields)?@Id={"@odata.id":"incidents(<incident id>)"}&@Filter=null&@ReturnFields={"AllColumns":false,"Columns":["title","description"]}
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0 
```

Replace the `incident id` in the Web API request above with the unique identifier of the case for which you want to find similar cases.

**Response**

```json
{
    "@odata.context": "[Organization URI]/api/data/v9.1/$metadata#incidents",
    "value": [
        {
            "@odata.type": "#Microsoft.Dynamics.CRM.incident",
            "@odata.etag": "W/\"1571835\"",
            "title": "Product question re warranty",
            "modifiedon": "2019-03-03T12:58:25Z",
            "incidentid": "f69e62a8-90df-e311-9565-a45d36fc5fe8"
        },
        {
            "@odata.type": "#Microsoft.Dynamics.CRM.incident",
            "@odata.etag": "W/\"1572750\"",
            "title": "Shipment question re order",
            "modifiedon": "2019-03-03T12:58:27Z",
            "incidentid": "129f62a8-90df-e311-9565-a45d36fc5fe8"
        }
    ]
}
```

#### Calling custom actions using adaptive cards

Create a web resource if you want to use embed a custom action within a suggestion. See the Power Apps topic on [Create your own actions](/powerapps/developer/common-data-service/custom-actions) for information on how to build a custom action. See the topic [Web resources in model-driven apps](/powerapps/maker/model-driven-apps/create-edit-web-resources) for information on how to create web resources. Upload these web resources under the **Active Conversation** form.
The supported custom actions are as follows.

**OpenForm custom action**

This custom action enables you to open any entity record.

```json
{
              "type": "Action.Submit",
              "title": "Open",
              "data": {
                             "CustomAction": "OpenForm",
                             "CustomParameters": {
                                           "entityName": "incident",
                                           "entityId": "c3356c37-bba6-4067-b1a1-8c66e1c203a1",
                                           "data": {}
                             }
              }
}
```

**SendKB custom action**

This custom action enables you to send a knowledge base article. 

> [!NOTE]
> The `CustomAction` key should contain `SendKB` and `kbLink` key should contain the link of the KB article. You cannot have another custom action with the same name as `SendKB`.

```json
{

          "type": "Action.Submit",
          "title": "Send",
          "data": {
                          "CustomAction": "SendKB",
                          "CustomParameters": {
                          "kbLink": "https://ocddemoebc.powerappsportals.com/knowledgebase/article/KA-01011/en-us"
                  }
          }
}
```

You can use the client-side APIs to open knowledge base articles. See [Client API reference for model driven apps](/powerapps/developer/model-driven-apps/clientapi/reference) for more information.


## Related information

[Build a smart assist agent](smart-assist-bot.md)<br />
[Sample code: Smart Assist for agents](https://github.com/microsoft/Dynamics365-Apps-Samples/tree/master/customer-service/omnichannel/smart-assist-bot)<br />
[Smart assist for representatives](../administer/smart-assist.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
