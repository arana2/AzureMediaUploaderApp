# AzureMediaUploaderApp
This web application using the Azure infrastructure to securely upload media to a blob container.

Project Workflow Image goes here

Detailed Description

Azure Services Used:

Azure Entra ID:

Stores the created user.
Assigns the user to a designated group.
Azure Logic Apps:

Automates the process of collecting new employee information, creating the new user, assigning the user to a group, and sending a welcome email to the new employee. Azure Email Service (part of Logic Apps connector):
Responsible for sending a welcome email to the user.
Azure Resource Groups

Azure Virtual Machines:

The user created and assigned to the Information Technology group will have access to (1) Azure Windows 11 Pro virtual machine and (1) Linux Ubuntu Server virtual machine.
Virtual Machine Administrator Login Role assignments are assigned to the Information Technology Group at the VM Level.

Steps

Conclusion This project was enjoyable and provided a learning experience in Azure's Manage Identities and Compliance domain. It did not involve any coding apart from understanding the JSON format.

Reference: https://github.com/madebygps/projects/blob/main/az-104/onboarder.md
