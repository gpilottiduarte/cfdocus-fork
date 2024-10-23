## Metadata_Start 
## code: en
## title: How to perform a batch import 
## slug: pam-devices-batch-import 
## seoTitle: Batch import 
## description:  
## contentType: Markdown 
## Metadata_End
## How to create the import

:::(warning) (Warning)
Read the instructions on how to fill in the fields in the spreadsheet.
The instructions can be found in the template file.
.
:::

:::(error) (Important)
It's important to note that when importing credentials to Microsoft Excel, it interprets the semicolon (;) character as a separator. Due to technical reasons related to Excel's architecture, the import spreadsheet will disregard the semicolon character and carry out the import process without errors. Therefore, you should avoid using semicolons in your credentials when importing via spreadsheet. However, if you register your credentials directly on the platform, you can use semicolons without issues.
:::

To upload the import file, follow these steps:

1. On the senhasegura platform, in the top upper left corner, click , represented by the nine squares, and select .
2. On the side menu, select .
3. On the top bar, click on , represented by the three vertical dots, and select the option .
4. On the pop-up window, click on , and select the desired file.
5. Click on .

## About the file processing trace

To verify the report upload, go to 

Files still being processed will be in a waiting state, once the processing is finished, the status will change to .

If the import is invalidated by an error, the record will turn red, and the  column will be marked .

:::(Info) (Info)
Check the processing details using the registration action .
:::

On the import details screen, download the information generated in operation. This file will have the line in which the detail occurred, the type of alert, and the description of the action taken by senhasegura.

It is important to mention that even if a file ends with an error, this does not mean that devices and credentials were not created or changed during the process. Therefore, correct the information indicated by senhasegura and continue importing the spreadsheet until the desired result has been achieved.

:::(Info) (Info)
The batch device import worksheet by default for other languages is in English.
:::

***

## Next
1. .
2. .
3. .
4. .

***

Do you still have questions? Reach out to the .