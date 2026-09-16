# Docker Container Lifecycle


☑️Key Lifecycle States
1. Created: Prepared but not yet active
2. Running: Actively execution its main
3. Paused: Processes are suspended in memory
4. Stopped: Gracefully or Abruptly Halted
5. Deleted: Permanently wiped out from the host

♦️State Focus: Created state 
🥇What Happen: Docker sets up a thin writable meta data layer over the read only image 
. commands = sudo docker create --name lifecycle-container ubuntu
# Explanation
. docker: Calls the Docker Command Line Interface (CLI) program to interact with the Docker engine.
. create Tells Docker to prepare and set up a new container in the Created state, keeping it ready to run later
. --name lifecycle-container: Assigns the custom name lifecycle-container to this specific container so you can manage or start it using a memorable name instead of an automatically generated container ID
. ubuntu: Specifies the base Docker image to build the container from.
