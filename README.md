# **Linux Fundamental Tutorial**

## **Introduction**

### <u>***LINUX :***</u>
Linux is an open source operating system that is made up of the kernel, the base component of the OS, and the tools, apps, and services bundled along with it.

Linux is a command line operating system based on unix. There are multiple operating systems that are based on Linux.


### <u>***Founder of LINUX :</u>***
Linus Torvalds (1991)


### <u>***Linux Kernel :***</u>
The `Linux kernel` is the main component of a `Linux operating system` (OS) and is the core interface between a computer’s hardware and its processes.


### <u>***Flavours of Linux :***</u>
The name `Linux` is actually an umbrella term for multiple OS's that are based on `UNIX` (another operating system). Thanks to `UNIX` being open-source, variants of Linux comes in all shapes and sizes - suited best for what the system is being used for.

For example, `Ubuntu` & `Debian` are some of the more commonplace distributions of `Linux` because it is so extensible. i.e. you can run `Ubuntu` as a server (such as websites & web applications) or as a fully-fledged desktop. For this series, we're going to be using `Ubuntu`.


### <a href="https://en.wikipedia.org/wiki/List_of_Linux_distributions"><u>***List of LINUX Distributions :***</u></a>
<img alt="Linux Distros" src="https://i0.wp.com/lignux.com/wp-content/uploads/2014/08/distros_linux.jpg?zoom=2">


### <u>***Popular Linux distros  :***</u>
* Android
* Arch Linux
* Centos
* Debian
* Elementary OS
* Fedora
* Gentoo Linux
* Kali Linux
* Linux Mint
* Manjaro Linux
* MX Linux
* Puppy Linux
* Slackware
* Solus
* Ubuntu and all its versions (Gnome, Kubuntu, Ubuntu mate, Xubuntu, and Lubuntu — just to name a few)
* Zorin OS

<!--  -->

## LINUX Commands (Ubuntu LTS 20.04)

### <u>***Running Your First few Commands :***</u>

| Command | Description |
| --- | --- |
| `echo` | Output any text that we provide |
| `whoami` | Find out what user we're currently logged in as! |


* Using `echo`
```bash
echo Hello World!
```
or
```bash
echo "Hello World!"
```

* Using `whoami` to find out the username of who we're logged in as
```bash
whoami
```


### <u>***Interacting With the Filesystem :***</u>

| Command | Full Name |
| --- |--- |
| `ls` | listing |
| `cd` | change directory |
| `cat` | concatenate |
| `pwd` | print working directory |
| `touch`	|	Create file|
| `mkdir` |	make directory (Create a folder)|
| `cp` | copy	(Copy a file or folder) |
| `mv` | move	(Move a file or folder) |
| `rm` | remove	(Remove a file or folder) |
| `file`|	file (Determine the type of a file) |


* **Listing Files in Our Current Directory (`ls`) :**  Using `ls` to to list the contents of the current directory.
```bash
ls # to listing the present directory
```
or
```bash
ls Folder # to listing the desired folder
```
* Using `ls` command with different flags

   * Using `ls` to list view of folders
   ```bash
   ls -l
   ```
   
   * Using `ls` to view hidden folders
   ```bash
   ls -a
   ```
   
   * Using `ls` to view hidden folders with list view
   ```bash
   ls -la
   ```
   
   * Using `ls` to view folder in folders (Recursive view)
   ```bash
   ls -R
   ```
   
   * Using `ls` to view hidden folders in list view with folder in folders
   ```bash
   ls -laR
   ```

   * Using `ls -lh` to list the permissions of all files in the directory
   ```bash
   ls -lh
   ```
   
* **Changing Our Current Directory (`cd`) :** Listing our new directory after we have used `cd`.
```bash
cd Folder
```

* **Outputting the Contents of a File (`cat`) :** `cat` is short for concatenating & is a fantastic way us to output the contents of files (not just text files!).
```bash
cat file.txt
```

* **Finding out the full Path to our Current Working Directory (`pwd`) :** Using `pwd` to list the full path of the current directory.
```bash
pwd
```

* **Creating Files and Folders (`touch`, `mkdir`) :**

   * Using `touch` to create a new file.
   ```bash
   touch note.txt
   ```

   * Creating a new directory with `mkdir`
   ```bash
   mkdir mydirectory
   ```

