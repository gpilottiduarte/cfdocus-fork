## Metadata_Start 
## code: en
## title: How to integrate DSM with Kubernetes 
## slug: how-to-integrate-dsm-with-kubernetes 
## seoTitle: How to integrate DSM with Kubernetes 
## description:  
## contentType: Markdown 
## Metadata_End
## Requirements:

1. You should have Kubernetes properly installed.
2. You should have the  tool installed.

:::(info) (Info)
- Follow the installation steps provided in the  documentation.
- Follow the creation and configuration steps specified in the  provider documentation.
:::

## Configuration in the senhasegura

1. Create an  in the DSM.
2. Create a  in senhasegura.
3. Create an  in senhasegura.
4. Create an  for the newly created application.
5. Add the  to the .
6. Copy the values of the  and  fields from the application's authorization.
7. Create a file with the  extension in Kubernetes.
8. Fill in the  file with the  and  values you copied earlier.
9. Execute the following command: 

In Kubernetes, follow the steps in the senhasegura documentation on External Secrets, available at .

By following these steps, the integration between DSM and Kubernetes via External Secrets will be configured, guaranteeing secure and effective management of the sensitive information needed to operate your environment

## Validate the integration


| Command | Description |
| --- | --- |
|  | Check the synchronization status. |
|  | Check the synchronization status. |
|  | Check the Pod creation. |
|  | Check the External Secrets contents. |
|  | Check if the synchronized secret has been created and that the data has been retrieved. |
|  | Check the External Secrets logs. |

---

Do you still have questions? Reach out to the .