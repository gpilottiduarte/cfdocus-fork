## Metadata_Start 
## code: en
## title: How to register a multi-factor authentication (MFA) provider 
## slug: how-to-add-multi-factor-authentication 
## seoTitle: How to register a multi-factor authentication (MFA) provider 
## description:  
## contentType: Markdown 
## Metadata_End
Registering a multi-factor authentication (MFA) provider is a crucial step in strengthening the security of information systems and ensuring that only authorized users have access to sensitive data and critical resources. MFA adds an extra layer of protection to the authentication process, requiring users to provide two or more verification factors before granting access to systems. This approach combines something the user knows (such as a password), something the user has (such as a security token or smartphone app), and sometimes something the user has (such as a fingerprint or facial recognition).

## Requirements

* Having the role of System Administrator.

## Register an MFA provider

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .  
2. In the side menu, select .  
3. In the  report, in the top bar, click , represented by three vertical dots icon,  and select .  
4. In the  window, the options are *RSA Authenticator, Duo Security, Radius* and *AuthID*.

:::(info) (Info)  
The following steps can be used for all multi-factor authentication providers,  for the  and  providers which have their own fields. For information, access the document on How to register an  provider.  
:::

### Register a provider

1. In the  window, fill in the fields:  
   1.  name of the authentication provider.  
   2.  select   
   3. : indicate the provider's endpoint.  
   4. : indicate the provider's  value.  
   5. : indicate the provider's key.  
2. Click on .

## Edit an MFA provider

1. To modify a previously registered provider, access the  report and, in the  column, click on , represented by the pencil and paper icon.  
2. The  window will open in edit mode. Make the necessary changes and click .

## Disable an MFA provider

1. To deactivate a previously registered device, access the  report and, in the  column, click on , represented by the pencil and paper icon.  
2. The  window will open in edit mode.  
3. In the  field, select .   
4. Click .

## Enable an MFA provider

1. To activate a previously registered device that is currently inactive, access the  report.  
2. In the filter bar, select  in the  drop-down menu and click on .  
3. In the  column, click on , represented by the pencil and paper icon.  
4. The  window will open in edit mode.  
5. In the  field, select .   
6. Click .


***
Do you still have questions? Reach out to the .
