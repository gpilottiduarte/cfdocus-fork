## Metadata_Start 
## code: en
## title: How to configure Jira Service Desk integration in senhasegura 
## slug: how-to-configure-jira-service-desk-integration-in-senhasegura 
## seoTitle: How to configure Jira Service Desk integration in senhasegura 
## description:  
## contentType: Markdown 
## Metadata_End
This guide shows how to configure the integration between senhasegura and Jira Service Desk using .

## Requirements

* Jira Service Desk API authentication data:  
  * API URL.  
  * User.  
  * API Token.

## Configure Jira Service Desk

1. On senhasegura, in the upper-left corner, click the , represented by nine squares, and select .  
2. In the side menu, select   
3. In the  report, in the top bar, click on  and select .  
4. In the  window, select .  
5. In the  window, fill in the fields:  
   * : name of the integration in senhasegura.  
   * : select .  
   * : Jira API URL.  
   * : Jira user with permission to query tickets.  
   * : token generated in your Atlassian account.  
6. Click .

:::(info) (Info)
* The integration uses the endpoint  and accepts requests only for *tickets* with the status .  
* A  is required for this integration.
:::

---

Do you still have questions? Reach out to the .