* **Removing Files and Folders (`rm`) :**

   * Using `rm` to remove a file.
   ```bash
   rm note.txt
   ```

   * Using `rm` recursively to remove a directory
   ```bash
   rm -R mydirectory
   ```

   * Using `rm` recursively forced removing a directory or a file
   ```bash
   rm -Rf note.text
   ```

   * Using `rm` interactively removing file or folder
   ```bash
   rm -i note.txt file.txt code.cpp mydirectory
   ```

   * Using `rm` recursively with interactively to remove a directory
   ```bash
   rm -iR note.txt code.cpp file.txt mydirectory
   ```

* **Copying and Moving Files and Folders (`cp`, `mv`) :**  
   
   * Using `cp` to copy a file
   ```bash
   cp note.txt note2.txt
   ```

   * Using `mv` to move a file
   ```bash
   mv note2.txt note3.txt
   ```

* **Determining File Type :** Using `file` to determine the contents of a file
```bash
file note
```


### <u>***Searching for Files :***</u>

* Using `find` to find a file with the name of `file.txt`
```bash
find -name file.txt
```

* Using `find` to find any file with the extension of `.txt`
```bash
find -name *.txt
```

* **Using `grep` :** `grep` has searched through this file and has shown us any entries of what we've provided and that is contained within this log file for the IP Address

  1. Using `wc` to count the number of entries in `access.log`
  ```bash
  wc -l access.log
  ```

  2. Using `grep` to find any entries with the IP address of `81.143.211.90` in `access.log`
  ```bash
  grep "81.143.211.90" access.log
  ```


### <u>***An Introduction to Shell Operators :***</u>


|Symbol / Operator | Description |
|---|---|
| `&`	| This operator allows you to run commands in the background of your terminal. |
| `&&` | This operator allows you to combine multiple commands together in one line of your terminal. |
| `>` |	This operator is a redirector - meaning that we can take the output from a command (such as using `cat` to output a file) and direct it elsewhere. |
| `>>` | This operator does the same function of the `>` operator but appends the output rather than replacing (meaning nothing is overwritten). |

* **Operator `>` :**
  1. Using the `>` Operator
  ```bash
  echo Hello > file.text
  ```

  2. Using `cat` to output the `file.txt` file
  ```bash
  cat file.txt
  ```

* **Operator `>>` :**
  1. Using the `>>` Operator
  ```bash
  echo World > file.text
  ```

  2. Using `cat` to output the `file.txt` file
  ```bash
  cat file.txt
  ```


### <u>***Introduction to Flags and Switches :***</u>

* Listing the options we can use with `ls`
```bash
ls --help
```

* The Man(ual) Page
```bash
man ls
```


### <u>***Permissions 101 :***</u>

* Using `ls -lh` to list the permissions of all files in the directory
```bash
ls -lh
```

The output might be
```
output:
-rw-r--r-- 1 ubuntu ubuntu 0 Feb 19 10:37 note.txt
-rw-r--rw- 8 ubuntu ubuntu 0 Feb 19 10:37 file.rtf
-r--rw-r-- 3 ubuntu ubuntu 0 Feb 19 10:37 main.py
-rw-r-xr-x 7 ubuntu ubuntu 0 Feb 19 10:37 play.c
-rwxr-xrwx 2 ubuntu ubuntu 0 Feb 19 10:37 code.cpp
```

Here

* `-r` -> Read
* `-w` -> Write
* `-x` -> Execute
* First set is use for `Owner`
* Second set is use for `Group`
* Third set is use for `Public`

To change the file permissions we have to use <a href="https://chmod-calculator.com/">Chmod Calculator</a>

* Using `chmod` command to change the file permissions
```bash
chmod 735 note.txt file # 735 = -rwx-wx-r-x
```


### <u>***Sudo User :***</u>

* **Switching Between Users :** Using `su` to switch to `user2` interactively
```bash
su user2
```
or
```bash
su -l user2
```

* To update the linux kernel using CLI (command Line Instructions)
```bash
sudo apt update
```

* To see update list the linux kernel using CLI (command Line Instructions)
```bash
sudo apt list --upgradable
```

* To see upgrade the linux kernel using CLI (command Line Instructions)
```bash
sudo apt upgrade
```

* To see install a programme, named `vim` using CLI (command Line Instructions)
```bash
sudo apt install vim
```


### <u>***Common Directories :***</u>

* `/etc` : This root directory is one of the most important root directories on your system. The etc folder (short for etcetera) is a commonplace location to store system files that are used by your operating system.

