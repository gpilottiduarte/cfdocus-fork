## Metadata_Start 
## code: en
## title: How to configure the integration with CA Service Desk Manager in senhasegura 
## slug: how-to-configure-the-integration-with-ca-service-desk-manager-in-senhasegura 
## seoTitle: How to configure the integration with CA Service Desk Manager in senhasegura 
## description:  
## contentType: Markdown 
## Metadata_End
This guide shows how to configure the integration between senhasegura and CA Service Desk Manager using REST API or SQL Server.

## REST API

### Requirements

* HTTPS connection between senhasegura and CA Service Desk Manager.  
* The following CA Service Desk Manager API authentication data:  
  * API URL.  
  * User.  
  * Password.

### Configure

1. On senhasegura, in the upper-left corner, click the , represented by a nine squares icon, and select .  
2. In the side menu, select .  
3. In the  report, in the top bar, click on  and select .  
4. In the  window, select . Fill in the fields:  
   1. : fill in with a name for the integration.  
   2. : indicates the status of the integration. Select .  
   3. : select Rest API.  
   4. : enter an user with permission to query tickets.  
   5. : enter user's password.  
   6. : enter the main URL of the integration.  
5. Click .

## SQL Server

### Requirements

* SQL Server connection between senhasegura and CA Service Desk Manager.  
* The following CA Service Desk Manager database authentication data:  
  * User.  
  * Password.  
  * Database hostname.  
  * Database port.  
  * Database name.  
  * Database instance.

### Configure

1. On senhasegura, in the upper-left corner, click the , represented by a nine squares icon, and select .  
2. In the side menu, select .  
3. In the  report, in the top bar, click on  and select .  
4. In the  window, select . Fill in the fields:  
   * : fill in with a name for the integration.  
   * : indicates the status of the integration. Select .  
   * : select SQL Server.  
   * : enter an user in SQL Server.  
   * : enter user's password in SQL Server.  
   *  enter the hostname or IP address of the SQL Server database.  
   *  enter the port for connection to SQL Server.  
   *  enter the name of the database.  
   *  enter a database instance.  
5. Click  

---

Do you still have questions? Reach out to the .