# tita-app
This is the official release package for the tita app

## Instructions:

### (1) Install deb on Tita:
    sudo dpkg -i tita-app.deb
If there are no errors, it is considered successful
### (2) Set app account password:
    sudo vi /usr/tita-app/config.json
Set ros2 namespace as account, such as titan3037211. Please enter the "ros2 topic list" to query. Set the password yourself and save it for future login use.
This is a demonstration：
{
    "mqtt_username": "tita3037211",
    "mqtt_password": "12345678"
}
### (3) Install APK on your Android device：
Please click on the following link to download
### (4) APK login
If you have not activated VIP and can only use offline mode, please skip login and select "跳过"，
please contact wuyunzhou@directdrivetech.com And provide your account password for VIP authorization,then you can log in with VIP account password.
### (5) APK Function Introduction
APK features include USB joystick, virtual joystick, and Bluetooth joystick，Offline mode can only use Bluetooth joystick.
#### Bluetooth Joystick User Manual
Restart Tita, it will enter Bluetooth pairing mode within 30 seconds of startup. Please complete Bluetooth pairing within 30 seconds.

<img src="https://github.com/user-attachments/assets/eebbe82c-5961-4f8a-b2d8-24ed1a350aac" width="300" />
<img src="https://github.com/user-attachments/assets/1573cc04-ac11-4967-aa17-710eba5f095a" width="300" />


