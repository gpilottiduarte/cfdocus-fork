## Metadata_Start 
## code: en
## title: Tenant audit 
## slug: cloud-security-tenant-audit 
## seoTitle: Tenant audit 
## description:  
## contentType: Markdown 
## Metadata_End
 provides an audit report to track all user actions within tenants. This report helps you monitor changes that occurred in a tenant.

## Tenant audit report

The audit report offers you the following information about actions performed on the tenants:

| Item | Description |
| --- | --- |
|  | The  column displays the name of the specific product where the action took place. |
|  | In the  column, you find the user responsible for the action. |
|  | The  column describes the specific action that the user performed. See the table of  below for more details on each type of event. |
|  | The  column specifies the type of entity that underwent a change. |
|  | The  column displays the name of the entity that was altered. |
|  | The  column provides the ID of the Entity that was altered. |
|  | The  column indicates the exact timestamp when the action occurred. |

:::(Info) (Info)
Users can change the entity’s name, but the entity ID remains always the same. This ensures that changes can be traced back to the original entity.
:::

To open detailed information about the changes made, click on the action row in the report. This will open a  file that displays the state before and after the modification.

## Tenant-level events

The table below displays the actions and events that can be listed in the audit report at the tenant level.

| Event | Description |
| --- | --- |
|  | A new account connected to the tenant has been created. |
|  | An account connected to the tenant has been updated. |
|  | Scan Entity has been acknowledged or unacknowledged. |
|  | Security policies have been globally updated for all accounts within the provider. |
|  | Security policies for an account have been updated. |
|  | The roles of a user connected to the tenant have been updated. |
|  | A new tenant has been created. |
|  | A new user has been invited to join the tenant. |
|  | A user connected to the tenant has been enabled. |
|  | A user connected to the tenant has been disabled. |
|  | An existing user has been associated with the tenant. |