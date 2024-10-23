## Metadata_Start 
## code: en
## title: How to manage SAML providers 
## slug: how-to-manage-saml-providers 
## seoTitle: How to manage SAML providers 
## description:  
## contentType: Markdown 
## Metadata_End
You can add or remove SAML providers in senhasegura. To do this, follow the steps below.

## Register a new provider

To add a new provider, follow the steps below:

1. On senhasegura, in the upper-left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. In the upper right corner, click on , represented by the three vertical dots, and select .
4. In the  window, fill in the following fields:

### General information tab

1. Type: select your SAML provider from the drop-down menu. In case it is not listed, select the SAML provider option.
2. : select .
3. : to give access to Domum senhasegura users, select D; to give access to local users only, select .
4. :  or  of the SAML application.
5. : enter the URL that will manage the SAML metadata.
6. : enter the domain or public IP of senhasegura.
7. : purely informative field to be used in SAML.
8. : fill in any relevant comments or observations.
9. In the  section:
   1.  indicate the URL used to log in.
   2.  indicate the URL used to log out.
   3.  choose the type of Redirect Bind from the drop-down menu. The options are  or .

### Security SAML tab

1.  text field for you to paste the contents of the  certificate.

:::(info) (Info)
To ensure that SAML works properly, all the settings mentioned in this guide must correspond exactly to those present in the IDP (Identity Provider). If there are discrepancies, authentication will fail.
:::

You can click  on any of the tabs.

## Update provider

1. On senhasegura, in the upper-left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. Identify the record you want to update and, in the  column, click , represented by the pencil and paper icon.
4. The  window will open in edit mode.
5. Edit the necessary information and click .

## Delete provider

1. On senhasegura, in the upper-left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. Identify the record you want to update. In the  column, click on the icon with three vertical dots and select , represented by the trash can icon.
4. In the confirmation modal, click .

---

Do you still have questions? Reach out to the .