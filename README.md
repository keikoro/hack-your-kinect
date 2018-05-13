# Hack your Kinect!
Info on how you can connect a Kinect to a computer and do stuff with it with the Python programming language (yay!).

## Background
This README is a complementary resource to a poster with the same title first presented at PyCon US 2018. It is currently a work in progress, so please bear with me while I continue to add more info.

## Hardware requirements
- a Microsoft Kinect
- a USB adapter for the right Kinect version; I highly recommend getting one of the original adapters by MS as I've both read online and heard first-hand accounts of cheaper copycat versions having caught fire*
- a Linux, MacOS or Windows machine
- a USB 3.0 port if you want to use the Kinect v2

*You can also find information on how to make your own Kinect (v2) USB adapter [in](https://www.reddit.com/r/xboxone/comments/7hstnk/xbox_one_x_kinect_adapter_diy/
) [several](https://www.reddit.com/r/xboxone/comments/7e02ne/xbox_one_x_kinect_power_mod/) [places](https://groups.google.com/forum/#!topic/openkinect/QFAetsTJrAA) on the web, and while I cannot vouch for any of these tutorials personally, I am using a Kinect v2 with a DIY adapter myself.

### Kinect versions
There are two different Kinect generations:
- The older Kinect for the Xbox 360 ("v1") with round corners
- The newer Kinect for the Xbox One ("v2") with square edges

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

## Resources / Credits / Thank You's / Contributors
Section for listing resources, giving credit, listing people who helped with the project & similar. Might also make sense as 2+ separate sections.

## Version History
v0.1 - 2018-05-13


