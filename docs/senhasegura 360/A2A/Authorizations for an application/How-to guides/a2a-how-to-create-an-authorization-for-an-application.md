## Metadata_Start 
## code: en
## title: How to create an authorization for an application 
## slug: a2a-how-to-create-an-authorization-for-an-application 
## seoTitle: How to create an authorization for an application 
## description:  
## contentType: Markdown 
## Metadata_End
This document provides a step-by-step guide on how to create authorizations for an application created in the  module.


## Requirements

* A created application. For more information, access the  documentation.

:::(Info) (Info)
senhasegura has no restrictions on the number of authorizations created for an application. However, after the first creation of an authorization, the other authorizations can be created following two different steps. For more information, continue reading this tutorial.
:::
***
## Create the first authorization for an application

To create the first authorization for an application, follow the steps below:

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .
2. In the side menu, select .
3. Select the desired application from the list and click the  in the  column to open a drop-down menu.
4. In the drop-down menu, click , identified by the key icon.
5. In the  window, in the upper-right corner, click , represented by the three vertical dots, to open a drop-down menu.
6. In the drop-down menu, click .
7. In the  window, fill in the following information:
    1.  tab: define the authorization general information.
        1. : define the period during which the authorization will remain active. Fill in the date in the first field and the time in the second field. Click the downward arrow in each field to view a calendar and a list of times. After the set period, access performed through this authorization will be revoked.
        2. : define the application status. The options are  and .
        3. : define the environment where the authorization will be active. Click the downward arrow to view a list of available environments.
        4. : define the system where the authorization will be active. Click the downward arrow to view a list of available systems.
    2.  tab: define the authorization’s security information.
        1. : check the modules to which users can have access permission through the APIs. The available options are *PAM Core, Certificate Manager, Task Manager, Dashboards, Web Proxy Session, Users,* and *A2A*. For more information about each module, access the corresponding documentation on senhasegura’s . 
        
        3. *: mandatory field with two options:  and .
             :::(Warning) (Attention)
            Be careful when granting reading and writing permission as this provides users with unrestricted access to data.
            :::

        1.  *: this option enables or disables sensitive information such as passwords and secrets to be returned in encrypted API calls. To decrypt this data, use the private key provided in the authorization settings.
        2.  : click , represented by the plus sign, to add one or more IP addresses that can access the application. Enter an asterisk to authorize any IP address. 
To delete an IP address, click the  of the corresponding IP address.

        1. : define which previous web addresses can send requests. If left empty, all websites are authorized. 
        2. : enhance security by adding an extra layer of protection through fingerprint-based certificate validation. When activated, the system will validate both OAuth authentication data and the fingerprint of the certificate provided within the request.

    1.  tab: define the credentials that can be accessed through this authorization.

        1. : enter an IP, hostname, or username to search and add a credential registered within . Click the downward arrow to view a list of available credentials. Click .

                ii. : check this box to create a new credential and fill in the , - click the downward arrow to view a list of available devices -  and  fields for the new credential. Click .
On the same screen, under the title , view a list with the added credentials and their corresponding ,  name, , and .
You can deactivate an added credential by clicking the corresponding  icon.
    
        :::(Info) (Info)
        The created credential can be   viewed    in  >  >     .
        :::

    1.  tab: define the devices that can be accessed through this authorization.
        1. : enter the device’s  or , or click the downward arrow to view a list with all the devices registered in . Click .
 On the same screen, under the title , view a list with the added devices and their corresponding , , , , and .
You can deactivate an added device by clicking the corresponding  icon.


        :::(Info) (Info)
            The available devices can be viewed in .
        :::

    1.  tab: define the protected information that can be accessed through this authorization.

        1. : add information that you wish to protect. Click the downward arrow to view the available options.
On the same screen, under the title , view a list with the added protected information and their corresponding , , , and .
You can deactivate protected information by clicking on the corresponding  icon.

8. Click .
              
              
## Create other authorizations for the same application

The next authorizations can be created following the steps described in the  section of this tutorial or following the steps below.

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .
2. In the side menu, select .
3. From the list, locate the application for which you want to create a new authorization.
4. In the  column, click , represented by the plus icon. 
5. In the  window, follow the instructions described in step 7 of the .
6. Click .

The created authorizations are displayed in a report on the  screen and the  screen. For more information, access the How to view an authorization for an application documentation.

***

Do you still have questions? Reach out to the .


              
                                                                           
     
        


        











