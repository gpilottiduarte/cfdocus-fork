## Metadata_Start 
## code: en
## title: How to perform remote access with SSH key via web proxy 
## slug: how-to-perform-remote-access-with-ssh-key-via-web-proxy 
## seoTitle: How to perform remote access with SSH key via web proxy 
## description:  
## contentType: Markdown 
## Metadata_End
This document introduces you to the steps required to remotely access a device on senhasegura via a web proxy and using an SSH key.

## Requirements

To start a session with SSH keys, the following requirements must be met:

- Valid access credentials.
- Have senhasegura user permission.
- Belong to an access group with permission to use credentials and devices to make remote sessions.

## Remote access with SSH key via web proxy

### Configuring the device using senhasegura

1. On senhasegura, in the upper-left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. In the  report, identify the device and credential used to configure remote access.
4. Once you have identified the device and credential, in the  column, click , represented by the computer icon. You’ll be connected to the device using this credential.

:::(info) (Info)
To perform this procedure directly on the device, connect SSH with the command .
:::

You must perform the following operations on the device:

1. Create an SSH key with the command .
2. Copy both the public key values and the newly created private key.
3. While still on the device, you must copy the public SSH key to the device. To do this, run the command . You can test the connection using the command .
4. If you don't copy the SSH key using the ssh-copy-id command, you won't be able to start a remote session.

On senhasegura, register an SSH key. To do this, follow the steps below:

1. On senhasegura, in the upper-left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. In the top bar, click on , represented by the three vertical dots, and select .
4. In the  window, fill in the fields:
    1. On the  tab:
        1. : fill in the user who owns the key. This user must exist on the device used previously.
        2. : indicate on which device the key was generated.
        3. : name of the SSH key. For example, id_rsa.
        4. : select .
    2. In the  tab:
        1.  paste the value of the private key you copied earlier. : when copying the key, don't forget to copy its entire contents, from  to .
        2. : paste the value of the public key you created earlier. : this key has the extension .
            1. If the key has a password, click  and add the key's password in the  field.
    3. In the  tab:
        1. : click on the sum icon to open the  modal.
        2. In the  modal, check the devices you want to access the SSH key.
            1. : The public key must be published on the devices selected in the modal
5. Click .

### Start a remote session with an SSH key

Having successfully completed the previous steps, you will now be able to start a remote session with your SSH key, by following the steps below:

1. On senhasegura, in the upper-left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. In the  report, identify the SSH key you want to use.
4. In the  column, click the three vertical dots and select .
5. In the  window, identify the device you want to access with the SSH key and click , represented by the computer icon.
6. You’ll be connected to the device using the SSH key you registered.

---

Do you still have questions? Reach out to the .