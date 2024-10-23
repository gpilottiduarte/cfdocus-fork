## Metadata_Start 
## code: en
## title: How to manage secrets 
## slug: how-to-manage-secrets 
## seoTitle: How to manage secrets 
## description:  
## contentType: Markdown 
## Metadata_End
## Register a secret

To register a secret, follow the steps below:

1. On senhasegura, in the upper left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. In the top bar, click the  button, represented by the three vertical dots, and select  from the drop-down menu.

In the  window, fill in the details of your secret according to the instructions below:

### In the Settings tab:

1. : name of the secret for management within senhasegura.
2. : identifier of the secret. The applications can find the file or variable that will be created through this identifier.
3. : indicates whether the secret is available for application use. By default, it is set to .
4. : secret environment.
5. : engine to be used. The default engine is Generic.
6.  date: date on which the secret will be automatically inactivated.
7. : user-defined for data segregation and internal filters.
8. : description of the secret's use.

### In the Cloud credentials tab:

1. Click the button, represented by the plus icon next to the word , to add a cloud credential.
2. In the  modal, select the cloud credentials that will be part of the secret and click .

:::(info) (Info)
These credentials come from Cloud IAM.
:::

### In the Credentials tab:

1. Click the button, represented by the plus icon, next to the word , to add a credential.
2. In the  modal, select the credentials that will be part of the secret and click Add.

:::(info) (Info)
These credentials come from PAM Core.
:::

### In the Ephemeral credentials tab:

1. Click the button, represented by the plus icon next to the word , to add an ephemeral credential.
2. In the  modal, select the ephemeral credentials that will be part of the secret and click .

### In the Key/Value tab:

1. Click the button, represented by the plus icon next to the words , to add a key/value pair.
2. When you click the plus button, two fields appear in the list below:
   1. : fill in the value of the key name.
   2. : fill in the value of the key.

### In the Auto-renewal tab:

Here, you must stipulate a secret renewal time for:
1. 
2. 
3. 

You manage these time intervals using the  parameters.

When you're ready, click .

#### Important

* When the information expires, it's deleted. However, some information, such as access keys, can no longer be recovered.
* Only PAM Core or Cloud IAM access group users can add cloud credentials and credentials for registering a secret.
* The Cloud IAM module manages cloud credentials.
* PAM Core manages credentials.
*  are provisioned by senhasegura directly at the destination via . Once the credential has been rotated, the  won't delete the old  and  information.

## View a secret

1. On senhasegura, in the upper left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. In the list, identify the secret you want to view and, in the  column, click on the icon represented by the three vertical dots and select  from the drop-down menu.

On the  window, you can view all the information about the secret.

## View the versions of a secret

1. On senhasegura, in the upper left corner, click , represented by the nine squares, and select 
2. In the side menu, select 
3. In the list, identify the secret you want to view and, in the  column, click on the icon represented by the three vertical dots and select  from the drop-down menu.

In the  history window, you can view the information and versions of the secret using the following fields:

1. : name of the secret.
2. : engine of the secret. The default engine is .
3. : identity of the secret.
4. In the  section:
   1. : version number of the secret.
   2. : date and time when this secret version was created.
   3. :
      1. : represented by the magnifying glass icon, opens the secret viewing form.
      2. : represented by the two arrows in opposite directions icon, opens the Version compare window.

## Update a secret

1. On senhasegura, in the upper left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. In the list, identify the secret you want to view and, in the  column, select , represented by the pencil and paper icon.
4. In the  window, change the information you need to change and click .

:::(info) (Info)
The form for editing secrets is the same as for registering secrets.
:::

## Compare two versions of a secret

1. On senhasegura, in the upper left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. In the list, identify the secret you want to view and, in the  column, click on the icon represented by the three vertical dots and select  from the drop-down menu.
4. In the  window, click on Compare, represented by the two arrows in opposite directions icon to open the version comparison window.

### In the Version compare window:

1. In the  drop-down menu, select the initial version you want to use for comparison.
2. In the  drop-down menu, select the version that will be compared with the selected version in .
3. You can’t compare a smaller version with a larger version. The version number in  menu must always be greater than in  menu.
4. Once you have selected the versions to compare, click on .

The changes will be shown according to the fields that have been altered. The display of changes between versions follows the pattern in *DIFF* programs, with additions in green and deletions in red.

## Change a secret's access keys

1. On senhasegura, in the upper left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. In the list, identify the secret you want to view and, in the  column, click on the icon represented by the three vertical dots and select  from the drop-down menu.

A pop-up window will indicate that rotating the access keys for that secret is underway. The process is done automatically.

## View a secret's error history

You can view the error history of a secret by going to .

To view the error history, select a secret from the list and, in the  column, click on the icon represented by the three vertical dots and select the View error history option.

:::(warning) (Caution)
* The option to view the error history will only be shown if an error has occurred in the secret.
* To view secrets, you need to be part of an access group with permission to manage secrets; otherwise, you can register a secret but won't see it in the filters and dashboards.
:::

---

Do you still have questions? Reach out to the .