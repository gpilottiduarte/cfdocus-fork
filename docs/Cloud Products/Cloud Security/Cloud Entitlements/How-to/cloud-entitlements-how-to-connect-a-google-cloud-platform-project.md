## Metadata_Start 
## code: en
## title: How to connect a Google Cloud Platform project 
## slug: cloud-entitlements-how-to-connect-a-google-cloud-platform-project 
## seoTitle: How to connect a Google Cloud Platform project 
## description:  
## contentType: Markdown 
## Metadata_End
In this article, you'll learn how to connect  to your Google Cloud Platform (GCP) projects.

## Requirements

- A  that contains the following roles:
    - 
    - 
    -  
    - 
    - 
    - 
    - 
- A  provisioned for the Service account.
- The following GCP APIs enabled:
    - Resource Manager.
    - Identity and Access Management (IAM).
    - Cloud Assets.

---

## Connect a Google Cloud Platform project

To connect your GCP project to , follow these steps:

1. Go to  left menu.
2. Click  to open a dropdown menu.
3. Select .
4. On the upper-right corner, click .
5. Select the option .
6. Enter a  to identify your GCP project within .
7. Enter your .
8. Upload the Service account key's .
9. If needed, attribute tags to the project. Separate each tag by pressing the  key.
10. Click .

If connected successfully, your GCP project will appear in the list of connected projects.

:::(Error) (Important)
If the connection is unsuccessful, review the project ID, the roles, and the enabled APIs. You can't use an ID from a project that is already connected to .
:::

To make any necessary changes, click the  button, represented by three vertical dots, and click .

Additionally, you can activate or deactivate the project by turning the  on or off.