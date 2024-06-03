# linux Command

## Basic Commands

`pwd` - present working device
```bash
  pwd
  #/home/root
```

`passwd` - change the password
```bash
  passwd
  #changing password for root
  #Current password: ************
  #New password: *********
```

`whoami` - username
```bash
  whoami
  # root
```

`cd` - change the current directory
```bash
  cd /etc
  cd Desktop
  cd ~
```

`ls` - list information or documents of the file
```bash
  ls
  ls /etc
```

`clear` or `L^` - clear the command window

`echo` - print the statement

`cal` - calendar
```bash
  cal -A x -B y z 20**
  # x,y : number
  # z : month
```

`date` - date
```bash
  date
  date -u
```

`history` or `history -c` - clears the history

`changing zsh <-> bash` - change bash to zshell or vice-versa
```
  which $SHELL
  chsh -s $(which $SHELL)
```

`ctrl+alt+t` - opening command

`ctrl+d` or `exit` - closing terminal

`sudo -i` - changing to root






## Some Keywords

`root`  - superuser's home directory 

`boat`  - kernel image

`etc`   - system configuration files

`home`  - use directory

`mnt`   - general purpose mount point

`proc`  - view of internal kernal data

`sys`   - kernel's view of hardware

`dev`   - special device files

`bin`   - binarier

`sbin`  - binaries

`lib`   - library

`usr`   - user library

