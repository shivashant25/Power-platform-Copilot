# Lab -02 Build apps through conversation.
  
## Exercise 1 Task 1: Create an app with the help of AI.

1.  Sign In to **powerapps portal** https://make.powerapps.com/environments/Default-cbc044cf-defc-4487-8475-4df2b4b237ca/home.
   
2.  In the text box, enter hotel housekeeping.

3.  A Dataverse table with data that includes typical hotel housekeeping tasks is created for you.


## Task 2 : Review the table for your app

>** Note**:
-**Suggestions**: These are suggested actions that you can ask the AI assistant to take to help you finalize the table.
-**View column**: Select to view the column name.
-**Edit table name**: View the table name and its properties.
-**Copilot**: Enter text to instruct the AI assistant on how to modify the table, such as remove room type column.
-**Create app**: Select Create app to create an app based on the table or select Cancel to start over.

1. In the Copilot text box enter, **Add columns** to track start and end time.

2. Copilot has added two new columns called, Start Time and End Time.

3. You can continue editing the table by adding features such as room status, change rooms, or set priority levels for each room. When you're ready to create your app, select Create app.

4. In Power Apps Studio, on the top right, select Copilot.

5 . In the Copilot panel, chat with Copilot and describe the changes you want to make such as Add a new screen.

## Excercise 2 : Create and edit topics in your Microsoft Copilot Studio copilot

## Task 1 : Create a topic

1. Open your copilot from the list on the Copilot page. For better visibility, close the Test copilot window for now.

2. From the Topics & Plugins page, select + Add > Topic > From blank.

3. On the Trigger node, select Edit under Phrases twice to see the Add phrases section.

4. Under Add phrases, enter text to add a trigger phrase for your topic.

5. Your copilot needs 5 to 10 trigger phrases to train the AI to understand your customers' responses. To add more trigger phrases, you can either:

  Select the "+" next to the text field.
  Paste a set of trigger phrases, each one on a separate line.
  Type a set of trigger phrases, pressing Shift+Enter after each one to place it on a separate line.
  Select Enter to complete adding the phrase(s).

6. Select Details to open the Topic details pane.

7. Add your copilot topic details:

Add a Name to identify the topic, such as **"Store hours"**. The Topics page lists all the topics defined in your copilot, by this name. A customer might see the topic name if the copilot can't determine which topic matches the customer's message.

The Description is never shown to users. Use it to describe the purpose of the topic for yourself and other copilot makers on your team.

Select **Save** at the top of the page to save your changes and add the topic to the topics list.

## Task 2 : Design a topic conversation path

When you create a topic, a Trigger node is inserted for you on the Topics & Plugins page. You can add more nodes to control the conversation.

1. Select a topic from the Topics & Plugins page of your copilot.

2. Select the "+" to add another node, which might be shown before or after any node. The locations you can add a node give you flexibility to edit any part of a conversation.

3. Select a node type to insert the node, Add a question node.

4. Select the "+" on any node, then select Ask a question. The Question node form appears.

5. In the Enter a message box, type the question you want to ask.

6. Select the menu under Identify, then either create or select an option. Your chosen entity determines what the copilot should listen for in the user's response.

7. Depending which Identify option you selected, you may have more properties you need to set.

For example, if you choose Multiple choice options, select + New option under Options for user to add choices the user can select. Each choice is presented as a multiple-choice button in a conversation, but users can also type their answers.

Select the variable name under Save response as and change the name of the default variable to something meaningful, like customerName or bookingDate. You can set the scope of the variable in the Variable properties pane as well.

## Task 3 : Configure question behavior

1. On the Question node, select the ... to see the the Node Menu, and then select Properties. The Question properties pane appears.

2. In the Question properties pane, select Question behavior to open the Question behavior pane.

## Task 4 : Edit topics with the code editor

1. On the Topics page, select + New topic.

2. In the upper-right corner of the authoring canvas, select the ... to see More options, then select Open code editor.

3. On the Topics page, select + New topic, In the upper-right corner of the authoring canvas, select the ... to see More options, then select Open code editor.

4.   ```
     
     kind: AdaptiveDialog
beginDialog:
  kind: OnRecognizedIntent
  id: main
  intent:
    displayName: Lesson 3 - A topic with a condition, variables and a prebuilt entity
    triggerQueries:
      - Buy items
      - Buy online
      - Buy product
      - Purchase item
      - Order product
      
  actions:
    - kind: SendMessage
      id: Sjghab
      message: I am happy to help you place your order.
      
   - kind: Question
      id: eRH3BJ
      alwaysPrompt: false
      variable: init:Topic.State
      prompt: To what state will you be shipping?
      entity: StatePrebuiltEntity
     
    - kind: ConditionGroup
      id: sEzulE
      conditions:
        - id: pbR5LO
          condition: =Topic.State = "California" || Topic.State = "Washington" || Topic.State     = "Oregon"

      elseActions:
        - kind: SendMessage
          id: X7BFUC
          message: There will be an additional shipping charge of $27.50.

        - kind: Question
          id: 6lyBi8
          alwaysPrompt: false
          variable: init:Topic.ShippingRateAccepted
          prompt: Is that acceptable?
          entity: BooleanPrebuiltEntity

        - kind: ConditionGroup
          id: 9BR57P
          conditions:
            - id: BW47C4
              condition: =Topic.ShippingRateAccepted = true

          elseActions:
            - kind: SendMessage
              id: LMwySU
              message: Thank you and please come again.          
   ```


5. Select Save, and then select Close code editor. The Question node now has many conditions to the question about shipping.

## Task 5 : Test your Microsoft Copilot Studio bot.

1. If the Test bot pane is hidden, open it by selecting Test your bot.

2. In the Type your message field, enter some text. If the text is similar to a trigger phrase for a topic, that topic will begin.

3. Select the bot response in the Test bot pane. This takes you to the topic and the node that sent the response. Nodes that have fired display a colored checkmark and a colored bottom border.

4. Continue the conversation, testing that the bot flows as intended in the topic.

5. Your conversation is not automatically cleared when you save a topic. If at any point you want to clear the conversation from your test bot and start over, select the Reset button.

## Track topic-to-topic.

1. At the top of the Test bot pane, set Track topic-to-topic to On.

2. Continue interacting with your bot. As you navigate to each node that fires, you can switch topics along with the conversation.

## Test variable values

1. Open the test bot.

2. Open the Variables pane and select the Test tab. If a variable has values, it appears here. Any empty variables appear as undefined.

3. To inspect variable properties, select the link in the value to display variable details.

## Save conversation snapshots

1. At the top of the Test bot pane, select the menu icon (⋮), then select Save snapshot.

2. Select Save to save the bot content and conversational diagnostics in a .zip archive file named botContent.zip.



