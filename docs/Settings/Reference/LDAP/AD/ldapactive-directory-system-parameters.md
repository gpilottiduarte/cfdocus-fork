## Metadata_Start 
## code: en
## title: LDAP/Active Directory - System Parameters 
## slug: ldapactive-directory-system-parameters 
## seoTitle: LDAP/Active Directory - System Parameters 
## description:  
## contentType: Markdown 
## Metadata_End
In this document, you will find all the information about the configuration parameters for LDAP/Active Directory servers.

## 

1. In senhasegura, in the upper left corner, click on the , represented by nine squares, and select .  
2. In the side menu, select .  
3. In the , select .

## 

In this report, it's possible to configure various aspects of LDAP and AD servers and authentication in senhasegura.

### 

| Item | Description |
| :---- | :---- |
| * | Radio button. When activating this option, all users without a group will be deactivated during LDAP/AD synchronization. |
|  | Radio button. If you choose , the server field will use a credential in the vault. If you choose , the screen will display a user field and a password field. |

### 

| Item | Description |
| :---- | :---- |
| * | Radio button. When activating this option, the username will be updated after login. |
| * | Radio button. When activating this option, the user's email address will be updated after login. |
| * | Radio button. When activating this option, the user's local password will be updated after login. |
| * | Radio button. When activating this option, the local user will be activated after login. |
| * | Radio button. When activating this option, users who are inactive in the system will have their login blocked in senhasegura. |

### 

| Item | Description |
| :---- | :---- |
|  | Represented by the addition icon, enables the fields to add domains in senhasegura. |
|  | Text field. Fill in with the complete address for the domain. |
|  | Text field. Fill in with the short address for the domain. |
|  | Deletes the domain record. |
