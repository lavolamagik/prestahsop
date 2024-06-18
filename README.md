# INSTALAR DOCKER COMPOSE
sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
sudo apt update
sudo apt install docker-ce

# INSTALAR DOCKER-COMPOSE
sudo curl -L "https://github.com/docker/compose/releases/download/1.26.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version

# INSTALAR GIT
sudo apt install git -y
git clone https://github.com/lavolamagik/prestahsop.git

#ACTIVAR LOS CONTENEDORES
cd prestahsop/
sudo docker-compose up -d
