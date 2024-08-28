# Lab-01: Create a canvas app with Copilot in Power Apps.

**Lab Scenario:**

In this exercise, you'll take on the role of a software developer tasked with creating a user-friendly canvas app using Power Apps Copilot. Your objective is to build an app designed to manage customer information effectively. Start by using Copilot to quickly generate a table with essential columns such as Customer ID, Full Name, Email, and Phone Number. Then, populate the table with sample data and make necessary adjustments, such as modifying column data types. Finally, design the app's interface to display and interact with the data, test its functionality, and publish the app for user access. This lab will showcase how Power Apps Copilot can streamline app development and enhance productivity.


### Task 1 – Create Power Platform environment

 In this task, you'll create and configure a new Power Platform environment to support app development and deployment. You'll set up essential details and adjust settings to meet your organizational needs.
 
1. In the new browser tab, navigate to the **Power Platform admin center** by visiting `https://aka.ms/ppac`

2. On **Sign into Microsoft Azure** tab you will see login screen, in that enter following email/username and then click on **Next**. 
   * Email/Username: <inject key="AzureAdUserEmail"></inject>

   ![screenshot of the prompt ](../Media/image7.png)

3. Now enter the following password and click on **Sign in**.
   * Password: <inject key="AzureAdUserPassword"></inject>
   
     ![screenshot of the prompt ](../Media/image8.png)

  >**Note**: Close the welcome tour prompt. 

4. In the site navigation, click on **Environments**, then click **+ New** on the toolbar.

   ![screenshot of the prompt ](../Media/new11.png)

5. Create a new Environment with the following settings:

   - **Name**: **Copilot (1)**
   - **Group**: **None (2)**
   - **Region**: **United States - Default (3)**
   - **Type**: **Sandbox (4)**
   - **Add a Dataverse data store?**: **Yes (5)**
  
    ![screenshot of the prompt ](../Media/copilot-final-1-1-1.jpg) 

6. Keep all other settings unchanged, Click on **Next**.  
 
9. On the **Add Dataverse** tab, under **Security group** use the **+ Select** button, and under **Open access**, select **None**.

   ![screenshot of the prompt ](../Media/select-2.jpg)

   ![screenshot of the prompt ](../Media/non-1.png)

10. Select **none (1)** and select **Save (2)**.
 
11. In the list of environments, your **Copilot** environment should now show as **Preparing**.

>**Note**:Your practice environment will take a few minutes to provision. Refresh the **Environments** list if needed.
 
12. When your environment shows as **Ready**, select your **Copilot** environment by selecting the ellipses next to the name to expand the drop-down menu and select **Settings**.
 
>**Note**: Browse through the various sections under **Settings** that interest you, but refrain from making any modifications.

## Task–02: Create an app with Copilot.

In this task, you'll use Power Apps Copilot to quickly create a canvas app, including generating and populating tables with data. You'll then design the app interface and test its functionality.

1. On the browser tab, go to `https://make.powerapps.com` to access Power Apps.

2. Enter the following prompt to search for an AI-generated table **build an app to manage real estate showings** , Select the Send button.

   ![screenshot of the prompt ](../Media/copilot-chat-prompt-1-1.png) 

3. Once Copilot AI generates a table based on your prompt, review the table to see the columns that have been created initially.

   ![screenshot of the prompt ](../Media/01/copilot-table-1.png)

4. In the text box at the bottom of the Copilot pane on the right side of the screen, type the following text: **add a column to track client full name**. Then, click the Send button.

   ![screenshot of the prompt ](../Media/01/copilot-table-new-column-1.png)

>**Note**: Copilot notifies you that the table is updated, and the new column should show as being added to the table.

4. Enter the following text: **add a column to track client email**. Then, click the Send button.

    ![screenshot of the prompt ](../Media/copilot-table-new-column-email-1-2.png)

>**Note**:
 - The data that's generated in your table might vary from the data that's shown in the table in the screenshots for this lab.
 - The Suggestions section in the lower-left corner of the screen provides you with different suggestions on how you can add to and modify your table.

5. Enter the following text:	**add an option for “Completed” to the Status column**. Select the Send button.

   ![screenshot of the prompt ](../Media/01/edit-table-1.png)

6. Enter the following text in the Copilot pane text box: **add 5 more rows of data**, Click Send. This action will insert five new rows of data for each existing column in your table.

    ![screenshot of the prompt ](../Media/copilot-table-new-rows-1-1.png)

