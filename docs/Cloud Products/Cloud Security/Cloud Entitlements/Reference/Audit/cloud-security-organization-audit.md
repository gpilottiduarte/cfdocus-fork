## Metadata_Start 
## code: en
## title: Organization audit 
## slug: cloud-security-organization-audit 
## seoTitle: Organization audit 
## description:  
## contentType: Markdown 
## Metadata_End
 provides an audit report to track all user actions within your organization. This report helps you monitor changes made at an organization level.

## Organization audit report

The organization audit report offers you the following information about actions performed:

| Item | Description |
| --- | --- |
|  | The  column displays the name of the specific product where the action occurred. |
|  | In the  column, you find the user responsible for the action. |
|  | The  column describes the specific action that the user performed. See the table of  below for more details on each type of event. |
|  | The  column specifies the type of entity that underwent a change. |
|  | The  column displays the name of the entity that was altered. |
|  | The  column provides the ID of the Entity that was altered. |
|  | The  column indicates the exact timestamp when the action occurred. |

:::(Info) (Info)
Users can change the entity’s name, but the entity ID will always remain the same. This ensures that changes can be traced back to the original entity.
:::

To open detailed information about the changes made, click on the action row in the report. This will open a  file that displays the state before and after the modification.

## Organization-level events

The table below displays the actions and events that can appear in the audit report at the organization level.

| Event | Description |
| --- | --- |
|  | A new organization has been created. |
|  | The user assigned to an organization as administrator has been removed from the organization. |
|  | A tenant has been created for the organization. |