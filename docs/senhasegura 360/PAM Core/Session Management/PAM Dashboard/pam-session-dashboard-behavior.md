## Metadata_Start 
## code: en
## title: Behavior 
## slug: pam-session-dashboard-behavior 
## seoTitle: Behavior 
## description:  
## contentType: Markdown 
## Metadata_End
In this article, you’ll find all the information about the  dashboard from . This dashboard provides an analysis of active users behavior.

:::(info) ()
The dashboard can only be accessed by a system administrator or system auditor user.
:::

## Behavior analysis

In the upper right corner, you’ll find the field that represents the period of the displayed data. Choose the period and click on the  icon to filter the data.

The date can be filtered by:

* .
* .
* .
* .
* .
* .
* .
* .
* : Choose the specific date.

## Graphics

|
|---|---|
|Daily progression chart displaying the number of accesses with associated security risks in senhasegura.
|Daily progression chart displaying the number of password views with some degree of associated security risks in senhasegura


## Lists

* : list of accesses with the highest risk on the most recent dates. The risk level is calculated based on the configured parameters.
    * : user that performs the session.
    * : the device used to make the access.
    * : the credential used in the session.
    * : date and time the user starts the session.
    * : number that indicates the risk level of that session. This number can go from 0 (zero) to 100 (one hundred).
    * : access details. 
        * : user details like name, e-mail, and IP number.
        * : user credential details (IP number, protocol, and port).
        * : session details.
        * : list of performed commands during a session.
* : list of password views with the highest risk on the most recent dates. The risk level is calculated based on the configured parameters.
    * 
    * 
    * 
    * 
    * 
    * : view details.
        * 
        * 
        * : user IP number, type of view, date and time of the view and device IP.
        * :
            *  
            * 
            * 
            * 
            * 
* : list containing the last five accesses, including accesses with no detected risk. Risky behaviors include accessing from an unusual destination, accessing from an unusual source, accessing with unusual credentials, accessing at unusual times, and accessing with unusual duration.
    * 
    * 
    * 
    * 
    * 
    * : Access details.
        * 
        * 
        * 
        * 
* : list containing the last five password views, including views with no detected risk. Risky behaviors include viewing from an unusual source, with unusual credentials, at unusual times, and with unusual password changes.
    * 
    * 
    * 
    * 
    * 
    * : view details.
        * 
        * 
        * 
        * 
