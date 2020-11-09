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
-	[Build_kernel script](https://github.com/s3437526/USAP_Assignment2)
-	[Project report - pending](https://duckduckgo.com)
-	[Install_manual script](https://github.com/s3437526/USAP_Assignment2/tree/develop/manual)
-	[?]()

***

:page_with_curl: **Resources used**


***

:computer: **Running the program**

***Building the kernel***

To run the program run the build_kernel script using the `./build_kernel` command in the directory which contains the script file. For example, if the script is located in /home/pi/ directory then run the script from that location.

The process will automatically download and install all the pre-requisites and commence the setup, build and installation of the kernel.

***Installing manual pages***

The install_manual script is run automatically on completion of the kernel instalaltion and therefore does not require explicit calling. If, however, you choose to run it, simply run it from the directory in which it resides by running the `./install_manual` command.

On successful completion the installation will reboot the Raspberry Pi.

***

:paperclip: **Additional comments about the program**

Manual pages for the build_kernel and install_manual scripts can be run using the man command as follows: `man build_kernel` and `man install_manual`.

The following steps were taken during the .config file creation to disable camera support:

****
![Alt text](/assets/images/Abilis AS102 DVB receiver.png "Mouseover text")
![Alt text](/assets/images/camera.png "Mouseover text")
![Alt text](/assets/images/search_cam.png "Mouseover text")
![Alt text](/assets/images/cam.png "Mouseover text")
![Alt text](/assets/images/v4l.png "Mouseover text")
![Alt text](/assets/images/bcm2835_camera_support.png "Mouseover text")

***

![Tux, the Linux mascot](/assets/images/tux.png)
[Duck Duck Go](https://duckduckgo.com)
<https://www.markdownguide.org>
<fake@example.com>
