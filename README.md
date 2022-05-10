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
![image](https://user-images.githubusercontent.com/9034375/167426186-51403794-e509-4488-bf08-ed59074661d7.png)


## add username password
### method 1
create a password.txt file
add useres in format

user1:password
user2:password

save and encrpyt the passwords with the command

```
mosquitto_passwd -U passwordfile

```

### method 2

```
mosquitto_passwd -c passwordfile user1

# add user2 to file

mosquitto_passwd -b passwordfile user2 password

# delete a user

mosquitto_passwd -D passwordfile user

# 

```
