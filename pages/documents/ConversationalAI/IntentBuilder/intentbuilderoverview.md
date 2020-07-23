---
pagename: Overview
redirect_from:
    - conversation-builder-intent-builder-overview.html
Keywords:
sitesection: Documents
categoryname: "Conversational AI"
documentname: Intent Builder
permalink: intent-builder-overview.html
indicator: both
---

The Conversation Builder platform's Intent Builder allows you to build multiple intent domains that can each hold one or many intents and entities. Most brands will find that one domain can handle all their intents, but sometimes breaking them up is necessary or desirable. For example, having a Main intent domain and a Small Talk intent domain is very common.

Intents direct a bot to be more flexible and respond to a wider variety of user input. Instead of looking for specific patterns in the input (for example, the pattern "bill"), the bot uses a Natural Language Understanding (NLU) engine to look for a defined intent. Then the bot triggers the dialog that's configured to respond to the intent. Therefore, once you configure your intents with robust *training phrases*, expressions like, "I have a question about billing", "Looking to check my account," or "What's my billing status?" yield the same intent and, thus, the same response from the bot.

<img class="fancyimage" style="width:800px" src="img/ConvoBuilder/ib_intentDetails.png">

{: .important}
See [here](intent-builder-natural-language-understanding.html) to learn more about the different NLU engines that are compatible with Conversation Builder.

### Access Intent Builder

**To access the Intent Builder application**

1. On the left sidebar in Conversational Cloud, click the <img style="width:30px" src="img/ConvoBuilder/icon_cb.png"> icon.
2. In the Conversational AI dashboard, click **Intent Builder**.

### High-level concepts

#### Domains

The following are key characteristics of a domain:

* A domain is a collection of related [intents](intent-builder-intents.html) and [entities](intent-builder-entities.html).
* A domain has a specified NLU provider and language.
* In a bot, you can associate one domain with each dialog. This allows you to associate the dialog's interactions with intents and entities from that domain. For example, you might [associate an intent with a Dialog Starter interaction](conversation-builder-assist.html) to use the intent to trigger the dialog's flow.

#### Training

Domains that use either the LivePerson NLU v2 engine or a 3rd-party NLU engine must be explicitly trained (i.e., you click the **Train** button that's available). This process takes the raw training data and uses it to create a “machine-learning” model that generalizes the data. The resulting model is then used to make predictions on user utterances. With these NLU engines, most of the work needed to be able to make predictions on user utterances is performed *at training time*, allowing for a faster response at run time.

In contrast, domains that use the LivePerson NLU v1 engine aren’t trained, and there is no machine-learning model created. The comparison of the user utterance against the intents and entities is performed at run time. With this NLU engine, be aware that the larger the domain, the more time the prediction response takes. This is because most of the work needed to be able to make predictions on user utterances is performed *at run time*.

### High-level workflow

When working in Intent Builder, you’ll use one of the following high-level workflows depending on the provider/version of the NLU engine used by the domain.

**LivePerson NLU v1 domain**

<img style="width:450px" src="img/ConvoBuilder/ib_highLevelWorkflow1.png">

**LivePerson NLU v2 domain or 3rd-party NLU domain**

<img style="width:725px" src="img/ConvoBuilder/ib_highLevelWorkflow2.png">

There are some iterative steps in each workflow.

If the domain is using a 3rd-party NLU engine, you'll need to [connect the NLU engine](intent-builder-natural-language-understanding.html#connect-a-3rd-party-nlu-engine) before you train.

### Starter packs

To get you quickly up and running with [intents](intent-builder-intents.html), LivePerson provides a set of starter packs that you can easily add to your Intent Builder environment. A starter pack is a ready-made domain that includes a set of well-defined, predefined intents. There are two kinds of starter packs available:

* Generic starter packs for a number of verticals: Telecommunications, Financial Services, and more.
* Cross-vertical starter packs that are appropriate for all verticals. These include starter packs for things like account management, billing and payment, “small talk,” and more.

**Screen**

Once you [add a domain using a starter pack](intent-builder-domains.html#add-a-domain-using-a-starter-pack), you can customize the domain as you see fit. It behaves like any other you might create manually or via an import file.

If you want a quick, low effort way to get up and running with well-defined intents, LivePerson recommends that you get started by using starter packs.

{: .important}
Starter packs for the [LP NLU v1 engine](intent-builder-natural-language-understanding.html#livepersons-nlu-engine) aren’t supported.
