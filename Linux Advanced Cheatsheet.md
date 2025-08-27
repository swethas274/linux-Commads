# 🐧 Linux Advanced Cheatsheet

This guide covers **advanced Linux commands and tools** for professionals, security researchers, and power users.  
Builds on top of Beginner + Intermediate levels.  

---

## 🔒 Security & Access Control
- **sudo** → run commands as root
- **visudo** → safely edit sudoers file
- **iptables** → firewall configuration
  ```bash
  sudo iptables -L
  sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT
ufw → simple firewall frontend

bash
Copy code
sudo ufw enable
sudo ufw allow 22/tcp
firewalld (RHEL/CentOS)

bash
Copy code
sudo firewall-cmd --add-port=8080/tcp --permanent
sudo firewall-cmd --reload
fail2ban → ban brute-force attacks (log-based)

SELinux (Fedora/RHEL)

bash
Copy code
getenforce
setenforce 0   # permissive
AppArmor (Ubuntu/Debian)

bash
Copy code
sudo aa-status
sudo aa-enforce /etc/apparmor.d/usr.bin.yourapp
🌐 Advanced Networking
ifconfig / ip → configure network interfaces

bash
Copy code
ip link set eth0 up
ip addr add 192.168.1.10/24 dev eth0
nmap → network scanner

bash
Copy code
nmap -sV 192.168.1.1
tcpdump → packet capture

bash
Copy code
sudo tcpdump -i eth0
wireshark / tshark → deep packet analysis

netcat (nc) → networking swiss-army knife

bash
Copy code
nc -lvp 4444
nc <ip> 4444
dig → DNS lookups

bash
Copy code
dig google.com
nslookup → alternative DNS lookup

ethtool → query NIC settings

mtr → traceroute + ping combined

⚙️ System Monitoring & Performance
dmesg → kernel ring buffer logs

vmstat → system performance

iostat (from sysstat) → CPU & I/O stats

iotop → monitor disk I/O usage

sar → system activity reports

free → memory usage

bash
Copy code
free -h
uptime → show load averages

lsof → list open files

bash
Copy code
lsof -i :22
strace → trace system calls

bash
Copy code
strace -p <PID>
perf → performance profiler

journalctl → view systemd logs

bash
Copy code
journalctl -xe
📦 Advanced File & Disk Management
lsblk → list block devices

blkid → get block device attributes

parted / fdisk → manage partitions

mkfs → create filesystem

bash
Copy code
mkfs.ext4 /dev/sdb1
tune2fs → adjust ext filesystems

fsck → check and repair filesystem

lvm (Logical Volume Manager)

bash
Copy code
pvcreate /dev/sdb
vgcreate myvg /dev/sdb
lvcreate -L 10G -n mylv myvg
🐚 Advanced Shell Usage
xargs → build and execute command lines

bash
Copy code
ls *.log | xargs rm
awk → text processing

bash
Copy code
awk '{print $1,$3}' file.txt
sed → stream editor

bash
Copy code
sed 's/foo/bar/g' file.txt
grep -r → recursive search

bash
Copy code
grep -r "keyword" /etc
cut → extract columns

bash
Copy code
cut -d':' -f1 /etc/passwd
sort | uniq → sort and remove duplicates

tee → write to file + stdout

bash
Copy code
ls | tee files.txt
🛠 Debugging & Development Tools
gdb → GNU debugger

bash
Copy code
gdb ./a.out
objdump → view binary info

bash
Copy code
objdump -d binaryfile
hexdump → hex view of file

readelf → ELF file inspection

nm → list symbols in binaries

ldd → show shared libraries

make / cmake → build automation

pkg-config → compile with correct flags

🐳 Containers & Virtualization
docker basics

bash
Copy code
docker ps
docker run -it ubuntu bash
docker exec -it <container> bash
podman → daemonless container runtime

vagrant → manage virtual machines

qemu / kvm → virtualization tools

🧩 Advanced Scripting
Trap signals

bash
Copy code
trap "echo 'Ctrl+C detected'; exit" SIGINT
Functions

bash
Copy code
myfunc() {
    echo "Hello $1"
}
myfunc World
Case statements

bash
Copy code
case $1 in
    start) echo "Starting...";;
    stop)  echo "Stopping...";;
    *)     echo "Usage: $0 {start|stop}";;
esac
Cron jobs → scheduled tasks

bash
Copy code
crontab -e
0 3 * * * /path/to/script.sh   # run daily at 3AM
at command → one-time scheduled task

bash
Copy code
echo "echo Hello" | at now + 2 minutes
🔐 Forensics & Security Analysis
chkrootkit → rootkit detector

rkhunter → rootkit scanner

auditd → track system events

bash
Copy code
auditctl -w /etc/passwd -p wa
strings → extract readable text from binaries

sha256sum / md5sum → file integrity check

gpg → encryption/signing

bash
Copy code
gpg -c file.txt
gpg file.txt.gpg
📊 Kernel & System Tuning
sysctl → modify kernel parameters

bash
Copy code
sysctl -a
sudo sysctl -w net.ipv4.ip_forward=1
/proc filesystem → live kernel data

bash
Copy code
cat /proc/cpuinfo
cat /proc/meminfo
uptime → check load averages

ulimit → manage resource limits

bash
Copy code
ulimit -n 4096
