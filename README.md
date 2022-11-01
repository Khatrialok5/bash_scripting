# Unix & Linux course

Table of Contents

```
  Part 1: Basics
  Part 2: User level commands
  Part 3: Admin commands
  Part 4: Shell scripting
  Part 5: Project
```

## **Part 1: Basics**

<details>
  <summary>Day 1 & 2: Intro to OS</summary>

- Contents
  - software basics
  - OS intro
  - Unix vs Linux vs Windows and their architecture
  - Linux installation
  - Putty and winscp tools setups
- Computer
  - Software
    - System Software -> Linux, interacts with hardware components
      - Device drivers and OS
    - Application Software -> All are application software except Operating Systems. e.g. Java, C/C++,Facebook, Twitter, Gmail
  - Hardware : hard disk, monitor,keyboard, RAM
- What is Operating Systems?

  - It is a platform where we can run all the application softwares
  - It is an interface between Application softwares and hardware components
  - Every OS has libraries (collection of C) and device drivers to communicate between application softwares and hardware components
    - Application Software
    - Shell
    - Libraries
    - Device Drivers
    - Hardware

- Device Drivers : Run devices and communicate with hardware components
  - All drivers are not part of OS.
  - Two types of drivers
    - Internal : Part of OS and are built in
      - They are to run internal parts of computer. e.g. keyboard, RAM, Monitor, mouse, hard disk, motherboard, USB drive,
    - External : you need to set up yourself
      - printer, scanner, fax machine

- **Categories of Operating System**
  - CUI/CLI : Character User Interface/ Command line interface
    - window command prompt
  - GUI : Graphical user interface
- Commands
  - dir : disk information report
- Single User OS
  - Only one user can use system resources such as files, apps, data
  - It does not support networking
  - Stand alone OS
- multiuser os
  - More than one user
  - can share system resources
  - Apps, data & files
  - It supports networking
  - Server OS e.g. Unix, Linux, Win-7,8,10,11
  - History of Microsoft Disk Operating System
    - First OS in the market
    - CUI, it does not support networking
    - Standalone OS
    - Was developed in Assembly language
  - History of Unix
    - Developed in year 1973
    - It is CUI
    - Supports networking
    - It is a Server OS
  - Freeware (Oracle, Virtual Box, Putty => they can be downloaded and used for free and features cannot be changed)
  - Open source
    - It can be downloaded including source code
    - You can also modify the program
    - It can be distributed. Below are distributions(similar to brands) /flavours of unix OS
      - e.g. Linux - modified version of Unix , by Linux Torvald
      - Solaris => from Sunsoft (with oracle corp 2010)
      - IBM - AIX : from IBM
      - HP-UX : from Hallet Packward
      - BSD-Unix : Berkely software division
      - Mac OS : Machintosh
  - GUI (Graphical User Interface)
    - Windows is first GUI OS released in the year 1990.
    - win1.0 -> 1990 then evolve
    - win95 -> 1995 => most popular OS in 1990s - stand alone OS
    - To support Internet, Microsoft corp added networking technology.win-NT, server OS
    - win98
    - win2000, win2003, winXP till 2015, many companies use this winXP
    - win7, win8, wi10, win11
    - win-12- with linux kernel

</details>

---

<details>
  <summary>Day 3 : Distributions flavours</summary>

- Virtualisation - VMware
  -
- Linux is a modified version of unix OS
- 1989 - Linux Torvalds has taken unix source code and modified/added some more features
  - 1999 - Apache software foundation has taken over linux product and released as Linux in the market
  - Apache Linux => first officially released version in the market
    - GUI OS, Open source
  - Fedora Linux
  - Suse Linux
  - Debian Linnux
  - CentOS
  - Ubuntu Linux
  - Kali Linux
- What are the distributions of Unix OS?
  - Linux, Solaris, IBM-AIX
- What are the distribution of Linux OS?
  - Most popular version is Ubuntu (open source),Red Hat Enterprise (Licensed version), CentoS (free ware)
  - Software environments - Learning -> Ubuntu - Development - Testing - Production
  </details>

---

<details>
  <summary>Day 4 : Different users settings</summary>
 
- Settings -> Users 
  - passwd username 
  - sudo passwd testuser => you need sudo for enabling users to set password 
