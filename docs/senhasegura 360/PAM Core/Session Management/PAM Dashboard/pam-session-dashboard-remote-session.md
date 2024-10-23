## Metadata_Start 
## code: en
## title: Remote Session 
## slug: pam-session-dashboard-remote-session 
## seoTitle: Remote Session 
## description:  
## contentType: Markdown 
## Metadata_End
In this article, you’ll find all the information about the  dashboard from . This dashboard will give a graphical visualization of all users' remote sessions.

:::(info) ()
The dashboard can only be accessed by a system administrator or system auditor user.
:::

## Remote session

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
* : choose the specific date.

## Cards

|||
|---|---|
|Accessed sessions of the RDP Web type.
|Accessed sessions of the SSH/Telnet type.
|Accessed sessions of the HTTP/VNC type.
|Accessed sessions of the RDP Gate type.
|Accessed sessions of the Jump Server type.
|Accessed sessions of the SQL type.
|Accessed sessions of the X11 type.

## Graphics

|
|---|---|
|The total number of accessed sessions divided per day.
|The total number of accessed sessions by proxy divided per day and type.


## List

* : shows the number of active sessions at the moment of searching, divided by type:
    * : the number that represents the session.
    * : the name of the user that performs the session.
    * : the originating IP address associated with the user.
    * : the user’s credential.
    * : the IP number representing the accessed device.
    * : the accessed protocol type.
    * : the date and time when the session started.
    * : the duration of a session.
    * : access details.
        * : includes user details like name, e-mail, and IP number.
        * : used credential details.
        * : some access details (IP number, time, protocol, and port).
        * : a list of performed commands during a session.