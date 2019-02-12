# pi-mqtt-sensor-bme680-container
Container that will read BME680 sensor data and output as MQTT on topic of choice. Created for Nutanix Xi-IoT but can be used with any MQTT Broker.


# Requires Docker and Docker Compose to install... 

sudo apt-get update
curl -fsSL get.docker.com -o get-docker.sh && sh get-docker.sh
sudo apt-get install -y python python-pip
pip install docker-compose

# to add the current user to the docker group and remove the need for sudo docker user:-

sudo groupadd docker
sudo gpasswd -a $USER docker

# test with:-

docker run hello-world

#Container start
edit the app.py file adding you mqtt broker address and topic
docker-compose build
docker-compose up -d