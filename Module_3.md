## Mongodb Server Setup through Docker:

  Step 1: Pull mongodb docker image.

  Command: "docker pull mongo:4.0.4"

  I had to choose an earlier version of mongodb because I was having many issues with the newer version containers not starting properly. 
    
![Mongo download](https://github.com/user-attachments/assets/12cac7b8-5267-4d18-bc9a-f82b4c4e7973)

  To see a list of your downloaded images use the command: "docker images"

![mongo image](https://github.com/user-attachments/assets/2942481c-0ea6-47fa-9da2-2e20173c94e6)

Step 2: Mongodb data directory 

 - Before running the container you have to make a file to store the mongodb data. 

 - On my local machine in the /home/roszek directory I made a new directory called mongodb_data

Step 3: Run the container

  Now to run the container use the command: "docker run -d -p 27017:27017 -v /directory/file/location:/data/db mongo:4.0.4"

  - -d: this flag means detatch. It allows the container to run in the background.
  - -p: this flag lets you match the container to a port. for mongodb the common port is 27017
  - -v: this flag means volume. Here we set the path to the directory that stores the mongodb container data and then map it to the default path to the mongodb database.

![mongo container ](https://github.com/user-attachments/assets/a1226e09-96e7-407f-82b2-d02136201eb9)

Step 4: Test connection

Now to test if we can connect to the container. 

In the screenshot above where we used the docker run command, the output gave a name for the new container. We can use that name to connect using the command "docker exec -it container_name mongo"

- -it: This flag means interactive. It automatically brings you into the container. 

![mongo test connect](https://github.com/user-attachments/assets/4c3ebe34-456b-4565-9a3e-8d4f74addbcb)

## Mongodb Exploitation

  To connect to the mongodb container use the command "mongosh <IP_ADDRESS>:<PORT>"  

  - for the ip_address use the ip of the machine hosting the docker container
  - for the port use the port used for the docker container  
  
  ![mongodb remote connection](https://github.com/user-attachments/assets/0b69cc7e-2b98-4c43-a6d0-1b25df346a0f)
