# rtcwake-linux
Program for autowakeup in linux when laptop is power off

# requirement
## rtcwake

Based on Ubuntu/Debian
> apt-get install util-linux

Alpine
> apk add util-linux

Based on Manjaro/Arch
> pacman -S util-linux

CentOS
> yum install util-linux

based on Fedora/Red Hat
> dnf install util-linux

Windows (WSL2)
> sudo apt-get update sudo apt-get install util-linux

MacOS (OS X)
> brew install util-linux

Raspbian
> apt-get install util-linux

## notify-send (optional)
based on Ubuntu/Debian  
> apt-get install libnotify-bin

Alpine  
> apk add libnotify

based on Manjaro/Arch  
> pacman -S libnotify

CentOS  
> yum install libnotify

base on Fedora/Red Hat  
> dnf install libnotify

Mac (OS X)    
> brew install libnotify

Raspbian    
> apt-get install libnotify-bin

# How to use
```
git clone https://github.com/Theman49/rtcwake-linux.git
cd rtcwake-linux
sudo chmod +x wakeup
```

# How to run
## Option 1: create an alias in .bashrc
copy script to /usr/local/bin
```
cp wakeup /usr/local/bin
```

go to home dir
```
cd ~
```

open .bashrc and add alias in the bottom of file
```
vim .bashrc
GG #vim command to go to bottom of file
o #vim comnmand to add new line
alias wakeup="/usr/local/bin"
:wq #vim command to save file and exit from vim
source .bashrc
```


## Option 2: copy script 'wakeup' to folder that exist on path
check what are folders in path
```
echo $PATH
```
> /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/bin:/usr/games:/sbin:/home/YOURPROFILE/bin

```
sudo cp wakeup /usr/local/sbin
```

# Run
```
Syntax: wakeup <hh:mm> [option]

options:
--help      : Print this Help.
-n      : Set wakeup time the next day.
-h [hours]  : Set wakeup time after [hours].
-m [minutes]    : Set wakeup time after [minutes].
```
