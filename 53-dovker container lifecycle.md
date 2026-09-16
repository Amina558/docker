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
.docker 
