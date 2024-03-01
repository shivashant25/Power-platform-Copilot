# Lab-02: Create an approval flow with Copilot in Power Automate.

## Task–01: Create an approval flow.

1. Sign in to Power Automate.

2. In the center of the Home page within Power Automate, in the text field on Start building your flow with Copilot, enter the following prompt:request approval when a Dataverse record is created,Select the Submit button,Screenshot of Copilot in Power Automate prompt text field.

3. From the prompt, Copilot provides the outline for a suggested flow that you can review. To accept the flow, select Next,Screenshot displaying the suggested Power Automate flow.
   
4. Review the connected apps and services. If a connection hasn't been made, edit or fix it and then select Create flow.

Screenshot of the Review your connected apps and services page.

The Edit with Copilot designer opens with your flow along with a Copilot chat window on the right.

Screenshot displaying the Edit with Copilot designer.

5. Set up some parameters by selecting the When a row is added, modified or deleted trigger.

A panel on the left side of the screen shows the trigger details, including an empty Table Name parameter that's required.

Screenshot displaying the When a row is added, modified or deleted trigger details.

6. From the Table Name dropdown menu, search for and select Real Estate Showings.

Screenshot highlighting the Table Name property in the When a row is added, modified or deleted trigger.

7. Select the Start and wait for an approval action.

Notice that the Approval Type parameter is missing.

Screenshot highlighting the Approval Type property in the Start and wait for an approval action.

8. From the Approval Type dropdown menu, select Approve/Reject - First to respond.

After you select the Approval Type, more parameters are now available.

Screenshot displaying the extra parameters after you select the approval type.

9. In the Copilot chat window, enter the following prompt:

Add "New Request for Real Estate Showing" as the Title parameter for the Start and wait for an approval action

It takes a few seconds for Copilot to process the prompt. When processing is complete, the Title parameter is populated with the prompt text.

Screenshot displaying how the Title parameter is populated with the prompt text.

10. For the Assigned To parameter, enter the email address that you're using for this lab. This email address is the one that receives the approval request.

11. For the Details parameter, enter the following text:

A new request for a real estate showing has been created. Please review the details below and approve or reject the request:

Property: Client: Client Email: Date: Time:

Screenshot displaying how the Details parameter is populated with text.

12. Place your curser next to Property: in the Details parameter and then select the lightning icon to open the Dynamic content pane.

Screenshot highlighting the Dynamic content icon.

13. In the Dynamic content pane, select See More to expand the list of available dynamic content.

Screenshot displaying where the See More link is located.

14. Scroll down until you find the Address field and then select it.

Screenshot displaying how the property field is selected.

The Address dynamic content field is now added to the Details parameter.

Screenshot displaying how the property dynamic content field is added to the Details parameter.

15. Complete the same steps for the Client, Client Email , Date, and Time fields.

When you're done with the rest of the fields, the values should resemble the following image.

Screenshot displaying how the Client, Client Email, Date, and Time dynamic fields are added to the details parameter.

16. With the Details parameter completed, you can collapse the Start and wait for an approval action by selecting the double arrow icon.

Screenshot showing the double arrow icon to collapse the Start and wait for an approval action.

17. Select the Condition action.

Screenshot showing the Condition action selected.

18. Select the Choose a value box and then select Outcome from the Dynamic content pane.

Screenshot of the Outcome dynamic content selected.

19. Select is equal to for the condition and then enter Approve for Value.

Screenshot showing the condition set to Approve.

20. Collapse the Condition action and then select the Update a row action under the True branch of the condition.

21. From the Table Name dropdown menu, search for and select Real Estate Showings.

22. Select the Row ID field and then select the Real Estate Showings unique identifier field from the Dynamic content pane.

23. Screenshot highlighting the Row ID field in the Update a row action.

Whenever you create a table in Microsoft Dataverse, a column is automatically created with the same name of the table. This column serves as the unique lookup ID for the record (or row) that was created.

24. Select Show all under Advanced parameters.

Screenshot displaying the Show all link under Advanced parameters.

25. Select Confirmed from the Status dropdown menu.

Screenshot displaying the Status property as Confirmed.

When a showing is approved, the Status field in the Real Estate Showings table is updated to Confirmed.

26. Collapse the Update a row action and then select the Update a row action under the False branch of the condition.

27. From the Table Name dropdown menu, search for and select Real Estate Showings.

 Select the Row ID field and then select the Real Estate Showings unique identifier field from the Dynamic content pane.

28. Select Show all under Advanced parameters.

29. Select Canceled from the Status dropdown menu.

