## Network Video Recorder
Turn your Raspberry PI spare Linux or MacOSdevice into a 4 channel IP Camera Network Video Recorder.

### Features

- 1 to 4 IP camera channels
- Disoverable by 3rd party client software
- Continuous recording
- Motion detection
- Video playback with motion events

### License
This software is free to use for home enthusiasts or for evalution by developers and system integrators looking to build their own products on the core funrtionality.

## Installation

### Raspberry Pi OS Requirements
The software requires a 64bit version of bullseye, preferably running on a Pi 4 but also works on the Raspberry Pi 3B+

### Linux OS Requirements
This software requires an Intel/AMD 64bit processor to run.

NOTE: The software has only been tested on Ubuntu 22.04

### MacOS Requirements
A 64-bit Intel CPU or Apple Silicon CPU
macOS Ventura (13) (or higher) 

### Network Requirements
Make sure the device this software is installed on is connected to the same network as your IP cameras.

### Raspberry Pi (bullseye)
#### Install and Run (latest version)

```sh
wget -c https://incax.com/vnvr/vnvr-linux-arm64.tar.gz -O - | tar -xz  && cd vnvr-linux-arm64 && sudo chmod +x configure && sudo ./configure && sudo ./nx-vnvr
```

### Ubuntu (linux x64)
#### Install and Run (latest version)

```sh
wget -c https://incax.com/vnvr/vnvr-linux-ubuntu64.tar.gz -O - | tar -xz && cd vnvr-linux-ubuntu64 && sudo chmod +x configure && sudo ./configure && sudo ./nx-vnvr
```
### Linux Install any missing dependencies
If the software prompts you, please install the missing dependences

You may be prompted to install one or both of the following

```sh
sudo apt install -y ffmpeg
sudo apt install -y gpac
```
Then run the software

### MacOS  Ventura (13) or higher
#### Download and setup

```sh
wget -c https://incax.com/vnvr/nx-vnvr-osx-install.tar.gz -O - | tar -xz && cd nx-vnvr-osx-install && chmod +x nx-vnvr
```
#### Install Homebrew

https://docs.brew.sh/Installation

#### Update homebrew 

```sh
brew update
```
```sh
brew upgrade
```

#### Install dependenicies

```sh
brew install ffmpeg
```
```sh
brew install mediamtx
```
```sh
brew install gpac
```
#### Run
```sh
./nx-vnvr
```


### How to run application

From the install directory
#### Linux
From installation folder
```sh
sudo ./nx-vnvr
```
#### MacOS
From installation folder
```sh
./nx-vnvr
```
### Camera discovery

On startup the software wil do a quick multicast discovery check and output information to the console.

For example:

```sh
TESTING MULTICAST DISCOVERY...
MULTICAST DISCOVERY found 192.168.1.105
MULTICAST DISCOVERY found 192.168.1.100
MULTICAST DISCOVERY found 192.168.1.107
MULTICAST DISCOVERY found 192.168.1.108
MULTICAST DISCOVERY found 192.168.1.109
MULTICAST DISCOVERY 5 cameras found
```

If no cameras are discovered, please check that the device running this software is connected to the same network as your cameras.

---

### Set up your cameras
When you run the software it will output a web browser URL.

For example: where 192.168.1.105 is the Raspberry Pi's IP address

```sh
-------------------
WEB BROWSER URL
http://192.168.1.102:8127/web
-------------------
```

Note: If the IP address displayed is 127.0.0.1 then check your network connection for the LAN IP address. Theh pass that IP address as a parameter.

For example:
```sh
sudo ./nx-vnvr 192.168.1.105
```

Best to use a different computer to access the web page.

## Web User Interface

When you first connect to the web page the software will search for IP cameras on your network.

If successful you will see the CAMERA CHANNELS window.

### Camera Channels
Start with Channel #1 and click "Select camera"

Next select a camera from the dropdown list then enter the cameras' login details.

Click "Connect" and if authenticated OK, then click "Save"

The camera will now appear in the web page.

Repeat for your remaining three cameras.

### Latency in web interface
There is some latency when viewing the live camera streams via the web browser user interface due to conversion to HLS.

Use one the client apps below to view the streams more effeciently.

## iOS, MacOs and Window's client apps
You can access the NVR via your iPhone, Mac or Windows PC using the free NX-V IP Camera viewer app available in the respective app store, links below.

[NX-V apps page](https://nx-v.uk)

			
