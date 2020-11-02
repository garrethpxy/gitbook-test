# Multilingual Bots

Converse Bots can also understand and speak more than one language. Access to this feature is configured per Converse installation. For access to this feature, please contact your administrator.

## Supported Languages 

Currently, Converse supports the following languages, with more on the way.

* English
* Vietnamese

## Language Selector

The **Language Selector** in the Navigation Bar allows you to manage a specific **Language Variant** for each Intent.

![Use the Language Selector to choose the language](../.gitbook/assets/image%20%2816%29.png)

## Intent Language Variants

Each Intent in your Multilingual Bot will have a Language Variant for each Language available. In other words, if the Bot can speak English and Vietnamese, it will have have an English variant and a Vietnamese variant. 

Language Variants allows us to edit only the Language-specific content of an Intent, while keeping other non language related Intent's properties shared across the Intent's variants. 

#### **The following properties are shared across Language Variants:**

* [Intent Details](intent-and-dialog-building/editing-an-intent.md#edit-intent-details) \(Intent Name, Tags, etc\)
* [Bot Response](intent-and-dialog-building/editing-an-intent.md#configuring-an-intents-response-using-the-state-editor) \(Conversation Flow structure, consisting of Dialog States and Transitions\)
  * This means you only need to build your Intent's Conversation Flow once, and all Language Variants will use it.
  * Likewise, when an Intent's Conversation Flow is changed, all Language Variants are affected.
* [Message Component](intent-and-dialog-building/editing-an-intent.md#modern-editor-message-components) within each Dialog State 

#### **The following properties can be configured per Language Variant:**

* [Intent Status](intent-and-dialog-building/change-an-intents-status.md#intent-statuses)
  * Each Language Variant can have its own Status. For example, an Intent's English Variant can be Activated while the Vietnamese Variant can be Inactive.
* [Training Phrases](teaching-your-bot.md#adding-and-deleting-phrases)
  * Each Language Variant has its own set of Training Phrases. 
* [Text Fields](multilingual-bots.md#language-specific-text-fields) within each Message Component.
  * These allow you to configure the text content of bot responses for each language.

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

![English and Vietnamese Bot Responses share the same flow structure](../.gitbook/assets/image%20%284%29.png)

This makes your Multilingual Bot easier to maintain, because you don't need to rebuild the Conversation structure for each Language Variant. However, this has some important side effects to note:

* Adding or Removing a Dialog State will apply to all of the Intent's Language Variants
* Adding or Removing a Message Component from a Dialog State will apply to all of the Intent's Language Variants

#### Language Specific Text Fields

The **Text Fields** within the Message Components can be customized per Language. 

For example, the following green boxes in the Button List component:

![](../.gitbook/assets/image%20%2812%29.png)

Follow these steps to change Text Fields to language specific content:

1. Navigate to the Intent Editor for the Intent you want to edit
2. Set the [Language Selector](multilingual-bots.md#language-selector) to the desired language 
3. Change the Text Fields to the content in the current selected language
4. Save the Changes

The table below lists the available Language Specific Text fields for each Message Component.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Message Component</th>
      <th style="text-align:left">Language-specific Text Fields</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Text Message</td>
      <td style="text-align:left">The single text field is editable</td>
    </tr>
    <tr>
      <td style="text-align:left">Button List</td>
      <td style="text-align:left">
        <ul>
          <li>Text Message</li>
          <li>Button Name</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Quick Replies</td>
      <td style="text-align:left">
        <ul>
          <li>Text Message</li>
          <li>Button Name</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Carousel &amp; Card</td>
      <td style="text-align:left">
        <ul>
          <li>Title</li>
          <li>Description</li>
          <li>Button Name</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### Activating / Deactivating Language Variants

Language Variant can be Activated or Deactivated individually from one another.

This means you can Activate the English Variant while keeping the Vietnamese Variant Inactive, and vice versa. This is useful in cases you only have one Language content prepared, or if a particular Intent is relevant in one language but not another.

Please be sure to Activate each Language Variant individually once you are done setting up the Training Phrases and Bot Responses!

### Archiving Intents

When an Intent is Archived, ALL Language Variants are affected. 

You should only change an Intent's Status to ARCHIVED if all Language Variants for this Intent are no longer valid.

## Working with Unhandled Phrases 

### View Unhandled Phrases for a Specific Language

* Navigate to the Unhandled Phrases page
* Set the Language Selector to your desired language
* The Unhandled Phrases displayed will be those for the specified language only. 
* Past Resolved and Invalid Phrases will also be Language specific

### Resolve Unhandled Phrases

#### Resolve to Existing or New Intent 

The Unhandled Phrases will be resolved to the Training Phrases for the Intent's Language Variant. Other Language Variant's Training Phrases will not be affected.



