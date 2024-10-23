## Metadata_Start 
## code: en
## title: Session failed due to a website certificate error 
## slug: pam-session-session-failed-due-to-a-website-certificate-error-1 
## seoTitle: Session failed due to a website certificate error 
## description:  
## contentType: Markdown 
## Metadata_End
In this document, you’ll find a step-by-step guide on how to check the possible issue in a failed certificate session.

## Scenario

An error message will appear when starting an HTTPS session on a website.

---
## Cause

The website has an invalid certificate.

---
## Solution
To proceed with authentication, you’ll need to create a macro and associate it with all device-related credentials configured for the respective web application.

## Step 1 - Create the macro

1. On senhasegura, in the top left corner, click on the , represented by the nine squares, and select .
2. In the side menu, select  >  > .
3. In the upper right corner, click on  the three vertical dots icon and click .
4. In the  registration window, fill in the required fields.
    1. In the * field, choose the User simulation option.
    2. In the * field, configure the script action as shown below:
        1. wait: 15000
        2. kpress: tab
        3. wait: 500
        4. kpress: return
        5. wait: 500
        6. kpress: tab
        7. wait: 500
        8. kpress: tab
        9. wait: 500
        10. kpress: tab
        11. wait: 500
        12. kpress: tab
        13. wait: 500
        14. kpress: return
        15. wait: 1000
5. Click .

## Step 2 -Associate the created macro with a credential

1. In the side menu select  > .
2. In the list of available credentials, in the  column click on the three vertical dots icon, and select .
3. In the  registration window, click on the  tab.
    1. In the  section, click on the  icon on the  field.
    2. In the  drop-down menu, choose the macro created in the previous step.
    3. In the  drop-down menu, choose .
4. Click .

When returning to the credentials screen, click on the computer icon on the right side of the chosen credential to test if the macro was associated correctly.

---
Do you still have questions? Reach out to the .