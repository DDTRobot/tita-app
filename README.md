# tita-app（V1.0.1）
This is the official release package for the tita app, based on Android.

## Instructions:

### (1) Install deb on Tita:
```bash
    #In TITA:
    git clone https://github.com/DirectDriveTech-DDT/tita-app.git
    cd tita-app
    sudo dpkg -i tita-app.deb
```

If there are no errors, it is considered successful
### (2) Set app account password:
    sudo vi /usr/tita-app/config.json
Set ros2 namespace as account, such as tita3037211. Please enter the "ros2 topic list" to query. Set the password yourself and save it for future login use.
This is a demonstration：
{
    "mqtt_username": "tita3037211",
    "mqtt_password": "12345678"
}
### (3) Install APK on your Android device：
Please click on the following link to download

[Download the app](https://github.com/DDTRobot/tita-app/blob/main/tita-app.apk)

### (4) APK login
If you have not activated VIP and can only use offline mode, please skip login and select "跳过"，
please contact wuyunzhou@directdrivetech.com And provide your account password for VIP authorization,then you can log in with VIP account password.

<img src="https://github.com/user-attachments/assets/39e30cfa-4601-4ff2-81a6-bd3700af9693" width="400" />

### (5) APK Function Introduction
APK features include USB joystick, virtual joystick, and Bluetooth joystick，Offline mode can only use Bluetooth joystick.
#### Bluetooth Joystick User Manual
Restart Tita, it will enter Bluetooth pairing mode within 30 seconds of startup. Please complete Bluetooth pairing within 30 seconds.

<img src="https://github.com/user-attachments/assets/eebbe82c-5961-4f8a-b2d8-24ed1a350aac" width="400" />
<img src="https://github.com/user-attachments/assets/1573cc04-ac11-4967-aa17-710eba5f095a" width="400" />
<img src="https://github.com/user-attachments/assets/f1d33550-bf4c-4a98-99e3-336234f5c44a" width="400" />
<img src="https://github.com/user-attachments/assets/23b11757-ed28-4b14-bafc-38b50418a9a3" width="400" />
<img src="https://github.com/user-attachments/assets/6e236953-625a-4101-ae36-cc52e8837148" width="400" />
<img src="https://github.com/user-attachments/assets/d85cad87-4f3f-4784-aaee-22a6c20af0ff" width="400" />
<img src="https://github.com/user-attachments/assets/27cfc651-f41d-446b-9107-22c3cca3d56e" width="400" />
<img src="https://github.com/user-attachments/assets/384c828d-c473-4548-a288-fa7a637deeab" width="400" />
<img src="https://github.com/user-attachments/assets/fc899c43-7a24-418d-b275-9a2aea5a981a" width="400" />

If your Android device is on the same LAN as Tita, Tita will be scanned. If it is not scanned, please repeat the operation and rescan.
If there are multiple Titas in the local area network, please manually select them.

<img src="https://github.com/user-attachments/assets/1e2908b8-67f1-4c5f-b316-b39529141653" width="400" />

<img src="https://github.com/user-attachments/assets/55a19d6f-1d12-48c6-a081-37a14aeff1fc" width="400" />


Bluetooth currently supports enabling follow mode: QR code follow, gesture follow. Please note that only one of the following three functions can be opened at a time.





<img src="https://github.com/user-attachments/assets/35515782-89c3-44a0-9c6e-6c0b743fa8f0" width="400" />





#### Virtual Joystick User Manual
This feature requires VIP authorization to log in and use.Through this method, 
you will be able to remotely control Tita from thousands of miles away.


<img src="https://github.com/user-attachments/assets/205a12e2-1715-4339-8ba7-93832e73ca53" width="400" />
<img src="https://github.com/user-attachments/assets/f2f08b1e-4f61-419c-ba89-c0a1bee1c5e6" width="400" />
<img src="https://github.com/user-attachments/assets/9a5e3103-dd4c-451e-a83c-180fd483df86" width="400" />
<img src="https://github.com/user-attachments/assets/7def1355-7202-47fd-a755-379f30eccd62" width="400" />
<img src="https://github.com/user-attachments/assets/40e4b58e-2a01-4847-8281-b380238c96f1" width="400" />


This also supports enabling follow mode: QR code follow, gesture follow. Please note that only one of the following three functions can be opened at a time.


<img src="https://github.com/user-attachments/assets/35515782-89c3-44a0-9c6e-6c0b743fa8f0" width="400" />




#### USB Joystick User Manual
This feature requires VIP authorization to log in and use.Through this method,
you will be able to remotely control Tita from thousands of miles away.


<img src="https://github.com/user-attachments/assets/dfcc2ebf-b961-4a7e-ab94-e5a3c30a182f" width="400" />


This feature requires the purchase of our USB accessory, as shown in the picture. 
By connecting the USB accessory to an Android device, it can be controlled with a remote control
and image transmission and reception can be achieved on the Android device.

<img src="https://github.com/user-attachments/assets/58888cad-bc9a-49f2-99db-ae8f6f30dfc5" width="400" />
<img src="https://github.com/user-attachments/assets/197418f1-a39e-4ce0-a01e-1686a6c8aa3c" width="400" />


<img src="https://github.com/user-attachments/assets/062ec300-baa0-4981-8765-650bc5a1511f" width="400" />

<img src="https://github.com/user-attachments/assets/845c0f0d-77bc-4f51-b765-da2dae4876e8" width="400" />


Select USB device,and view Image

This also supports enabling follow mode: QR code follow, gesture follow. Please note that only one of the following three functions can be opened at a time.

<img src="https://github.com/user-attachments/assets/35515782-89c3-44a0-9c6e-6c0b743fa8f0" width="400" />

### (6) Customer LAN image transmission development interface
        ffmpeg -re -i /dev/video2        -c:v libx264 -profile:v baseline -preset ultrafast -tune zerolatency        -pix_fmt yuv420p -g 30        -rtsp_transport tcp -f rtsp rtsp://192.168.100.197:8554/test
Deb has integrated SRT and WebRTC ultra-low latency image transmission to local servers（Delay as low as 100ms at 60 frames per second）. Refer to the above instructions to push the stream.(Change 192.168.100.197 to your LAN IP address,and change your video dev)
For more parameters, please refer to the official ffmpeg tutorial.

![屏幕截图 2025-06-09 144016](https://github.com/user-attachments/assets/0dca1307-f9ef-476a-abeb-f2a1a6457036)
![屏幕截图 2025-06-09 142135](https://github.com/user-attachments/assets/b642e219-719c-46a7-84ec-531d092e8fa4)
![image](https://github.com/user-attachments/assets/4a854062-70ae-4027-be04-58b8ee6219fa)



Browser WebRTC Streaming Test：

![image](https://github.com/user-attachments/assets/9a61825d-915a-4fed-8bad-a556a4d0f57b)


To our incredible clients: ​​Thank you for growing with us.​​ You didn’t just use our product; you helped shape it. When we were a fledgling solution with ambitious dreams, you chose to believe. Your feedback became our blueprint, your challenges our compass, and your trust our foundation.
﻿
We often call early versions a ‘minimum viable product,’ but to us, it felt like sending a child into the world. And you—our pioneering partners—​​nurtured it as your own​​. You patiently endured bugs, advocated for features, and celebrated every upgrade. Your partnership transformed our ‘baby’ into what it is today: stronger, smarter, and more resilient.
﻿
Thank you for being more than clients. Thank you for being believers, collaborators, and the reason we strive for excellence.If you have any questions, please contact wuyunzhou@directdrivetech.com




