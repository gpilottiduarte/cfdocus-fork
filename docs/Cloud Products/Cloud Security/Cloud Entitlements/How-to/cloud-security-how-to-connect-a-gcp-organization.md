## Metadata_Start 
## code: en
## title: How to connect a Google Cloud Platform organization 
## slug: cloud-security-how-to-connect-a-gcp-organization 
## seoTitle: How to connect a Google Cloud Platform organization 
## description: In this article, you’ll learn how to connect a Google Cloud Platform (GCP) organization, including all its projects, to Cloud Entitlements. 
## contentType: Markdown 
## Metadata_End
In this article, you’ll learn how to connect a Google Cloud Platform (GCP) organization, including all its projects, to .

## Requirements

- A GCP organization.
- A  with the following roles:
    - 
    - 
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

## Setup a service account with organization-level permissions in Google Cloud Platform

Before you connect your organization to , you must create a service account with organization-level permissions. To do so, follow the steps:

1. Access the .
2. Click the  and switch to your .
3. Go to .
4. Click  with the required permissions.
5. Click .
6. Navigate to .
7. In , click  to add a service account as a principal.

:::(Info) (Info)
As an organization, you can select from service accounts created within projects. If needed, you can create a new service account in  > .
:::

8. Paste the  and select the .
9. Click .
10. Go to  and select the service account selected as a principal.
11. Click  > .
12. Create and download the new key in .

## Connect a Google Cloud Platform organization

To connect your GCP organization to , follow these steps:

1. Go to  left menu.
2. Click  to open a dropdown menu.
3. Select .
4. On the upper-right corner, click .
5. Select the option .
6. Enter a  to identify your GCP organization within .
7. Enter your .

:::(Info) (Info)
Your organization ID can be found in the GCP Console by clicking the  > .
:::

8. Upload the Service account key's .
9. Click .

If connected successfully, your GCP organization will appear in the list of connected organizations.

:::(Error) (Important)
If the connection is unsuccessful, review the organization ID, the attributed roles, and the enabled APIs. You can't connect an organization already connected to the same  tenant.
:::

To make any necessary changes, click the  button, represented by three vertical dots, and click .

Additionally, you can activate or deactivate the organization by turning the  on or off.