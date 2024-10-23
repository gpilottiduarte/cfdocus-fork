## Metadata_Start 
## code: en
## title: How to manage authorizations per application 
## slug: how-to-manage-authorizations-per-application-in-devops-secret-manager 
## seoTitle: How to manage authorizations per application 
## description:  
## contentType: Markdown 
## Metadata_End
To use senhasegura's  features, you must authorize your applications registered with senhasegura.

## Create an authorization per application in DevOps Secret Manager

To create an authorization per application, follow the steps below:

1. On senhasegura, in the top left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. The main screen will list all the applications registered in the senhasegura.
4. To create a new authorization by application, identify the application you want to authorize and, in the  column, click on the plus icon.

In the  window, fill in the following steps:

1. On the  tab:

   1. : indicate which resources the application will be authorized to access.
   2. : in the drop-down menu, select the date from the calendar that opens in the first field, and the time in the second field.
   3. : indicate whether you want the authorization to be active or not. By default, authorization will be set to Yes.
   4. : enables or disables encryption of information marked as sensitive.
   5. : enables or disables authorization to create DSM applications.
   6. : in the drop-down menu, select the authorization environment. To learn how to register environments, access the How to register environments in DevOps Secret Manager documentation.
   7. : in the drop-down menu, select the authorization system.
   8. : list of IP addresses that will be allowed. Click on the plus icon to add as many IPs as you like. To allow any IP address, fill in *.
   9. : list of  allowed for this authorization. To allow any referer, create an empty list.
   10. : enter the certificate's fingerprint that will be used with this authorization.
2. In the  tab, in the  option, add the secrets that will be part of this authorization. To do this, follow the steps below:

   1. Click on the plus icon next to the word .
   2. In the  modal, select the ones you want to add to the authorization.
   3. Click .
3. In the  tab, in the  option, add the encryption keys that will be part of the authorization. To do this, follow the steps below:

   1. Click on the plus icon next to the word .
   2. In the  modal, select the ones you want to add to the authorization.
   3. Click .
4. Click .

## How to change an authorization per application in DevOps Secret Manager

To change an authorization per application in the DSM, access the list of applications through 

In the list, identify the application and the authorization you want to change. To do this, follow the steps below:

1. In the  column, click the represented by the three vertical dots icon and, in the drop-down menu, select the  option.
2. In the  window, make the necessary changes. This is the same window described in How to create an authorization per application in DevOps Secret Manager.
3. Click .

:::(info) (Info)
To download the authorization's private key, click the three vertical dots icon and select  from the drop-down menu.
:::

## How to view an authorization

To view an authorization by application in the DSM, access the list of applications through 

In the list, identify the application and authorization you want to view. To do this, follow the steps below:

1. In the  column, click , represented by the key icon.
2. In the , fill in:
   1. : authentication method used by the application.
   2. : name of the application.
   3. : unique value when the user marks authentication for AWS and has at least one ARN.
   4. : client identification. It must be a string as this example: .
   5. : secret of the client. Must be a string as this example: .
   6. In the  section:
      1. : code of the secret in senhasegura.
      2. : application name in senhasegura.
      3. :  name of the secret's identity. This is mandatory when creating a new secret and can't be the same as the Name field.

To view information about the secret, click on the magnifying glass icon and you'll be redirected to the  window with all the information about that secret.

---

Do you still have questions? Reach out to the .