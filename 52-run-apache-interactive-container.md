# Run Apache Interactive Container
# pull Apache image from docker hub
commands = [sudo docker pull httpd]
commands = [ sudo docker run -it httpd /bin/bash]
1. docker: this tells our computer to open the docker software
2. run: this tools create and run the container
3. -it: this stands for interactive terminal
4. httpd: this is the name of app we want to use .httpd is Apache Web Server, a tool to host websites
5. /bin/bash: This tells the container to open a command prompt (terminal) instead of starting the website
<img width="1920" height="350" alt="image" src="https://github.com/user-attachments/assets/a740001f-c0ef-4ab6-97a0-0c81431b3669" />
<img width="1920" height="103" alt="image" src="https://github.com/user-attachments/assets/a7c35175-3535-441b-964b-6742afe305de" />
# Inside the docker container
. commnand = whoami > This command ask the system who is the current user logged in right now
. command = echo "hey im merry" > hello.txt 
this 

