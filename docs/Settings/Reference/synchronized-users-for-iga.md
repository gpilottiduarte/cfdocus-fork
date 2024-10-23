## Metadata_Start 
## code: en
## title: Synchronized users for IGA 
## slug: synchronized-users-for-iga 
## seoTitle: Synchronized users for IGA 
## description:  
## contentType: Markdown 
## Metadata_End
This document provides a general overview of the  functionality.

## Path to access

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .
2. On the side menu, select .

## Top bar

| Item              | Description                                                                                     |
| ----------------- | ----------------------------------------------------------------------------------------------- |
|  | Represented by the magnifying glass icon, it displays or hides the search fields on the screen. |
|        | Represented by the counterclockwise arrow icon, it refreshes the page.                          |
|  | Represented by the three vertical dots icon, it shows all the possible actions for the report.  |
|  | Represented by the printer icon, it opens a new page for printing the report.                   |
|    | Represented by the paper sheet icon, it downloads the report.                                   |

## Search fields

| Item                       | Description                                                                                                                                                                                                           |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|                     | User registration code in senhasegura.                                                                                                                                                                                |
|               | Name of the user.                                                                                                                                                                                                     |
|                   | UUID, Universally Unique Identifier, of the user.                                                                                                                                                                     |
|  | User identification in senhasegura.                                                                                                                                                                                   |
|             | Drop-down menu with the options , which displays all user records; , which displays only synchronized user records and , which displays user records that are not synchronized. |
|   | Calendar to display the date of the last synchronization. This field serves as the start date for the user synchronization filter.                                                                                    |
|                  | This field serves as the end date for the user synchronization filter.                                                                                                                                                |

## Report fields

* .
* .
* .
* 
* 
* 
* In the  column, you can view the synchronization details. To do this, click , represented by the magnifying glass icon.

## SCIM synchronization details window

When you click to view the synchronization details, the  window will open. It contains the following fields:

| Item              | Description                  |
| ----------------- | ---------------------------- |
|  | Details of the SCIM request. |

The synchronization details will be shown in plain text below the  label. They will be shown similarly to the example below

### SCIM Request example

`yaml
{
"schemas":
	[ 
"urn: ietf: params: schemas: core: 2.0: User" 
],
"userName: "romi_w\u00e1",
"name": {
		"formatted": "Romi W\u00e1,
		"familyName": "W\e001~,
		"givenName": "Romi",
	} 
"emails": [
		{ 
			"value": "romi_w\u001e1@example.com",
			"type": "work",
			"primary": true
		}
	    ]
}
`