* `/var` : The `/var` directory, with `var` being short for variable data,  is one of the main root folders found on a Linux install. This folder stores data that is frequently accessed or written by services or applications running on the system.

* `/root` : Unlike the `/home` directory, the `/root` folder is actually the home for the `root` system user. There isn't anything more to this folder other than just understanding that this is the home directory for the `root` user. But, it is worth a mention as the logical presumption is that this user would have their data in a directory such as `/home/root` by default.

* `/tmp` : This is a unique root directory found on a Linux install. Short for `temporary`, the `/tmp` directory is volatile and is used to store data that is only needed to be accessed once or twice. Similar to the memory on your computer, once the computer is restarted, the contents of this folder are cleared out.



### <u>***Terminal Text Editors :***</u>

* <u>Nano :-</u> <a href="https://en.wikipedia.org/wiki/GNU_nano">GNU nano</a> is a text editor for Unix-like computing systems or operating environments using a command line interface. It emulates the <a href="https://en.wikipedia.org/wiki/Pico_(text_editor)">Pico</a> text editor, part of the Pine email client, and also provides additional functionality. ie. -
  - Searching for text
  - Copying and Pasting
  - Jumping to a line number
  - Finding out what line number you are on

Using `nano` to write text
```bash
nano code.cpp
```

To exit nano, press `Ctrl + X`. 

* <u>VIM :-</u> <a href="https://www.vim.org/">VIM</a> a contraction of Vi IMproved) is a free and open-source, screen-based text editor program. It is an improved clone of Bill Joy's vi. The benefits of VIM are -
  - Customisable - you can modify the keyboard shortcuts to be of your choosing
  - Syntax Highlighting - this is useful if you are writing or maintaining code, making it a popular choice for software developers
  - VIM works on all terminals where nano may not be installed
  - There are a lot of resources such as <a href="https://vim.rtorr.com/">cheatsheets</a>, tutorials, and the sorts available to you use.

Using `vim` to write text
```bash
vim code.cpp
```

To write in vim editor press `Insert`. To exit first press `Esc`, then type `:wq`.


### <u>***General/Useful Utilities :***</u>

* Downloading Files
```bash
wget https://upload.wikimedia.org/wikipedia/commons/thumb/b/b6/Image_created_with_a_mobile_phone.png/1200px-Image_created_with_a_mobile_phone.png
```

* Transferring Files From Your Host - SCP (SSH)
```bash
scp important.txt ubuntu@192.168.1.30:/home/ubuntu/transferred.txt
```
vice-versa
```bash
scp ubuntu@192.168.1.30:/home/ubuntu/documents.txt notes.txt 
```

* Serving Files From Your Host - WEB
```bash
python3 -m http.server
```


### <u>***Processes 101 :***</u>

* Viewing Processes
```bash
ps
```
```bash
ps aux
```
```bash
top
```

* Kill a process
```bash
kill <PID number>
```
i.e.
```bash
kill 1373
```

* Getting Processes/Services to Start on Boot
```bash
systemctl <option> <service>
```
i.e.
```bash
systemctl start apache2
```
* some common flag to use with systemctl
   - Start
   - Stop
   - Enable
   - Disable

* To see foreground processes
```bash
fg
```


### <u>***Maintaining Your System - Automation :***</u>

Users may want to schedule a certain action or task to take place after the system has booted. Take, for example, running commands, backing up files, or launching your favourite programs on, such as <a href="https://www.spotify.com/">Spotify</a> or <a href="https://www.google.com/intl/en_in/chrome/">Google Chrome</a>.

We're going to be talking about the `cron` process, but more specifically, how we can interact with it via the use of crontabs . `Crontab` is one of the processes that is started during boot, which is responsible for facilitating and managing `cron` jobs.

<img alt="GNU nano" src="https://assets.tryhackme.com/additional/linux-fundamentals/part3/cron1.png">

A `crontab` is simply a special file with formatting that is recognised by the `cron` process to execute each line step-by-step. Crontabs require 6 specific values:

|Value | Description |
|---|---|
| MIN |	What minute to execute at |
|HOUR |	What hour to execute at |
| DOM |	What day of the month to execute at |
| MON |	What month of the year to execute at |
| DOW |	What day of the week to execute at |
| CMD |	The actual command that will be executed. |

