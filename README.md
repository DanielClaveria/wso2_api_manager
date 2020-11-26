# wso2_api_manager

# Instalación de Docker

Referencia: https://docs.docker.com/engine/install/ubuntu/

* con usuario root
```bash
apt-get update

sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
    
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo apt-key fingerprint 0EBFCD88

sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

apt-get update

#Instalar Docker
sudo apt-get install docker-ce docker-ce-cli containerd.io

#validar instalación
docker --version
```

# Instalación de docker-compose

Referencia: https://docs.docker.com/compose/install/

```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

#modificar permisos para ejecuta
sudo chmod +x /usr/local/bin/docker-compose

#verificar instalación
docker-compose --version
```

# Descargar códigos fuentes

* como root:

```bash
#crear carpeta de trabajo: 
cd /opt
mkdir wso2apimanager.fraccion.cl

#Clonar repositorio

git clone https://github.com/DanielClaveria/wso2_api_manager.git
```
# Configuración temporal de api-manager.

```bash
#editar archivo de configuración de ApiManager
nano /opt/wso2/wso2_api_manager/conf/apim/repository/conf/deployment.toml
```
* modificar hostname indicando la IP del server.
* Está forma no es óptima, se recomienda manetener localhost y utilizar dominio gestionado por nginx y certificado SSL

hostname = "[11.11.11.11]"

# Instalar Api Manager + MySql Server

```bash
#en la carpeta creada por git clone, ejecutar script el docker-compose

cd /opt/wso2/wso2_api_manager

#ejecuta la "receta" docker definida por el docker-compose
docker-compose up -d
```

# validar acceso a los servicios WSO2 Api Manager:

* https://TU.IP.PUBLICA:9443/carbon
* https://TU.IP.PUBLICA:9443/publisher
* https://TU.IP.PUBLICA:9443/devportal



