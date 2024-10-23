## Metadata_Start 
## code: en
## title: Reference for API Logs 
## slug: dsm-reference-for-api-logs 
## seoTitle: Reference for API Logs 
## description:  
## contentType: Markdown 
## Metadata_End
On the senhasegura DevOps Secret Manager, you can consult the logs of the operations that took place via the DSM API through the API Logs report. Access it through .

## Top bar

| Item                      | Description                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------- |
|     | Represented by the magnifying glass icon. Displays or hides the search fields on the screen. |
|           | Represented by the counterclockwise arrow icon. Refreshes the page.                          |
|     | Represented by the three vertical dots icon. Displays the possible actions for the page.     |
|     | Represented by the printer icon. It opens a new page for printing the report.                |
|       | Represented by the sheet of paper icon, downloads the report.                                |
|  | Represented by the clock icon, it opens the window for scheduling the report.                |

When you click , a range of fields is displayed. These are used to refine your search results. They are:

| Field                    | Description                                                                                                                                                                                          |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|           | Drop-down menu. Shows the possible event options for the DSM API. These are: *Update, Create, Delete,* and *Read.*                                                                                  |
|        | HTTP code of the response obtained from the request.                                                                                                                                                 |
|     | Type of entity passed to the API request. For example:                                                                                                                              |
|       | Entity code in senhasegura.                                                                                                                                                                          |
|     | Entity name. In this case, it will be the name of the request registered with senhasegura.                                                                                                           |
|  | Application code. In this case, it will be the application code used in the request to the DSM API.                                                                                                  |
|     | Application's name.                                                                                                                                                                                  |
|   | Requisition authorization code. For example:.                                                                                                                      |
|              | IP address from which the request was made.                                                                                                                                                          |
|                       | Date and time the request was made. There are two separate drop-down menus, the first to open the calendar and choose the day and the second with the hour and minute intervals you can choose from. |

In addition to these options, you have two buttons: , which applies the parameters passed into the fields, and , which clears all the parameters.

The report is shown below, in list format, containing the following fields:

* .
* .
* 
* 
* 
* 
* .
* .
* .
* : IP address of the server that received the request.
* : date and time of the request, displayed in the  format.