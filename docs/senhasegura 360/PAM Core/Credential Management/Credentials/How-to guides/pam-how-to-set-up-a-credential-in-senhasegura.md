## Metadata_Start 
## code: en
## title: How to setup up a credential in senhasegura 
## slug: pam-how-to-set-up-a-credential-in-senhasegura 
## seoTitle: How to set up a credential in senhasegura 
## description:  
## contentType: Markdown 
## Metadata_End
In this tutorial, we’ll provide a step-by-step guide to setting up a credential in senhasegura. Ensure you fulfill the requirements below before proceeding with the configuration steps.

## Requirements

- Be registered/enabled as a PAM operator in senhasegura.
- Have a device created.

## How to set up a credential

There are two ways to access the  configuration area.

The first way is via the  menu on the top toolbar. To configure a credential using quick actions, follow the steps below:

1. Click on the  icon, represented by a sheet of paper with a sum sign, and select .

The second way is from the . To do this, follow the steps below:

1. In the top left corner of the senhasegura platform, click on the , represented by the nine squares, and select .
2. In the side menu, select .
3. Click on the  icon, represented by the three vertical dots, and click .

Both actions will open a new pop-up window, which you must fill in with your data.

## In the Information tab

1. *.
2. *.
3. .
4. *.
5. .
6. Enable * as  or  to categorize the status.
7. Set the password for the credential (limit 256 characters, 70 if the password change is set to automated).
8. Choose to generate a random password according to the password policy.
9. Optionally, fill in the  for identification of the credential.
10. Click the  button.

## In the Execution settings tab

1.  choose the parent credential from the drop-down menu. Note that when you select a parent credential, the child credential will assume the same password as the parent credential. Whenever there is a manual or automated password change on the parent credential, the child credential will also be modified and assume the same password as the parent credential.
2. In the  section:
    1.  check this checkbox to make automated credential password exchange active.
    2. 
    3. : choose the plugin for automated credential password exchange from the drop-down menu.
    4.  select the template for automated credential password exchange from the drop-down menu.
3. In the  section:
    1.  select this checkbox to use your own credential to perform authentication.
    2.  select the credential that will perform authentication from the drop-down menu.
4. In the  section, in the  option, select the  or  option. This option enables credential reconciliation. For more information, go to the documentation on 

## In the Session settings tab

1. : select the connectivity options to which this credential will have access.
2. In the  section:
    1.  select this checkbox if you want this credential only to have access to one or more remote applications. If you choose this option, you must indicate which remote applications will be accessed by this credential. Fill in the fields below:
        1.  click the add button to add the applications used. Clicking on the add button will take you to two drop-down menus:
            1.  select the application you want to give access to the credential from the drop-down menu.
            2. : select the connection protocol that this remote application will use.
    2. : select this checkbox to use your own credential to authenticate.
    3.  enter the credential that will be used for authentication.
    4. : indicate the device where authentication will take place.
3. In the  section:
    1.  upload the certificate file.
    2.  upload the key file for authentication.
    3.  password for the key file.

:::(error) (Alert)
- The certificate will only be used when registering a credential to connect to an Oracle database. For more information, see the documentation on .
- When you upload a certificate, it will be linked to the credential at the time of upload. However, be aware that if you need to edit this credential after saving it, there will be no indication that the certificate file has been uploaded.
- You can replace the certificate by simply uploading the file again if necessary.
:::

## In the Additional settings tab

1.  enter the identifier of the web service used in the credential.
:::(Info) (Info)
If the  field is blank when creating a credential, the system will automatically assign a UUID (Universally Unique Identifier). The generated UUID will then be displayed in the  field in the interface. You can change this value to one of your preferences.
:::
2. : defines the owner of the credential, the user indicated in this field will be the only one with access to the credential.
3. : this field is used to specify the location of the credential in the files. This functionality is particularly useful when there is a need to change the password in the files. By providing the path, it is possible to identify precisely where to change the credential on the server.
4.  fill in your TOTP key. For more information, see the documentation on .

:::(Error) (Alert)
For the TOTP feature to work properly, your secret key must be entered in upper case.
:::

5. In the  section:
    1.  by clicking on the plus sign, you can enter additional parameters for authentication. In this case, you can enter the following parameters: Name, Surname, and Value.
    2. : fill in relevant remarks in case necessary.

:::(Warning) (Important)
- The limit of credentials varies according to the license contracted with senhasegura.
- The existence of a parent credential does not prevent the password of the child credential from being changed manually or automatically.
:::

## How to edit a credential

To edit a credential, follow the steps below:

1. On the senhasegura platform, in the top left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. In the list, identify the credential you want to edit, and in the  column, click on the icon represented by the three vertical dots and select the  option, represented by the pencil and paper icon, from the drop-down menu.
4. In the  window, edit the settings you want according to the instructions in this document.
5. Click .

***

## Next

1. .
2. .
3. .
4. .
5. .
6. .
7. .
8. .
9. .

***

Do you still have questions? Reach out to the .