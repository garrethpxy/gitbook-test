# Collecting User Inputs using Slot Filling

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

![](../.gitbook/assets/image%20%2825%29.png)

## Creating Intent with Slot Filling

### Defining the Slot Fillers

1\) After creating the Intent, open up the **Slot Fillers** to define the entities that need to be capture in the conversation.

![](../.gitbook/assets/image%20%2820%29.png)

2. Click on **Add Slot Filers**

3. ****Enter a **Variable Name** for the slot. This variable name will be used to store the entity captured from the user's input.

4. From the **Select Slot** dropdown list, choose the Named Entity defined in the Ontology that will be captured in this Slot.   
  
_Note: **date**, **datetime** and **time** are system default entities that can be used to capture date and time variable._

![](../.gitbook/assets/image%20%2823%29.png)

### Configuring State for Slot Filling

1\) Enable **Data Collection** in the State that would be capturing the user's input

2\) Select **Slot** as the Variable Type to enable slot filling for this State

3\) Select the **Variable** defined in the earlier section \([Defining the Slot Fillers]()\)

![](../.gitbook/assets/image%20%2824%29.png)

4. Toggle **Skip if Answer exists in the Context** to allow the Bot to skip the state \(i.e. not responding with the content of the state\), if the slot is already filled in the previous user's input.

### Configuring Slot Validation for Slot Filling

1\) **Slot Validation** can be enabled to ensure that users are providing the correct inputs to the required slot defined in each State.   
  
For example, the user's input should contain a date type input when the State require a date, or a City name when the State is expecting to capture a location. 

2\) Select **Slot Validation** under **Validation Type** in the **Data Collection** Block

3\) Configure the number of **Maximum Attempts** before the Bot break out of the guided flow to a failure/error State as configured in **Next State After Exceed Max Attempt**

4\) Provide an appropriate **Validation Message** to let the user know what is the expected input required. 

![](../.gitbook/assets/image%20%2826%29.png)