10. In the text box, in the lower part of the Copilot pane to the right of the screen, enter the following text: **add a column to track Client Address (1)**. Select the **Send button (2)**,Select the **Create (3)**

    ![screenshot of the prompt ](../Media/01/client-address-1.png)

    > **Note**: Your table may have several columns. Consider removing any columns that you do not plan to use:The list of columns that you need are: ID ,	Address , Date , Time , Status , Agent Name, Client Full Name, Client Email.

 > **Note**: When you first open the app, you might see a welcome message.just click the **Skip** button.

12. The app that has been built for you should show in **Edit** mode.

    ![screenshot of the prompt ](../Media/01/reordsgallery-1.png)


## Task–03: Make edits using Copilot to edit your app.

In this task, you'll use Power Apps Copilot to make edits to your app, such as modifying existing elements, adding new features, and adjusting data. Copilot will guide you through streamlining and enhancing your app’s functionality and design.

1. In the Data pane on the right side of the table, click the **ellipsis (three dots)**. From the menu that appears, Choose **Edit** data.

   ![screenshot of the prompt ](../Media/copilot-edit-data.png)

2. Select the **ID** column header from the table.	From the dropdown menu, Select the **Edit** column option.
   
   ![screenshot of the prompt ](../Media/01/copilot-edit-column-1.png)
  
3. In this example, you need to change the Data type from "Single line of text." To do this, go to the Edit column pane, select **#Autonumber** from the Data type dropdown menu, then click **Save**. Finally, select the **Close** button in the lower-right corner of the Edit table dialog.

   ![screenshot of the prompt ](../Media/01/save-column-1.png)

4. Click on the **Ellipse** , Choose refresh.

   ![screenshot of the prompt ](../Media/01/copilot-refreshed-table-1.png)

5. Select the **Tree view** icon to return to the Tree view.

6. On the app's main screen, Select **RecordsGallery1** to display Real Estate Showings and then select the **edit** button to put the gallery in edit mode.

   ![screenshot of the prompt ](../Media/01/editing-1.png)

7. Select the Title and then set the Text value to the following formula: **ThisItem.'client Address'**
  
8. Select the Subtitle and then set the Text value to the following formula: **ThisItem.'Client Email'**
    
9. Select the Body and then set the Text value to the following formula: **ThisItem.Status**

10. A single record in the gallery should now resemble the following image.

    ![screenshot of the prompt ](../Media/01/copilot-checkmark-2.png)

11. On the app's main screen, select the **Form control**.

    ![screenshot of the prompt ](../Media/copilot-checkmark-1-1.png)

12. On the Properties pane on the right, under the Fields property, select Edit fields.

    ![screenshot of the prompt ](../Media/01/copilot-edit-fields-1.png)

13. In the Fields pane, expand the ID field.

14. From the Control type dropdown menu, change the type to View text.

    ![screenshot of the prompt ](../Media/01/copilot-view-text-1.png)

    >**Note**:previously changed the ID field to Autonumber, you don’t want users entering their own number; Dataverse automatically enters the numbers for you.

15. In the Fields pane, select the X in the upper-right corner to close the pane.

16. Make a new request for a property that shows in the app by selecting the **Play** button from the upper part of the screen.

    ![screenshot of the prompt ](../Media/01/copilot-play-1.png)

17. In the left pane, select the +New button.

    ![screenshot of the prompt ](../Media/01/copilot-new-1.png)

18. Though you could modify the form to automatically fill in the fields for you, for this lab, you'll complete this step manually to observe how the app works.

    ![screenshot of the prompt ](../Media/copilot-checkmark-1-1.png)

19. Fill in the fields with the following information:

    - Agent Name - < Your name >

    - Client Full Name - < Your name >

    - Client Email - < Your email >

    - Date - < Any future date >

    - Time - < Any future time >

    - Status - Pending

    - Address - 210 Pine Road, Portland, OR 97204

  > **Note** : This address is one of the addresses from the Microsoft Excel file in Module 1, and it's the same file that you uploaded and turned into the Real Estate Properties 
   table.Though you'd usually have a lookup field to the Real Estate Properties table, this lab doesn't provide one to keep it simple.

20. Select the check mark in the upper-right corner of the screen.

21. Screenshot of the completed form, showing the check mark that you select to save your changes.

22. Select the X in the upper-right corner to close out of the app.

23. If a dialog appears saying Did you know?, select OK.

24. The new request is added to the left of the list of requests.

25. From the upper part of your screen, select the Save button to save the new app that you created.

    ![screenshot of the prompt ](../Media/copilot-save.png)

26. If the system prompts you, save the app name as Real Estate Showings.

27. Exit the app to return to the Power Apps home page.
