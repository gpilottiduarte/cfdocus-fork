## Metadata_Start 
## code: en
## title: How to integrate with JumpCloud 
## slug: saml-jumpcloud 
## seoTitle: How to integrate with JumpCloud 
## description:  
## contentType: Markdown 
## Metadata_End
This tutorial provides a guide on how to integrate senhasegura with JumpCloud, using SAML as the authentication protocol. The configuration of the integration occurs in parallel, alternating the inclusion of information from one environment to the other, until completion.

## Requirements:

* .
*  with all users who will access senhasegura via JumpCloud.

## Step 1: Create the application in JumpCloud

1. On the left sidebar of JumpCloud, locate the  section.
2. Select .
3. Click .
4. In the search field, look for .
5. In , click .

### In the General Info tab

1. Fill in the  field with the name of your application.

### In the SSO tab
Add the information:

1. : unique identifier.
2. : 
3. : 
4. :  select the information that users will use to log in.
5. : select one of the SAML 2.0 options corresponding to the previous field.
6. : select .
7. : leave it blank.
8. : 
9. : replace the default name with another identification.

### In the User Groups tab

1. Select the group that will access the application and click .
2. A confirmation message of the new SSO connection will appear. 
3. Click  to complete the process.

If successful, the application appears on the  page.
:::(Info) (Info)
Click on the certificate download link in the blue pop-up message at the upper-right corner. You’ll need this information later.
:::
:::(Warning) (Caution)
Keep JumpCloud open for the next configurations.
:::
***
## Step 2: Enable the SAML provider in senhasegura

1. In the top-left corner of the senhasegura platform, click , indicated by the box of nine squares, and select .
2. Select .
3. In the list of providers, locate the  option.
4. In the  column, make sure the option is enabled.
    4.1 If necessary, click , the icon represented by a checkmark (✓).
***
## Step 3: Create a SAML provider in senhasegura

1. In the top-left corner of the senhasegura platform, click , indicated by the box of nine squares, and select . 
2. Select .
3. In the top-right corner, click , the icon represented by three vertical dots (⁝).
4. Select .

### In the Main information tab
Add the information:

1. : select .
2. : keep it as .
3. : fill in with the same name entered in the  field.
4. : fill in with the URL. 
    4.1 Find this information in the JumpCloud  tab. Click on the  button.
5. : fill in with the URL of senhasegura or the domain.
6. : automatic fill-in.
7. : fill in with the URL. 
    7.1 Find this information in the JumpCloud  tab. Copy the information from the  field.
8. : select .

### In the Security SAML tab
Add the information:

1. Download the provider's certificate and copy its content.
2. : paste the certificate content.
    :::(Info) (Info)
    If you haven't saved the certificate information, go to the left sidebar menu of the application you created, click , and then select .
    ::: 
2. Click .

The system displays a success message, and the provider appears listed on the home page.
***
## Step 4: Access senhasegura via JumpCloud

1. On the home page of the senhasegura platform, click .
2. Click . You’ll be redirected to the JumpCloud authentication screen to enter your credentials.
3. After authentication, click on the senhasegura application to access the vault.
***
Do you still have questions? Reach out to the .
