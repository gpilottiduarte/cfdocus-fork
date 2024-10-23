## Metadata_Start 
## code: en
## title: How to deactivate the restriction rule by credential and devices 
## slug: pam-session-how-to-deactivate-the-restriction-rule-by-credential-and-devices 
## seoTitle: How to deactivate the restriction rule by credential and devices 
## description:  
## contentType: Markdown 
## Metadata_End
On senhasegura, the standard configuration at the access control is when a user is part of more than one access group with different rules, and this group will follow the restriction rule by credential and device combined.

For example, if the ABC credential is in two or more groups with different access rules when the credential tries to access or view a password in some device, senhasegura will look through all the groups that the ABC credential is part of and read not only the credential rule but the device rule as well, to allow the access.

To deactivate this standard rule and change the configuration to the most restrictive access group rule only by credential, follow the steps in this document.

:::(info) ()
For more information about the meaning of the Access control configurations fields, access the  document.
:::

## Requirements

* Be an admin user.
---

## Deactivate standard rule

1. On senhasegura, in the upper-left corner, click , identified by the nine squares icon, and then select .
2. In the side menu, select  >  .
3. In the available tabs, select .
4. On the *, select .
5. Click .

A confirmation notice will be displayed. Now, senhasegura will restrict the access for the user added in more than one group, according to the most restrict group’s rule, validating only the credentials rule.

---

### Use case: senhasegura restriction rule

#### senhasegura standard
: Yes
: Test
Groups that  credential is part of:

* : access to device 1 with no justification.
* : access to device 2 with justification.
* : access to device 3 with justification and approval.

By the senhasegura standard rule, when accessing a device, the rule that will be applied is the one established on the  and on the access device. In other words, when the credential tries to access , it won’t request a justification since this is the rule from the  to which this device belongs.

#### Changed standard
: No
: Test
Groups that  credential is part of:

* : access to device 1 with no justification.
* : access to device 2 with justification.
* : access to device 3 with justification and approval.

When the standard rule is modified, the  field is set as . When the user tries to access , he must enter a justification and wait for approval to access the device since the rule that is now being applied is the  rule, regardless of the device that is being accessed, because the most restrictive one that is being considered, and now only the rule applied on the credential is valid.

---
## Next:


Do you still have questions? Reach out to the .