## Metadata_Start 
## code: en
## title: RADIUS server 
## slug: radius-server 
## seoTitle: RADIUS server 
## description:  
## contentType: Markdown 
## Metadata_End
This document provides a general overview for the RADIUS server functionality.

## Path to access

1. On senhasegura, in the upper left corner, click on , represented by the nine squares, and select .
2. In the side menu, select .

## Top bar

| Item                 | Description                                                                                                                                                                                          |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|     | Represented by the magnifying glass icon, it displays or hides the search fields on the screen.                                                                                                      |
|           | Represented by the counterclockwise arrow icon, it refreshes the page.                                                                                                                               |
|     | Represented by the three vertical dots icon, it shows all the possible actions for the report.                                                                                                       |
|              | Represented by the plus icon, it opens the screen.                                                                                                                            |
|     | Represented by the printer icon, it opens a new page for printing the report.                                                                                                                        |
|       | Represented by the paper sheet icon, it downloads the report.                                                                                                                                        |
|  | Represented by the clock icon, it opens the  form. |

## Search fields

| Item               | Description                                                                             |
| ------------------ | --------------------------------------------------------------------------------------- |
|        | Filter by the server's senhasegura registration code.                                   |
|  | Filter by server hostname.                                                              |
|      | Filter by the server's listening port.                                                  |
|   | Filters according to the server's status in senhasegura. It can be  or . |

## Report fields

The results are displayed in a list, as shown below:

* .
* .
* .
* : system timeout time. Shown in seconds.
* s: maximum number of login attempts on the RADIUS server.
* In the  column, you have two options:
  * : represented by the pencil and paper icon, opens the  window in edit mode.
  * : accessible by clicking on the three vertical dots icon and selecting the  option. This opens the  window.

## RADIUS Server window

The  window can be accessed in two ways:

1. To register a new server.
2. To change a server

In both cases, the fields are as follows:

| Item                   | Description                                                                                                                                                                                                                       |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|      | Text field for entering the IP address or hostname of the server.                                                                                                                                                                 |
|          | Text field to enter the port where the server listens.                                                                                                                                                                            |
|       | Radio button for selecting the server status. It can be  or .                                                                                                                                                      |
|    | The server's secret key. Note that if you don't change the secret key, the current value of the field will be kept.                                                                                                               |
|    | Text field for entering the server timeout time.                                                                                                                                                                                  |
|  | Text field for entering the maximum number of login attempts that senhasegura will make on the RADIUS server.                                                                                                                     |
|      | The button is in the bottom-left corner of the window. Hovering over it displays information about editing and accessing the server.  that this button is only available when the window is open in edit mode. |

## RADIUS authentication test window

| Item          | Description                                                           |
| ------------- | --------------------------------------------------------------------- |
|    | Label indicating the IP address or hostname of the server and port.   |
|  | Text field for entering the username used in the authentication test. |