Let's use the example of backing up files. You may wish to backup `cmnatic`'s  "Documents" every 12 hours. We would use the following formatting: 
```bash
0 *12 * * * cp -R /home/cmnatic/Documents /var/backups/
```
An interesting feature of crontabs is that these also support the wildcard or asterisk (`*`). If we do not wish to provide a value for that specific field, i.e. we don't care what month, day, or year it is executed -- only that it is executed every 12 hours, we simply just place an asterisk.

This can be confusing to begin with, which is why there are some great resources such as the online <a href="https://crontab-generator.org/">"Crontab Generator"</a> that allows you to use a friendly application to generate your formatting for you! As well as the site <a href="https://crontab.guru/">"Cron Guru"</a> !

Crontabs can be edited by using `crontab -e`, where you can select an editor (such as Nano) to edit your `crontab`.

<img alt="crontab" src="https://assets.tryhackme.com/additional/linux-fundamentals/part3/cron2.png">

<img alt="0 *12 * * * cp -R /home/cmnatic/Documents /var/backups/" src="https://assets.tryhackme.com/additional/linux-fundamentals/part3/cron3.png">


### <u>***Maintaining Your System - Package Management :***</u>

* <u>**Introducing Packages & Software Repos :**</u>\
\
When developers wish to submit software to the community, they will submit it to an  `apt` repository. If approved, their programs and tools will be released into the wild. Two of the most redeeming features of Linux shine to light here: User accessibility and the merit of open source tools.
\
\
When using the `ls` command on a Ubuntu 20.04 Linux machine, these files serve as the gateway/registry.

<img alt="ubuntu@ip-10-10-29-121:/etc/apt$" src="https://assets.tryhackme.com/additional/linux-fundamentals/part3/apt1.png">

<img alt="GNU nano 2.9.3" src="https://assets.tryhackme.com/additional/linux-fundamentals/part3/apt2.png">

\
Whilst Operating System vendors will maintain their own repositories, you can also add community repositories to your list! This allows you to extend the capabilities of your OS. Additional repositories can be added by using the `add-apt-repository` command or by listing another provider! For example, some vendors will have a repository that is closer to their geographical location.

* <u>**Managing Your Repositories (Adding and Removing) :**</u>\
\
Normally we use the `apt` command to install software onto our Ubuntu system. The `apt` command is a part of the package management software also named `apt`. Apt contains a whole suite of tools that allows us to manage the packages and sources of our software, and to install or remove software at the same time.
\
\
Let's walk through adding and removing a repository using the `add-apt-repository` command we illustrated above. Whilst you can install software through the use of package installers such as `dpkg`, the benefits of apt means that whenever we update our system - the repository that contains the pieces of software that we add also gets checked for updates. 
\
\
In this example, we're going to add the text editor Sublime Text to our Ubuntu machine as a repository as it is not a part of the default Ubuntu repositories. When adding software, the integrity of what we download is guaranteed by the use of what is called `GPG` (Gnu Privacy Guard) keys. These keys are essentially a safety check from the developers saying, "here's our software". If the keys do not match up to what your system trusts and what the developers used, then the software will not be downloaded.
\
\
So, to start, we need to add the `GPG key` for the developers of Sublime Text 3.

1. Let's download the `GPG key` and use `apt-key` to trust it: 
```bash
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
```

2. Now that we have added this key to our trusted list, we can now add Sublime Text 3's repository to our apt sources list. A good practice is to have a separate file for every different community/3rd party repository that we add.

   2.1. Let's create a file named `sublime-text.list` in `/etc/apt/sources.list.d` and enter the repository information like so:

   <img alt="Sublime-Text-3" src="https://assets.tryhackme.com/additional/linux-fundamentals/part3/sources1.png">

   2.2. And now use Nano or a text editor of your choice to add & save the `Sublime Text 3` repository into this newly created file:

    <img alt="Sublime-Text-3" src="https://assets.tryhackme.com/additional/linux-fundamentals/part3/sources2.png">

   2.3. After we have added this entry, we need to update apt to recognise this new entry -- this is done using the `apt update` command

   2.4. Once successfully updated, we can now proceed to install the software that we have trusted and added to apt using `apt install sublime-text`

Removing packages is as easy as reversing. This process is done by using the `add-apt-repository --remove ppa:PPA_Name/ppa` command or by manually deleting the file that we previously fulfilled. Once removed, we can just use 
```bash
apt remove [software-name-here]
```
i.e.
```bash
apt remove sublime-text
```


### <u>***Clear & Exit :***</u>

* To clear the terminal
```bash
clear
```

* To exit the terminal
```bash
exit
```