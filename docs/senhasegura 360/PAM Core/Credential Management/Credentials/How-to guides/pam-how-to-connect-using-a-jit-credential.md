## Metadata_Start 
## code: en
## title: How to connect using a JIT credential 
## slug: pam-how-to-connect-using-a-jit-credential 
## seoTitle: How to connect using a JIT credential 
## description:  
## contentType: Markdown 
## Metadata_End
Once you have set up your JIT credential, you can access it by following the steps below:

1. In the top left corner, click the , represented by the nine squares, and select .
2. In the side menu, select .
3. In the list, identify the previously configured JIT credential and click , represented by the computer icon.
4. A new window or tab will open in your browser with the following message: 
5. In case of success, you'll be redirected to the session on the configured device.
6. Otherwise, an error message will indicate that access couldn’t be provisioned with the following message: An error occurred while provisioning the credential.

:::(Warning) (Warning)
- When using the  credential mode, the credential to which the configuration is being made will be the target of the enable and disable template. In this case, use another credential to authenticate yourself at the JIT stage.
- When using the  mode, the credential where the JIT is being configured won't be the target of the template. A new dynamic credential will be created on the target device using the  pattern (senseg prefix followed by 7 digits). In this case, the credential itself can be used to authenticate itself on the target device.
:::

---

Do you still have questions? Reach out to the .
