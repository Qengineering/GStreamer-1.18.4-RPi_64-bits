# GStreamer-1.18.4-RPi_64-bits
![output image]( https://qengineering.eu/images/GStreamer_32_30FPS.webp )<br/>
## GStreamer + OpenCV on a Raspberry Pi 4
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)<br/><br/>
An working example of the GStreame 1.18.4.<br/>
It works on a Raspberry Pi with an 32 or 64-bits OS.<br/>
If you want to use the new 32-bits **rpicamsrc** see https://github.com/Qengineering/GStreamer-1.18.4-RPi_32-bits <br/>

------------

## Dependencies.<br/>
To run the application, you have to:
- A Raspberry Pi 4. 
- GStreamer 1.18.4 installed. [Install GStreamer](https://qengineering.eu/install-gstreamer-1.18-on-raspberry-pi-4.html) <br/>
- OpenCV 64 bit installed. [Install OpenCV 4.5](https://qengineering.eu/install-opencv-4.5-on-raspberry-64-os.html) <br/>
- Code::Blocks installed. (```$ sudo apt-get install codeblocks```)
- A working Raspicam or Webcam

------------

## Installing the app.
To extract and run the app in Code::Blocks <br/>
$ mkdir *MyDir* <br/>
$ cd *MyDir* <br/>
$ wget https://github.com/Qengineering/GStreamer-1.18.4-RPi_64-bits/archive/refs/heads/main.zip <br/>
$ unzip -j master.zip <br/>
Remove master.zip, LICENSE and README.md as they are no longer needed. <br/> 
$ rm master.zip <br/>
$ rm LICENSE <br/>
$ rm README.md <br/> <br/>
Your *MyDir* folder must now look like this: <br/> 
GStreamerTest64.cpb <br/>
main.cpp <br/>

------------

## Running the app.
To run the application load the project file GStreamerTest64.cbp in Code::Blocks.<br/> 
Next, follow the instructions at [Hands-On](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html#HandsOn).<br/>
On this [page](https://qengineering.eu/install-gstreamer-1.18-on-raspberry-pi-4.html) you can see how to make the **webcam** work.

------------

## Frame rate.
The Raspicam supports many sizes and frame rates, as you can see [here](https://www.raspberrypi.org/documentation/raspbian/applications/camera.md).<br/>
You can switch between the different options by altering the parameters in the pipeline.<br/>
As long it's a valid combination, it will work. For instance:<br/>
```
    //pipeline parameters
    int capture_width = 640 ;
    int capture_height = 480 ;
    int display_width = 640 ;
    int display_height = 480 ;
    int framerate = 90 ;
```

![output image]( https://qengineering.eu/images/GStreamer_32_90FPS.webp )<br/>
