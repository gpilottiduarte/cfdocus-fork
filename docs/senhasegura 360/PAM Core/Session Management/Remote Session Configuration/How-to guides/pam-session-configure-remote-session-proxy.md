## Metadata_Start 
## code: en
## title: How to configure a remote session (proxy) 
## slug: pam-session-configure-remote-session-proxy 
## seoTitle: How to configure a remote session (proxy) 
## description:  
## contentType: Markdown 
## Metadata_End
This document will guide you through a step-by-step on how to configure the global parameters for your remote session (proxy).

### Configure a session

1. On senhasegura, in the upper left corner, click , identified by the nine squares icon, and then select .
2. In the side menu, select  >  . 
3. At the  tab, fill in the mandatory fields identified with the asterisk.
    :::(info) ()
    To understand the meaning of each parameter, access the  document.
    :::
    :::(warning) ()
    All fields are set with a default value, as recommended by senhasegura. However, you can customize your session according to your needs.
    :::
4. At the  section, if necessary, change the fields below:
    1. Enable file transfer for download?*
    2. Enable file transfer for upload?*
        :::(error) ()
        The  parameter underwent a beta update and was divided into two parameters:  and . Currently, If you select  for either of these parameters, both download and upload functions will be . To completely  file transfer, select  for  parameters.
        :::
    3. Enable Ctrl+Alt+Del?*
    4. Enable copy and paste?*
    5. Enable use of personal credentials?*
    6. Enable triggers for files transfers?*
    7. Convert /r/n to /n on SSH sessions when using the browser?*
    8. Enable download for local access?*
    9. PuTTY installation path*
    10. Users can change PuTTY installation directory?*
    11. senhasegura server IPv6 interface*
    12. Color depth
    13. RDP drive letter*
    14. Enable support for SSH domain credentials?*
    15. Mask for connection string when using SSH domain credentials*
    16. Connection banner: write it down the message to be displayed at the beginning of a session.
5. At the  section, if necessary, change the fields below:
    1. Enable SUDO automation in Linux sessions?*
    2. SSH terminal type*
6. At the  section, if necessary, change the fields below:
    1. Ignore certificate errors?*
    2. Enable RAIL over RDP?*
    3. Enable wallpaper in RDP sessions?*
    4. Include hostname in local login in RDP sessions?*
7. At the  section, if necessary, change the fields below:
    1. Indexing session texts?*
    2. Enable input text index import?*
    3. Enable output text index import?*
    4. Enable user input recording?*
    5. Enable session recording?*
    6. Enable RemoteApp in session?*
    7. Enable session purge?*
    8. Days for purge*
    9. Number of simultaneous user sessions (zero indicates unlimited)*
    10. Web session image quality*
    11. Number of video frames (fps)*
    12. Keyboard Layout*
    13. Web session image type*
    14. Enable livestream in real time?*
    15. Session text language (OCR)*
    16. Enable approval for session videos?*
    17. Enable the download of the session video?*
    :::(warning) ()
    After selecting the  and  in the RDP session through Web Proxy on Windows devices, make the adjustment inside the session at the Windows settings to the same keyboard and language selected at the parametrization.
    :::
8. In the lower right corner, click .

After saving, a confirmation notice will be displayed and your remote session will be configured and ready to use.

***
### Next:




Do you still have questions? Reach out to the .