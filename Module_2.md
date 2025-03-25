## Module 2: Port Scanning With Nmap

  In this first scan I used the nmap -sS <IP_ADDRESS> command to list the results of a TCP SYN scan. This scan shows open TCP ports aswell as the name of the services using the ports.  
  - -sS: This option tells nmap to do a TCP SYN scan.

  - The output from this scan gives us 23 open ports with many vulnerable services like ftp, telnet, ssh, http, etc.
  
![Nmap -sS Scan ](https://github.com/user-attachments/assets/b2ad3988-f9ba-483f-be7e-4e3182924339)

  In this next scan I used the nmap -sU <IP_ADDRESS> command to list the results of a UDP scan. This scan shows open UDP ports aswell as the name of the services using the ports. 
  - -sU: This option tells nmap to do a UDP scan.

  - The output from this scan gives us 7 open ports with vulnerable services like rpcbind, and netbios.
    
![nmap -sU scan](https://github.com/user-attachments/assets/f1ad556b-fe04-4480-b449-069aad7555e0)

  In this next scan I used the nmap -sV <IP_ADDRESS> command to list more detailes about the services being used. The extra details help in determining versions of the services to see what ports/services can be exploited and what can not be exploited.
  - -sV: This option tells nmap to have a more detailed scan output.

  - The output from this scan gives the same 23 ports from the TCP SYN scan but we get a more detailed look at the versions of the services being used for example, vsftpd 2.3.4, smbd 3.X - 4.X, Apache httpd 2.2.8, etc.
    
![namp -sV scan](https://github.com/user-attachments/assets/5e6e28c9-ffee-47bd-a0a1-8d81a44c001e)

  In this final scan I used the nmap -O <IP_ADDRESS> command to show detailes about the systems operating system.
  - -O: This option tells nmap to scan the operating system of the target machine.

  - The output from this scan gives us the same open ports from the TCP SYN scan but it also gives us the operating system type and version the target machine is using. We get that the machine is using Linux and the version is 2.6.9 - 2.6.33.

![nmap -O scan](https://github.com/user-attachments/assets/098350a9-6c36-424a-993a-2a9a5c59a61c)
