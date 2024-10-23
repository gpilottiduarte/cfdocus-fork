## Metadata_Start 
## code: en
## title: How to manage the Master Key backup directory 
## slug: how-to-configure-master-key-backup 
## seoTitle: How to manage the Master Key backup directory 
## description:  
## contentType: Markdown 
## Metadata_End
Before creating the master key, it's necessary to configure the export location for the encrypted data.

## Configure storage directory for encrypted data

1. On senhasegura, in the upper left corner, click , represented by nine squares, and select .  
2. In the side menu, select .  
3. In the  report, click on , represented by three vertical dots, and select  from the dropdown menu.  
4. In the  window, fill in the data:  
   1. : choose the backup mode from the drop-down menu. The options are *Local Directory* or *SSH \- Rsync*.  
      1. Keep the default settings for the local directory.
      2. For SSH-Rsync, see the instructions below.  
   2. : select  for the server to be accessible right after creation.  
   3. : indicate the backup directory path on the server. For example: .  
5. Click .

### SSH-Rsync Mode

If you choose the  mode, you should additionally fill in this data:

1. : IP address or domain of the backup server host.  
2. : port number that the backup server will be listening on.  
3. : select from the drop-down menu the credential that will authenticate on the backup server.  
   1. This credential should have already been registered in senhasegura.  
4. Click . 

:::(info) (Info)  
This directory is the same directory where the credential backup was configured.  
:::

## How to change the storage directory for encrypted data

1. In senhasegura, in the upper left corner, click on , represented by nine squares, and select .  
2. In the side menu, select .  
3. In the  report, identify the directory you want to change and, in the  column, click on , represented by the pencil and paper icon.  
4. The  window will open in edit mode, edit the information you want and click .

## How to deactivate a storage directory for encrypted data

1. In senhasegura, in the upper left corner, click on , represented by nine squares, and select .  
2. In the side menu, select .  
3. In the  report, identify the directory you want to change and, in the  column, click on , represented by the pencil and paper icon.  
4. The  window will open in edit mode.  
5. In , select  and click .

## How to reactivate a storage directory for encrypted data

1. In senhasegura, in the upper left corner, click on , represented by nine squares, and select .  
2. In the side menu, select .  
3. In the  report, in the top bar, select  in the  drop-down menu to filter inactive servers in senhasegura.  
4. Identify the server you want to reactivate and, in the  column, click on , represented by the pencil and paper icon.  
5. The  window will open in edit mode.  
6. In , select  and click .

---

Do you still have questions? Reach out to the .