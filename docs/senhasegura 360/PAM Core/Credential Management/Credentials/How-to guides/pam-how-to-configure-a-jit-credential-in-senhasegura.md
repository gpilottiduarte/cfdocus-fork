## Metadata_Start 
## code: en
## title: How to configure a JIT credential in senhasegura 
## slug: pam-how-to-configure-a-jit-credential-in-senhasegura 
## seoTitle: How to configure a JIT credential in senhasegura 
## description:  
## contentType: Markdown 
## Metadata_End
The senhasegura platform offers the possibility of using Just-In-Time (JIT) credentials. This configuration manages the use time of services, such as when an account is created or activated or needs specific permissions added during a period to perform actions.

:::(Info) (Info)
Be aware that after this access, the account is deleted, inactivated, or removed.
:::

JIT access configuration is done when you register or edit a credential. If you are registering a credential, access the documentation on . In case you are editing a credential, follow the steps below:

1. At the senhasegura platform, in the top left corner, click on , represented by the nine squares, and select .
2. In the side menu, select .
3. In the list of credentials, locate the credential you want to edit and in the  column, click on the three vertical dots icon and select the  option from the drop-down menu.

:::(Info) (Info)
Before registering a JIT-type credential, you must first  configure the  and  templates for the systems the credentials will use. These templates will be configured in the credentials and then used when the proxy session is initialized. For more information on configuring execution templates, access the Templates documentation.


:::

In both modes, the  form will open. In the form, go to the  tab and fill in the following fields:

1.  select the  field
2. In the   drop-down menu, select one of the two options:
    1.  the JIT credential will be created when the Proxy session is requested to be initialized and will be deleted when the session ends. The creation and removal of a JIT credential is a previously defined privilege that makes it possible to create a credential for a specified period, which will be automatically deleted after that period.
    2.  the JIT credential will be activated when it requests the initialization of the Proxy session and will be inactivated at the end of the session.
3. In the  section, check the  option if you want to use the credential in question to connect. If not, uncheck the option and enter a credential for authentication in the  drop-down menu.

According to the  you have chosen, one of the two sections will be enabled.

In case you selected , fill in the following fields:

1. In the  drop-down menu, select one of the registered plugins.
2. In the  drop-down menu, select one of the registered templates.
3. In the  drop-down menu, select one of the registered plugins.
4. In the  drop-down menu, select one of the registered templates.

In case you selected , fill in the following fields:

1. In the  drop-down menu, select one of the registered plugins.
2. In the  drop-down menu, select one of the registered templates.
3. In the  drop-down menu, select one of the registered plugins.
4. In the  drop-down menu, select one of the registered templates.

Click the  button.

---

Do you still have questions? Reach out to the .