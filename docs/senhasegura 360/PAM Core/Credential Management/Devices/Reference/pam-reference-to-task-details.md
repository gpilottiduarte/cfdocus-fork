## Metadata_Start 
## code: en
## title: Reference for task details 
## slug: pam-reference-to-task-details 
## seoTitle: Reference to task details 
## description:  
## contentType: Markdown 
## Metadata_End
Whenever necessary, you can access the details of each request for batch operations awaiting your approval. To access the task details screen for requests, access .

## Request details

In the list of requests, in the  column, you can view the details of that request by clicking on , identified by the ID card icon.

| Field                    | Description                                                               |
| ------------------------ | ------------------------------------------------------------------------- |
|       | Name of the user who made the request.                                    |
|  | Operation status. It can be*Pending*, *Approved*, or *Disapproved*. |
|              | Identification number of the request to be approved.                      |
|    | Date and time the request was made.                                       |
|      | The expiration date for the request.                                      |
|       | Number of approvals of the request.                                       |
|    | Number of disapprovals of the request.                                    |

## Responses

| Field                   | Description                                                                           |
| ----------------------- | ------------------------------------------------------------------------------------- |
|       | Name and username of the approver user of the request.                                |
|          | Access level of the approver user.                                                    |
|       | Response to the request. It can be*Not answered*, *Approved*, or *Disapproved*. |
|           | Date of reply. If there is no response, this field will be blank.                     |
|  | Justification for the action. If there is no justification, this field will be blank. |

## Request details tab

### Information

| Field             | Description                                                                                                                                                                            |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|       | Application registration code on senhasegura.                                                                                                                                          |
|   | What action was requested.                                                                                                                                                             |
|   | Current status of the request. If the request has already expired, the last status of the request will be shown.It can be *Pending Approved*, *Expired*, or *Disapproved*. |
|  | Displays which changes have been requested.                                                                                                                                            |

### Affected entities section

Since bulk operations can be performed on various senhasegura artifacts, it's worth noting that you can have different ways of presenting the information.

For example, when secrets come from a bulk operation in the , there will be no Affected Entities section. Therefore, the fields for Credentials and Devices are shown below.

#### Affected entities - Devices

| Field                 | Description                                        |
| --------------------- | -------------------------------------------------- |
|           | Code of the affected entity. In case, the device. |
|  | Name of the affected device.                       |
|   | IP address or hostname of the device.              |
|         | Type of device.                                    |
|       | Manufacturer of the affected device                |
|      | Model of the affected device.                      |

#### Affected entities - Credentials

| Field              | Description                                           |
| ------------------ | ----------------------------------------------------- |
|        | Code of the affected entity. In case, the credential. |
|  | User name of the affected credential.                 |
|      | Type of credential.                                   |
|    | Domain of the credential                              |
|    | Device to which the credential is linked.             |

:::(Info) (Info)
For more information on a device's registration fields, access the Reference documentation for devices.
:::