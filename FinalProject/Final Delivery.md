# Final Project : SAMBA File Server

## Table of Content:

1. Introduction
2. Step by Step installing SAMBA
   * Pre-Requisites
   * Installing SAMBA on Ubuntu
   * Configuration of SAMBA
   * Running SAMBA
3. Final Quotes

## Introduction:

![samba](/FinalProject/img/samba.jpg)

SAMBA is an open source software that allows the user share files between linux/unix machines and Windows devices. However , SAMBA also works with MacOs Devices following a proper configuration.
Today , we are going to focus how to set-up SAMBA and run it on a Local Area Network as a file server.

## Step by Step Installing SAMBA.

![sambaexample](/FinalProject/img/sambaexample.jpg)

The process of installation of SAMBA is not the hardest but takes its time. It has many configurations to implement devices such as printers. We are going to focus on a simple file server.

### Pre-Requisites

*  Configuration of the Hypervisor.
   If you are running Linux on a Virtual Machine , this configuration is mandatory. A Virtual machine default configuration uses internet provided by the host machine. However , in order to make Samba run properly , our virtual machine must have its own ip provided by the router.

   ![hypervisorcfg](/FinalProject/img/2nd3.png)

### Installing SAMBA on Linux Ubuntu 20.04

1. We must install SAMBA and all its dependencies using the following command. `sudo apt install samba`

![sambainstall](/FinalProject/img/f1.png)

2. Check the status of the Samba Service using the following command. `systemctl status smbd`

![sambastatus](/FinalProject/img/f2.png)

3. Set up Samba to work on your Local Area Network.
   * The location of the configuration file of samba is located in /`etc/samba/smb.conf`. We are going to create a file from zero saving the first one as a backup.
   Type in the terminal: `sudo mv /etc/samba/smb.conf /etc/samba/smb.conf.bak`. It is important to use "sudo" at the beginning because of the permissions of the folder. The command is going to take the original samba configuration file and keep it with a different name.

   ![sambabackup](/FinalProject/img/f3.png)

   * Then , It is important to stop the samba service because it does not have a configuration file. `sudo systemctl stop smbd`. Use `sudo systemctl status smbd` to check if the service is stopped.
   ![sambaservice](/FinalProject/img/f4.png)

   * Using a text editor (in this case , we are going to use "nano") create a new "smb.conf" file. `sudo nano /etc/samba/smb.conf`. The file must contain two sections: "global" and "shares".
   Type the following:
     > [global]
      server string = Final Project Server
      workgroup = WORKGROUP
      security = user
      map to guest = Bad User
      name resolve order = bcast host
      include = /etc/samba/shares.conf
    
        The most important thing here is the "workgroup". Here you must type the name of the Local Area Network you want samba running. in this case , the workgroup is going to be the default one "WORKGROUP".

    ![sambaconfig](/FinalProject/img/f5.png)


    The last line "Include" is going to let me use two different files to organize my global parameters and my share's parameters.
    * Now , we have to create the "shares.conf" which is the file that is going to complement the first one. `sudo nano /etc/samba/shares.conf`. 
    Here we must type the following:
        >[final-project-files]
    path = /home/student/Desktop/ShareableFolder/public
    force user = smbuser
    force group = smbgroup
    create mask = 0664
    force create mode = 0664
    directory mask = 0775
    force directory mode = 0775
    public = yes
    writable = yes
    [final-project-protected-files]
    path = /home/student/Desktop/ShareableFolder/protected
    force user = smbuser
    force group = smbgroup
    create mask = 0664
    force create mode = 0664
    directory mask = 0775
    force directory mode = 0775
    public = yes
    writable = no

    This is an example of a protected folder and a public folder. The only difference between them is "writable" value.

    In "path" you are going to type the path of the directory you want to share.
    "Force user/group" this is going to be defined later.
    The following lines are going to be the permissions. It is important to enter the same numbers because windows and linux read permissions in different ways. This is going to solve many compatibility issues.

    Once those files are created , save them.

    * Now, we have to create the "group" and the "user". Use the following commands:
      - sudo groupadd --system smbgroup
      - sudo useradd --system --no-create-home --group smbgroup -s /bin/false smbuser'
  
    It is important that you enter the same values for group and user that you entered previously.
      * Then , we are going to use the command "chown" to change the user and group permissions to the parent directory where the files are located. In my case the name of the directory is "ShareableFolder".
      `sudo chown -R smbuser:smbgroup /home/student/Desktop/ShareableFolder`
      `sudo chmode -R g+w /home/student/Desktop/ShareableFolder`

      ![lstest](/FinalProject/img/f6.png)
    * After that , We are ready to turn on SAMBA using the following command.
    `sudo systemctl start smbd`

    ![final](/FinalProject/img/f7.png)
    * In order to access to your SAMBA file server on a windows computer. You must identify your Local IP. Then , type it down in your file browser.
  ![finalito](/FinalProject/img/f8.png)
  ![finalito](/FinalProject/img/f9.png)

## Final Quotes:
    
This project was challenging. It takes you deeper to group and user permissions. Also , it is a good tool when you want to share files between your laptop and your desktop computer. I actually used it the whole semester because i do not usually use my laptop at home, but all the files from different classes were there. Using samba, i was able to always share the files between my laptop and my computer.



    





   
    


