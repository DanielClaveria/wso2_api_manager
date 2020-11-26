# wso2_api_manager

# Instalación de Docker

```bash
apt-get update
apt-get install apt-transport-https ca-certificates curl softwareproperties-common
apt-get update
apt-get install docker-ce
docker - -version
```
# Instalación de docker-compose

Referencia:
https://docs.docker.com/compose/install/

```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

# Clonar repositorio
como root:

#crear carpeta de trabajo: 
mkdir /opt/wso2



#Clonar repositorio

```bash
git clone https://github.com/DanielClaveria/wso2_api_manager.git
```

