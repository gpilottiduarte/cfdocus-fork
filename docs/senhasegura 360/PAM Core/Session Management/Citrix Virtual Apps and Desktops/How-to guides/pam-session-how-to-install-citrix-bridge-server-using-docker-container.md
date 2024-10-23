## Metadata_Start 
## code: en
## title: How to install Citrix Bridge Server using Docker container 
## slug: pam-session-how-to-install-citrix-bridge-server-using-docker-container 
## seoTitle: How to install Citrix Bridge Server using Docker container 
## description:  
## contentType: Markdown 
## Metadata_End
In this document, you’ll find a step-by-step guide on how to perform the installation of Citrix Bridge Server via docker, which is responsible for communicating with Citrix Virtual Apps and Desktops through an  protocol exclusive to Citrix.

## Requirements

* Linux with .
*  module to transfer files.
* RDP port (3389) open.
* Network connection to the Citrix Virtual Apps and Desktops server.
* Network connection to the server where applications run.
* Have the senhasegura Citrix Proxy container already installed.

---
## Install via Docker container

1. Download the  to get the  file.
2. Open the  application of your preference to unzip the file.
    1. Type .
    2. Press the  key.
    3. The message  will be displayed, confirming that the image was generated.
3. Import the container image, type:
    1. 
4. Start the container, type:
    `
    sudo docker run -d \
        --net host \
        --name xrdp-citrix-senhasegura-image_0.9.5-8 
        --device /dev/fuse \
        --cap-add SYS_ADMIN
    xrdp-citrix-senhasegura-image:0.9.5-8
    `
5. Perform the validation, type:
    1. 

This is the expected result after performing these steps:

`
CONTAINER ID   IMAGE                                   COMMAND       CREATED         STATUS         PORTS     NAMES
c679f44df088   xrdp-citrix-senhasegura-image:0.9.5-8   "/start.sh"   7 minutes ago   Up 7 minutes             xrdp-citrix-senhasegura-image_0.9.5-8
`

If file transfer and copy and paste don’t work, start the container by adding the command .

`
sudo docker rm -f xrdp-citrix-senhasegura-image_0.9.5-8

sudo docker run -d \
    --net host \
    --name xrdp-citrix-senhasegura-image_0.9.5-8 \
    --device /dev/fuse \
    --cap-add SYS_ADMIN --privileged xrdp-citrix-senhasegura-image:0.9.5-8
`

Citrix Server can also be installed and configured using the senhasegura Extended Service OVA, to find out how to perform this installation, access the How to install Citrix Bridge Server using senhasegura Extended Services OVA document.

---
### Next





Do you still have questions? Reach out to the .