## Lab-03: Build a basic Power Automate flow in Microsoft Copilot Studio.

# Task-01: Create a new topic.

1.Login to **https://copilotstudio.microsoft.com/**

  ![screenshot of the prompt ](../Media/03/login-1.png)

2.Choose the **Copilot** Environment then Create a new copilot named **User 1 Contoso Customer** 
   
  ![screenshot of the prompt ](../Media/03/login-2.png)
	
3. Select the **New Topic** drop down at the top of the page and **choose the From Blank** 
  option. Enter **Check Weather** as the name of your topic.

5.Click on edit Phrases then enter simple trigger phrases, such as **What is the weather** and **What is the temperature today**, until you have at least five trigger phrases. Select the **Edit** button within the node to open a pane to the right of the screen where you can add the trigger phrases.

  ![screenshot of the prompt ](../Media/03/phrases.png)

6.Create a **new Question node** below the trigger phrase node and then enter text, such as: `Of course, I can share the weather with you! Can you tell me the name of the region where you want to know the weather?`

  ![screenshot of the prompt ](../Media/3.1/question.png)

8.Rename the variable to **Region**. To do so, select the name of the variable within the node. Within a pane that appears to the right of the screen.

  ![screenshot of the prompt ](../Media/3.1/phraese1.png)

9.Within the top right corner of the screen, select the **Save** button to ensure that your work is saved.

## Task-02: Create your Power Automate flow

1.Select the **Add node button** below the question node to add a new node to the topic. Select **Call an action > Create a flow**. Power Automate opens in a new browser window 

   ![screenshot of the prompt ](../Media/3.1/get-temp.png)

3. Click on In the first node **When Power Virtual Agents Calls a flow** new flow window that opens, select the **Add an input** within the first scaffolded action. Then, select **Text**.

  ![screenshot of the prompt ](../Media/3.1/powerflow.png)
       
   ![screenshot of the prompt ](../Media/3.1/txt.png)

4. Within the first column, enter `Region` (leaving the second column empty).

   ![screenshot of the prompt ](../Media/3.1/region.png)

6. Then, select the **Insert new step** button to **add a new action**.

7. Select the **Add an action** option from the menu.

8. Enter `weather` in the search bar and then select **Get current weather by MSN Weather**.
    
    ![screenshot of the prompt ](../Media/3.1/weather.png)

9. A new node appears, where you can enter the location , from the Dynamic content drop-down menu, select **Region** and then keep units as **Imperial**.

  ![screenshot of the prompt ](../Media/3.1/getcurrent.png)

10.Select the **Return value(s) to Microsoft Copilot Studio** node at the end of the flow, then select **Add an output > Number** . Place your cursor in the **Enter a value to respond** text box. Select **Temperature** from dynamic data to add it to the response text box. Then, enter **Temperature** in the Title field.

  ![screenshot of the prompt ](../Media/03/temperature.png)

12. The flow is almost complete, select the template title and rename it to `Get Temperature`.

13. Select **Save** on the flow in Power Automate to ensure that it saves. Wait a moment until the green banner appears, indicating success then Select **Publish** .

![screenshot of the prompt ](../Media/03/save.png)

## Task-03 : Connect a Power Automate flow with Microsoft Copilot Studio.

1.In this task, you connect a Power Automate flow with Microsoft Copilot Studio `https://web.powerva.microsoft.com`

2. Open your existing topic in Microsoft Copilot Studio, entitled **Weather**, and return to the bottom of your flow, as shown in the following screenshot. Select **Call an action**. Your new Power Automate flow displays in the list. From the list, select **Get Temperature**.

![screenshot of the prompt ](../Media/03/get-temperature.png)

>**Note**: If the flow does not show up, save the Check Weather topic and refresh the page.

4. Select **Enter or select a value** and then select the **Region** variable that you created in previous steps of this lab. 

![screenshot of the prompt ](../Media/3.1/shit.png)

5. Add a Condition node so that you can check if the **Temperature** variable is greater than 75.

6. For the true branch, if the Temperature is greater than 75, add the following text within the 
  Message node:

`For {Topic.Region} the temperature is {Topic.Temperature} and that is getting warm! Consider cooling off with one of our cold brew coffees.`

>**Note**: The braces { } are variables to display dynamic data. To enter variables into the node, use the {X} button on the Message node and then select a variable from the list.

7. For the All other conditions branch, add the following text within the message node: The temperature for **{Region}** is `{Topic.Temperature}`. Where the braces { } are variables to display dynamic data.
   
![screenshot of the prompt ](../Media/3.1/enter-for.png)

15. To end the conversation, select the **Add node** button below the condition. Select **Topic management** and then choose **End conversation**.

      ![screenshot of the prompt ](../Media/3.1/endcon.png)

16. **Save** your topic using the button found in the top right corner of the screen and then Click on **test your copilot** and test it out 

    ![screenshot of the prompt ](../Media/3.1/endotput.png)
	
17. You successfully created a Power Automate flow and a new topic in Microsoft Copilot Studio that used the flow to provide real-time data from an external service to the user.

