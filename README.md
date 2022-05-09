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

## Connection is refused edit /etc/mosquitto/conf.d/mosquitto.conf add to the bottom of file.

```
allow_anonymous true
listener 1883 0.0.0.0

```
## node-red setup
![Alt text](./images/Node-Red.png?raw=true "NODE-RED")
