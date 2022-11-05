## Virtual Network Video Recorder for IP cameras
Turn your Raspberry PI or spare Linuz box into a 4 channel IP Camera Network Video Recorder.

### License
This software is free to use for home enthusiasts or for evalution by other developers and system integrators looking to build their own products on the core funrtionality.

## Raspberry Pi NVR Installation

### OS Requirements
The software requires a 64bit version of bullseye, preferably running on a Pi 4

##N etwork Requirements
Make sure your Raspberry Pi is connected to the same network as your IP cameras.

### Download

```sh
wget -c https://xtreme-iot.online/CloudGlu/download/vnvr-linux-arm64.tar.gz -O - | tar -xz
```
```sh
cd vnvr-linux-arm64
```

### Prepare
```sh
sudo chmod +x configure
sudo ./configure
```
### To run
```sh
sudo ./nx-vnvr
```

### Install any missing dependencies
If the software prompts you, please install missing dependences

```sh
sudo apt install -y ffmpeg
sudo apt install -y gpac
```
### Set up your cameras
When you run the software it will output a web browser URL.

For example: where 192.168.1.105 is the Raspberry Pi's IP address

```sh
-------------------
WEB BROWSER URL
http://192.168.1.102:8127/web
-------------------
```

Best to use a different computer to access the web page.

### Camera discovery
When you first connect to the web page the software will search for IP cameras on your network.

If successful you will see the CAMERA CHANNELS window.

### Camera Channels
Start with Channel #1 and click "Select camera"

Next select the camera from the dropdown list and enter the cameras' login details.

Click "Connect" and if authenticated OK, then click "Save"

The camera will now appear in the web page.

Repeat for your remaining three cameras.

### iOS, MacOs and Window's client apps
You can access the NVR via your iPhone, Mac or Windows PC using the NX-V IP Camera viewer app available for free in the respective app stores.

			
