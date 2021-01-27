# Collect User Inputs using Slot Filling

## Introduction

Slot Filling enables the Bot to pick out specific pieces of information from user utterance. These specific information could be a date, time or named entities \(e.g. city\) defined in the Ontology. The information that have picked out can then be slotted in variables of the preceding states of the conversation flow. 

#### Example

The following screenshots shows an example of Slot Filling in action, where the named entity \('paris'\) and date \('this wednesday'\) on the user utterance were extracted, and printed in the response to the user message

![](../.gitbook/assets/image%20%2821%29.png)

![](../.gitbook/assets/image%20%2822%29.png)

## Set Up Slot Filling

### Defining the Named Entities in Ontology

1\) Click on the Ontology tab on the navigation bar to access the Ontology Manager.

2\) Create a new Individual under the **Term** Class

3\) Enter the name of the entity as the **\#label** and include the different possible answers as the **\#altLabel** 

![](../.gitbook/assets/image%20%2817%29.png)

4\) Define the **\#slot** that this named entity will be used in. The slot will be used in configuring the Intent to pick out the named entity. 

![](../.gitbook/assets/image%20%2819%29.png)

### Creating Intent with Slot Filling

#### Defining the Slot Fillers

1\) After creating the Intent, open up the **Slot Fillers** to define the entities that need to be capture in the conversation.

![](../.gitbook/assets/image%20%2820%29.png)



