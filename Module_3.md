## Mongodb Server Setup through Docker:

  Step 1: Pull mongodb docker image.

  Command: "docker pull mongo:4.0.4"

  I had to choose an earlier version of mongodb because I was having many issues with the newer version containers not starting properly. 
    
![Mongo download](https://github.com/user-attachments/assets/12cac7b8-5267-4d18-bc9a-f82b4c4e7973)

  To see a list of your downloaded images use the command: "docker images"

![mongo image](https://github.com/user-attachments/assets/2942481c-0ea6-47fa-9da2-2e20173c94e6)

# Before running the container you have to make a file to store the mongodb data. 

 - On my local machine in the /home/roszek directory I made a new directory called mongodb_data

  Now to run the container use the command: "docker run -d -p 27017:27017 -v /directory/file/location:/data/db mongo:4.0.4"

  - -d: this flag means detatch. It allows the container to run in the background.
  - -p: this flag lets you match the container to a port. for mongodb the common port is 27017
  - -v: this flag means volume. Here we set the path to the directory that stores the mongodb container data and then map it to the default path to the mongodb database. 
