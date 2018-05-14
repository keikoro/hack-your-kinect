# Hack your Kinect!
Info on how you can connect a Kinect to a computer and do stuff with it with the Python programming language (yay!).

## Background
This README is a complementary resource to a poster with the same title first presented at PyCon US 2018. It is currently a work in progress, so please bear with me while I continue to add more info.

## Hardware requirements
- a Microsoft Kinect
- a USB adapter for the right Kinect version; I highly recommend getting one of the original adapters by MS as I've both read online and heard first-hand accounts of cheaper copycat versions having caught fire*
- a Linux, MacOS or Windows machine
- a USB 3.0 port if you want to use the Kinect v2

*You can also find information on how to make your own Kinect (v2) USB adapter in several places on the web, see references & further reading section below.

### Kinect versions
There are two different Kinect generations:
- Kinect v1: the older Kinect with round corners (Kinect for Xbox 360, Kinect for Windows)
- Kinect v2: the newer Kinect with square edges (Kinect for Xbox One, Kinect for Windows v2) 

Make sure you are getting the right adapter (drivers, libraries) for the Kinect generation you are planning to use.

## Drivers
There are two different projects/efforts regarding free drivers for using Kinects with a PC: **OpenKinect** and **OpenNI**. I am using the OpenKinect drivers personally, so I am going to list instructions for these first.

### Kinect v1

#### MacOS
Follow the instructions for MacOS listed in the [README for libfreenect](https://github.com/OpenKinect/libfreenect#osx). If you already use Homebrew (which I recommend you do), they boil down to:
```
$ brew install libfreenect
```

You can now run the test program included with the install:
```
$ freenect-glview
```

#### Linux
Depending on your Linux distribution, installing libfreenect might be as easy as running:
```
$ sudo apt-get install freenect
```

You should also install the `udev rules` [as explained in the libfreenect repo](https://github.com/OpenKinect/libfreenect/tree/master/platform/linux/udev).

For manual build instructions, see the full Linux instructions on [openkinect.org](https://openkinect.org/wiki/Getting_Started#Linux) and/or the [libfreenect repo's README](https://github.com/OpenKinect/libfreenect#linux).

## Contributing
I am looking to feature examples of Python scripts for either Kinect version which were inspired by my poster presentation or this repository, so if you have written a program you want to share, and if I also manage to get it working on my end, I would be happy to link it here. Please open an issue to make me aware of it!

## References & further reading
### General info
[Wikipedia page on Kinect](https://en.wikipedia.org/wiki/Kinect)  
[Microsoft page on Kinect for Windows](https://developer.microsoft.com/en-us/windows/kinect)  
[Specs comparison Kinect v1 vs. v2](http://www.imaginativeuniversal.com/blog/2014/03/05/Quick-Reference-Kinect-1-vs-Kinect-2/)

### Drivers and libraries
#### OpenKinect
[OpenKinect project](https://openkinect.org)  
[libfreenect](https://github.com/OpenKinect/libfreenect) drivers/libraries (Kinect v1)  
[libfreenect2](https://github.com/OpenKinect/libfreenect2) drivers/libraries (Kinect v2)  
[Python bindings for libfreenect2](https://github.com/37/py3freenect2) (for Kinect v2)

#### OpenNI
[OpenNI](https://structure.io/openni) resource page, incl. OpenNI 2 SDK binaries  
Fork of [PrimeSensor Modules](https://github.com/avin2/SensorKinect) for OpenNI + [patch](https://github.com/avin2/SensorKinect/pull/5)  
[Python bindings for OpenNI](https://github.com/jmendeth/PyOpenNI)

#### OpenKinect vs. OpenNI
[Stackoverflow post #1](https://stackoverflow.com/questions/6086981/what-is-the-difference-between-openni-and-openkinect)  
[Stackoverflow post #2](https://stackoverflow.com/questions/19181332/libfreenect-vs-openni)  

### Python libraries / tools to use with Kinect
[OpenCV-Python](https://docs.opencv.org/3.4.1/d6/d00/tutorial_py_root.html)  
[pygame](https://www.pygame.org)  

#### Processing
[Python mode for Processing](http://py.processing.org/)  
[How to use the Kinect with Processing](http://shiffman.net/p5/kinect/) (examples based on Java mode)  

### How-to make your own Kinect v2 adapter
Note: I have not done any of these tutorials/walk-throughs myself (yet), so cannot attest to their accuracy or helpfulness, but I am currently using a Kinect v2 with such a DIY adapter!

[How to Connect Kinect 2 for Xbox One with PC](https://stackoverflow.com/q/25952296/1923870) Stackoverflow post   
[DIY Kinect V2 adapter](https://groups.google.com/d/msg/openkinect/QFAetsTJrAA/SIyi5C12AQAJ) thread on OpenKinect Google group  
[DIY Kinect Adapter with Disassembly for Xbox One S, X and PC](https://youtu.be/7lQ93qzggos) YouTube video  
[Reddit thread 1](https://www.reddit.com/r/xboxone/comments/7e02ne/xbox_one_x_kinect_power_mod/)  
[Reddit thread 2](https://www.reddit.com/r/xboxone/comments/7hstnk/xbox_one_x_kinect_adapter_diy/) (incl. links to more YouTube videos)  

## Version History
v0.1.1 - 2018-05-14


