## Metadata_Start 
## code: en
## title: How to manage an application 
## slug: how-to-manage-an-application-in-devops-secret-manager 
## seoTitle: How to manage an applications 
## description:  
## contentType: Markdown 
## Metadata_End
## Requirements

* Have registered applications to allow them to access the DSM's secrets.

## Register an application with DevOps Secret Manager

To register a new application, follow the steps below:

1. On senhasegura, in the top left corner, click the , represented by the nine squares, and select .
2. In the side menu, select .
3. The main screen will list all the applications registered on senhasegura. To register a new application, click , represented by the three vertical dots, and select  from the drop-down menu.

In  window, fill in the following steps:

1. In the  tab:
   1. : enter a name to identify the application.
   2. : in the drop-down menu, select the desired method.
   3. : in the drop-down menu, select the line of business for that application. You can register new lines of business within senhasegura.
   4. : in the drop-down menu, select the type of application being registered. You can register new application types within the senhasegura instance.
   5. : checkbox to enable or disable the application. By default, assume the Yes value.
   6. : enter the tags you want to link with the application. They must be separated by commas.
   7. : enter the description text for the application.
   8. : click on the button identified by the plus next to it, and fill in the Amazon AWS ARN of the resource that will be registered with the application.
2. In the  tab, in the  option, select the desired option:  or .
3. Click .

:::(info) (Info)
AWS ARN refers to the unique identifiers of AWS resources.
:::

## Change an application registered in DevOps Secret Manager

To change an application already registered in the DSM, access the list of applications through 

In the list, identify the application you want to change. To do this, follow the steps below:

1. In the  column, click the three vertical dots icon and select  from the drop-down menu.
2. In the  window, make the necessary changes.
3. Click .

## View an application registered in DevOps secret Manager

To view an application already registered in the DSM, access the list of applications through .

In the list, identify the application you want to view. To do this, follow the steps below:

1. In the  column, click the three vertical dots icon and select the , represented by the three horizontal lines icon, on the drop-down menu.
2. The  window will open in view mode.

In this window, you can view the information about the application:

1. : authentication method registered with the application.
2. : name of the application.
3. : client identification. It must be a string in this pattern: .
4. : client secret. To view it, click the eye icon.
5. : client's system.
6. : application environment.

## View an authorization by application

To view the authorizations of an application already registered in the DSM, access the list of applications through 

In the list, identify the application you want to view. To do this, follow the steps below:

1. In the  column, click on , represented by the key icon.
2. In the  by application window, you can analyze a list of all the authorizations that this application has.

## Manage the automatic provisioning of secrets

When you register a new application, you can determine whether it will automatically provision the secrets stored in the DSM.

## Requirements

* Registered provisioning profiles.

To manage the automatic provisioning of secrets, follow the steps below:

1. In the  window, in the  tab, check the  option on the  field.
2.  section:
   1.  .
      1. Click the plus icon to open the  field under the name.
         1. In the drop-down menu, select one of the profiles you created earlier.
   2.  .
      1. Click on the plus icon to open the following fields:
         1. : in the drop-down menu, select the credential's device.
         2. : in the drop-down menu, select the profile you created earlier.
3. Click .

---

Do you still have questions? Reach out to the .