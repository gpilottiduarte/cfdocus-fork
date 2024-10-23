## Metadata_Start 
## code: en
## title: LDAP/AD servers 
## slug: ldapad-servers 
## seoTitle: LDAP/AD servers 
## description:  
## contentType: Markdown 
## Metadata_End
In this document you'll find a reference guide for the LDAP/AD servers on senhasegura.

## Path to access

1. On senhasegura, in the upper-left corner, click the  represented by the nine squares, and select   
2. On the side menu, select 

## Top bar

| Item  | Description |
| :---- | :---- |
|  | Represented by the magnifying glass icon. Displays or hides the search fields on the screen. |
|  | Represented by the counterclockwise arrow icon. Refreshes the page. |
|  | Represented by the three vertical dots icon. Displays the possible actions for the page. |
|  | Open the  window. |
|  | Represented by the printer icon. It opens a new page for printing the report. |
|  | Represented by the sheet of paper icon, downloads the report. |
|  | Represented by the clock icon. It opens the window for scheduling the report. |

## Search fields

When you click on , a series of fields are displayed. These are used to refine your search results. They are:

| Item | Description |
| :---- | :---- |
|  | Filters by the host of the LDAP/AD server. |
|  | Filters by LDAP/AD server status. Can be or. |

In addition to these options, you have two buttons: , which applies the parameters passed into the fields, and , which clears all the parameters.

## Report fields

In the server list, you have the following fields:

*  displays the server's registration code within senhasegura.  
*  displays the server's address or hostname.  
*  displays the port on which the LDAP/AD server listens  
*  displays the user name for connecting to the server.  
*  displays the server's Base DN parameters.  
*  displays a specific representation of a user account's username or path in the directory. For example, .  
*  displays the filter expression used to specify search criteria for locating user accounts or other objects in the directory. For example: .  
*  displays whether the server uses SSL.  
*  displays whether the server requires DN for the bind process.  
*  displays the domain name in which the server is registered.  
*  also known as NetBIOS Domain Name, is the shortened version of the domain name in a network environment that uses directory services. This field displays the short name used to log into the Windows network. For example:   
*   
*  displays whether the server is active or not.  
* In the  column, you have two options:  
  *  opens the LDAP Server window in edit mode.  
  *  opens the LDAP connection test window.

## LDAP server window

When you click on  or , the  window will open. This window contains the following fields:

| Item | Description |
| :---- | :---- |
|  | LDAP server host. |
|  | Port where the LDAP server will listen. |
|  | Radio button to indicate the status of the server in senhasegura. It can be  or . |
|  | Drop-down menu for choosing the credential that will be used to authenticate to the LDAP/AD server. |
|  | Drop-down menu for choosing the connector used with the LDAP/AD server. |
|  | Server DN base. |
|  | Account form. |
|  | Account filter format. |
|  | Name of the domain to which the account belongs. |
|  | Short name for the domain to which the account belongs. |
|  | Radio button to indicate whether the server should use a domain credential. |
|  | Indicates the account's unique username |
|  | Indicates whether the DN will be used as a unique identifier. |
|  | Radio button to indicate whether the member will be identified by DN. |
|  | Radio button to indicate whether the Bind process will require DN. |
|  | Indicates the name of the group to which the server belongs. |
|  | Indicates the DN of the group in question. |
|  | Indicates the attributes of the group in question. |
|  | Indicates the scope of the group in question. |
|  | Indicates a filter expression to be used in the group in question. |
|  | Indicates which member attributes are required for the group in question. |
|  |  |
|  | Radio button to indicate the use of SSL. By default, it is set to No. |

## Authentication test window

By clicking on the three vertical dots in the  column and selecting the  option, the  window will open with the following fields:

| Item | Description |
| :---- | :---- |
|   | Label indicating the name and port of the LDAP server being tested for authentication. |
|  | Base DN parameters do connect to the server in question. |
|  | Field for entering the user’s username used in the authentication test. |
|  | Field for entering the user's password that will be used in the authentication test. |

