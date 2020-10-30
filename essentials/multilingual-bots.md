# Multilingual Bots

Converse Bots can also understand and speak more than one language. Access to this feature is configured per Converse installation. For access to this feature, please contact your administrator.

## Supported Languages 

Currently, Converse supports the following languages, with more on the way.

* English
* Vietnamese

## Language Selector

The **Language Selector** in the Navigation Bar allows you to manage a specific **Language Variant** for each Intent.

![Use the Language Selector to choose the language](../.gitbook/assets/image%20%2813%29.png)

## Intent Language Variants

Each Intent in your Multilingual Bot will have a Language Variant for each Language available. In other words, if the Bot can speak English and Vietnamese, it will have have an English variant and a Vietnamese variant. 

Language Variants allows us to edit only the Language-specific content of an Intent, while keeping other non language related Intent's properties shared across the Intent's variants. 

#### **The following properties are shared across Language Variants:**

* [Intent Details](intent-and-dialog-building/editing-an-intent.md#edit-intent-details) \(Intent Name, Tags, etc\)
* [Bot Response](intent-and-dialog-building/editing-an-intent.md#configuring-an-intents-response-using-the-state-editor) \(Conversation Flow structure, consisting of Dialog States and Transitions\)
  * This means you only need to build your Intent's Conversation Flow once, and all Language Variants will use it.
  * Likewise, when an Intent's Conversation Flow is changed, all Language Variants are affected.
* [Message Component](intent-and-dialog-building/editing-an-intent.md#modern-editor-message-components) within each Dialog State 

#### **The following properties are language-specific, and can be configured per Language Variant:**

* [Intent Status](intent-and-dialog-building/change-an-intents-status.md#intent-statuses)
  * Each Language Variant can have its own Status. For example, an Intent's English Variant can be Activated while the Vietnamese Variant can be Inactive.
* [Training Phrases](teaching-your-bot.md#adding-and-deleting-phrases)
  * Each Language Variant has its own set of Training Phrases. Training Phrases must be written in the language of the Intent Language Variant.
* Text Content within each Message Component

## Configuring Multilingual Intents

### Adding Training Phrases 

Each Language Variant has a set of Language-specific Training Phrases. You will need to configure a set of Training Phrases for each Language.

1. Access the [Teaching Tool](teaching-your-bot.md#accessing-the-teaching-tool) 
2. Set the [Language Selector](multilingual-bots.md#language-selector) to the desired Language 
3. Add Training Phrases as described in [Teaching Your Bot](teaching-your-bot.md#adding-and-deleting-phrases)
4. Train the Bot 

#### Train the Bot in a specific Language

After adding the Training Phrases for a specific language, you should [Train your Bot](teaching-your-bot.md#training-your-bot) so that it will learn from the newly added Training Phrases and become even better at interpreting user's intentions.

**Important note: You can only train your Bot in one Language at a time.** 

### **Configuring Bot Responses**

#### Shared Conversation Flow Structure across Language Variants

In Converse, Bot Responses between Language Variants will follow the same flow structure and each Dialog State will contain same Message Components. 

&lt;screenshot&gt;

This makes your Multilingual Bot easier to maintain, because you don't need to rebuild the Conversation structure for each Language Variant. However, this has some important side effects to note:

* Adding or Removing a Dialog State will apply to all of the Intent's Language Variants
* Adding or Removing a Message Component from a Dialog State will apply to all of the Intent's Language Variants

#### Customize Text Fields per Language

Naturally, the **Text Fields** within the Message Components can be customized per Language.

&lt;screenshot&gt;

To do so:

1. Navigate to the Intent Editor for the Intent you want to edit
2. Set the [Language Selector](multilingual-bots.md#language-selector) to the desired language 
3. Change the Text Fields to the content in the current selected language
4. Save the Changes

#### Text Fields for each Message Component

&lt;table&gt;

## Step-By-Step

The follow steps cover the process of creating an Intent that enables a Multilingual Bot to understand both English and Vietnamese Chat User inputs, and respond in the correct language. 

The same steps can be followed for any other pair of Bot Languages \(e.g. English and Chinese\).

#### Create a new Intent

[Create a new Intent](intent-and-dialog-building/create-an-intent.md#creating-an-intent) with the name: "How do I create an account"

![](../.gitbook/assets/image%20%281%29.png)

#### Add English training phrases for the English Variant

To edit the English Variant of this Intent, ensure that the Bot Selector is set to English

![](../.gitbook/assets/image%20%287%29.png)

Click on the "Phrases" button below the Intent Name to open the Phrase Panel. Add the English Training Phrases to this panel.

![](../.gitbook/assets/image%20%282%29.png)

#### Build English response content for the English Variant

To build the bot response, we will use the [State Configuration Panel](intent-and-dialog-building/editing-an-intent.md#state-configuration-panel)

In the Content Block, switch to the Modern Editor using Toggle shown below

![](../.gitbook/assets/image%20%286%29.png)



Add a Button List component 

![](../.gitbook/assets/image%20%283%29.png)

Configure the Button List component like so:

![](../.gitbook/assets/image%20%2810%29.png)

Test the Bot out on the Admin Chat with Quick-Test

![](../.gitbook/assets/image%20%285%29.png)

Switch Language Selector to the Vietnamese 

Add Vietnamese training phrases for the English Variant

Add Vietnamese response content for the English Variant

Train Bot in both Languages

Test your Bot

## Working with Unhandled Phrases 

## 



