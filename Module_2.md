## Module 2: Port Scanning With Nmap

  In this first scan I used the nmap -sS <IP_ADDRESS> command to list the results of a tcp SYN scan. This scan shows open TCP ports aswell as the name of the services using the ports.  
    * -sS: this option tells nmap to do a TCP SYN scan
  
![Nmap -sS Scan ](https://github.com/user-attachments/assets/b2ad3988-f9ba-483f-be7e-4e3182924339)

  In this next scan I used the nmap -sU <IP_ADDRESS> command to list the results of a UDP scan. This scan shows open UDP ports aswell as the name of the services using the ports. 
![nmap -sU scan](https://github.com/user-attachments/assets/f1ad556b-fe04-4480-b449-069aad7555e0)

  In this next scan I used the nmap -sV <IP_ADDRESS> command to list more detailes about the services being used. The extra details help in determining versions of the services to see what ports/services can be exploited and what can not be exploited.
![namp -sV scan](https://github.com/user-attachments/assets/5e6e28c9-ffee-47bd-a0a1-8d81a44c001e)

  In this final scan I used the nmap -O <IP_ADDRESS> command to show detailes about the systems operating system.
![nmap -O scan](https://github.com/user-attachments/assets/098350a9-6c36-424a-993a-2a9a5c59a61c)
