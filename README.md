# flask-app-ecs
Simple flask app to be run on ECS
# Docker need to be install
apt install docker.io

sudo systemctl start docker
sudo systemctl enable docker

# add the current user into docker group
sudo usermod -aG docker $USER
newgrp docker

# To build and run this 

docker build -t flask-app .

docker run -d -p 80:80 flask-app

# Allow the required port in aws console and try to access via public ip 
