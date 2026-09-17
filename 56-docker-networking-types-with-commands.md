# Docker Networking
    lists the network
    commands = docker network ls
   <img width="1920" height="164" alt="image" src="https://github.com/user-attachments/assets/076cb96e-47ad-424d-ada2-b7c139fc803a" />
   
 # Built-in Network Drivers
 <img width="844" height="267" alt="image" src="https://github.com/user-attachments/assets/d2fa8b29-89c3-4040-b6d3-487aac4a2bcb" />
 <img width="743" height="108" alt="image" src="https://github.com/user-attachments/assets/01506ac3-21b1-4f87-a91d-a5dba0fbdca9" />
 
# Create a seperate network
Creating separate custom networks in Docker is essential for three main reasons:
1. Container Isolation & Securit
2. Automatic Name Resolution (DNS)
3. Traffic Control & Organization

        commands = sudo docker network create portfolio-network

<img width="1920" height="231" alt="image" src="https://github.com/user-attachments/assets/77a957b6-773d-4f79-a121-a46e71ac41dc" />

# Create a psql Container 
commands =  sudo docker run -d \
> --name portfolio-db-container \
> --network portfolio-network \
> -e POSTGRES_PASSWORD=amina@123 \
> -e POSTGRES_DB=portfolio_db \
> -e POSTGRES_USER=amina \
> postgres:15

<img width="1920" height="991" alt="image" src="https://github.com/user-attachments/assets/5de57b33-7bc9-4695-aa48-d902700e7065" />

    ☑️Copy the SQL file into the container 


 <img width="1920" height="130" alt="image" src="https://github.com/user-attachments/assets/d32c9c23-ab66-44f2-82ed-ea60ce1fb81d" />

    ☑️Execute the SQL file using psql inside the container
    commands = docker exec -it portfolio-db psql -U amina -d portfolio_db -f /tmp/init.sql 

<img width="1920" height="658" alt="image" src="https://github.com/user-attachments/assets/82d48845-bb2d-43bd-9c18-c29f3fb8bac7" />

    ☑️Create php container to run php
    commands = sudo docker run -d --name portfolio-web --network portfolio-network -p 8080:80 -e PGHOST=portfolio-db-container -e PGDATABASE=portfolio_db -e PGUSER=amina -e PGPASSWORD=amina@123 -e PGPORT=5432
     php:8.2-apache

 <img width="1920" height="780" alt="image" src="https://github.com/user-attachments/assets/e6975a87-6f15-454e-99a0-165fa352e436" />

     ☑️Update apt and install the Postgres C-library dependency 
     commands = sudo docker exec -it portfolio-web apt-get update 
                sudo docker exec -it portfolio-web apt-get install -y libpq-dev
                
<img width="1920" height="818" alt="image" src="https://github.com/user-attachments/assets/af9e6115-9563-46ec-b053-e1dd1379dff4" />
  
     ☑️Copy the index.php file into the container 

<img width="1920" height="905" alt="php" src="https://github.com/user-attachments/assets/1757d35e-fb18-4648-835b-f81d4a235c0f" />

 # Access the website
      http://192.168.1.15:8080

  <img width="1920" height="1080" alt="Screenshot (974)" src="https://github.com/user-attachments/assets/f063bf92-ca56-4192-8900-33c65ab2a585" />
    




             





 
 

 
 
