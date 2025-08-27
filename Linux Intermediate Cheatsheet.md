# 🐧 Linux Intermediate Cheatsheet

A collection of **intermediate-level Linux commands and concepts**.  
This builds on top of the basics and helps you manage processes, networking, users, permissions, and more.  

---

## ⚡ Process Management
- **ps** → show running processes
  ```bash
  ps aux
  ps -ef
top → real-time process monitoring

htop → interactive process viewer (install separately)

kill → terminate a process

bash
Copy code
kill <PID>
kill -9 <PID>   # force kill
jobs → list background jobs

bg / fg → resume jobs in background/foreground

bash
Copy code
bg %1
fg %1
🔑 Permissions & Ownership
chmod → change file permissions

bash
Copy code
chmod 644 file.txt
chmod +x script.sh
chown → change ownership

bash
Copy code
chown user:user file.txt
umask → default permission mask

bash
Copy code
umask 022
🌐 Networking
ip addr → show IP addresses

bash
Copy code
ip addr show
ping → check connectivity

bash
Copy code
ping google.com
curl → transfer data from/to server

bash
Copy code
curl http://example.com
curl -I http://example.com   # headers only
wget → download files

bash
Copy code
wget http://example.com/file.zip
netstat (deprecated, use ss) → show connections

bash
Copy code
netstat -tulnp
ss → modern replacement for netstat

bash
Copy code
ss -tulwn
traceroute → trace route to host

bash
Copy code
traceroute google.com
📦 Package & Service Management
Debian/Ubuntu:

bash
Copy code
sudo apt update && sudo apt upgrade
sudo apt install package-name
sudo apt remove package-name
CentOS/RHEL:

bash
Copy code
sudo yum install package-name
sudo yum remove package-name
systemctl → manage services

bash
Copy code
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
sudo systemctl enable nginx
sudo systemctl status nginx
📚 Disk & File Utilities
df → check disk space

bash
Copy code
df -h
du → check folder size

bash
Copy code
du -sh /var/log
mount / umount → mount/unmount storage

bash
Copy code
mount /dev/sdb1 /mnt
umount /mnt
find → search for files

bash
Copy code
find / -name "file.txt"
find . -type f -size +10M
locate → fast file search (uses database)

bash
Copy code
locate passwd
file → check file type

bash
Copy code
file script.sh
strings → extract human-readable text

bash
Copy code
strings binaryfile
📦 Compression & Archiving
tar → archive/extract

bash
Copy code
tar -cvf archive.tar file1 file2
tar -xvf archive.tar
tar -czvf archive.tar.gz folder/
tar -xzvf archive.tar.gz
gzip / gunzip

bash
Copy code
gzip file.txt
gunzip file.txt.gz
zip / unzip

bash
Copy code
zip archive.zip file1 file2
unzip archive.zip
🌍 Environment Variables
echo → print variables

bash
Copy code
echo $PATH
export → set environment variable

bash
Copy code
export VAR=value
env → show environment variables

printenv → print variable values

bash
Copy code
printenv PATH
🛠 Useful Shortcuts & Tricks
alias → create command shortcuts

bash
Copy code
alias ll='ls -la'
history | grep → search command history

!! → run last command

!n → run nth command from history

Ctrl+R → reverse search in history

Ctrl+A → jump to start of line

Ctrl+E → jump to end of line

🐚 Shell Scripting Basics
Basic Script Example

bash
Copy code
#!/bin/bash
echo "Hello, World!"
Variables

bash
Copy code
NAME="Swetha"
echo "Hello $NAME"
Conditionals

bash
Copy code
if [ -f file.txt ]; then
    echo "File exists"
else
    echo "File not found"
fi
Loops

bash
Copy code
for i in 1 2 3
do
    echo "Number $i"
done
Execute script

bash
Copy code
chmod +x script.sh
./script.sh
🧩 Log Files (Common Locations)
System logs → /var/log/syslog

Authentication logs → /var/log/auth.log

Kernel logs → /var/log/kern.log

Service logs → /var/log/<service>/





