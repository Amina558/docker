# Docker Port Mapping
The process of building a specific port on the host machine to specific port inside the docker container
   
             
                              
  localhost      8080 → 80         Apache      
    :8082      ------------->       :80 
    [ External User / Browser ] 
          │
          ▼ (Traffic hits Host Port 8082)
   ┌──────────────┐
   │  Docker Host │
   └──────┬───────┘
          │ (Docker Network Bridge)
          ▼ (Traffic forwarded to Container Port 80)
   ┌──────────────┐
   │  Container   │ (Runs apache/Web App)
   └──────────────┘

 # 8082-----> host port number
 ▶️ always put in left side 
 # 80--------> container port number 
 ▶️ always put in right side 

 # Run Apache 
 Command = sudo docker run -dt --name my-website -p 8082:80
 
 1. docker run:Tells Docker to create and start a new container from a specified image.
 2. -dt: d stands for detached. Runs the container in the background
 3. --name my-website: Assigns a custom name (my-website) to your container so you can easily reference or stop it later instead of using an automatically generated random name.
 4. -p 8082:80: (port mapping): Maps port 8082 on your host machine (left) to port 80 inside the container (right).
 5. httpd: The name of the Docker image used to build the container.

<img width="1920" height="1080" alt="Screenshot (899)" src="https://github.com/user-attachments/assets/56261223-1cb5-452a-9078-bec668181e39" />
<img width="1920" height="1080" alt="Screenshot (900)" src="https://github.com/user-attachments/assets/d2f73bf4-8b9a-4b50-b8a2-0d49427da43f" />

# website page

<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/1a187d3a-73ef-4203-a29d-5dae7715acfc" />



    
