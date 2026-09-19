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




