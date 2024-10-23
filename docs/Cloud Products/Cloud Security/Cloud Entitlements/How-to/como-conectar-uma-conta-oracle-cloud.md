## Metadata_Start 
## code: en
## title: How to connect an Oracle Cloud account 
## slug: como-conectar-uma-conta-oracle-cloud 
## seoTitle: How to connect an Oracle Cloud account 
## description:  
## contentType: Markdown 
## Metadata_End
In this document, you will learn how to connect an Oracle Cloud (OCI) compartment to the , including all users and groups under the compartment.

## Requirements

* An OCI account with permission to generate API keys.  
* A group with policies with the following statements:  
    *   
    *   
    * 
    
    For more information on creating a group with policies, see  and .

## Generate an API key for a user in Oracle Cloud

1. Access your Oracle Cloud Infrastructure account.  
2. Click the  > .  
3. In , click .  
4. Click .  
5. Select .  
6. Click , and click .  
7. Copy the contents of the file preview. It should be in the following format:

`
[DEFAULT]
user=
fingerprint=
tenancy=
region=
key_file=
`

## Connect an OCI organization

1. Go to .  
2. In the left menu, click , and select .  
3. Click .  
4. Fill in the following fields according to the configuration file:  
   1. *: enter a name.  
   2. *: enter the value of user from the configuration file.  
   3. *: select the region shown in the configuration file.  
   4. *: enter the value of fingerprint from the configuration file.  
   5. *: enter the value of tenancy from the configuration file.  
   6. *: enter the value of tenancy from the configuration file.  
   7. : if set during the creation of the API key, add the passphrase for the .pem file.  
   8. : enter tags to identify the organization.  
5. Attach the private key file you downloaded previously.  
6. Click .

If connected successfully, your OCI compartment will appear in the list of connected accounts. Otherwise, you must restart the process by using another API key in Oracle Cloud. You can't connect a compartment that is already connected to .

---

Do you still have questions? Reach out to the .
