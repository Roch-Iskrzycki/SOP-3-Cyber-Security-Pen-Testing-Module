## Mongodb Server Setup through Docker:

  Step 1: Pull mongodb docker image.

  Command: "docker pull mongo:4.0.4"

  I had to choose an earlier version of mongodb because I was having many issues with the newer version containers not starting properly. 
    
![Mongo download](https://github.com/user-attachments/assets/12cac7b8-5267-4d18-bc9a-f82b4c4e7973)

  To see a list of your downloaded images use the command: "docker images".

![mongo image](https://github.com/user-attachments/assets/2942481c-0ea6-47fa-9da2-2e20173c94e6)

Step 2: Mongodb data directory 

 - Before running the container you have to make a file to store the mongodb data. 

 - On my local machine in the /home/roszek directory I made a new directory called mongodb_data.

Step 3: Run the container

  Now to run the container use the command: "docker run -d -p 27017:27017 -v /directory/file/location:/data/db mongo:4.0.4".

  - -d: this flag means detatch. It allows the container to run in the background.
  - -p: this flag lets you match the container to a port. for mongodb the common port is 27017.
  - -v: this flag means volume. Here we set the path to the directory that stores the mongodb container data and then map it to the default path to the mongodb database.

![mongo container ](https://github.com/user-attachments/assets/a1226e09-96e7-407f-82b2-d02136201eb9)

Step 4: Test connection

Now to test if we can connect to the container. 

In the screenshot above where we used the docker run command, the output gave a name for the new container. We can use that name to connect using the command "docker exec -it container_name mongo".

- -it: This flag means interactive. It automatically brings you into the container. 

![mongo test connect](https://github.com/user-attachments/assets/4c3ebe34-456b-4565-9a3e-8d4f74addbcb)

## Mongodb Exploitation

  To connect to the mongodb container use the command "mongosh <IP_ADDRESS:PORT>".

  - for the ip_address use the ip of the machine hosting the docker container.
  - for the port use the port used for the docker container.  
  
  ![mongodb remote connection](https://github.com/user-attachments/assets/0b69cc7e-2b98-4c43-a6d0-1b25df346a0f)

  In the next step use the command "show dbs" to list the available databases .
  
  ![mongo show dbs](https://github.com/user-attachments/assets/d6b6c6a4-1192-4e79-a86b-ad3b29533f3d)

  To enter one of the databases use the command "use <database_name>".

  Once inside of the database use the command "show collections" to see what data is stored inisde the database.

  Then use the command "db.colletion_name.find()" to see what data is inside the collection.

  Inside the system.version collection screenshot below we can see the mongodb version the container is running. 
  
  ![mongo admin collections](https://github.com/user-attachments/assets/c3263ac8-84de-409e-9dc9-b55e6782eb23)

  Now If you want to move to another database use the "show dbs" command again, then "use <database_name>" to enter the other databases, then use "show collections" and "db.colletion_name.find()" to view the information.

  In the config database there is a collection named system.sessions displayed below. This collection gives information about active server sessions including session ID's, timestamps, and status.

  ![mongo config collections](https://github.com/user-attachments/assets/439f9b18-210d-41ff-a4b4-af5b0f0aab96)

  The final database we have access to is the local database. Using the same commands "show dbs", "use <database_name>", "show collections", and "db.colletion_name.find()" 

  The startup_log shows information redgarding mongod instances, runtime options, and proccess ID's.

  ![mongo local collections](https://github.com/user-attachments/assets/4cbf457c-9334-4c76-ac3d-c966ad117878)
  ![mongo local collections 2](https://github.com/user-attachments/assets/f6a78d51-b883-47ba-b4c0-866547c5f04d)
  ![mongo local collections 3](https://github.com/user-attachments/assets/ac4cde0d-d7c0-48b6-a63e-e30029ade3f9)
