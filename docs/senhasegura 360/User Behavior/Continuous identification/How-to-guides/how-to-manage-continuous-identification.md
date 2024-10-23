## Metadata_Start 
## code: en
## title: How to manage Continuous identification 
## slug: how-to-manage-continuous-identification 
## seoTitle: How to manage Continuous identification 
## description:  
## contentType: Markdown 
## Metadata_End

This document provides a step-by-step guide on how to configure the  feature of  to request the user to re-authenticate in  after suspicious events, as well as to view the generated reauthentication logs.

## Requirements
- Administrator permission.

## Path to access
1. On , in the upper-left corner, click the , represented by the nine squares, and select .

***

## Configure Continuous identification
To configure the triggers that will prompt user reauthentication requests in , follow the steps below:

:::(info) (Info)
By default, this feature is disabled. To enable it, set the parameters to a value other than zero.
:::

1. In the side menu of the  screen, select .
2. On the  screen, select  and go to the  section at the bottom of the screen.
3. In the  section, fill in:
   - *: define how many points the user must lose for re-authentication to be triggered.
     : the points lost for each action are defined in other sections of .
   
   - *: define how many high-risk sessions the user must perform for re-authentication to be triggered.
     : high-risk session definitions are tied to audited commands and their criticalities, which can be configured and viewed in .
   
   - *: define how many audited commands the user must enter in a session for reauthentication to be triggered.
     : blocked commands are audited commands configured as  or , and can be configured and viewed in .
   
   - *: define how many times the user must attempt to start a session at a prohibited time for their access group before reauthentication is triggered.
     : time access permissions are defined and viewed in .
   
   - *: define how many times the user must attempt to view a password at a prohibited time for their access group before reauthentication is triggered.
     : password viewing time permissions are defined and viewed in .

:::(info) (Info)
The items marked with an asterisk are required.
:::

:::(warning) (Attention)
After successful user re-authentication, the attempt count will be reset. This means that, for example, if the * parameter is set to 3, after the user makes these 3 attempts and re-authenticates in , re-authentication will only be requested again if they make another 3 attempts in their next logged-in session.
:::

## View re-authentication logs
To view the reauthentication logs requested from users due to suspicious actions, follow the steps below:

1. In the side menu of the  screen, select .
2. Search for the desired events using the filters , and .
3. View the report with the columns , and .
4. In the  column, click , represented by the key icon, to get more information about the selected re-authentication event.

---

Do you still have questions? Reach out to the .