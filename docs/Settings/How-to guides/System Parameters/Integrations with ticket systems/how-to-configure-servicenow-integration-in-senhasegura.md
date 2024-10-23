## Metadata_Start 
## code: en
## title: How to configure ServiceNow integration in senhasegura 
## slug: how-to-configure-servicenow-integration-in-senhasegura 
## seoTitle: How to configure ServiceNow integration in senhasegura 
## description:  
## contentType: Markdown 
## Metadata_End
This guide shows how to configure the integration between senhasegura and  using the .

## Requirements

* ServiceNow API authentication data:  
  * API URL.  
  * User.  
  * Password.

## Configure ServiceNow

1. On senhasegura, in the upper-left corner, click the , represented by nine squares, and select .  
2. In the side menu, select   
3. In the  report, in the top bar, click on  and select .  
4. In the  window, select .  
5. In the  window, fill in the fields:  
   * : name of the integration in senhasegura.  
   * : select .  
   * : ServiceNow API endpoint.  
   * : ServiceNow user with permission to query tickets.  
   * : password for authentication.  
6. Click .

:::(info) (Info)

* The integration uses the endpoint   and the approval flow accepts requests only for *tickets* with the status .

:::

---

Do you still have questions? Reach out to the .