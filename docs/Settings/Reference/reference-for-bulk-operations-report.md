## Metadata_Start 
## code: en
## title: Bulk operations report 
## slug: reference-for-bulk-operations-report 
## seoTitle: Bulk operations report 
## description:  
## contentType: Markdown 
## Metadata_End
For a bulk operation to be carried out, an approving user must authorize it. To view pending requests, access . The fields below refer to the request search report.

## Bulk operations

| Field              | Description                                                                                                                                                                           |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|             | Request ID number.                                                                                                                                                                    |
|         | Drop-down menu that filters according to the operation requested.                                                                                                                     |
|         | Drop-down menu that filters by the current status of the request. It can be:*Pending approval, Pending approval, Pending execution, Running, Success, Error,* and *Canceled.* |
|  | Displays a calendar that lets you choose the request creation date.                                                                                                                   |
|          | Displays a calendar that lets you choose the deadline for searching requests.                                                                                                         |

To perform the search, click on the  button; to clear the fields and restart the process, click on the  button.

The bulk operations list will appear below the filter form, with the following fields:

* .
* .
* .
* : indicates the number of tasks closed in that operation.
* : indicates the total number of tasks in that operation.
*  date the operation was created.
*  column:
  * , identified by the identity card icon.
  * , identified by the three horizontal bars icon.

## Request details window

When you click on  in the  column, a window will open. In this window, we will see the following fields:

| Field             | Description                                                                                                                                                                                                                                              |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|     | It shows the name and user name of the requester for that operation.Next to this field is the type of operation, in this case,Bulk operation. Then you have the status of the operation, which can be *Pending,Approved,* or *Rejected.* |
|            | Request ID on senhasegura.                                                                                                                                                                                                                               |
|  | Date and time the request was made. Presented in the  format.                                                                                                                                                                     |
|    | It indicates the expiration date of the request. Presented in the  format.                                                                                                                                                        |
|     | It indicates the number of approvals that the request has received.                                                                                                                                                                                      |
|  | It indicates the number of disapprovals that the request has received.                                                                                                                                                                                   |

### Responses session

In the same window, just below the request details, you have the  section, which shows the details of the responses given to the request.

| Field         | Description                                                                                                                                                                           |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Approver      | Name of the user who approved or disapproved the request.This field can also display the text " |
| Level         | Approver user level.                                                                                                                                                                  |
| Response      | It indicates whether the user in question has already provided an answer.                                                                                                             |
| Date          | Response date. Presented in the  format.                                                                                                                       |
| Justification | Text field with the approving user's written justification. If no justification has been provided, the field will be blank.                                                           |

### Request details session

Below, you'll find 

| Field             | Description                                              |
| ----------------- | -------------------------------------------------------- |
|       | Code of the request in senhasegura.                      |
|   | Action that was indicated in the bulk operation request. |
|   | Updated status of the request.                           |
|  | The status of the request. Can be  or .   |

:::(warning) (Caution)
Below these fields, you'll have a session that is variable. So, the fields below will vary according to the module in which the request was made, with a different type of detail for bulk operations for credentials, devices or DSM.
:::

#### Affected entities - Devices

When analyzing a bulk operation on devices, these fields will appear. Note, however, that only in this case will you be able to see these fields.

| Field            | Description                                                  |
| ---------------- | ------------------------------------------------------------ |
|           | Code of the entity added by the bulk operation request.      |
|  | Name of the device affected by the bulk operation request.   |
|   | IP address or hostname of the device.                        |
|         | Type of device affected by the bulk operation request.       |
|       | Vendor of the affected device by the bulk operation request. |
|      | Model of the device affected by the bulk operation request.  |

#### Justification

When analyzing a bulk operation in DSM secrets, these fields will appear. Note, however, that only in this case will you be able to see these fields.

| Field              | Description                                 |
| ------------------ | ------------------------------------------- |
|  | Governance code for the bulk operation.     |
|         | Reason for carrying out the bulk operation. |

#### Affected entities - Credentials

When analyzing a bulk operation in credentials, these fields will appear. Note, however, that only in this case will you be able to see these fields.

| Field         | Description                                                      |
| ------------- | ---------------------------------------------------------------- |
|        | Code of the credential affected by the bulk operation.           |
|  | Username of the credential affected by the bulk operation.       |
|      | Type of credential affected by the bulk operation.               |
|    | Domain of the credential affected by the bulk operation.         |
|    | Device linked to the credential involved in the batch operation. |

## Bulk operation task window

When you click the  button in the  column, a window will open. In this window, you can filter the tasks for each bulk operation. The fields below refer to the search report for the tasks in the bulk operation.

| Field           | Description                                                                                                                                                                    |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|          | Task's code registered in senhasegura.                                                                                                                                         |
|   | Entity's code registered in senhasegura.                                                                                                                                       |
|      | Drop-down menu to filter according to approval status.                                                                                                                         |
|    | Drop-down menu to filter according to task priority.                                                                                                                           |
|  | Opens a calendar for entering the start date of the bulk operation's execution interval. This date indicates the start of the interval.                                  |
|       | Opens a calendar for entering the start date of the bulk operation's execution interval. This date indicates the end of the interval.                                    |
|    | Opens a calendar for entering the start date of the batch operation execution interval. This date indicates the start of the end interval for bulk operation executions. |
|       | Opens a calendar for entering the start date of the batch operation execution interval. This date indicates the end of the end interval for bulk operation executions.   |

To perform the search, click on the  button; to clear the fields and restart the process, click on the  button.

The list of tasks in the bulk operation will appear below the filter form, with the following fields:

* .
* .
* 
* .
* 
* 
* 
*  column:
  * : it opens the Bulk operation task window.

### Bulk operation task

By clicking on the  button in the  column, you're redirected to the Bulk operation task window. This window contains the following fields:

| Field            | Description                                                                |
| ---------------- | -------------------------------------------------------------------------- |
|           | Task's code, as registered in senhasegura.                                 |
|       | Descriptive name of the action to be performed in the task.                |
|       | Current status of the task.                                                |
|    | Entity code, as registered in senhasegura.                                 |
|  | Name of the entity, as registered in senhasegura.                          |
|   | Start date of the bulk operation execution interval.                       |
|     | End date of the bulk operation execution interval.                         |
|     | Text fields to show the messages related to the task.                      |
|         | Field highlighted in red. It indicates the value before the task request.  |
|           | Field highlighted in green. It indicates the value after the task request. |