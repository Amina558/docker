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


# Inside the docker
1. command = whoami: this command asks the system who is the current user logged in right now
2. command = echo "hey im merry" > hello.txt : this create file named hello.txt and write a sentence "hey im merry"
3. command = ls :lista the files and folder
4. command = cat hello.txt : this command open the files and display the contents directly on the screen
<img width="1920" height="211" alt="image" src="https://github.com/user-attachments/assets/9b1946e7-cb8c-404d-9ac7-21dfb6112ecd" />


# exit
<img width="1920" height="95" alt="image" src="https://github.com/user-attachments/assets/c768493b-e55f-4bd4-a9e0-e2fcb60110b3" />

# List the docker
command = sudo docker container ls -a
<img width="1920" height="243" alt="image" src="https://github.com/user-attachments/assets/717c159c-3d66-4c87-bb38-a0799c68a1d6" />




