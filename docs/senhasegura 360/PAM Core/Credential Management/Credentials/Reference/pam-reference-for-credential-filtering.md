## Metadata_Start 
## code: en
## title: Reference for credential filtering 
## slug: pam-reference-for-credential-filtering 
## seoTitle: Reference for credential filtering 
## description:  
## contentType: Markdown 
## Metadata_End
To access the credentials report, access 

## Top bar

| Item                      | Description                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------- |
|     | Represented by the magnifying glass icon. Displays or hides the search fields on the screen. |
|           | Represented by the counterclockwise arrow icon. Refreshes the page.                          |
|     | Represented by the three vertical dots icon. Displays the possible actions for the page.     |
|              | Represented by the sum icon, it opens the credential registration form.                      |
|     | Represented by the printer icon. It opens a new page for printing the report.                |
|       | Represented by the sheet of paper icon, it downloads the report.                             |
|  | Represented by the clock icon. It opens the window for scheduling the report.                |

When you click on , a series of fields are displayed. These are used to refine your search results. They are:

| Item                             | Description                                                                                                                                  |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
|                      | Filter by the credential's registration code in senhasegura.                                                                                 |
|                  | Filters by the device registered with senhasegura to which the credential is linked.                                                         |
|                | Filters by the name of the user registered with senhasegura.                                                                                 |
|         | Drop-down menu. Filter by credential type. The options are:*Domain Admin, Domain User, Local Administrator, Local User, and SSH Ke*y.      |
|            | Drop-down menu. Filters by taking into account whether the credential has JIT access enabled. It can beYesorNo.                              |
|  | Filters for additional information that has been registered with the credential.                                                             |
|             | Drop-down menu. Filter according to device type.                                                                                             |
|                 | Filters according to the device model to which the credential is linked.                                                                     |
|                  | Drop-down menu. Filter by the vendor of the device to which the credential is linked.                                                        |
|                  | Drop-down menu. Filter by credential domain.                                                                                                 |
|                    | Drop-down menu. Filter by the site that is registered with senhasegura.                                                                      |
|            | Drop-down menu. Filter according to the connectivity protocol the credential has.                                                            |
|         | Filters according to the tags that are linked to the credential.                                                                             |
|             | Filters are made according to the tags linked to the device.                                                                                 |
|              | Text field. Filters according to the Password ID for access via webservice.                                                                  |
|                  | Drop-down menu. Filter by the status of the credential in senhasegura. It can be  or .                     |
|                | It opens a calendar for you to choose the last date the credential was used. This date will serve as the start date for the filter interval. |
|                   | It opens a calendar for you to choose the last date the credential was used. This date will serve as the end date of the filter range.       |
|           | Drop-down menu. Filters according to the status of the credential's Password field. It can be or .                  |

In addition to these options, you have two buttons: , which applies the parameters passed into the fields, and , which clears all the parameters.

Below is a list of all the credentials and devices that meet the filtering criteria. The results are grouped by device and presented as follows:

* : indicates the device's name in senhasegura followed by the IP address or hostname, where applicable.
  * For example: .
  * The device name is followed by some information about the device, in order: 
    * For example: .

:::(info) (Info)
Note that the device name is clickable. Clicking on the device name will take you to the  window. For more information on this window, see the reference on devices or the document on how to add a device to senhasegura.
:::

Thus, within each section grouped by device, you have information on the credentials linked to the device that match the filtering criteria applied. The credential fields are presented as follows:

* .
* .
* 
* .
* : refers to additional information. This field is filled in when registering a new credential, specifically in the  field of the credential registration form.
* .
* .
*  refers to the last credential query.
* 
* In the  column, you have three options:
  * : represented by the computer icon, starts the session on the indicated device with the indicated credential.
  * : opens the Secure credential password display and transfer form.
  *  opens a drop-down menu with the possible actions for the credential. They are:
    * .
    * .
    * .
    * .
    * .
    * .