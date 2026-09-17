# Run portfolio using two Container 
    *️⃣Visual idea: 
    Logos of docker,
    APache
    PostgrSQL

    portfolio-project/
    ├── docker      # Orchestrates both containers
    └── src/         # Web application source files
    └── index.php    # Your main PHP application file

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
    

  
