# Multilingual Bots

Converse Bots can also understand and speak more than one language. Access to this feature is configured per Converse installation. For access to this feature, please contact your administrator.

## Supported Languages 

Currently, Converse supports the following languages, with more on the way.

* English
* Vietnamese

## Language Selector

The **Language Selector** in the Navigation Bar allows you to manage a specific **Language Variant** for each Intent.

![Use the Language Selector to choose the language](../.gitbook/assets/image%20%281%29.png)

## Intent Language Variants

Each Intent in your Multilingual Bot will have a Language Variant for each Language available. In other words, if the Bot can speak English and Vietnamese, it will have have an English variant and a Vietnamese variant. 

Language Variants allows us to edit only the Language-specific content of an Intent, while keeping other non language related Intent's properties shared across the Intent's variants. 

#### **The following properties are shared across Language Variants:**

* [Intent Details](intent-and-dialog-building/editing-an-intent.md#edit-intent-details) \(Intent Name, Tags, etc\)
* [Bot Response](intent-and-dialog-building/editing-an-intent.md#configuring-an-intents-response-using-the-state-editor) flow structure, consisting of Dialog States and Transitions
* [Message Component](intent-and-dialog-building/editing-an-intent.md#modern-editor-message-components) within each Dialog State 

#### **The following properties are language-specific, and can be configured per Language Variant:**

* [Intent Status](intent-and-dialog-building/change-an-intents-status.md#intent-statuses)
  * Each Language Variant can have its own Status. For example, an Intent's English Variant can be Activated while the Vietnamese Variant can be Inactive.
* [Training Phrases](teaching-your-bot.md#adding-and-deleting-phrases)
  * Each Language Variant has its own set of Training Phrases. Training Phrases must be written in the language of the Intent Language Variant.
* Text Content within each Message Component

## How to configure Intents in Multilingual Bots

The follow steps cover the process of creating an Intent that enables a Multilingual Bot to understand both English and Vietnamese Chat User inputs, and respond in the correct language.

Create a new Intent

Add English training phrases for the English Variant

Build English response content for the English Variant

Switch Language Selector to the Vietnamese 

Add Vietnamese training phrases for the English Variant

Add Vietnamese response content for the English Variant

Train Bot in both Languages

Test your Bot

## Working with Unhandled Phrases 

## 



