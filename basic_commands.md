Perfect 👍 You want the **entire Linux Basics guide** formatted as a `README.md` file code block so you can copy-paste directly.
Here it is:


# 🐧 Linux Basics Cheatsheet

A beginner-friendly list of **essential Linux commands** and keywords.  
Useful for quick reference while learning Linux.  

---

## 📂 Navigation & File Management
- **pwd** → print working directory
  ```bash
  pwd
  # /home/user
  ```

* **cd** → change directory

  ```bash
  cd /etc
  cd Desktop
  cd ~   # home directory
  ```
* **ls** → list files and directories

  ```bash
  ls
  ls -l   # detailed list
  ls -a   # show hidden files
  ```
* **mkdir** → create directory

  ```bash
  mkdir projects
  ```
* **rmdir** → remove empty directory

  ```bash
  rmdir projects
  ```
* **touch** → create empty file

  ```bash
  touch notes.txt
  ```
* **cp** → copy file/directory

  ```bash
  cp file1.txt file2.txt
  cp -r dir1/ dir2/
  ```
* **mv** → move/rename file

  ```bash
  mv old.txt new.txt
  ```
* **rm** → remove file

  ```bash
  rm file.txt
  rm -r folder/
  ```

---

## 📖 Viewing & Editing

* **cat** → display file content

  ```bash
  cat file.txt
  ```
* **less** → view file page by page

  ```bash
  less file.txt
  ```
* **head** → show first lines of a file

  ```bash
  head file.txt
  ```
* **tail** → show last lines of a file

  ```bash
  tail -f logfile.log   # live logs
  ```
* **nano** → open file in Nano editor

  ```bash
  nano file.txt
  ```

  * `Ctrl+O` → save
  * `Ctrl+X` → exit
* **vim** → open file in Vim editor (if installed)

  ```bash
  vim file.txt
  ```

---

## ⚡ System Info & Utilities

* **whoami** → print current username

  ```bash
  whoami
  ```
* **hostname** → show computer name

  ```bash
  hostname
  ```
* **uname** → system info

  ```bash
  uname -a
  ```
* **date** → show system date/time

  ```bash
  date
  date -u   # UTC time
  ```
* **cal** → calendar

  ```bash
  cal
  cal -A 2 -B 1 8 2024   # Aug 2024 with context
  ```
* **history** → list commands history

  ```bash
  history
  history -c   # clear history
  ```
* **clear** → clear terminal screen

---

## 🔑 Permissions & Users

* **passwd** → change user password

  ```bash
  passwd
  ```
* **sudo -i** → switch to root user
* **exit** / `Ctrl+D` → exit terminal or log out
* **chmod** → change permissions

  ```bash
  chmod 755 script.sh
  ```
* **chown** → change file owner

  ```bash
  chown user:user file.txt
  ```

---

## 📚 Help & Documentation

* **man** → manual pages

  ```bash
  man ls
  ```
* **--help** → quick help for commands

  ```bash
  ls --help
  ```
* **info** → extended documentation

  ```bash
  info coreutils
  ```

---

## 📌 Process & System Monitoring

* **ps** → list processes

  ```bash
  ps aux
  ```
* **top** → live process viewer
* **htop** → interactive process viewer (if installed)
* **kill** → stop process

  ```bash
  kill -9 <PID>
  ```

---

## 📦 Package Management (varies by distro)

* Debian/Ubuntu:

  ```bash
  sudo apt update
  sudo apt install package-name
  ```
* RedHat/CentOS:

  ```bash
  sudo yum install package-name
  ```
* Arch:

  ```bash
  sudo pacman -S package-name
  ```

---

## 🔑 Important Directories

* `/root` → root user’s home directory
* `/boot` → kernel & boot loader files
* `/etc` → system configuration files
* `/home` → user directories
* `/mnt` → temporary mount point
* `/proc` → kernel & process info
* `/sys` → system hardware info
* `/dev` → device files
* `/bin` → essential binaries
* `/sbin` → system binaries
* `/lib` → system libraries
* `/usr` → user programs & libraries

---

## ⌨️ Useful Shortcuts

* **Ctrl+Alt+T** → open terminal
* **Ctrl+L** → clear screen (same as `clear`)
* **Ctrl+C** → stop running process
* **Ctrl+Z** → suspend process
* **fg** → bring suspended job to foreground

```

---

✅ This is a **complete README.md** for beginners in Linux.  
Would you like me to also make a **condensed 1-page cheatsheet version** (minimal commands only) so you can keep it as `Linux_Quick_Ref.md` alongside this detailed one?
```
