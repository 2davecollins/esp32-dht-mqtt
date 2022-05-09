# Configuration manual

## Set up MQTT Broker on Ubuntu
```code
sudo apt-add-repository ppa:mosquitto-dev/mosquitto-ppa
sudo apt-get update
sudo apt-get install mosquitto
sudo apt-get install mosquitto-clients
sudo apt clean

systemctl status mosquitto.service
systemctl stop mosquitto.service
systemctl start mosquitto.service

```
