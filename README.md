# SOP-3-Cyber-Security-Pen-Testing-Module

<img src="https://www.lumificyber.com/wp-content/uploads/2023/08/blog_penetration_tester.jpg" width="400"/>

## Module 1: Anonymous Connections
  In this module I will use a Kali Linux Virtual Machine to connect anonymously to services like FTP, SMB, Telnet, Rsync, and RDP on vulnreble virtual machines.
|
## FTP: 
  The ftp anonymous connection is a simple proccess that requires a machine to have a port using the ftp service to be open.
  
Here in this screenshot we can see an nmap scan showing the open ports on the vulnreble metasploit virtual machine. 
In the list of ports it shows port 21 ftp is open. 
![Nmap -sS Scan ](https://github.com/user-attachments/assets/37751bec-7478-4db8-b37a-32a7fa53eda3)

The next step is to establish the anonymous connection using the ftp command ftp <IP_Address> with the credentials user=anonymous and the password can be anything.
Shown in this next screenshot below.

![FTP anon connect](https://github.com/user-attachments/assets/70e6d0d2-86bd-4554-997c-7fa6bb9c700c)

The ftp service has a help menu you can open by typing "help". This will give you a list of commands that you can use while on the ftp server. 

![FTP Help menu](https://github.com/user-attachments/assets/f8d17bfa-c8ce-4d8e-a618-48871ca05a82)

The last step for the anonymous ftp is to list directories. In the help menu we can see both the "ls" and "dir" commands to list directories. 
Using the "ls -la" command to list all directories and hidden directories.

![FTP pwd ls -la](https://github.com/user-attachments/assets/c7d08528-1a9a-4cce-bbd9-87f88a3dc3ad)

