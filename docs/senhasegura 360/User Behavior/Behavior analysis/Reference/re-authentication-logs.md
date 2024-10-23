## Metadata_Start 
## code: en
## title: Re-authentication logs 
## slug: re-authentication-logs 
## seoTitle: Re-authentication logs 
## description:  
## contentType: Markdown 
## Metadata_End
In this document, you’ll find detailed information about the ’s  screen, which allows the administrator to view a report of all identity verification events triggered in senhasegura.

## Requirements

- Administrator permission.
-  feature configured. Access the document on  for more information.

## Path to access

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .
2. In the side menu, select .

---

## Top bar

|       |                                                                        |
|---------------|---------------------------------------------------------------------------------------|
|  | Represented by the magnifying glass icon, it displays or hides the search fields on the screen. |
|     | Represented by the counterclockwise arrow icon, it refreshes the page.                |
|  | Represented by the three vertical dots icon, it displays a drop-down menu with possible actions for the report. |
|  | Represented by the paper sheet icon, it downloads the report.                           |
|  | Represented by the clock icon, it opens the  screen.                  |

## Search fields

|     |                                                                                                                                       |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|       | Text field that filters re-authentication events by their unique identification code.                                                            |
|  | Text field that filters re-authentication events by the trigger that initiated them. Available options are View attempts at prohibited times, Blocked commands, Session attempts at prohibited times, High-risk sessions, Rating drop, and Token TOTP. Clear the field to enable the All option.   events marked with TOTP token are related to TOTP token requests at login. |
|     | Text field that filters re-authentication events by the user who re-authenticated.                                                                 |
|     | Field that filters re-authentication events by the period in which they occurred. Format . Use this field to enter the start date of the period. The downward arrow opens a calendar. If the  field is enabled, use it to enter the start time of the interval.  |
|    | Field that filters re-authentication events by the period in which they occurred. Format . Use this field to enter the final date of the period. The downward arrow opens a calendar. If the  field is enabled, use it to enter the end time of the interval. |
|   | Drop-down menu that filters re-authentication events by their status. Available options are Success and Failure. Clear the field to enable the  option. |

## Report fields

- .
- .
- .
- .
- .
-  in this column, you can access:
  -  represented by the key icon, it opens the  screen that displays a report of the selected re-authentication event.

## Details screen

In this section, you’ll find all the information about the  screen, which displays a report of the selected re-authentication event.

|           |                                                                                   |
|-------------------|--------------------------------------------------------------------------------------------------|
|       | Field that displays the senhasegura username associated with the re-authentication.            |
|         | Field that displays the status of the re-authentication. Possible options are  and . |
|        | Field that displays the trigger that initiated the re-authentication. Possible options are *View attempts at prohibited time, Blocked commands, Session attempts at prohibited time, High-risk sessions, Rating drop*, and *Token TOTP*.   TOTP token-related events display records of login attempts using a TOTP token. |
|           | Field that displays the date and time when the re-authentication was triggered.                   |
|  | Field that displays the method used in the re-authentication.                                   |
|        | Field that displays the browser used at the time of re-authentication.                          |
|             | Field that displays the IP address of the device where the re-authentication was performed.     |
|       | Field that displays the geographic location of the device.                                      |

## Details section

In this section of the  screen, you'll find all the information about the trigger that initiated the re-authentication.

### Rating drop

When the trigger that initiates re-authentication is related to a rating drop, the following information about the events that caused the rating drop is displayed:


 
 * : the event that caused the rating drop.                           
 * : the date and time of the event.                                                                  
 *  : the score lost by the user due to the event.                                                 
 * : in this column, you can access:
     *  represented by the key icon, it opens the  screen.
     *  represented by the play icon, it opens the  screen.

### High-Risk Sessions

When the trigger that initiates re-authentication is related to a high-risk session, the following information about the sessions is displayed:


- : the credential used during the session.
- : the device used during the session.
- : the protocol used during the session.
- : the type of proxy session.
- : the unique identification code of the session.
- : the start time of the session.
- : the end time of the session.
- : the duration of the session.
- :  in this column, you can access:
  - : represented by the play icon, opens the  screen.
  - : represented by the magnifying glass icon, opens the Session logs screen.
  - : represented by the key icon, opens the  screen.
  - : represented by the paper icon, opens the  screen.

### Blocked commands

When the trigger that initiates re-authentication is related to blocked commands, the following information about the commands is displayed:


Here is the information formatted as a list:

- : the command executed during the session.
- : the criticality level of the session.
- : the action performed during the session.
- : the type of session.
- : the credential used during the session.
- : the device used during the session.
- : the unique identification code of the session.
- : the start time of the session.
- : the end time of the session.
- : the duration of the session.
- : in this column, you can access
  - : represented by the play icon, it opens the  screen.
  - : represented by the pencil and paper icon, it opens the  screen.
  - : represented by the magnifying glass icon, it opens the  screen.
  - : represented by the key icon, it opens the  screen.
  - : represented by the paper icon, it opens the  screen.

### Session attempts at prohibited times

When the trigger that initiates re-authentication is related to access attempts during prohibited hours, the following information about the access attempts is displayed:


- : the credential used during the access attempt.
- : the device used during the access attempt.
- : the day of the week when the access attempt occurred.
- : the date of the access attempt.
- : the time of the access attempt.

### View atempts at prohibited times

When the trigger that initiates re-authentication is related to password viewing attempts during prohibited hours, the following information about the attempts is displayed:

Here is the information formatted as a list with the specified configuration:

- : the credential used during the viewing attempt.
- : the device used during the viewing attempt.
- : the day of the week when the viewing attempt occurred.
- : the date of the viewing attempt.
- : the time of the viewing attempt.

