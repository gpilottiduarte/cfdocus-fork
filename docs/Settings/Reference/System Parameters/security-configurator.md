## Metadata_Start 
## code: en
## title: Security configurator 
## slug: security-configurator 
## seoTitle: Security configurator 
## description:  
## contentType: Markdown 
## Metadata_End
In this document, you will find all the information about the  section of the senhasegura settings.

## Path to access

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .  
2. In the side menu, select 

## Segurity

### User accounts maintenance

| Item | Description |
| :---- | :---- |
|  | Indicates the value, in minutes, for the session (login) to automatically expire. |
|  | Indicates the number of unsuccessful login attempts in a login session before the account is locked. |
|   | Checkbox to indicate if an inactive account will be locked. |
|  | If the  option is enabled, this will indicate the number of days without access before the account is locked. |
|  | Checkbox to indicate if the user must change their password on first access. |
|  | Checkbox to indicate if the password will automatically expire. |
|  | If the  option is enabled, this will indicate the number of days until the password expires. |
|  | Maximum time for the user to log in before the CSRF token expires. |

:::(info) (Info)  
CSRF (Cross-Site Request Forgery) is an attack where a malicious website induces an authenticated user on another site, such as a bank, to perform an unwanted action, like a financial transfer. Without CSRF protection, a malicious link can perform this action as if it were the user themselves, using valid session cookies. To prevent this, CSRF tokens are used.  
:::

### Multi-factor authentication

| Item | Description |
| :---- | :---- |
|  | Checkbox to indicate if MFA authentication will be required for all users. |
|  | Checkbox to indicate if the use of digital certificates will be required for all users. |
|  | Checkbox to indicate if the use of an external solution for MFA authentication will be allowed. |
|  | Checkbox to indicate if the option to trust the computer will be enabled and for how long, at maximum, it will be possible to trust the computer. In other words, with this configuration enabled, it won't be necessary to use the token for the defined time period. |
|  | Checkbox to indicate if expired authentication tokens will be accepted and for how long an expired token will be considered valid. |

### Password security level

| Item | Description |
| :---- | :---- |
|  | Indicates the minimum number of characters for the password. |
|  | Indicates the minimum number of numbers for the password. |
|  | Checkbox to indicate if password reuse won't be allowed |
|  | If the  option is enabled, indicates how many passwords, retroactively, cannot be reused. |
|  | Checkbox to indicate if the password must contain symbols. |

### Access control by IP

| Item | Description |
| :---- | :---- |
|  | Radio button. Indicates whether all IP addresses will be denied or allowed. |
|  | IP ranges. |
|  | Starting address of the IP range. |
|  | Ending address of the IP range. |
|  | Dropdown menu. Indicates the action to be taken for this IP range. Can be  or . |

### Adaptive MFA by location

| Item | Description |
| :---- | :---- |
|  | IP ranges. |
|  | Starting address of the IP range. |
|  | Ending address of the IP range. |
|  | Dropdown menu. Indicates the action to be taken for this IP range. Can be  or . |
