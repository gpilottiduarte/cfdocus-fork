## Metadata_Start 
## code: en
## title: How to configure and start an MS SQL Server session with HeidiSQL 
## slug: pam-session-how-to-configure-and-start-an-ms-sql-server-session-with-heidisql-1 
## seoTitle: How to configure and start an MS SQL Server session with HeidiSQL 
## description:  
## contentType: Markdown 
## Metadata_End
In this article, you will find a step-by-step guide on how to configure and start an MS SQL Server-type Database Proxy session in the HeidiSQL database manager.

:::(warning) ()
Database Proxy has a default limit of 2.000 simultaneous connections. This can be changed, but there will be a significant provisioning increase in memory, taking into account that each connection slot uses around 64kb of memory. To make this increase, contact the support team.
:::

## Requirements

* Have a credential configured for using the Database Proxy. To find out how to register a credential, access the documentation on .
* Have the HeidiSQL application installed.
---

## Configure the database

1. Open the  application.

1. On the home screen, in the bottom left corner, click the button .

1. At  tab, fill in the fields with the following information:

    3.1.: choose the option .  
    3.2. : choose the option .
    3.3. : enter the IP number of the vault to be accessed.
    3.4. : enter the information as the example below:

    3.5. : enter your password to access the safe.
    3.6. : enter the default port number of the database (1433). If you use a port number other than the default, enter the number used.
    4. Click .

After these steps, the saved database will be listed in the application's side menu.

## Start the Database Proxy session
1. In  application, navigate to the left-side menu.
2.  Double-click on the database you want to access.
3. Or click on the desired database and then click .

All configured databases will be available in the side menu.

---
### Next:



Do you still have questions? Reach out to the .
