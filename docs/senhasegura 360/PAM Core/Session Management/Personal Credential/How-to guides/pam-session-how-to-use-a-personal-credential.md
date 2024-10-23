## Metadata_Start 
## code: en
## title: How to use a personal credential 
## slug: pam-session-how-to-use-a-personal-credential 
## seoTitle: How to use a personal credential 
## description:  
## contentType: Markdown 
## Metadata_End
In this document, you’ll find a step-by-step guide on how to use a personal credential to access a remote session.

:::(warning) ()
Only with the  parameter enabled the user will  be able to access the remote session with their personal credential. To enable this parameter, access the  document.
:::

---
## Requirements

* Ensure that the  parameter is enabled for the session.

:::(info) ()
Personal credentials are only available for Terminal Proxy and RDP Proxy sessions.
:::

---
## Access with a personal credential
:::(warning) ()
We recommend that users and devices using a personal credential don't have typed text indexing configured, in order to not infringe the user's right to privacy. But if the user's personal password or personal data is displayed on the screen due to output from the target device, these texts can be indexed, if configured, and they’ll be present in the session video.
:::

### Via Proxy Terminal

1. In the terminal application of your choice, log in to senhasegura.
2. Enter the protocol, your senhasegura user, and the senhasegura vault IP address or hostname. ex.: 
3. Press .
4. Enter your password.
5. With the senhasegura session started, enter the protocol, your  and the IP address or hostname from the device you want to access. ex.: 
6. Press .
7. Enter your password.
8. Press .

Now, the senhasegura session via Terminal Proxy will be used by the personal credential.

### Via RDP Proxy

1. In the RDP application, log in to senhasegura.
2. Click .
3. On the home screen, type:
    1. senhasegura user.
    2. Credential password.
    3. Device to be accessed.
    4. Personal credential.
    5. Personal credential password.
4. Click .

Now, the personal credential will use the senhasegura session via RDP Proxy.

:::(info) ()
The use of personal credentials doesn’t prevent the use of Access Groups with workflow, MFA tokens, emergency access, audited commands, or any other mechanism available for proxy sessions.
:::

---
### Next:



Do you still have questions? Reach out to the .