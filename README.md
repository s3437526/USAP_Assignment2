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

`./config_generator [local_IP_address]`where "local_IP_address" is the client computer's local network IP address. This is used for the purpose of displaying the kernel setup GUI to the user.
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


**Please note:** upon review of specification compliance, it was identified that the commits did NOT have my full name, rather only my student ID. in order to remedy this I attempted to amend this as early as possible to allow a significant portion to have the additional details, however, this change did not seem to take effect. I provide below screenshots of the .gitconfig file and git config --list files showing my credentials matching my github commits.  

|Screenshots|
|:----|
|.gitconfig file
|![.gitconfig file](/assets/images/gitconfig.png)
|gitconfig --list file
|![gitconfig --list file](/assets/images/gitconfig\ --list.png)|

***

:page_with_curl: **References/Bibliography**

A CLOUD CURU (2019). This XML file does not appear to have any stype information associated with it. The document tree is shown below. [https://acloud.guru/forums/aws-certified-cloud-practitioner/discussion/-LrQ4NJR-woGZ2R0k_sY/this_xml_file_does_not_appear](https://acloud.guru/forums/aws-certified-cloud-practitioner/discussion/-LrQ4NJR-woGZ2R0k_sY/this_xml_file_does_not_appear)

Anna (2020). What is ‘meta refresh redirect’ and why is it considered a critical issue? [https://help.ahrefs.com/en/articles/2433739-what-is-meta-refresh-redirect-and-why-is-it-considered-a-critical-issue](https://help.ahrefs.com/en/articles/2433739-what-is-meta-refresh-redirect-and-why-is-it-considered-a-critical-issue)

ask ubuntu (2011). How to execute script in different directory? [https://askubuntu.com/questions/74780/how-to-execute-script-in-different-directory](https://askubuntu.com/questions/74780/how-to-execute-script-in-different-directory)

Balena (2020). Controlling onboard LEDs on Rpi4. [https://forums.balena.io/t/controlling-onboard-leds-on-rpi-4/126102/5](https://forums.balena.io/t/controlling-onboard-leds-on-rpi-4/126102/5)

Brookes, T. (2018). How to Create a Markdown Table. [https://www.makeuseof.com/tag/create-markdown-table/](https://www.makeuseof.com/tag/create-markdown-table/)

Burer S. (2015). Relative Paths and the Working Directory in R. [https://www.youtube.com/watch?v=fe6GA200dks](https://www.youtube.com/watch?v=fe6GA200dks)

Check Point Software Technologies LTD (2011). How to read the Linux /proc/stat file. [https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit_doGoviewsolutiondetails=&solutionid=sk65143](https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit_doGoviewsolutiondetails=&solutionid=sk65143)

CIS232 – UNIX Shell Programming (2015). Getting started with awk. [https://www.youtube.com/watch?v=u8RXKFTekqw](https://www.youtube.com/watch?v=u8RXKFTekqw)

CODE PROJECT (2013). The xml file does not appear to have any style information associated with it in eb service using asp.net.  [https://www.codeproject.com/Questions/702150/the-xml-file-does-not-appear-to-have-any-style-inf](https://www.codeproject.com/Questions/702150/the-xml-file-does-not-appear-to-have-any-style-inf)

Computer Hope (2019). Linux yes command. [https://www.computerhope.com/unix/yes.htm](https://www.computerhope.com/unix/yes.htm)

Computer Hope (2019). Bash mapfile builtin command. [https://www.computerhope.com/unix/bash/mapfile.htm](https://www.computerhope.com/unix/bash/mapfile.htm)

Computer Hope (2020). The bash shell. [https://www.computerhope.com/unix/ubash.htm](https://www.computerhope.com/unix/ubash.htm)

ContentKing (2020). HTML Redirect code to another page: meta refresh explained. [https://www.contentkingapp.com/academy/redirects/faq/html-meta-redirect/](https://www.contentkingapp.com/academy/redirects/faq/html-meta-redirect/)

FANDOM (2002). Copy, cut and paste. [https://vim.fandom.com/wiki/Copy,_cut_and_paste](https://vim.fandom.com/wiki/Copy,_cut_and_paste)

Fresh2Refresh (2020). C – printf and scanf. [https://fresh2refresh.com/c-programming/c-printf-and-scanf/](https://fresh2refresh.com/c-programming/c-printf-and-scanf/)

Garry Explains (2020). Everyone Needs to Learn a Little Bit of AWK!. [https://www.youtube.com/watch?v=jJ02kEETw70](https://www.youtube.com/watch?v=jJ02kEETw70)

Geerling, J. (2015). Controlling PWR and ACT LEDs on the Raspberry Pi. [https://www.jeffgeerling.com/blogs/jeff-geerling/controlling-pwr-act-leds-raspberry-pi](https://www.jeffgeerling.com/blogs/jeff-geerling/controlling-pwr-act-leds-raspberry-pi)

Git (2020). 2.6 Git Basics – Tagging. [https://git-scm.com/book/en/v2/Git-Basics-Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)

Gite, V. (2020). How To – Linux / UNIX Create a Manpage. [https://www.cyberciti.biz/faq/linux-unix-creating-a-manpage/](https://www.cyberciti.biz/faq/linux-unix-creating-a-manpage/)

GitHub (2018). Handle relative paths in Markdown export #846. [https://github.com/laurent22/joplin/issues/846](https://github.com/laurent22/joplin/issues/846)

GitHub (2020). Phoronix Test Suite 10.0.1. [https://github.com/phoronix-test-suite/phoronix-test-suite](https://github.com/phoronix-test-suite/phoronix-test-suite)

GitHub Guides (2014). Mastering Markdown [https://guides.github.com/features/mastering-markdown/](https://guides.github.com/features/mastering-markdown/)

GitHub Guides (2020). Markdown Syntax. [https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)

GitHub (2018). Linking from one .md file to another. [https://github.community/t/linking-from-one-md-file-to-another/1249](https://github.community/t/linking-from-one-md-file-to-another/1249)

GNU (2020). 7.4.10 The exit Statement. [https://www.gnu.org/software/gawk/manual/html_node/Exit-Statement.html](https://www.gnu.org/software/gawk/manual/html_node/Exit-Statement.html)

Hewlett Packard Enterprise (2009). Print the last character of a string using awk. [https://community.hpe.com/t5/languages-and-scripting/print-the-last-character-of-a-string-using-awk/td-p/5162994](https://community.hpe.com/t5/languages-and-scripting/print-the-last-character-of-a-string-using-awk/td-p/5162994)

Incredigeek.com (2019). Linux, Send USR1 signal to pid.  [https://www.incredigeek.com/home/linux-send-usr1-signal-to-pid/](https://www.incredigeek.com/home/linux-send-usr1-signal-to-pid/)

IT SOLUTIONS confirm Blog (2018). Mastering Vim: Undo, redo and repeat. [https://blog.confirm.ch/mastering-vim-undo-redo-and-repeat/](https://blog.confirm.ch/mastering-vim-undo-redo-and-repeat/)

Kili, A. (2016). How to Sort Output of ‘ls’ Command By Last Modified Date and Time. [https://www.tecmint.com/sort-ls-output-by-last-modified-date-and-time/](https://www.tecmint.com/sort-ls-output-by-last-modified-date-and-time/)

Kjohri (2020). Signals in Linux. [https://www.softprayog.in/programming/signals-in-linux](https://www.softprayog.in/programming/signals-in-linux)

Koalaman (2020). ShellCheck – A shell script static analysis tool. [https://github.com/koalaman/shellcheck](https://github.com/koalaman/shellcheck)

Lester Work Space (2018). Raspberry pi on board LED control. [https://lesterlo.wordpress.com/2018/10/14/raspberry-pi-on-board-led-control/](https://lesterlo.wordpress.com/2018/10/14/raspberry-pi-on-board-led-control/)

Linux Man Page Howto (2020). 3. How should a formatted man page look? [https://tldp.org/HOWTO/Man-Page/q3.html](https://tldp.org/HOWTO/Man-Page/q3.html)

Linux Man Page Howto (2020). 2. How are man pages accessed? [https://tldp.org/HOWTO/Man-Page/q2.html](https://tldp.org/HOWTO/Man-Page/q2.html)

Linuxize (2020). Bash if..else statement. [https://linuxize.com/post/bash-if-else-statement/](https://linuxize.com/post/bash-if-else-statement/)

Linuxize (2020). How to Extract (Unzip) tar.xz File. [https://linuxize.com/post/how-to-extract-unzip-tar-xz-file/](https://linuxize.com/post/how-to-extract-unzip-tar-xz-file/)

LinuxHowtos.org (2020). /proc/stat explained. [http://www.linuxhowtos.org/System/procstat.htm](http://www.linuxhowtos.org/System/procstat.htm)

Liv4IT (2019). How To write AWK Commands And Scripts In Linux.  [https://www.youtube.com/watch?v=41DOjQidWHI](https://www.youtube.com/watch?v=41DOjQidWHI)

Maruthamuthu, M. (2019). Linux Shell script to monitor CPU utilization with email alert. [https://www.2daygeek.com/linux-shell-script-to-monitor-cpu-utilization-usage-and-send-email/](https://www.2daygeek.com/linux-shell-script-to-monitor-cpu-utilization-usage-and-send-email/)

Markdown Guide (2020). Basic Syntax – The Markdown elements outline in John Gruber’s design document. [https://www.markdownguide.org/basic-syntax/](https://www.markdownguide.org/basic-syntax/)

Mckay, D. (2019). How to Copy and Paste Text at Linux’s Bash Shell. [https://www.howtogeek.com/440558/how-to-copy-and-paste-text-at-linuxs-bash-shell/](https://www.howtogeek.com/440558/how-to-copy-and-paste-text-at-linuxs-bash-shell/)

Microsoft (2015). Back navigation caching. [https://docs.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/dev-guides/dn265017(v%3dvs.85)](https://docs.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/dev-guides/dn265017(v%3dvs.85))

Might, M. (2011). Shell programming with bash: by example, by couter-example. [http://matt.might.net/articles/bash-by-example/](http://matt.might.net/articles/bash-by-example/)

Miller, P. (2020). COSC2672 Home. [https://rmit.instructure.com/courses/70649](https://rmit.instructure.com/courses/70649)

Miller, P., et al. (2020). Completing the Phoronix Part of the Assignment 2 submission. [https://rmit.instructure.com/courses/70649/discussion_topics/993416](https://rmit.instructure.com/courses/70649/discussion_topics/993416)

Miller, P., et al. (2020). Assignment 2 Discussion. [https://rmit.instructure.com/courses/70649/discussion_topics/888290](https://rmit.instructure.com/courses/70649/discussion_topics/888290)

Miller, P., et al. (2020). Discussion. [https://rmit.instructure.com/courses/70649/discussion_topics](https://rmit.instructure.com/courses/70649/discussion_topics)

Miller, P (2020). OSC2672  > Announcements> Pheronix Test Suite – Which Test Suites Have Been Useful. [https://rmit.instructure.com/courses/70649/discussion_topics/983460](https://rmit.instructure.com/courses/70649/discussion_topics/983460)

Moran, B. (2007). Meaning of: kill -USR2. [https://lists.freebsd.org/pipermail/freebsd-questions/2007-August/156889.html](https://lists.freebsd.org/pipermail/freebsd-questions/2007-August/156889.html)

Newell, G. (2020). How to Use the Linux ‘top’ Command to Show Running Processes. A real-time system resource monitor helps alert you to system bottlenecks. [https://www.lifewire.com/linux-top-command-2201163](https://www.lifewire.com/linux-top-command-2201163)

nixCraft (2019). How do I Find Out Linux CPU Utilization? [https://www.cyberciti.biz/tips/how-do-i-find-out-linux-cpu-utilization.html](https://www.cyberciti.biz/tips/how-do-i-find-out-linux-cpu-utilization.html)

Okoi, M.D. (2019). How to Count Word Occurrences in a Text File. [https://www.tecmint.com/count-word-occurrences-in-linux-text-file/](https://www.tecmint.com/count-word-occurrences-in-linux-text-file/)

Openbenchmarking.com (2020). Rodinia. [https://openbenchmarking.org/test/pts/rodinia-1.2.2](https://openbenchmarking.org/test/pts/rodinia-1.2.2)

Oxygen XML Editor (2017). Mycontent not showing up when I use the xslt stylesheet. [https://www.oxygenxml.com/forum/topic14579.html](https://www.oxygenxml.com/forum/topic14579.html)

phoenixNAP Global IT Services (2019). How To Check CPU Utilization IN Linux With Command Line. [https://phoenixnap.com/kb/check-cpu-usage-load-linux](https://phoenixnap.com/kb/check-cpu-usage-load-linux)

Phoronix Test Suite (2020). Open-Source, Automated Benchmarking. [http://www.phoronix-test-suite.com/](http://www.phoronix-test-suite.com/)

Raspberrypi (2012). Can we control the on-board leds. [https://www.raspberrypi.org/forums/viewtopic.php?t=12530](https://www.raspberrypi.org/forums/viewtopic.php?t=12530)

Raspberry Pi (2016). Control PWR and ACT LEDs on Raspberry Pi 2 B from Python. [https://raspberrypi.stackexchange.com/questions/44004/control-pwr-and-act-leds-on-raspberry-pi-2-b-from-python](https://raspberrypi.stackexchange.com/questions/44004/control-pwr-and-act-leds-on-raspberry-pi-2-b-from-python)

Raspberrypi (2020). Video options in config.txt. [https://www.raspberrypi.org/documentation/configuration/config-txt/video.md](https://www.raspberrypi.org/documentation/configuration/config-txt/video.md)

Raspberrypi.org (2020). Kernel building. [https://www.raspberrypi.org/documentation/linux/kernel/building.md](https://www.raspberrypi.org/documentation/linux/kernel/building.md)

rxaviers (2020). Gist:7360908. [https://gist.github.com/rxaviers/7360908](https://gist.github.com/rxaviers/7360908)

SASIKALA (2010). The Ultimate Bas Array Tutorial with 15 Examples. [https://www.thegeekstuff.com/2010/06/bash-array-tutorial/](https://www.thegeekstuff.com/2010/06/bash-array-tutorial/)

Seadude (2020). Chapter 1 – Internal Gitbook Links. [https://seadude.gitbooks.io/learn-gitbook/content/chapter1/internal.html](https://seadude.gitbooks.io/learn-gitbook/content/chapter1/internal.html)

Seadude (2020). Chapter 2 – External Gitbook Links. [https://seadude.gitbooks.io/learn-gitbook/content/chapter2/external.html](https://seadude.gitbooks.io/learn-gitbook/content/chapter2/external.html)

Shotts, W (2020). Errors and Signals and Traps (Oh My!) - Part 1. [https://linuxcommand.org/lc3_wss0140.php](https://linuxcommand.org/lc3_wss0140.php)

ShellCheck (2020). ShellCheck. [https://www.shellcheck.net/](https://www.shellcheck.net/)

StackExchange (2011). Cout total number of occurrences using grep. [https://unix.stackexchange.com/questions/6979/count-total-number-of-occurrences-using-grep](https://unix.stackexchange.com/questions/6979/count-total-number-of-occurrences-using-grep)

StackExchange (2012). How to SCP from linux server to Windows client. [https://superuser.com/questions/414803/how-to-scp-from-linux-server-to-windows-client](https://superuser.com/questions/414803/how-to-scp-from-linux-server-to-windows-client)

StackExchange (2014). Run a process to particular/dedicated pid only. [https://unix.stackexchange.com/questions/131514/run-a-process-to-particular-dedicated-pid-only](https://unix.stackexchange.com/questions/131514/run-a-process-to-particular-dedicated-pid-only)

StackExchange (2015). Bash – get pid for a script using the script filename. [https://unix.stackexchange.com/questions/237896/bash-get-pid-for-a-script-using-the-script-filename](https://unix.stackexchange.com/questions/237896/bash-get-pid-for-a-script-using-the-script-filename)

StackExchange (2015). Skip the first 6 lines/rows in a text file with awk. [https://unix.stackexchange.com/questions/198065/skip-the-first-6-lines-rows-in-a-text-file-with-awk](https://unix.stackexchange.com/questions/198065/skip-the-first-6-lines-rows-in-a-text-file-with-awk)

StackEchange (2016) Control PWR and ACT LEDs on Raspberry Pi 2 B from Python. [https://raspberrypi.stackexchange.com/questions/44004/control-pwr-and-act-leds-on-raspberry-pi-2-b-from-python](https://raspberrypi.stackexchange.com/questions/44004/control-pwr-and-act-leds-on-raspberry-pi-2-b-from-python)

StackExchange (2016). Apart from USR1 and USR2, which signals can I safely use for custom interrupting behavior? (in python). [https://unix.stackexchange.com/questions/307396/apart-from-usr1-and-usr2-which-signals-can-i-safely-use-for-custom-interrupting](https://unix.stackexchange.com/questions/307396/apart-from-usr1-and-usr2-which-signals-can-i-safely-use-for-custom-interrupting)

StackExchange (2017). AWK question: Print N lines, starting from the rhird line after given /pattern/. [https://unix.stackexchange.com/questions/369498/awk-question-print-n-lines-starting-from-the-third-line-after-given-pattern](https://unix.stackexchange.com/questions/369498/awk-question-print-n-lines-starting-from-the-third-line-after-given-pattern)

Stackoverflow (2014). Send signal between scripts (bash). [https://stackoverflow.com/questions/25668841/send-signal-between-scripts-bash](https://stackoverflow.com/questions/25668841/send-signal-between-scripts-bash)

Stackoverflow (2013). Exception handling in shell scripting?. [https://stackoverflow.com/questions/6961389/exception-handling-in-shell-scripting/6961470](https://stackoverflow.com/questions/6961389/exception-handling-in-shell-scripting/6961470)

Techiebounceer (2020). Control the Power and ACT led of Raspberry pi 4. [https://www.techiebouncer.com/2020/02/control-power-and-act-led-of-raspberry.html](https://www.techiebouncer.com/2020/02/control-power-and-act-led-of-raspberry.html)

The GitHub Blog (2013). Relative links in markup files. [https://github.blog/2013-01-31-relative-links-in-markup-files/](https://github.blog/2013-01-31-relative-links-in-markup-files/)

The WP Guru (2018). How to embed images in GitHub Readme Files. [https://www.youtube.com/watch?v=R6euByfGaN4](https://www.youtube.com/watch?v=R6euByfGaN4)

unix.com (2009). Shell Programming and Scripting – awk, What’s NF and NR? [https://www.unix.com/shell-programming-and-scripting/118605-awk-whats-nf-nr.html](https://www.unix.com/shell-programming-and-scripting/118605-awk-whats-nf-nr.html)

unix.com (2012). AIX Assigning PID for a Process. [https://www.unix.com/aix/184571-assigning-pid-process.html](https://www.unix.com/aix/184571-assigning-pid-process.html)

Vidanovic, B. (2020). How to Find and Replace All in Vim With Substitute Command. [https://bojanvidanovic.com/posts/how-to-find-and-replace-all-in-vim-with-substitute-command/](https://bojanvidanovic.com/posts/how-to-find-and-replace-all-in-vim-with-substitute-command/)

W3schools.com (2020). HRML <meta>  content Attribute. [https://www.w3schools.com/tags/att_meta_content.asp](https://www.w3schools.com/tags/att_meta_content.asp)

W3schools.com (2020). XSLT <xsl:value-of> [https://www.w3schools.com/xml/ref_xsl_el_value-of.asp](https://www.w3schools.com/xml/ref_xsl_el_value-of.asp)

Williams, A. (2020). LINUX FU: MONITOR DISKS. [https://hackaday.com/2020/11/05/linux-fu-monitor-disks/](https://hackaday.com/2020/11/05/linux-fu-monitor-disks/)

Vranish, J. (2017). Simple Way to Start (and Stop!) Background Processes in Bash. [https://spin.atomicobject.com/2017/08/24/start-stop-bash-background-process/](https://spin.atomicobject.com/2017/08/24/start-stop-bash-background-process/)

xiaolee (2020). GitHub relative link in Markdown file. [https://ask.xiaolee.net/questions/1007808](https://ask.xiaolee.net/questions/1007808)

XML Tutorial (2020). <xsl:value-of>. [https://www.xmltutorial.info/xslt/xslvalue-of/](https://www.xmltutorial.info/xslt/xslvalue-of/)

Yogita Sharma (2015). How to calculate CPU Usage -/proc/stat vs top. [https://medium.com/@yogita088/how-to-calculate-cpu-usage-proc-stat-vs-top-e74f99f02d08](https://medium.com/@yogita088/how-to-calculate-cpu-usage-proc-stat-vs-top-e74f99f02d08)

Zach (2020). Build a Simple Raspberry Pi LED Power/Status Indicator. [https://howchoo.com/g/ytzjyzy4m2e/build-a-simple-raspberry-pi-led-power-status-indicator](https://howchoo.com/g/ytzjyzy4m2e/build-a-simple-raspberry-pi-led-power-status-indicator)

ZEROTOUCH (2019). Ls by date | List Unix files with ‘ls’ in date order. [https://www.zerotouch.com/faqs/111/ls-by-date](https://www.zerotouch.com/faqs/111/ls-by-date)
