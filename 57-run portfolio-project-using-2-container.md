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
    
