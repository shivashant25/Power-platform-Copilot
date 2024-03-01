# Lab-05: Share a cloud flow.

## Task-01: Add an owner to a cloud flow
Adding an owner to a cloud flow is the most common way to share a cloud flow. Any owner of a cloud flow can perform these actions:
•	View the run history.
•	Manage the properties of the flow (for example, start or stop the flow, add owners, or update credentials for a connection).
•	Edit the definition of the flow (for example, add or remove an action or condition).
•	Add or remove other owners (but not the flow's creator), including guest users.
•	Delete the flow.
If you're the creator or an owner of a cloud flow, you'll find it listed on the Team flows tab in Power Automate.
 Note
Shared connections can be used only in the flow in which they were created.
Owners can use services in a cloud flow but can't modify the credentials for a connection that another owner created.
To add more owners to a cloud flow:
1.	Sign in to Power Automate, and then select My flows.
2.	Select the flow that you want to share, select the vertical ellipsis (⋮), and then select Share.
3.	Enter the name, email address, or group name for the person or group that you want to add as an owner.
The user or group you've selected becomes an owner of the flow.
Congratulations—you've created your team flow!
## Task-02: Add a list as a co-owner
You can add SharePoint lists as co-owners of a cloud flow so that everyone who has edit access to the list automatically gets edit access to the flow. After the flow is shared, you can simply distribute a link to it. More information: Training: Create and set up a SharePoint list
Use a list when the flow is connected to SharePoint, and use a group in all other cases.
 Important
•	SharePoint users must have Edit permission or be a member of the Members or Owners group to run flows in SharePoint.
•	Adding a list as a co-owner is not available in GCC High and DoD tenants.
Remove an owner
When you remove an owner whose credentials are used to access Power Automate services, you should update the credentials for those connections so that the flow will continue to run properly. To learn more, go to Modify a connection.
1.	On the flow details page, in the Owners section, select Edit.
2.	Select Delete (the trash can) for the owner you want to remove.
3.	In the confirmation dialog box, select Remove.
Congratulations—the user or group that you removed is no longer listed as an owner of the flow.
## Task-03: Modify a connection
You might need to change the owner of a connection in a cloud flow if you remove the existing owner or if you just want to use a different account to sign in to an action or trigger.
1.	Go to the flow that you want to modify.
2.	Select Edit.
3.	Select the ellipsis (...) in the step where you want to edit the connection.
4.	If you have a connection already, select it; if not, select Add new connection to create a new connection, and then select Sign in to create your new connection.
Share a cloud flow with run-only permissions
Instant flows (that is, flows that use a manual trigger such as a button or an item being selected) can be shared by using run-only permissions. Any user who's added as a run-only user won't have access to edit or modify the flow in any way; they'll only have permissions to trigger the flow.
To add a run-only user:
1.	On the flow details page, in the Run only users section, select Edit.
2.	In the Manage run-only permissions panel, specify the users and groups you want to provide run-only access to.
3.	As an owner, you can specify whether run-only users will need to provide their own connections or you can choose use a connection that's already defined in the flow.
 
Congratulations—the user or group now has access to run the flow.
## Task-04: To remove a run-only user:
1.	On the flow details page, in the Run only users section, select Edit.
2.	In the Manage run-only permissions panel, select Delete (the trash can) next to the user whose access you want to remove, and then select Save.
Congratulations—the user or group no longer has access to run this flow.
Send a copy of a cloud flow
You can send a copy of a cloud flow to another user, who can then use the definition of the flow as a template. It provides a good way for you to share the general structure of a cloud flow without sharing any connections, while also allowing the recipient to modify their flow independently of yours, so they can make it fit their needs.
>Note : Sending a copy creates an independent instance of the flow for the recipient. You can't revoke access to the flow after you share it.
To send a copy of a cloud flow
1.	On the flow details page command bar, select Send a copy.
2.	On the Send a copy panel, you can edit the name and description of the flow you want to share, and specify the users with whom you want to share it.
 
3.	The recipient will receive an email stating that you have shared a cloud flow template with them, and they can then create their own instance of that flow.
