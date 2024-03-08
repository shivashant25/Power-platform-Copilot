# Lab-05: Share a cloud flow.

# Task-01 : Create A cloud Flow

1.	Sign into Power Automate.
2.	On the menu to the left, select Solutions.
3.	Select the solution in which you'll create your flow.
4.	Select New > Automation > Cloud flow > Automated.

>**Note**: If an automated cloud flow doesn't meet your requirements, you can create any other type of flow, Power Automate opens.

5.	Use the available connectors and triggers to build your flow. we'll build a flow that sends a notification when an email arrives in your inbox.
6.	Give your flow a name as **my child flow**.
7.	Search for, new email in the Search all triggers box.
8.	Select the When a new email arrives (V3) trigger.
9.	Sign in to the outlook.
10.	Select Create.
11.	Select New step.
12.	Search for Notification, and then select the Send me a mobile notification action.

13.	Add the Subject dynamic token to the Text field of the Send me a mobile notification card.
14.	Select Save to save your flow.
Your flow should look like the following screenshot.

15.	Select Solutions to see your flow in the solution.

## Task-02: Add an owner to a cloud flow.

1. Adding an owner to a cloud flow is the most common way to share a cloud flow. Any owner of a cloud flow can perform these actions:
   
2.	View the run history.
   
3.	Manage the properties of the flow (for example, start or stop the flow, add owners, or update credentials for a connection).
   
4.	Edit the definition of the flow (for example, add or remove an action or condition).
   
6.	Add or remove other owners (but not the flow's creator), including guest users.
   
7.	Delete the flow.

> Note: The creator or an owner of a cloud flow, you'll find it listed on the Team flows tab in Power Automate, Shared connections can be used only in the flow in which they were created.Owners can use services in a cloud flow but can't modify the credentials for a connection that another owner created.To add more owners to a cloud flow:

8.	Sign in to **https://make.powerautomate.com/**, and then select My flows.
   
9.	Select the flow that you want to share, select the vertical ellipsis (⋮), and then select Share.
    
10.	Enter the name, email address, or group name for the person or group that you want to add as an owner.
    
11. The user or group you've selected becomes an owner of the flow.

Congratulations—you've created your team flow!

## Task-02: Add a list as a co-owner

You can add SharePoint lists as co-owners of a cloud flow so that everyone who has edit access to the list automatically gets edit access to the flow. After the flow is shared, you can simply distribute a link to it. 

1. Create and set up a SharePoint list.
   
2. Use a list when the flow is connected to SharePoint, and use a group in all other cases.
   
>**Note**: SharePoint users must have Edit permission or be a member of the Members or Owners group to run flows in SharePoint, Adding a list as a co-owner is not available in GCC High and DoD tenants, Remove an owner.When you remove an owner whose credentials are used to access Power Automate services, you should update the credentials for those connections so that the flow will continue to run properly.  go to Modify a connection.

3.	On the flow details page, in the Owners section, select Edit.
   
4.	Select Delete (the trash can) for the owner you want to remove.
   
5.	In the confirmation dialog box, select Remove.
   
Congratulations—the user or group that you removed is no longer listed as an owner of the flow.

## Task-03: Modify a connection

You might need to change the owner of a connection in a cloud flow if you remove the existing owner or if you just want to use a different account to sign in to an action or trigger.

1.	Go to the **flow** that you Had created previously.
   
2.	Select **Edit**.
	
3.	Select the ellipsis in the step where you want to edit the connection.
   
4.	If you have a connection already, select it; if not, select Add new connection to create a new connection, and then select Sign in to create your new connection.
Share a cloud flow with run-only permissions.

5. Instant flows (that is, flows that use a manual trigger such as a button or an item being selected) can be shared by using run-only permissions. Any user who's added as a run-only user won't have access to edit or modify the flow in any way; they'll only have permissions to trigger the flow.To add a run-only user:
   
6.	On the flow details page, in the Run only users section, select Edit.
   
7.	In the Manage run-only permissions panel, specify the users and groups you want to provide run-only access to.
   
8.	As an owner, you can specify whether run-only users will need to provide their own connections or you can choose use a connection that's already defined in the flow.
 
**Congratulations—the user or group now has access to run the flow.!!**

## Task-04: **Send a copy of a cloud flow**

>**Note**: You can send a copy of a cloud flow to another user, who can then use the definition of the flow as a template. It provides a good way for you to share the general structure of a cloud flow without sharing any connections, while also allowing the recipient to modify their flow independently of yours, so they can make it fit their needs.
Sending a copy creates an independent instance of the flow for the recipient. You can't revoke access to the flow after you share it.

1.	On the flow details page command bar, select Send a copy.
   
2.	On the Send a copy panel, you can edit the name and description of the flow you want to share, and specify the users with whom you want to share it.
 
3.	The recipient will receive an email stating that you have shared a cloud flow template with them, and they can then create their own instance of that flow.