- [Install Chrome in Ubuntu](https://www.geeksforgeeks.org/how-to-install-chrome-in-ubuntu/)
  - Ctrl + Shift + Y => To check for download progress
</details>

---

<details>
  <summary>Day 5 : Install putty, remote server, Linux Features, Architecture, File System</summary>

- putty
  - Work with remote server
  - PuTTY is a terminal emulator application which can act as a client for the SSH, Telnet, rlogin, and raw TCP computing protocols. The word "PuTTY" has no meaning, though 'tty' is sometimes used to refer to the Unix terminals, as an acronym for 'teletype'.
  - PuTTY is the recommended application to use for SSH connections from a Windows operating system. PuTTY allows you to access your files and email stored on the engineering servers. It also provides a UNIX environment to run programs that some courses require.

- [Download putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
  - Install and open the Putty app
  - In configuration, you will see Host Name (or IP address)
  - To get IP address, in Ubuntu terminal, type `ifconfig`. If it is not found, install it.
  - Look for inet
    - If you have two adapters, you choose the second one.
    - Device Manager -> VirtualBox Host-Only Ethernet Adapter e.g. 192.168.56.151
    - Add that address under HostName
  - You will have **Network error: Connection refused.**
    - Because SSH connection type is used. Set SSH up in Ubuntu
    - [`sudo apt-get update`](https://www.cyberciti.biz/faq/what-does-sudo-apt-get-update-command-do-on-ubuntu-debian/#:~:text=The%20sudo%20apt%2Dget%20update%20command%20is%20used%20to%20download,list.)
      - sudo : Sudo stands for either "substitute user do" or "super user do" and it allows you to temporarily elevate your current user account to have root privileges.
      - apt : Advanced Package Tool, more commonly known as APT, is a collection of tools used to install, update, remove, and otherwise manage software packages on Debian and its derivative operating systems, including Ubuntu and Linux Mint.
    - `sudo apt install ssh`
    - After you install ssh, you will be able to connect.
      - <img src="./img/putty_ssh_to_ubuntu.jpg">
  - Change font size
    - Right click -> change settings -> Appearance -> Change
  - Create some files in putty server and check them in Ubuntu server
  - Duplicate Session
    - Connect to the same server, and you can connect with different user names
  - clear or Ctrl + l -> clear the terminal
  - `exit` from the login session. You need to `exit`, instead of closing it. 
  - `hostname` : is a computer name
- **winscp**
  - window secure copy
  - Its main function is file transfer between a local and a remote computer. 
  - WinSCP is a popular SFTP client and FTP client for Microsoft Windows! Copy file between a local computer and remote servers using FTP, FTPS, SCP, SFTP, WebDAV or S3 file transfer protocols. 
- *[Transfer files from windows to the server](https://winscp.net/eng/index.php)*
  - Download the setup.exe file
  - cp means secure copy
  - After installation, enter IP address , username and password.
- You can also use [Filezilla](https://filezilla-project.org/download.php?type=client)

- **Features of Linux - Theory Part**
  - Basic features of all OS : Win, Unix, Linux
    - Multi user OS
      - multiple users can chare the same OS
      - <img src="./img/multiusers_connection.png">
    - Multi tasking OS 
      - In window, type Services and check for all the things that are currently running 
      - In Linux, `ps -ef | wc -l`
        - ps is process 
        - to see the details, run `ps -ef`
  - Ony for Unix and Linux 
    - Open Source OS
    - Portable OS
      - Software can work with different hardwares.
      - Independent of hardware e.g. intel/amd, spark, ibm, apple hardware,
    - Secure OS
      - Virus
      - Hacking
      -  
    - Shell scripting
      - Data processing
      - Automation of Admin activities (linux, hadoop, dba, aws, devops)
      - Job scheduling - crondev
      - Files backup
      - Data backup 
      - Development of gateways 
      - Dba backup scripts 
    - GUI 
    
- **Linux File System Theory**
  - Window 
    - DVD or Drive iso.image
    - iso.img
    - PC
    - Reboot OS-> BIOS -> F1 to F12, DEL, ESC 
      - First Boot -> Pen drive , F10 -> Save changes then reboot
    - A - Z drives letter concept for window
      - A and B are reserved for floppy disk..
      - C is reserved for Hard disk
    - In windows, there are two types of users: 
      - Admin : root user
      - Gust : normal user 
  - **Linux**
    - In Linux, there is no drive letter concepts. In linux, directory ( ~ folders) hierarchy.
    - forward slash / is the top level directory 
  - Top Level directory / 
  - /root /home /boot /etc /bin /sbin /usr /opt 
    - /root - root user 
    - /home - normal user
    - /boot - If there is an expected shutdown, 
      - To travel from Mamo to Cophenhagen, you need to use transport methods e.g. car, bike, train
      - Travel from Mamo to Cophenhagen without transport vehicles (bootable files), you will not be able to reach the destination (OS)
      - grub2 -> RHEL 7.0, 8.0 is the boot loader, depending on version, it will change.
        - ground unified boot loader version 2
        - LILO - Linux loader 
    - /etc contains configuration files
    - /bin contains normal user executable commands
    - /sbin contains root user executable commands (super user)
    - /usr - program files - install packges in this directory 
    - /op - is optional for usr , third parties software e.g. Ansible 
  - **Three Types of files**
    - Regular file
      - It contains data
        - can be text e.g. Notepad, pdf, word files 
        - binary e.g. .exe files, images, audio, video
    - Directory is like folder from Window.
      - `ls`
      - contains sub directories and files
      - dash - is file
      - d is directory 
    - Device files 
      - Device drivers `cd /dev/`
      - all device drivers starts with c `ls -l`, link file `l`
      - <img src="./img/drivers.png">

- **Linux Architecture**
  - <img src="https://www.tutorialspoint.com/operating_system/images/linux_architecture.jpg">
  - [Reading about Linux Kernel](https://developer.ibm.com/articles/l-linux-kernel/)

  - <img src="https://www.engineersgarage.com/wp-content/uploads/2016/07/ArticleImage-12104-1.png">
  - <img src="https://1.bp.blogspot.com/-SgpOeYaAw-w/XGRSQeQj_AI/AAAAAAAAB-w/Ry2y07-PWjIhVt2rKZAKxStzhvTO9FhIQCLcBGAs/s1600/Kernel_Architecture.JPGe">
  - Architecture : Simple definition -> is a flow of data between different components of a project 
    - Browser, Facebook -> Middleware -> Database -> Hadoop-> BI tools
  - Linux architecture is a flow of data between different components of a Linux OS
  - There are two layers in Linux OS
    - Shell
    - Kernel
    ```
    echo $SHELL
    echo $0 
    echo $PATH 
    ```
    1. User request goes to the shell 
    2. Shell check whether the command exists
    3. Kernel takes the request, executes and generates outputs to hardware device 
  - Layers
    - C, C++, Java, Hadoop
    - Operating System
      - Shell 
        - Command interpreter 
        - It is an interface between user and kernel
        - Is an outer layer of Linux OS
        - How shell validates the command (shell scripting)
      - Kernel
        - Core layer of Linux system and consists of two layers:
          - Device Drivers - interacts with Hardware components
          - Libraries - communicates with Applications
            - keyboard driver, libraries -> scanf -> printf goes to output library -> output function -> output device driver -> screen 
    - Hardware
  - [filetypes](https://www.geeksforgeeks.org/how-to-find-out-file-types-in-linux/)
    - <img src="./img/filetypes.png">
    - <img src="https://www.2daygeek.com/wp-content/uploads/2019/01/find-identify-file-types-in-linux-4.png">
    - [Files permission reading](https://devconnected.com/linux-file-permissions-complete-guide/)
  - Finished session - 11
  - If you cannot push the repo from terminal, Ubuntu, read this [thread](https://stackoverflow.com/questions/71495330/can-not-push-on-github-through-ubuntu-terminal)
  - [Quickly set up GitHub SSH example](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/GitHub-SSH-Key-Setup-Config-Ubuntu-Linux)

---

<details>
  <summary>Day 6</summary>
</details>

---

<details>
  <summary>Day 7</summary>
</details>

---

<details>
  <summary>Day 8</summary>
</details>

---

<details>
  <summary>Day 9</summary>
</details>

---

<details>
  <summary>Day 10</summary>
</details>

---

<details>
  <summary>Day 11</summary>
</details>

---

<details>
  <summary>Day 12</summary>
</details>

---

## **Part 2: User level commands**

- Contents
  - whoami, who, last, man
  - date, cal, ls and its options
  - working with directories
  - absolute path vs relative path
  - working with files
  - hard links vs softlink files
  - editors : gedit, vi, vim, nano
  - pattern matching chars, \*, ?, [], {}
  - filters like pipe, head, tail, tr, tee
  - grep command
  - tar
  - Permission (security)
    - read, write, execute
  - killing jobs

## **Part 3: Admin commands**

-

## **Part 4: Shell scripting**

## **Part 5: Project**
