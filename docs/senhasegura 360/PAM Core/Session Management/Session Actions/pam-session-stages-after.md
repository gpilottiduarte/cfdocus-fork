## Metadata_Start 
## code: en
## title: About Actions after a session 
## slug: pam-session-stages-after 
## seoTitle: About Actions after a session 
## description:  
## contentType: Markdown 
## Metadata_End
This document contains information about actions that can happen after a session.

Once the session ends, the administrator and auditors can review the details individually and consult the general table of sessions, credentials, and user behaviors. Additionally, the used credential is available for blocking or recycling actions.

## Possible actions
 During the session, several actions may have occurred. All of these actions are available in the session logs.

 Session recording will be played as it occurred.

 Users can request by e-mail that one or more auditors evaluate the session. The session will be divided into an audit report, and the solicitor can include an explanatory text.

 By default, senhasegura will purge session files according to the configured interval. But when a session is protected from this purge, it will be available for as long as it takes.

 If necessary, export the session video in MP4 format for an external audit.

 Audited commands detected in the session add scores to the session. This score reflects in the Device, Credential, and User operators, providing to the administrator a significant overview of the risks involved in the business.

 Any text typed or presented in the session is available in a report containing the text of all other sessions that have occurred. It allows the administrator to search for text that has appeared in a specific period on any device.
:::(Info) ()
The texts entered during the session will be mapped only in the language configured in the system parameters or the segregated parameters.
:::

 
