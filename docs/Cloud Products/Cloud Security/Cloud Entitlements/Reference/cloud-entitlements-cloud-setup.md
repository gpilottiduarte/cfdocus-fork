## Metadata_Start 
## code: en
## title: Setup 
## slug: cloud-entitlements-cloud-setup 
## seoTitle: Setup 
## description:  
## contentType: Markdown 
## Metadata_End
In , you can connect your Cloud Service Providers (CSPs) and obtain information about them.

## Path to access

To set up CSPs for a tenant:

1. Access .  
2. On the  product, click .  
3. On the left menu, click , and select the desired provider.

## Amazon Web Services

On the left-side menu click  >  to consult the following information:

| Item | Description |
| :---- | :---- |
|  | Displays the type of account connected to . You can connect either an AWS account or an AWS organization. |
|  | Displays the ID of the AWS account or, for AWS organizations, the Organizational unit’s (OU) management account ID. |
|  | Informs the name of the account or organization within . |
|  | Displays the AWS account access key. This field is only available for  administrators. A warning will be displayed for the corresponding account if the access key is no longer valid.  connected organizations don’t display an access key. |
|  | Indicates the date and time when the account or organization was connected to . |
|  | Indicates the synchronization status of the account or organization with . Synchronization begins automatically every 15 minutes after completion or after a reprocess is initiated. |
|  | Switch to activate or deactivate the account or organization within . : deactivating the account or organization will remove the account's identities and recommendations from the report. |

In the  column, represented by the three vertical dots, you have three options:

- : edits the information of the AWS account or organization.  
- : redirects to the security policy screen of the selected account or organization.  
- : reprocesses the account or organization, synchronizing the data with the CSP.

## Google Cloud Platform

On the left-side menu, click  >  to consult the following information:

| Item | Description |
| :---- | :---- |
|  | Displays the type of account connected to . You can connect either a GCP project or a GCP organization. |
|  | Displays the ID of the GCP project or GCP organization. |
|  | Informs the name of the account or organization within . |
|  | Indicates the date and time when the account or organization was connected to . |
|  | Indicates the synchronization status of the account or organization with . Synchronization begins automatically every 15 minutes after completion or after a reprocess is initiated. |
|  | Switch to activate or deactivate the account or organization within . : deactivating the account or organization will remove the account's identities and recommendations from the report. |

In the  column, represented by the three vertical dots, you have three options:

- : edits the GCP project or organization’s information.  
- : redirects to the security policy screen of the selected project or organization.  
- : reprocesses the project or organization, synchronizing the data with the CSP.

## Microsoft Azure

On the left-side menu, click  >  to consult the following information:

| Item | Description |
| :---- | :---- |
|  | Displays the ID of the tenant. |
|  | Informs the name of the tenant within . |
|  | Indicates the date and time when the tenant was connected to . |
|  | Indicates the synchronization status of the tenant with . Synchronization begins automatically every 15 minutes after completion or after a reprocess is initiated. |
|  | Switch to activate or deactivate the tenant within . : deactivating the account or organization will remove the account's identities and recommendations from the report. |

In the  column, represented by the three vertical dots, you have three options:

- : edits the Azure tenant’s information.  
- : redirects to the security policy screen of the selected tenant.  
- : reprocesses the tenant, synchronizing the data with the CSP.

:::(Warning) (Attention)
If an invalid access key is used to connect providers to the tenant in , the user responsible for the connection will receive an email notification. Additionally, an alert will be displayed in the list. Accounts with an invalid access key won’t have their data updated in .
:::

## Oracle Cloud (OCI)

On the left-side menu, click  >  to consult the following information:

| Item | Description |
| :---- | :---- |
|  | Displays the type of account connected to . You can connect with an Oracle Cloud compartment. |
|  | Displays the ID of the Oracle Cloud compartment. |
|  | Informs the name of the compartment within . |
|  | Indicates the date and time when the compartment was connected to . |
|  | This indicates the compartment's synchronization status with . Synchronization starts automatically every 15 minutes, either after a process completes or after a reprocess starts. |
|  | Switch to activate or deactivate the compartment within . : deactivating the account or organization will remove the account's identities and recommendations from the report. |

In the  column, represented by the three vertical dots, you have three options:

- : edits the information of the OCI compartment.  
- : redirects to the security policy screen of the selected compartment.  
- : reprocesses the compartment, synchronizing the data with the CSP.
