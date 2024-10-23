## Metadata_Start 
## code: en
## title: Reference for DSM automations 
## slug: reference-devops-secret-manager-automations 
## seoTitle: Reference for DSM automations 
## description:  
## contentType: Markdown 
## Metadata_End
The automations within the senhasegura DevOps Secret Manager are accessible through the 

On the screen, you'll find the following information:

| Item                   | Description                                                                                                                                     |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
|  | Represented by the magnifying glass button, it hides or shows the filter options.                                                               |
|        | Represented by the counterclockwise arrow, it updates the information on the screen.                                                            |
|  | Represented by the three vertical dots, it opens a drop-down menu with four options:*+New, Print report, Export CSV,* and *Schedule report.* |

When you click , a series of fields are displayed. These are used to refine your search results. They are:

| Item                    | Description                                                                                                                |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------- |
|             | Application code in senhasegura.                                                                                           |
|           | Application name.                                                                                                          |
|           | Tags registered in senhasegura for that application.                                                                       |
|    | Applications for which automation is intended.                                                                             |
|         | Secret registered at senhasegura.                                                                                          |
|            | Tags registered in the automation.                                                                                         |
|  | It opens a calendar to choose the time interval for the automation search. Start with the date the automation was created. |
|          | It opens a calendar for you to choose the end date of the automation registration interval.                                |
|        | Drop-down menu to filter according to automation status. It can be  or .                                    |

In addition to these options, you have two buttons:

* : applies the parameters that have been passed into the fields.
* : clears all the parameters.

The report is shown below, in list format, containing the following fields:

* 
* 
* 
* 
* 
* 
*  displays the date and time in the format  of the last automation execution.
* .

## Automation update window

In the  column, by clicking on the icon represented by the three vertical dots, you can update or delete the automation. The Update option opens the  window.

### Information tab

| Item                  | Description                                                                         |
| --------------------- | ----------------------------------------------------------------------------------- |
|         | Name of the automation.                                                             |
|      | A checkbox that can be  or . Indicates the status of the automation. |
|  | Description of automation.                                                          |
|         | Automation tags. Type in the tags and separate them with a comma.                   |

### Trigger tab

| Item               | Descrição                                                                                                                                       |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------- |
|      | Opens the  modal. This is used to add triggers to the automation. For example, when this event occurs, the execution will be carried out. |
|  | Opens the  modal. This informs which applications will be affected when the trigger is started.                                       |
|       | Opens the  modal. This informs which secrets will be affected when the trigger is started.                                                 |

You can click the sum sign next to each word. This will open the corresponding modal. Each modal has different search fields, as shown below.

### Triggers

| Item      | Description                           |
| --------- | ------------------------------------- |
|  | Filter according to the trigger name. |

### Application

| Item             | Description                     |
| ---------------- | ------------------------------- |
|         | Name of the application.        |
|       | System of the application.      |
|  | Environment of the application. |

### Secrets

| Item          | Description             |
| ------------- | ----------------------- |
|      | Name of the secret.     |
|  | Identity of the secret. |
|    | Engine of the secret.   |

In addition to these options, all the modals have two buttons: , which applies the parameters passed into the fields, and , which clears all the parameters.

Below, we have the list field, which contains all the secrets, filtered or not, which are presented with the following fields:

* : by clicking on the ticked checkbox, you'll select all the fields listed.
*  clicking on the unticked checkbox will delete the current selection, whatever it may be.

On the left, you'll see a checkbox. By ticking this checkbox, you select this item.

At the end of each modal, you have two buttons:

* : add the selected triggers, applications, or secrets.
* : cancel the operation.

### Action tab

In the  section:

| Item                   | Description                                                                  |
| ---------------------- | ---------------------------------------------------------------------------- |
|             | Drop-down menu showing the plugins available in senhasegura.                 |
|  | A drop-down menu shows the activation templates registered with senhasegura. |

In the  section:

| Item                 | Description                                                                                                                                                                                                    |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|     | By clicking the sum sign, you add two new drop-down menus below the word .                                                                                                                    |
|      | A drop-down menu is added when you click the plus sign next to the word . Displays a list of the devices available in senhasegura.                                                              |
|  | A drop-down menu is added when you click the sum sign next to the word . This displays a list of the credentials available for connection according to the device chosen in the previous field. |

## Automation visualization window

In the  column, by clicking the  option, represented by the magnifying glass icon, you can view the automation details. This action will open the automation preview window.

| Item                     | Description                                  |
| ------------------------ | -------------------------------------------- |
|                   | Automation ID.                               |
|                 | Automation name.                             |
|        | Creation date of the automation.             |
|       | Last execution of the automation date.       |
|              | Automation status.                           |
|          | Automation description.                      |
|                 | Tags related to automation.                  |
|             | Triggers linked to automation.               |
|         | Applications linked to automation.           |
|              | Secrets linked to automation.                |
|               | Plugin used to execute the automation.       |
|             | Template used to execute the automation.     |
|  | Device and credential related to automation. |