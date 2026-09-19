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
    List volumes: docker volume ls  
<img width="1920" height="256" alt="image" src="https://github.com/user-attachments/assets/92d4cbbb-f4bf-4025-9427-699bdaee6c43" />




