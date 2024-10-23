## Metadata_Start 
## code: en
## title: How to configure the Active Directory authentication 
## slug: configure-active-directory-authentication 
## seoTitle: How to configure the Active Directory authentication 
## description:  
## contentType: Markdown 
## Metadata_End
Learn how to configure Active Directory authentication by following the steps described in this article.

## Requirements

* A user who is part of the Domain Admins group.
*   in the list of authentication providers.
*  in senhasegura
*  whose credentials can be used to query users in the same domain.
* Integrate a Windows Server Active Directory (AD) with LDAP.

:::(info) (Info)
For security reasons, Active Directory LDAP is set as the default authentication provider. There’s no fallback for users setting local authentication.
:::

---
## Configure authentication via Active Directory
To configure authentication in senhasegura via Active Directory, follow these steps:

1. In the top-left corner, click , represented by the nine squares icon, and select .
2. In the side menu, select .
3. In the top-right corner, click the  icon, represented by the three vertical dots.
4. Select .
5. Fill out the  form. 
     5.1 : enter the hostname or IP address of the AD server.
     5.2 : enter the LDAP communication port number.
     5.3 : keep it as .
     5.4 : select the credential that will be used for user authentication on the server and user synchronization between servers. 
    5.5 : enter the base to be used for LDAP queries.
     5.6 : select the format for the queries.
     5.7 : enter the domain name of the LDAP server account.
     5.8 : enter the abbreviation of the LDAP server account domain name.
     5.9 : set the server's priority. The lower the number, the higher the priority of the server.
     5.10 : indicate whether the authentication will use an SSL connection or not. If using an SSL connection, make sure to add the correct port.
     5.11 : indicate whether the object is a DN or not.
     5.12 : indicate whether the authentication will require the Bind-DN to authenticate and connect to the server.
6. Click .

The  home page lists the server.

You can make edits to the registered information. To do so, locate the server in question and click , identified by a pencil and paper icon, to make the necessary changes.

:::(Info) (Info)
It's possible to register multiple Active Directory servers in senhasegura, assigning them a priority order. senhasegura uses this order to authenticate users, attempting to log in first to the highest-priority server. If the first authentication attempt fails, the system moves on to the next server in the list and so on. If login fails on all registered AD servers, the user receives a notification stating that senhasegura was unable to authenticate their access.
:::
***
## Test authentication
:::(Warning) (Caution)
Ensure that the LDAP provider is enabled in . This action is necessary to perform the authentication test that follows.
:::
1. In the  column, locate the saved server and click  of the corresponding server.
2. Select .
3. Fill out the  form with the following information: Base DN, User, and Password.
4. Click .

If successful, an authentication message will be displayed on the screen, indicating that the server is ready for use.
***
Do you still have questions? Reach out to the .
