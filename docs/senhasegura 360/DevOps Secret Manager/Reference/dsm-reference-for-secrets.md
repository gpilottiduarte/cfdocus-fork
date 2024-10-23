## Metadata_Start 
## code: en
## title: Reference for secrets 
## slug: dsm-reference-for-secrets 
## seoTitle: Reference for secrets 
## description:  
## contentType: Markdown 
## Metadata_End
You can access the secrets list report through .

:::(warning) (Caution)
To view secrets, you need to be part of an access group with permission to manage secrets; otherwise, if you register a secret, you won't be able to view it in the filters and dashboards.
:::

On the screen, you'll find the following information:

## Top bar

| Item                      | Description                                                                           |
| ------------------------- | ------------------------------------------------------------------------------------- |
|     | Represented by the magnifying glass button, it hides or shows the filter options.     |
|           | Represented by the counterclockwise arrow, it updates the information on the screen.  |
|     | Represented by the three vertical dots, it opens a drop-down menu with three options. |
|       | Open the window to register a new secret                                              |
|     | Identified by the printer icon. It opens a new page for printing the report.          |
|       | Identified by the sheet of paper icon, downloads the report.                          |
|  | Identified by the clock icon, it opens the window for scheduling the report.           |

When you click on , a series of fields are displayed. These are used to refine your search results. They are:

| Item                      | Description                                                                                                                                              |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
|             | Name of the registered secret.                                                                                                                           |
|           | A drop-down menu with the option to filter the results according to the Engine used in the secret. The options are *Ansible, Generic, GitLab*, and *Kubernets*. |
|      | A drop-down menu with the environments registered on senhasegura.                                                                                        |
|          | A drop-down menu with  and  options. Indicates the status of the secret in senhasegura.                                                                 |
|            | A drop-down menu with the options  and . Indicates whether or not the secret contains any errors.                                                   |
|         | Name of the identity registered with senhasegura.                                                                                                        |
|          | Option to filter according to a specific version of a secret. If left blank, the newest version is displayed.                                            |
|  | Opens a calendar to choose the start date of the interval that will be used for the filter by the secret expiration date.                                |
|            | Opens a calendar to choose the end date of the interval that will be used for the filter by the secret expiration date                                   |

In addition to these options, you have two buttons: , which applies the parameters passed into the fields, and , which clears all the parameters.

In the  list, you have the following extra fields:

* : code used to register the secret with senhasegura.
* : tags registered for the secret.
* In the  column you have the three vertical points options with the  options.