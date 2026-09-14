# INSTALLATION OF DOCKER

STEPS TO INSTALL DOCKER 

# Add Docker's Official GPG Key
sudo apt update
sudo apt install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

> Add the repository to Apt sources:

# sudo tee /etc/apt/sources.list.d/docker.sources <<EOF
# Types: deb
# URIs: https://download.docker.com/linux/ubuntu
# Suites: $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}")
# Components: stable
# Architectures: $(dpkg --print-architecture)
# Signed-By: /etc/apt/keyrings/docker.asc
# EOF


# sudo apt update

2. INSTALL THE DOCKER PACKEGES.
   To install the latest version, run:
# sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin



3. AFTER INSTALLATION VERIFY DOCKER IS RUNNING
  # sudo systemctl start docker
  # sudo systemctl status docker

  <img width="1920" height="965" alt="image" src="https://github.com/user-attachments/assets/055fd044-713d-41fa-8f0c-a727fb6885b9" />

  <img width="658" height="80" alt="image" src="https://github.com/user-attachments/assets/eb7e5b1b-2e79-4e3a-b0d5-1dc983a2a0fa" />



       
