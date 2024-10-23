## Metadata_Start 
## code: en
## title: About Related Users 
## slug: about-related-users 
## seoTitle: About Related Users 
## description:  
## contentType: Markdown 
## Metadata_End
The Related Users function in senhasegura allows associating a single system user with multiple credential usernames used across various devices. This is done through the use of the  mask in access group criteria.

## 

Let's use the example of a user named . In senhasegura, her username is . However, in the company, Alice uses the username  to access device A and  to access device B.

### 

In a conventional scenario, when using the \[\#USERNAME\#\] mask in an access group, the associated credentials are those that strictly correspond to the username in senhasegura, which, in Alice's case, is . This means that, without additional adjustments, only the credentials linked to  would be accessible through this group.

### 

With the  functionality, it's possible to extend Alice's access to other usernames associated with her. By configuring  as a  for Alice, the use of the  mask in an access group can then include credentials associated with both  (the default name) and  (the related name).

This functionality ensures greater flexibility and efficiency in managing user access to various devices, simplifying the authentication process without compromising security.

---

Do you still have questions? Reach out to the .