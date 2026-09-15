# Run Ubuntu Interactive Container 
# Pull Ubuntu image 
command = [sudo docker pull ubuntu]
<img width="1920" height="217" alt="image" src="https://github.com/user-attachments/assets/4a42a916-bc70-4adb-877b-d4c6d8df2b84" />
# Run Ubuntu Interactive Container
command = [sudo docker run -it ubuntu /bin/bash]
<img width="1920" height="72" alt="image" src="https://github.com/user-attachments/assets/7e3c7ee1-eb36-4843-95ec-662381298737" />
# Check current user
 command = [whoami]
 <img width="1920" height="84" alt="image" src="https://github.com/user-attachments/assets/d8780a35-a984-486f-81aa-41bb807bac3a" />
 # check files
 commands = [ls]
 <img width="1920" height="365" alt="image" src="https://github.com/user-attachments/assets/3837e944-9660-43c3-a156-e8348f314230" />
 # Check ubuntu version
 commandsb = [cat /etc/os-release]
 <img width="1920" height="353" alt="image" src="https://github.com/user-attachments/assets/1f4170f7-4499-43db-94d0-d5ce2d74e4c7" />
 # create a new Container 
 commands = [sudo docker run -d --name my-ubuntu-container ubuntu]
 1. docker run: the main command that tells docker to create and start a new container.
 2. -d: stands for detached.
 3. --name my-ubuntu-container: This gives your container a friendly, custom nickname (my-ubuntu-container) so you can easily stop or delete it later using that name instead of a random number.
 4. ubuntu: This is the official image docker will used to built the container.
    
 check [sudo docker container ls -a]
 <img width="1920" height="284" alt="image" src="https://github.com/user-attachments/assets/0244b842-571c-44ee-a036-6ba0720dab74" />
# Login into that container(hey-dc-ubuntu)
 commands = sudo docker exec -it hey-dc-ubuntu /bin/bash
 
<img width="1920" height="187" alt="image" src="https://github.com/user-attachments/assets/5347d0f0-0af0-44b5-9fc0-064de3b45644" />

<img width="1920" height="251" alt="image" src="https://github.com/user-attachments/assets/1b6edfd1-c547-47b8-b949-2a5669991eb6" />




 