When a showing is rejected, the Status field in the Real Estate Showings table is updated to Canceled.

## Task-03: Update the flow ,send an email and Run the App.

30. Collapse the Update a row action.

31. In the Copilot chat window, enter the following prompt and then submit:

Under the "Update a row" action for both branches in the condition, add a new "Send an email (V2)" action

After a few seconds, Copilot should explain what it did, as shown in the following image.

Screenshot displaying how Copilot explains what it did.

The updated flow should display.

Screenshot of the updated flow with a new Send an email action.

32. Select the Send an email action under the True branch of the condition.

33. Select the To field, remove the example@example.com email address, and then select the Client Email field from the Dynamic content pane.

34. For the Subject field, enter the following text into the Copilot chat window and then press the Enter key on your keyboard:

Add "Your request for a real estate showing has been approved" as the Subject parameter for the Send an email action

The Subject field should populate with the prompt text.

Screenshot displaying how the Subject field is populated with the prompt text.

35. For the Body field, enter the following text into the Copilot chat window and then press the Enter key on your keyboard:

Add "Good day - Your request for a real estate showing has been approved. Please see below for details." as the Body parameter for the Send an email action

The Body field should populate with the prompt text.

Screenshot displaying how the Body field is populated with the prompt text.

36. Enter the following content after the Body text:

Property:

Agent Name:

Showing Date:

Showing Time:

Add the Address, Agent Name, Date, and Time fields from the Dynamic content pane to the appropriate lines in the Body text.

Screenshot displaying how the Address, Agent Name, Date, and Time dynamic content fields are added to the Body text.

Add the Response summary field from the Dynamic content pane to the end of the Body text.

Screenshot displaying how the Response summary field is added to the Body text.

Collapse the Send an email action.

Select the Send an email action under the False branch of the condition.

Select the To field, remove the example@example.com email address, and then select the Client Email field from the Dynamic content pane.

For the Subject field, enter the following content into the Copilot chat window and then press the Enter key on your keyboard:

Add "Your request for a real estate showing has been rejected" as the Subject parameter for the Send an email action

For the Body field, enter the following text into the Copilot chat window and then press the Enter key on your keyboard:

Add "Good day - Your request for a real estate showing has been rejected. Please see below for details." as the Body parameter for the Send an email action

37. Enter the following content after the Body text:

Property:

Agent Name:

Showing Date:

Showing Time:

Add the Address, Agent Name, Date, and Time fields from the Dynamic content pane to the appropriate lines in the Body text.

38. Add the Response summary field from the Dynamic content pane to the end of the Body text.

Screenshot displaying how the Response summary field is added to the Body text for the rejected email.

Collapse the Send an email action.

39. Rename the flow to Request Approval for Real Estate Showing by selecting the request approval when a Dataverse record is created text in the upper-left corner of the screen.

Screenshot highlighting the renaming of the flow.

Save the flow by selecting the Save button in the upper-right corner of the screen.

Screenshot of the Save button.

Test the flow by selecting the Test button in the upper-right corner of the screen. Select Manually and then select Test.

Screenshot of the Test Flow process.

To submit a real estate showing request, go to the Real Estate Showings app in Power Apps.

40. Run the app and then select +New to create a new showing request.

Fill in the fields with the following information:

Agent Name - < random name >
Client Full Name - < Your name >
Client Email - < Your email > (the email that you're using for this lab)
Date - < Any future date >
Time - < Any future time >
Status - Pending
Address - 210 Pine Road, Portland, OR 97204
 Note

41. This address is one of the addresses from the Microsoft Excel file in Module 1; it's the same file that you uploaded and turned into the Real Estate Properties table.

Usually, you would have a lookup field to the Real Estate Properties table, but not for this lab to keep it simple.

Select the check mark in the upper-right corner of the screen.

42. Select the X in the upper-right corner to close out of the app.

The flow runs and sends an approval email to the email address that you provided in the flow that you built.

Sign in to the email account that you're using for this lab and then wait for the email to arrive.

>Note : If the flow doesn't run immediately, make sure that you wait for it. It might take up to 10 minutes for the flow to be triggered, especially on the first try.

The approval should resemble the following image.

Screenshot displaying the approval email in Outlook.

43. Select Approve.

Add a comment and then select Submit.

Screenshot of the approval in Outlook.

44. The flow continues to run; it updates the row and sends an email to the requestor. The email that's sent to the requester resembles the following image.

Screenshot of the approval email that's sent to the client.

Check the flow and notice that the flow is now marked as Succeeded in the run history.

Screenshot displaying how the flow is marked as succeeded.

