# SOP-3-Cyber-Security-Pen-Testing-Module

<img src="https://www.lumificyber.com/wp-content/uploads/2023/08/blog_penetration_tester.jpg" width="400"/>

## Module 1: Anonymous Connections
  In this module I will use a Kali Linux Virtual Machine to connect anonymously to services like FTP, SMB, Telnet, Rsync, and RDP on vulnerable virtual machines.
|
## FTP: 
  The ftp anonymous connection is a simple proccess that requires a machine to have a port using the ftp service to be open.
  
Here in this screenshot we can see an nmap scan showing the open ports on the vulnerable metasploit virtual machine. 
In the list of ports it shows port 21 ftp is open. 

![Nmap -sS Scan ](https://github.com/user-attachments/assets/37751bec-7478-4db8-b37a-32a7fa53eda3)

The next step is to establish the anonymous connection using the ftp command ftp <IP_Address> with the credentials user=anonymous and the password can be anything.
Shown in this next screenshot below.

![FTP anon connect](https://github.com/user-attachments/assets/70e6d0d2-86bd-4554-997c-7fa6bb9c700c)

The ftp service has a help menu you can open by typing "help". This will give you a list of commands that you can use while on the ftp server. 

![FTP Help menu](https://github.com/user-attachments/assets/f8d17bfa-c8ce-4d8e-a618-48871ca05a82)

The last step for the anonymous ftp is to list directories. In the help menu we can see both the "ls" and "dir" commands to list directories and the "pwd" command to print our current working directory. 
Using the "pwd" command to show the current working directory and "ls -la" command to list all directories and hidden directories below.

![FTP pwd ls -la](https://github.com/user-attachments/assets/c7d08528-1a9a-4cce-bbd9-87f88a3dc3ad)


## SMB: 
  For the smb anonymous connection it requires a machine to have port 139 and port 445 open using the netbios-ssn service.

  In the screenshot below it shows an nmap scan to show open ports on the vulnerable metasploit virtual machine.
  In the list of ports in shows port 139 and port 445 using the netbios-ssn service to be open. 

![Nmap -sS Scan ](https://github.com/user-attachments/assets/dde5f0c5-62fd-4210-b1fb-babcaf096ec0)

You can use the smbclient help menu by entering the command "smbclient -?" for usage.

![smb help 1](https://github.com/user-attachments/assets/639bfc0a-c985-4cbe-87c5-bb24f6061276)
![smb help 2](https://github.com/user-attachments/assets/275e2cfc-b251-4e1b-a64f-97efe8e650cf)

To access shared resources using smbclient you can use the "-L" option to list the shares.

![SMB anon connect](https://github.com/user-attachments/assets/f47bad77-20f7-46a4-81bb-c6c8f847d9ca)


## Telnet:
  Telnet does not require authentication when connecting, so if the port is open you can easily connect anonymously.
  Telnet requires port 23 using telnet to be open to establish connections. 
  In the nmap scan below it shows port 23 telent to be open.

![Nmap -sS Scan ](https://github.com/user-attachments/assets/1c905eef-63da-44e3-a8c0-1099c865280c)

To establish the telnet connection use the command "telnet <IP_Address>"

![Telnet anon connect ](https://github.com/user-attachments/assets/17363043-2127-4bf0-9388-aa4c6632f22f)

## Rsync:

  This first screen shot below shows the target machines files in the msfadmin direcotry using the ls command to show the contents before the rsync connection.

![metasploit ls without rsync](https://github.com/user-attachments/assets/34a5c31e-43a7-4ded-b26e-28fb15b2bbe5)

  For the rsync connection both machines need to have rsync and matching host key types. In my first attempt in establishing the connection I ran into an issue with host key types. 
  these host key type mismatches were blocking the connection. Shown in the screen shot below. 
  
![rsync error](https://github.com/user-attachments/assets/bae19153-d547-42d8-95e3-12af7b1dbf3d)

To fix this issue I had to input the host key algorithms in the rsync command. 

rsync -av -e 'ssh -oHostKeyAlgorithms=+ssh-rsa' /home/roszek/Desktop/usernames.txt msfadmin@192.168.1.189:/home/msfadmin

-av: stands for a(Archive mode) this option preserves permissions and v(verbose) this option shows more details in the output.\
-e ssh: This option is how you can select ssh for the file transfer.\ 
-oHostKeyAlgorithms=+ssh-rsa: This option inputs the correct host key algorithm to establish the file transer connection. 

![rsync connection](https://github.com/user-attachments/assets/ee14803a-fe25-4ff8-8817-f33ad0b37eb0)






