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

  ## Task 1: What does the 3-letter acronym SMB stand for?

  - Server Message Block
  
  ## Task 2: What port does SMB use to operate at?

  - 445  
  ![nmap](https://github.com/user-attachments/assets/603dd0e4-be33-4d04-85a2-e69281e262ca)

  ## Task 3: What is the service name for port 445 that came up in our Nmap scan?

  - microsoft-ds
  ![nmap](https://github.com/user-attachments/assets/378799cf-ac08-46f1-b19d-3dc3dabe9852)

  ## Task 4: What is the 'flag' or 'switch' that we can use with the smbclient utility to 'list' the available shares on Dancing?

  - -L  
  ![list shares](https://github.com/user-attachments/assets/5ffc5933-4e59-4493-8dd5-cf93b1968357)

  ## Task 5: How many shares are there on Dancing?

  - 4  
  ![list shares](https://github.com/user-attachments/assets/f453e174-b4b6-4432-aeb8-12214b8e87ba)

  ## Task 6: What is the name of the share we are able to access in the end with a blank password?

  - Workshares  
  ![workshares](https://github.com/user-attachments/assets/4f10ad5e-565d-444e-a619-01761c2a48f0)

  ## Task 7: What is the command we can use within the SMB shell to download the files we find?

  - get  
![flag download](https://github.com/user-attachments/assets/61a15596-6f5d-4d1e-a764-f06f88927746)


  ## Task 8: Root Flag
  
![cat flag](https://github.com/user-attachments/assets/cc20f65b-2554-4565-ad36-13f1750e510a)

  
  ## Pwned Box
![dancing pwned](https://github.com/user-attachments/assets/84ef51c9-624c-449e-872f-4c8e2f4d9284)

## Redeemer Box

  ## Task 1: Which TCP port is open on the machine?

  - 6379  
  ![nmap](https://github.com/user-attachments/assets/9fe28435-6a6f-4df8-b12e-3ecea70c1698)

  ## Task 2: Which service is running on the port that is open on the machine?

  - Redis  
  ![nmap](https://github.com/user-attachments/assets/5875147c-ccb1-4b0a-8795-29f964f269ae)

  ## Task 3: What type of database is Redis? Choose from the following options: (i) In-memory Database, (ii) Traditional Database

  -In-memory Database  
  
  ## Task 4: Which command-line utility is used to interact with the Redis server? Enter the program name you would enter into the terminal without any arguments.

  - redis-cli  
![redis connect](https://github.com/user-attachments/assets/39424ad6-b715-491a-aa3e-68db09617645)

  ## Task 5: Which flag is used with the Redis command-line utility to specify the hostname?

  - -h  
![redis connect](https://github.com/user-attachments/assets/d0e647b2-62af-45b9-9754-a463de196e97)

  ## Task 6: Once connected to a Redis server, which command is used to obtain the information and statistics about the Redis server?

  - Info  
  ![redis info](https://github.com/user-attachments/assets/fa32d754-1a04-4e75-8eb7-d393e8d35f4b)

  ## Task 7: What is the version of the Redis server being used on the target machine?

  - 5.0.7  
  ![redis info](https://github.com/user-attachments/assets/af2e7fc1-d167-4720-996a-b585629fb8f1)

  ## Task 8: Which command is used to select the desired database in Redis?

  - select    
  
  ## Task 9: How many keys are present inside the database with index 0?

  - 4    
![keys db0](https://github.com/user-attachments/assets/b9ced55f-9e58-433a-8286-277b6b364ed5)

  ## Task 10: Which command is used to obtain all the keys in a database?

  - keys *  
![view all keys](https://github.com/user-attachments/assets/c890781a-7bfd-413e-a111-942408224594)

  ## Task 11: Root Flag

  ![get flag](https://github.com/user-attachments/assets/06be9a9b-6385-4e96-9c67-01348779f156)

  ## Pwned Box: 
  
  ![redeemer pwned](https://github.com/user-attachments/assets/2cddfa5f-b63f-447f-8366-3952dd4e0ea6)

