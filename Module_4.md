## Meow Box

  ## Task 1: What does the acronym VM stand for?  
  - Virtual Machine

  ## Task 2: What tool do we use to interact with the operating system in order to issue commands via the command line, such as the one to start our VPN connection? It's also known as a console or shell.  
  - Terminal

  ## Task 3: What service do we use to form our VPN connection into HTB labs?
  - OpenVPN

  ## Task 4: What tool do we use to test our connection to the target with an ICMP echo request?
  - Ping

  ## Task 5: What is the name of the most common tool for finding open ports on a target?
  - Nmap

  ## Task 6: What service do we identify on port 23/tcp during our scans?

  - Telnet

  - The nmap scan used the option -sV to scan for versions and open ports.
  ![nmap](https://github.com/user-attachments/assets/6030517d-23a0-479a-91dc-638ff0c39133)

  ## Task 7: What username is able to log into the target over telnet with a blank password?

  - Root

  - For the telnet login the command used was "telent <IP_ADDRESS>" and loged in with root username. 
  ![telnet login](https://github.com/user-attachments/assets/d010ef5c-be6d-4bbf-a9c1-3eed06d0cca2)

  ## Submit Root Flag: 

  - Once connected to find the root flag use the ls command to list directories and files. This will show a directory called snap and a file called flag.txt.
  - Use the cat command on flag.txt to see the contents of the file. 

  ![root flag](https://github.com/user-attachments/assets/f67d64d9-bf7d-480f-a405-8ecd0475a410)

  ## Pwned Box 

  ![meow pwned](https://github.com/user-attachments/assets/bc1e229f-e078-4b3b-b024-cce0221e1c4f)


## Fawn Box

  ## Task 1: What does the 3-letter acronym FTP stand for?  
  
  - File Transfer Protocol
    
  ## Task 2: Which port does the FTP service listen on usually?
  
  - 21
    
  ## Task 3: FTP sends data in the clear, without any encryption. What acronym is used for a later protocol designed to provide similar functionality to FTP but securely, as an extension of the SSH protocol?
  
  - SFTP
  
  ## Task 4: What is the command we can use to send an ICMP echo request to test our connection to the target?

  - Ping
    
  ## Task 5: From your scans, what version is FTP running on the target?

  - vsftpd 3.0.3
    
![nmap](https://github.com/user-attachments/assets/070c3f27-790f-4ab7-bcaf-36f1703c2fc4)

  
  ## Task 6: From your scans, what OS type is running on the target?
  
  - Unix
    
![nmap](https://github.com/user-attachments/assets/2e4845a5-61b0-4f3e-9a52-392b81eacd54)

  ## Task 7: What is the command we need to run in order to display the 'ftp' client help menu?

  - fpt -?
  
  ## Task 8: What is username that is used over FTP when you want to log in without having an account?

  - anonymous
  
  ## Task 9: What is the response code we get for the FTP message 'Login successful'?

  - 230

  ![anon ftp](https://github.com/user-attachments/assets/10f8c1c8-3235-4e0e-811a-df2e7a5acef0)

  ## Task 10: There are a couple of commands we can use to list the files and directories available on the FTP server. One is dir. What is the other that is a common way to list files on a Linux system.

  - ls
  
  ## Task 11: What is the command used to download the file we found on the FTP server?

  - get
  
  ## Task 12: Root Flag

  - Once logged into ftp anonymously we can find the root flag by running the ls command.
  - In the list of files and directories it shows a file called flag.txt.
  - We can use the "get flag.txt" command to download the file to our system.

![ls and flag download](https://github.com/user-attachments/assets/0dc7b784-2737-4333-9c4c-09d8693f12a1)

  ## Pwned Box
  
![fawm pwned](https://github.com/user-attachments/assets/ddd07c93-4c2d-44c1-a03c-2438f9dcf458)

## Dancing Box

  ## Task :
  ## Task :
  ## Task :
  ## Task :
  ## Task :
  ## Task :
  ## Task :

## Redeemer Box

  ## Task :
  ## Task :
  ## Task :
  ## Task :
  ## Task :
  ## Task :
  ## Task :
  ## Task :
  ## Task :
  ## Task :
  
