## Metadata_Start 
## code: en
## title: File transfer through senhasegura Windows web proxy session error 
## slug: pam-core-ts-file-transfer-windows-session-error-1 
## seoTitle: File transfer through senhasegura Windows session error 
## description:  
## contentType: Markdown 
## Metadata_End
This document will guide you through a step-by-step on how to fix the possible error with file transfer on the Windows web proxy remote session.

## Scenario
senhasegura couldn’t map a remote drive, used by senhasegura on remote Windows web proxy session, to transfer files.

***
## Cause
The remote drive it’s not visible in Explorer due to misled configurations in Windows.

***
## Solutions
To solve this problem the configurations must be done in two steps. First, in a remote session into a Windows device through senhasegura, and second at the senhasegura platform.

#### Windows web proxy remote session

1. At Windows search bar type: .
2. Click on the correspondent option.
3. At  select  >  >  >  > .
4. Double-click on  item, and select .
5. Click on .
6. Click .
7. Close this window.
8. At Windows search bar type: 
9. Select  >  >  >  >  > .
10. Double-click  on  item, and in  type  (zero). 
1. Click .
2. Reboot the computer.
3. At  >  confirms if the remote disk was mapped (commonly it will be indicated by the letter G:).

:::(warning) ()
If your computer is already using the letter G for another disk, it’ll give the remote disk a different letter. You must make this change on the senhasegura platform as well.
:::

#### At senhasegura platform

1. On senhasegura, in the upper left corner click the  and select .
2. In the side menu, select  > . 
3. At the  tab:
    1. *: Select .
    2. *: Select  or the letter that represents the remote disc.

***
Do you still have questions? Reach out to the .