## Metadata_Start 
## code: en
## title: Attack path 
## slug: cloud-entitlements-attack-path 
## seoTitle: Attack path 
## description:  
## contentType: Markdown 
## Metadata_End
In this document, you’ll find all the information about ’s  page. This page shows which actions or permissions can be used to trigger an attack, escalate privileges, or exploit a vulnerability within your connected AWS accounts. You can access a detailed map on how each policy is attached to a user or group to mitigate the vulnerability accordingly.

## Path to access

1. Access .
2. On the home page, click  in the  block.
3. Click  on the left menu.

---

## Attack paths list

|  |  |
| --- | --- |
|  | Contains the name of the policies identified as vulnerable to attacks. There are four policies in total: , , , and . |
|  | Contains the number of identities that were assigned the vulnerable policy. |

By clicking on any policy from the list, you’ll access the  screen for the selected policy.

### List of identities screen

|  |  |
| --- | --- |
|  | Contains the AWS account connected to . |
|  | Indicates the type of the identity. Possible types are:  and . |
|  | Shows the principal name. |
|  ID | Shows the AWS account ID. |
|  | Date/time of the last synchronization between  and AWS. |

By clicking on any principal from the list, you’ll access the  modal for the selected principal.

### Identity details modal

The  modal shows a graphical representation of how the identity has the attached policy. It shows a map of the , , , , , , and  that lead to the attack path. This interactive map can be used to identify which action must be taken to mitigate the vulnerability, be it detaching a policy or a role from a user, removing a user from a group, or reconfiguring resources or actions.

|  |  |
| --- | --- |
|  | Field to filter the search for elements on the map. When a term matches the inserted pattern, the elements are visually highlighted. |
|  | Button to expand the map configuration options. |
|  | Field to select the map model. There are three models: , , and . |
|  | Button to zoom in on the map. |
|  | Button to zoom out on the map. |
|  | Button to reset the zoom to the initial state. Does not change the chosen layout. |