## Metadata_Start 
## code: en
## title: Reference for application 
## slug: reference-for-applications 
## seoTitle: Reference for applications 
## description:  
## contentType: Markdown 
## Metadata_End
Access the secrets list report through the .

On the  screen, you will find the following information:

## Top bar

| Item                   | Description                                                                                          |
| ---------------------- | ---------------------------------------------------------------------------------------------------- |
|  | Represented by the magnifying glass icon, it hides or shows the filter options.                      |
|        | Represented by the counterclockwise arrow icon, it updates the information on the screen.            |
|  | Represented by the three vertical dots, it opens a drop-down menu with the options for . |
|           | Opens the registration window for a new application.                                                          |
|       | Identified by the printer icon. It opens a new page for printing the report.                         |
|         | Identified by the sheet of paper icon, downloads the report.                                         |
|    | Identified by the clock icon, it opens the window for scheduling the report.                          |

When you click on , a series of fields are displayed. These are used to refine your search results by:

| Item                            | Description                                                                                                                                                  |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|                     | Application code on senhasegura.                                                                                                                             |
|                   | Application name.                                                                                                                                            |
|                | Application system.                                                                                                                                          |
|           | Application environment.                                                                                                                                     |
|      | Drop-down menu with lines of business options, as registered in the DSM.                                                                                     |
|      | Drop-down menu with application types as registered in the DSM.                                                                                              |
|                   | Tags inserted into the application at the time of registration.                                                                                              |
|                | Drop-down menu with the options for the status of the application. The available options are:  or .                                  |
|  | Drop-down menu with the authentication methods available on senhasegura. The available options are: *No authentication, OAuth 1.0, OAuth 2.0*, and *AWS*. |
|                | Drop-down menu with the status of the application in senhasegura.The available options are:  or .                                             |
|             | Opens a calendar for you to choose the creation date. This will indicate that all applications created from this date will be filtered out.                  |
|                  | Opens a calendar for you to choose an end date for the filter. This will indicate that all applications created up to this date will be filtered.            |

In addition to these options, you have two buttons: , which applies the parameters passed in the fields; and , which clears all the parameters.

In the list of secrets, you still have the following fields:

* : description of the application.
* Action : displays the options *to view this application's authorizations, change this application*, and *view this application*.

## Application Configuration window

The  window will be shown whenever you register or change an application. It contains the following fields:

### Settings tab

| Item                            | Description                                                                                                                               |
| ------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
|       | Text field for entering a name to identify your application.                                                                              |
|  | Drop-down menu with possible authentication methods. The available options are: *No authentication, OAuth 1.0, OAuth 2.0,* or *AWS*. |
|       | Drop-down menu with the lines of business available for the application. You can register your own lines of business.                     |
|       | Drop-down menu with the application types available for the application. You can register your own application types.                     |
|                | Status selector for creating or modifying the application. The available options are:  or .                       |
|                   | Text field for inserting tags. Helps organize and filter applications.                                                                    |
|            | Text field for entering the application description.                                                                                      |
|        | Used when the authentication method is AWS. Enter the ARN of the AWS credential here.                                                     |

### Automatic provisioning tab

| Item                                    | Description                                                                                                                            |
| --------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| Automatic provisioning of secrets       | Indicates the status of automatic provisioning. The available options are:  or .                       |
| Cloud dynamic  provisioning profile     | It indicates which cloud profiles can be used in the application. Only available if automatic provisioning is set to   |
| Credential dynamic provisioning profile | It indicates which credential profiles can be used in the application. Only available if automatic provisioning is set to . |