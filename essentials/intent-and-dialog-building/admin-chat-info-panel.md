# Admin Chat Info Panel

When creating Guided Flows it is often useful to see the data stored in the [Conversation Context](conversation-context.md). To do so, you can use the **Admin Chat Info Panel** feature.

## **Toggle the Info Panel**

Click on the "..." menu button on the top-left of the Admin Chat header, and then click on the "Show Info Panel" item. You can use the same menu item to hide the Info Panel.

![](../../.gitbook/assets/65.png)![](../../.gitbook/assets/66.png)

## **Usage Scenarios**

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Scenario</b>
      </th>
      <th style="text-align:left"><b>Example</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p><b>Inspect Data Collected from User</b>
        </p>
        <p>In this scenario, the first State asks the Chat User &quot;What city would
          you like to go to?&quot;, and also has the Data Collection block activated
          to collect the user&apos;s reply in the <em><b>city</b></em> variable.</p>
        <p>After the Chat User replies with &quot;Bali&quot;, this value is stored
          in the Conversation Context in the <em><b>city</b></em> variable</p>
      </td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/67.png" alt/>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>Inspect</b>  <a href="editing-an-intent.md#service-action-block">Service Action</a><b> Inputs and Outputs</b>
        </p>
        <p>When executing external services via Service Action, it is useful to see
          what is being sent to the Service as <em>Inputs</em> and what is being returned
          in the response as <em>Data</em> and or <em>Display</em>
        </p>
      </td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/68.png" alt/>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>Inspect Service Action Errors</b>
        </p>
        <p>As errors can occur in Service calls, Service Action provides error handling
          capabilities.</p>
        <p>If an error occurred, you will see the Error Code and Message on the Info
          Panel.</p>
      </td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/69.png" alt/>
      </td>
    </tr>
  </tbody>
</table>

