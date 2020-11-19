# USAP Assignment 2
## By Aleksandar Alduk S3437526
### CPT264 – UNIX (Linux) Systems Administration and Programming (USAP), Study Period 3, 2020

***

:question: **Purpose**

This program was designed to automate the build and compilation of a custom kernel script which includes changes from the baseline kernel image.

**NOTE:** This is written to run on a Raspberry Pi 4 armhf architecture.

***

:open_file_folder: **Files in the project**

The main user interactive files in the project are:
-	[Build_kernel script (this page)](https://github.com/s3437526/USAP_Assignment2)
-	[Phoronix Performance Report](tests/results/PhoronixTest_Results.md)
-	[Install_manual script and manuals](manual)
-	[Config_generator script (this page)](https://github.com/s3437526/USAP_Assignment2)
-	[Tests/Results](tests)

These need to be changed to the MASTER URL!!!

***

:computer: **Running the program**

***Building the kernel***

To run the program run the build_kernel script using the `./build_kernel` command in the directory which contains the script file. For example, if the script is located in /home/pi/ directory then run the script from that location.

The process will automatically download and install all the pre-requisites and commence the setup, build and installation of the kernel.

***Installing manual pages***

The install_manual script is run automatically on completion of the kernel instalaltion and therefore does not require explicit calling. If, however, you choose to run it, simply run it from the directory in which it resides by running the `./install_manual` command.

On successful completion the installation will reboot the Raspberry Pi.

***Generating .config file***

This script is ***NOT*** required to be run if there is already a working version of the .config file in the root directory. If, however, there is a desire to create a new .config file, it may be run as follows:

`./config_generator [local_IP_address]`where "local_IP_address" is the client computer's local network IP address. This is used for the purpose of exporing the kernel setup GUI to the user.
Be sure that xterm is correctly setup, and the ***CORRECT*** local IP address is being used.

Read the manual page for the config_generator script for more information.

***

:paperclip: **Additional comments about the program**

Manual pages for the build_kernel, install_manual, and config_generator scripts can be run using the man command as follows: `man build_kernel`, `man install_manual`, and `man config_generator` respectively.

The following steps were taken during the .config file creation to disable camera support:

||
|:----------------------------------------------------------------------------:|
|Searched for "Abilis AS102 DVB receiver" term and disabled all returns|
|![Abilis AS102 DVB receiver disabled](/assets/images/Abilis%20AS102%20DVB%20receiver.png "Abilis AS102 DVB receiver")|
||
|Searched for "camera" term and disabled all returns|
|!["Camera" xterm search query items disabled](/assets/images/camera.png "Camera driver disabled")|
||
|Searched for "cam" term and disabled all returns|
|![Webcam disabled](/assets/images/search_cam.png "Webcam driver disabled")|
||
|Disabled webcam gadget|
|!["Cam" search pattern query disabled](/assets/images/cam.png "Cam driver disabled")|
||
|Searched for "V4L" and disabled all returns|
|!["V4L" video drivers search disabled](/assets/images/v4l.png "V4L drivers disabled")|
||
|Searched for "BCM2835 Camera" and disabled returns|
|![BCM2835 camera support disabled](/assets/images/bcm2835_camera_support.png "BCM2835 camera disabled")|

***
