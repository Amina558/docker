# 🟤Docker Volume 
    The Container Data Dilemma
    . Containers are Ephemeral: By default, any data created inside a container is lost when the container is deleted.
    . Tightly Coupled: Data stored inside a container cannot easily be shared with other active containers or processes outside Docker.

# 🟤What is a Docker Volume
     . Decoupled Lifecycle: Volumes exist independently of container lifecycles, safely preserving data during updates or removals.
     . Managed by Docker: Stored in a dedicated host directory (`/var/lib/docker/volumes/`) isolated from standard host modifications.
     . High Performance: Bypasses the copy-on-write mechanism of container storage drivers, delivering native disk read/write speeds.

# 🟤Essential Volume CLI Commands
    . docker volume create portfolio-db-vol  →  Creates a new named volume explicitly.
    . docker volume ls   →  Lists all available volumes on the local Docker host.
<img width="1920" height="256" alt="image" src="https://github.com/user-attachments/assets/92d4cbbb-f4bf-4025-9427-699bdaee6c43" />

# 🟤Container connected to the volume and run
     commands = sudo docker run -d --name portfolio-db-container --network portfolio-network -e POSTGRES_DB=portfolio_db -e POSTGRES_USER=amina -e POSTGRES_PASSWORD=amina@123 -v portfolio-db-vol:/var/lib/postgresql/data postgres:15

➡️Explanation

    .docker run: Tells Docker to create and start a brand-new container.
    .-d (Detached Mode) Runs the container in the background. It frees up your terminal so you can keep typing other commands while the database runs silently.
    
     ☑️Identification & Networking
    . --name portfolio-db-container: Gives the container a friendly, custom name (portfolio-db-container) 
    . --network portfolio-network: Connects this container to a specific virtual network called portfolio-network 

    ☑️Environment Variables
    . The -e flag sets up settings inside the container.
    . -e POSTGRES_DB=portfolio_db: Creates a new database named portfolio_db inside PostgreSQL as soon as it starts up.
    . -e POSTGRES_USER=amina: Creates a master user account (admin) named amina.
    . -e POSTGRES_PASSWORD=amina@123: sets the password for the amina user to amina@123.

     ☑️ Storage (Data Persistence)
     . -v portfolio-db-vol:/var/lib/postgresql/data: Creates a volume link (-v). It connects a folder on your physical computer (portfolio-db-vol) to the folder inside the container where PostgreSQL stores its data (/var/lib/postgresql/data).
     




