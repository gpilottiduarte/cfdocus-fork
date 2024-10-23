## Metadata_Start 
## code: en
## title: Monitoring center 
## slug: domum-dashboard-monitoring-center 
## seoTitle: Monitoring center 
## description:  
## contentType: Markdown 
## Metadata_End
The dashboard in  shows an overview of Domum usage by vendors, third-party users, groups of internal users, and internal users.

You can find the following in the Monitoring center:

* : the broadcast icon above the  field shows the communication between the senhasegura platform and the gateway service. 
    * By clicking on the icon, you can see the . 
    * The icon colors indicate the status of the communication.
        * : currently established communication without any failures in the last 12 hours.
        * : service not configured.
        * : currently established communication, but some failures could have happened in the past 12 hours.
        * : communication is unavailable.
* : selects information for a specific vendor or internal user group.
* : indicates the number of accesses via Domum when viewing the dashboard. 
    * By clicking on the text, you can reach the . 
* : indicates the number of providers registered in senhasegura. 
    * By clicking on the text, you can access the . 
* : indicates the number of third-party users registered in senhasegura. 
    * By clicking on the text, you can access the .
* : indicates the number of allowed accesses, including both third-party users and internal users.
* : indicates the number of internal user groups with access to senhasegura. 
    * By clicking on the text, you can access the .
* : indicates the number of internal users with access to Domum.
* : displays on the map the region where suspicious accesses originate. 
    * You can use the search bar to type the name of the location you want to look up.
* : displays the connection between the number of accesses and the authorized period for each provider in the last 12 hours.
* : displays the list of remote sessions in progress when viewing the dashboard. The field classifies the sessions by protocols used to access and manage network resources:
    * : number of RDP web sessions in progress.
    * : number of SSH/Telnet sessions in progress.
    * : number of HTTP VNC sessions in progress.
    * : number of SQL sessions in progress.

:::(info) ()
If there is a suspicious active session, it may be dropped. On the list  find the session you want and click the  icon. In the confirmation box click . The session will be dropped and the user will be logged out.
:::
* * *
Do you still have questions? Reach out to the .