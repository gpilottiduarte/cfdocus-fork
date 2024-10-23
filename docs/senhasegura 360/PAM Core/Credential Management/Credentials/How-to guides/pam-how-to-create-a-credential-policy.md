## Metadata_Start 
## code: en
## title: How to create a credential policy 
## slug: pam-how-to-create-a-credential-policy 
## seoTitle: How to create a credential policy 
## description:  
## contentType: Markdown 
## Metadata_End
A credential policy is a set of rules that regulate how an organization manages user authentication credentials. These policies should specify rules for password complexity, expiration, and storage, among other aspects, ensuring that user credentials are robust, secure, and updated frequently, thus reducing the risk of unauthorized access to the system.

## How to create a credential policy in senhasegura

1. In the top left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. Click the View actions icon, represented by the three vertical dots, and select .

A pop-up window called  will open. Fill in the fields accordingly:

1. : a name that will identify the credential policy on the platform.
2. : select  to keep the policy active on the platform.
3. On the  tab:
    1. : in the drop-down menu, select the password strength criteria you want. You can register the criteria for .
    2. : defines the priority for applying the policy if senhasegura finds more than one policy that applies to the credential. The higher the priority, the higher the number in this field.
    3. : the password can be viewed simultaneously. Regardless of which user has custody of the password, all others belonging to this policy can view the password.
    4. : enabling this option allows users to perform proxy sessions simultaneously with the same credential. With this option disabled, only one session will be allowed at a time.
    5. : the interval in which senhasegura will automatically change the password after a user has viewed it. In the first field, enter a number; in the second field, enter the unit (Months, Days, Hours, or Minutes).
    6.  defines the maximum period of validity for a password, starting from the last time it was changed. After the defined period, the password will expire automatically, regardless of frequency of use, including logins and remote sessions. The user will be required to choose a new password to continue accessing the system. Example: If you set this field to *3 Months*, the user's password will expire 3 months after the last password change, even if they use it regularly for any type of access, including remote sessions. In the first field, enter a number; in the second field, enter the unit (*Months, Days, Hours, or Minutes*).
    7. : establishes how long credentials from the same policy receive the same password. The count starts when the first password change for a credential occurs in that policy. For example, if the field has a time limit of five hours, all the other credentials that carry out change executions within this period will receive the same password. In the first field, enter a number; in the second field, enter the unit (*Months, Days, Hours, or Minutes*).

:::(Error) (Important)
* When the  option is enabled, and a user withdraws the password, which will cause the password to remain in their custody, another user will still be able to withdraw the password.
* When the  option is enabled, and a user withdraws the password, which will cause the password to remain in their custody, another user will not be able to withdraw the password.
:::

:::(Info) (Info)
If you set the password strength to "High," the system will automatically block the options for passwords to be reused.
:::

4. In the  section, select the  checkbox if you want the password to expire on any day of the week. If not, select the checkbox for the days you want the passwords to expire. Remember that some credentials can’t be recycled daily, either because of the target device's security policies or because of any impacts it may have on the business.
5. In the  section:
    1. : click on the  button, represented by the plus sign, to add expiration criteria per appointment time. When you click on the button, a drop-down menu will appear. To add an hour, select the desired time from the drop-down menu. If you want to delete it, click the trash can icon next to the time field.
    2. : click on the  button, represented by the plus sign, to add expiration criteria by lapse time. To add a time, select the time you want from the drop-down menu. If you want to delete it, click the trash can icon next to the time field.
6. In the  tab:
    1. : indicate which devices will be affected by this policy.
    2. : indicate which device models will be affected by this policy.
    3. : indicate relevant information about the policy.
    4. : indicate which device tags are affected.
    5.  indicate which credential tags are affected.
    6. In the  section, indicate which sites will be affected by the policy. Check  to apply the policy to all registered sites.
    7. In the  section, indicate which devices will be affected by the policy. Check  to apply the policy to all registered devices.
    8. In the  section, indicate which credential types will be affected by the policy. Check  to apply the policy to all registered credentials.

:::(Error) (Important)
Changing the criteria is impossible once the policy has been saved.
:::

7. Click .

:::(Warning) (Warning)
The above fields determine actions that influence the client's business rules or the target device's security rules. Configuration errors in these fields can lead to the credential becoming unavailable.
:::

## How to edit a credential policy

1. In the top left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. On the list screen, identify the policy you want to edit and click  in the  column, identified by the paper and pencil icon.
4. Edit the credential policy options according to the form described in the section .
5. Click .

---

Do you still have questions? Reach out to the .