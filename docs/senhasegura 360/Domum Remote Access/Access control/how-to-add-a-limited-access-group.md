## Metadata_Start 
## code: en
## title: How to add a limited access group 
## slug: how-to-add-a-limited-access-group 
## seoTitle: How to add a limited access group 
## description:  
## contentType: Markdown 
## Metadata_End
In this document, you’ll find a step-by-step guide on how to register a limited access group in .

## 

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select    
2. In the side menu, select .  
3. In the report window, click the  menu, represented by the three vertical dots icon, and select .  
4. In the  window, fill in:  
   1. *: enter the access group name.  
   2. *: select the status of the group created. The options are  and   
   3.  enter a description for the created group.  
        ::: (warning) ()  
        These policies are applied at the moment of access request for limited users and they have no effect        after      the link is sent to the user. 
        :::

   4.  tab:  
      1. In , check the desired options:  
         1. Checkbox : allows users to view the password. Selecting this option will enable the  option.  
         2.  checkbox: this option will only be available if the  checkbox is marked. In such case, use the drop-down menus to define the number of , and the number of .  
         3.  checkbox: mark this checkbox to indicate that the approval for viewing a password is granted in levels. In the  tab, define the  hierarchy.

      2. In , check the desired options:  
         1. Checkbox : allows users to start a session. Selecting this option will enable the  option.  
         2. Checkbox : this option will only be available if the   checkbox is marked. If this option is enabled, you must define the number of approvals required to view the password in the  drop-down menu, and the number of disapprovals required to cancel the request in the  drop-down menu.  
         3.  checkbox: mark this checkbox to indicate that the approval for starting a session is granted in levels. In the  tab, define the approvers’ hierarchy.

      3. In , choose  or  for the following options:  
         1. *: requires the user to enter an ITSM code when providing a justification.  
         2. *: allows a limited user to request access.

        :::(info) (Info)  
      * Keep in mind your approval workflow before enabling this option.  
       * Limited Users can only request access to credentials they had previous access to.  
        * Limited Users need at least one active access to request new access.   
        :::

  5.  tab:  
     1. Click the  icon and select the users who will approve the password and session requests enabled in the  tab.  
     2. The added approvers will be listed in the table. If the  option is enabled, define the level for each approver in the  column.  
          
        :::(warning) ()   
        For an approver to access the approval workflow screen, they must have at least the PAM Operator profile.   
        

        

5. Click 

A confirmation message will be displayed, and the group will appear in the report list.   

Do you still have questions? Reach out to the .

