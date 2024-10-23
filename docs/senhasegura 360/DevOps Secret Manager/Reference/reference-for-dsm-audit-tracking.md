## Metadata_Start 
## code: en
## title: Reference for DSM Audit Tracking 
## slug: reference-for-dsm-audit-tracking 
## seoTitle: Reference for DSM Audit Tracking 
## description:  
## contentType: Markdown 
## Metadata_End
You can consult the logs of DSM operations in the . Access it through the .

## Top bar

| Item                 | Description                                                                                 |
| -------------------- | ------------------------------------------------------------------------------------------- |
|     | Identified by the magnifying glass icon. Displays or hides the search fields on the screen. |
|           | Identified by the counterclockwise arrow icon. Refreshes the page.                          |
|     | Identified by the three vertical dots icon. Displays the possible actions for the page.     |
|     | Identified by the printer icon. It opens a new page for printing the report.                |
|       | Identified by the sheet of paper icon, downloads the report.                                |
|  | Identified by the clock icon, it opens the window for scheduling the report.                |

When you click , a range of fields is displayed. These are used to refine your search results. They are:

| Field                      | Description                                                                                              |
| -------------------------- | -------------------------------------------------------------------------------------------------------- |
|                | Operation code on senhasegura. For example: .                                     |
|         | Operation type. For example,Application created.                                                         |
|            | Entity that was changed in the operation. For example,Secret.                                            |
|         | Entity's code in senhasegura.                                                                            |
|       | Entity's name.                                                                                           |
|            | Origin, within the DSM, of the operation. For examp: .                                    |
|              | User that performed the operation.                                                                       |
|          | Username of the user who performed the operation.                                                        |
|  | Opens a calendar for choosing the start date of the filter for the period of execution of the operation. |
|             | Opens a calendar for choosing the end date of the filter by the period of execution of the operation.    |

In addition to these options, you have two buttons: , which applies the parameters passed into the fields, and , which clears all the parameters.

The report is shown below, in list format, containing the following fields:

* 
* 
* 
* 
* 
* 
* 
* 
* : IP address of the user who performed the execution.
* : change that was made in the execution.
* : date and time of execution, displayed in the  format.

## Audit tracking window

In the  column, by clicking on , represented by the magnifying glass icon, you can view the details of that operation.

In the  window, you'll see the following information:

| Field                 | Description                                                                                                      |
| --------------------- | ---------------------------------------------------------------------------------------------------------------- |
|           | Operation code on senhasegura. For example: .                                             |
|       | Origin, within the DSM, of the operation. For example:.                                      |
|    | Operation type. For example:.                                                       |
|           | The IP address of the user who performed the execution.                                                          |
|    | Date and time of execution. This will be displayed in the  format.                           |
|         | The user who performed the operation. The user's name will be displayed, followed by their username in brackets. |
|    | Entity's code in senhasegura.                                                                                    |
|       | Entity that was changed in the operation. For example:.                                          |
|  | Entity's name. For example: .                                                                            |

The changes will be shown according to the changes made. You will then have the fields as shown here.

In the first table, you can see what has been modified. For example,  followed by cells indicating the  of what has been modified.

| Field         | Description |
| ------------ | -------------------------------------------------------------------------- |
|          | Shows how the field looked before the modification. For example: . |
|  | Shows how the field looks after modification. For example: .         |

For fields modified through an operation, a table will be added following this model, making it easier to see what has been modified and how.