# rtcwake-linux
Program for autowakeup in linux when laptop is power off

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
Syntax: wakeup <hh:mm> [option]

options:
--help      : Print this Help.
-n      : Set wakeup time the next day.
-h [hours]  : Set wakeup time after [hours].
-m [minutes]    : Set wakeup time after [minutes].
source .bashrc
```


## Option 2: copy script 'wakeup' to folder that exist on path
check what are folders in path
```
echo $PATH
```
> /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/bin:/usr/games:/sbin:/home/theman49/bin

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
