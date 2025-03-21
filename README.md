# SOP-3-Cyber-Security-Pen-Testing-Module

<img src="https://www.lumificyber.com/wp-content/uploads/2023/08/blog_penetration_tester.jpg" width="400"/>

## Module 1: Anonymous Connections
  In this module I will use a Kali Linux Virtual Machine to connect anonymously to services like FTP, SMB, Telnet, Rsync, and RDP on vulnreble virtual machines.
|
## FTP: 
  The ftp anonymous connection is a simple proccess that only requires a machine to have a port using the ftp service to be open.
  
Here in this screenshot we can see an nmap scan showing the open ports on the vulnreble metasploit virtual machine. 
In the list of ports it shows port 21 ftp is open. 
![Nmap -sS Scan ](https://github.com/user-attachments/assets/37751bec-7478-4db8-b37a-32a7fa53eda3)

The next step is to establish the anonymous connection using the ftp command ftp <IP_Address>
Shown in this next screenshot below.

![FTP anon connect](https://github.com/user-attachments/assets/70e6d0d2-86bd-4554-997c-7fa6bb9c700c)



