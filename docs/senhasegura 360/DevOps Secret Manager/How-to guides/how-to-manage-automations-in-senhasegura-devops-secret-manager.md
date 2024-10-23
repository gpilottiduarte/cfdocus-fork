## Metadata_Start 
## code: en
## title: How to manage DSM automations 
## slug: how-to-manage-automations-in-senhasegura-devops-secret-manager 
## seoTitle: How to manage DSM automations 
## description:  
## contentType: Markdown 
## Metadata_End
Within senhasegura , you can register automations to simplify everyday actions.

## Requirements

* A previously created application or secret.
* A credential that will be used to perform the automation action.
* A device on which the automation will be executed.
* An execution template of the  type for the desired executor.

## How to register automation in DSM

To create an automation, follow these steps:

1. In senhasegura, in the top left corner, click the , represented by the nine squares, and select 
2. In the side menu, select .
3. In the top bar, click on , represented by the three vertical dots, and select  from the drop-down menu.

### Automation window

In this window, you'll fill in your automation data. The fields present are:

1. : name that identifies the automation within the senhasegura instance.
2. : option to choose whether the automation will be registered as active. The options are  or . By default, this option is set to .

#### Information tab

1. : fill in a description of the automation.
2. : add the tags that will identify the automation.

#### Trigger tab

In  section, you'll define the trigger that will start the automation. To do this, fill in the following fields:

1. Click the sum icon next to the word  to open the  modal.
2. In the  modal, select the triggers (actions) that will be used to start the automation. You can choose as many as you like.
3. Click .

In  section, you'll define which applications or secrets will be affected by the trigger. To do this, fill in the following fields:

1. :

   1. Click the sum icon next to the word  to open the  modal.
   2. In the  modal, select the applications affected when the trigger is started. You can choose as many as you like.
   3. Click .
2. :

   1. Click the sum icon next to the word  to open the  modal.
   2. In the  modal, select the secrets that will be affected when the trigger is started. You can choose as many as you like.
   3. Click .

#### Action tab

In  section, you'll define the template containing the commands executed in the application(s) or secret(s) when the trigger is activated. To do this, fill in the following fields:

1. From the  drop-down menu, select one of the plugins that are registered with senhasegura.
2. From the  drop-down menu, select one of the templates for that plugin.
   1. When creating automation, you can include an activation template by clicking the sum icon next to the  drop-down menu. This will open the  window where you can fill in the necessary details.

::: (error) (Important)
When a template is created using the on-the-fly creation option, this template doesn't automatically appear in the drop-down menu list. You'll need to re-enter all the information by reloading the page or manually adding a new automation.
:::

In  section, you'll add the devices on which the template will run. To do this, fill in the following fields:

1. Click the sum icon next to the word . This adds two drop-down menus just below the icon.
2. From the  drop-down menu, select one of the devices registered with senhasegura.
3. From the  drop-down menu, select the credential used for authentication on the indicated device.

At the end, click  to finish registering the automation.

## How to update an automation in DSM

To update automation, follow these steps:

1. In senhasegura, in the top left corner, click the , represented by the nine squares, and select .
2. In the side menu, select .
3. In the list that appears on the main page, select the automation you want to update and, in the  column, click the icon represented by the three vertical dots to open a drop-down menu.
4. From the drop-down menu, select .
5. The  window will open in edit mode, containing the same fields as the registration step.
6. Change what you want and click .

::: (info) (Info)
You'll find an eye icon in the bottom right corner of the  window. You can access information about the automation by hovering your mouse over it. This information includes the name and username of the person who created the automation and the name and username of the last person who made changes to it.
:::

## How to view the details of automation in DSM

In the  window, when opened in detail view, you can analyze various information about the automation. To do this, follow the steps below:

1. In senhasegura, in the top left corner, click the , represented by the nine squares, and select .
2. In the side menu, select .
3. In the list on the main page, select the automation you want to view the details of and, in the  column, click on , represented by the magnifying glass icon.
4. In the  window, you'll have the following fields:
   1. : contains the code of the automation.
   2. : contains the name of the automation.
   3. : the date when the automation was created.
   4.  the date when the automation was last run.
   5. : indicates the current status of the automation.
   6. : a brief description of the automation.
   7. : the tags that help categorize the automation.
   8. : the actions that will activate the templates.
   9. : the applications that will be affected by the template.
   10. : the secrets that will be affected by the template.
   11. : the plugin that is used in automation.
   12. : the name of the template that will perform the action when the trigger is activated.
   13. : contains the address of the device and the credential that will be used for authentication.

## How to delete an automation in DSM

To delete an automation, follow the steps below:

1. In senhasegura, in the top left corner, click the , represented by the nine squares, and select 
2. In the side menu, select .
3. In the list on the main page, identify the automation you want to delete and, in the  column, click the icon represented by the three dots and, in the drop-down menu, select .
4. A window will display a message that the deletion of that automation was successful.

:::(warning) (Warning)
Deleting an automation has no intermediate steps, so when you click Delete, the automation will be deleted without confirming the deletion.
:::

## How to activate automation in DSM

To activate automation, which for whatever reason has a status of  in the  field, follow these steps:

1. In senhasegura, in the top left corner, click the , represented by the nine squares, and select 
2. In the side menu, select .
3. On the list page, in the top bar, select the  option from the  drop-down menu and click .
4. In the list, identify the automation you want to activate, click, in the  column, the icon represented by the three vertical dots, and select  from the drop-down menu.
5. The  window will open in edit mode.
6. In the  field, check .
7. Click .

---

Do you still have questions? Reach out to the .