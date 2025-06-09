# tita-app
This is the official release package for the tita app

## Instructions:

### (1) Install deb on Tita:
    sudo dpkg -i tita-app.deb
If there are no errors, it is considered successful
### (2) Set app account password:
    sudo vi /usr/tita-app/config.json
Set the account password for the ros2 namespace, such as titan3037211. Please enter the ros2 topic list to query. Set the password yourself and save it for future login use.
This is a demonstration：
{
    "mqtt_username": "tita3037211",
    "mqtt_password": "12345678"
}
### (3) Set app account password:
