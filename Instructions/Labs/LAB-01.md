# Lab-01: Create a canvas app with Copilot in Power Apps.

### Task 1 – Create environment
 
1.  Open a new browser tab and navigate to the Power Platform admin center `https://aka.ms/ppac` 

2.  Log in with your Microsoft 365 credentials.
 
3.  Skip the welcome tour by closing the prompt, or select **Get Started** to begin the tour and select **Next** through each prompt. At the end, select **Done** to finish the tour.
 
4.  Select **Environments** from the site navigation and select **+ New** from the toolbar.

5.  For **Name**, enter Copilot`

6.  For **Type**, select **Sandbox**. 

7.  Change the toggle on **Add a Dataverse data store?** to **Yes**. Leave all other selections as default and select **Next**.
 
8.  On the **Add Dataverse** tab, under **Security group** use the **+ Select** button, and under **Open access**, select **None**.

9.  Select **Done** and select **Save**.
 
10. In the list of environments, your **Copilot** environment should now show as **Preparing**.

11. Your practice environment will take a few minutes to provision. Refresh the **Environments** list if needed.
 
12. When your environment shows as **Ready**, select your **Copilot** environment by selecting the ellipses next to the name to expand the drop-down menu and select **Settings**.
 
13. Explore the different areas in **Settings** that you are interested in but do not make any changes.

## Task–02: Create an app with Copilot.

1.	On the Home page in Power Apps, Make sure you in the environment you previously created, in the center text field, enter the following prompt to search for an AI-generated table **build an app to manage real estate showings**, Select the Send button.

  ![screenshot of the prompt ](/Instructions/Media/copilot-chat-prompt.png) 

5.	After Copilot AI generates a table based on your prompt, look through the table to view the columns that are created for the start of your table.

  ![screenshot of the prompt ](/Instructions/Media/copilot-table.png)

8.	In the text box, in the lower part of the Copilot pane to the right of the screen, enter the following text: **add a column to track client full name**.Select the Send button.

 ![screenshot of the prompt ](/Instructions/Media/copilot-table-new-column.png)

>**Note**: Copilot notifies you that the table is updated, and the new column should show as being added to the table.

12.	In the text box, in the lower part of the Copilot pane to the right of the screen, enter the following text: **add a column to track client email**. Select the Send button.

 ![screenshot of the prompt ](/Instructions/Media/copilot-table-new-column-email.png)

>**Note**:
- The data that's generated in your table might vary from the data that's shown in the table in the screenshots for this lab.
- The Suggestions section in the lower-left corner of the screen provides you with different suggestions on how you can add to and modify your table.

16.	In the text box, in the lower part of the Copilot pane to the right of the screen, enter the following text: **add a column to track Address**. Select the Send button.

17.	On the right of the screen, it appears as if you're having a conversation with a Copilot AI bot while adding to and modifying your table. This area is where you can scroll through and view the changes or additions that you've made to your table.

18.	Screenshot showing Copilot conversation history.

19.	Edit the Status column within the table. In the text box within the Copilot pane, enter the following text and then send it:

20.	add an option for “Completed” to the Status column

21.	The system might take a minute to load. When it does, the Status column shows as updated and includes the option for Completed.

22.	Select the Status column name dropdown menu and then select View column where you can view the columns’ properties and the current status details and data.

23.	Screenshot of the Status column properties with the updated choices.

>Note : If your column choices aren't the same as the ones that are shown in the screenshot, enter the following command into the Copilot pane text box and then send it:

24.	the status choices should be Pending, Confirmed, Cancelled, and Completed

25.	Select the X in the upper-right corner of the pane to close it.

26.	Next, you'll add more data to your table and the existing columns.

27.	In the Copilot pane text box, enter and send the following text:

28.	add 5 more rows of data

29.	Five more rows of data are added for each existing column in the table.

30.	Screenshot of the Real Estate Showings table showing five added rows of data.

>Note: Your table should have several columns. However, to continue following the modules in this learning path, try to remove some columns that you won't use.

32.	The list of columns that you need are:
33.	ID
34.	Address
35.	Date
36.	Time
37.	Status
38.	Agent Name
39.	Client Full Name
40.	Client Email

41.	Use what you've learned with the Copilot Chat window to adjust your table to match the precceding list. Make sure that you refer to the Suggestions section if you need to remove a column, change a column name, or add a column.

42.	To create the app, select the Create app button in the lower-right corner of the screen.

43.	Screenshot of the Create app button in the lower-right corner of the screen.

44.	When the app first loads, a dialog might appear stating Welcome to Power Apps Studio. If so, select the Skip button.

45.	The app that has been built for you should show in Edit mode.

46.	Screenshot of the generated app in Power Apps Studio.

47.	Select the Data icon from the left navigation bar. Copilot has created a Dataverse table that's now displaying in the Environments section.

48.	Screenshot of the Dataverse table called Real Estate Showings in the Data panel of Power Apps Studio.

>Note: Currently, Copilot is only supported for Dataverse. You can't use any other data access point at this time.

## Task–03: Make edits using Copilot to edit your app.

1.	Next, you'll edit the table now that the app has been created.

2.	Within the Data pane, hover your mouse cursor over the table. To the right of the table, select the ellipsis (...).

3.	From the menu, select Edit data.

4.	Screenshot showing the action of selecting the Edit data option.

5.	In the Edit table dialog, you can add your own columns to the table or modify existing columns.

6.	Screenshot of the Edit table dialog with the Real Estate Properties data.

7.	Select the ID column header from the table.

8.	From the dropdown menu, select the Edit column option.

9.	Screenshot showing the action of editing a column within the Edit table dialog.

10.	In this example, you don't want the Data type to be a Single line of text. To change that value, go to the Edit column pane, and then from the Date type dropdown menu, select # Autonumber.

11.	Select Save.

12.	Screenshot highlighting the Autonumber data type and the Save button.

13.	Select the Close button in the lower-right corner of the Edit table dialog.

14.	The table should now show as Refreshed in the Data pane.

15.	Screenshot showing that the Real Estate Showings table has been refreshed.

16.	Modify the gallery in the application so that it displays the relevant data. Select the Tree view icon to return to the Tree view.

17.	On the app's main screen, select RecordsGallery1 to display Real Estate Showings and then select the edit button to put the gallery in edit mode.

18.	Select the Title and then set the Text value to the following formula:

19.	ThisItem.Address

20.	Select the Subtitle and then set the Text value to the following formula:

21.	ThisItem.'Client Email'

22.	Select the Body and then set the Text value to the following formula:

23.	ThisItem.Status

24.	A single record in the gallery should now resemble the following image.

25.	Screenshot of a single record in the Real Estate Showings Gallery.

26.	On the app's main screen, select the Form control.

27.	Screenshot of the selected form control from the app's main screen.

28.	On the Properties pane on the right, under the Fields property, select Edit fields.

29.	Screenshot showing the Edit fields option on the Properties pane.

30.	In the Fields pane, expand the ID field.

31.	From the Control type dropdown menu, change the type to View text.

32.	Screenshot showing the action of changing the ID control type to View text.

33.	Because you previously changed the ID field to Autonumber, you don’t want users entering their own number; Dataverse automatically enters the numbers for you.

34.	In the Fields pane, select the X in the upper-right corner to close the pane.

35.	Make a new request for a property that shows in the app by selecting the Play button from the upper part of the screen.

36.	Screenshot of the Play button in Power Apps Studio.

37.	In the left pane, select the +New button.

38.	Screenshot highlighting the add New record button in Power Apps Studio.

39.	Though you could modify the form to automatically fill in the fields for you, for this lab, you'll complete this step manually to observe how the app works.

40.	Fill in the fields with the following information:

41.	Agent Name - < Your name >

42.	Client Full Name - < Your name >

43.	Client Email - < Your email >

44.	Date - < Any future date >

45.	Time - < Any future time >

46.	Status - Pending

47.	Address - 210 Pine Road, Portland, OR 97204

>Note: This address is one of the addresses from the Microsoft Excel file in Module 1, and it's the same file that you uploaded and turned into the Real Estate Properties table.Though you'd usually have a lookup field to the Real Estate Properties table, this lab doesn't provide one to keep it simple.

48.	Select the check mark in the upper-right corner of the screen.

49.	Screenshot of the completed form, showing the check mark that you select to save your changes.

50.	Select the X in the upper-right corner to close out of the app.

51.	If a dialog appears saying Did you know?, select OK.

52.	The new request is added to the left of the list of requests.

53.	From the upper part of your screen, select the Save button to save the new app that you created.

54.	Screenshot of the Save button in Power Apps Studio.

55.	If the system prompts you, save the app name as Real Estate Showings.

56.	Exit the app to return to the Power Apps home page.
