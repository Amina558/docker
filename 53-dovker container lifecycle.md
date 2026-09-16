# Docker Container Lifecycle


☑️Key Lifecycle States
1. Created: Prepared but not yet active
2. Running: Actively execution its main
3. Paused: Processes are suspended in memory
4. Stopped: Gracefully or Abruptly Halted
5. Deleted: Permanently wiped out from the host

# ♦️State Focus: Created state 
🥇What Happen: Docker sets up a thin writable meta data layer over the read only image 
. commands = sudo docker create --name lifecycle-container ubuntu
# Explanation

1. docker: Calls the Docker Command Line Interface (CLI) program to interact with the Docker engine.
2. create Tells Docker to prepare and set up a new container in the Created state, keeping it ready to run later
3. --name lifecycle-container: Assigns the custom name lifecycle-container to this specific container so you can manage or start it using a memorable name instead of an automatically generated container ID
4. ubuntu: Specifies the base Docker image to build the container from.

<img width="1920" height="734" alt="image" src="https://github.com/user-attachments/assets/bdc7b9f9-da91-47cd-8137-291ff0fb25d6" />

♦️Status Focus: Running State
🥇What Happen: The primary process begins execution inside the isolated space
. commands = sudo docker start lifecycle-container

<img width="1920" height="77" alt="image" src="https://github.com/user-attachments/assets/a64826b3-71f2-4e78-85a1-1ea498cd52b7" />

