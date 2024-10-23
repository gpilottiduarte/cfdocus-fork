## Metadata_Start 
## code: en
## title: About automated elevation of privileges 
## slug: pam-session-about-automated-elevation-of-privileges 
## seoTitle: About automated elevation of privileges 
## description:  
## contentType: Markdown 
## Metadata_End
senhasegura can allow users to perform elevated tasks, such as SUDO, without needing to know the credential's password.

In these cases, users will have their interactivity captured and senhasegura will perform the elevation using the same credential used to authenticate on the target device.

For automated elevation to be used, the  must be set to . To configure remote sessions, access the document .

Elevation of privileges is valid for Terminal Proxy or terminal sessions via Web Proxy, where before using a privileged command, the user must type  for it to be executed.

If the elevation of privilege is disabled for the session, you’ll be prompted for the device credential password when attempting to perform the action.
