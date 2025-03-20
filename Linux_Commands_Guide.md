# Linux Commands Guide (Debian-Based Systems)

## Introduction
Linux commands are the backbone of system administration and daily operations. This guide covers essential commands for Debian-based distributions like Ubuntu, Linux Mint, and Debian itself. From basic file handling to advanced system management, this guide will help you master Linux.

---

## 1. Basic Commands
These commands are essential for navigating the filesystem and handling files.

### 1.1 File & Directory Management
| Command | Description | Example |
|---------|-------------|---------|
| `ls` | Lists files and directories in the current directory. | `ls -l` (detailed list) |
| `cd [dir]` | Changes the current directory to `[dir]`. | `cd /home/user/Documents` |
| `pwd` | Prints the current working directory. | `pwd` |
| `mkdir [dir]` | Creates a new directory named `[dir]`. | `mkdir new_folder` |
| `rm [file/dir]` | Removes a file or directory (use `rm -r` for directories). | `rm file.txt` or `rm -r old_folder` |
| `cp [source] [destination]` | Copies a file or directory. | `cp file.txt /home/user/backup/` |
| `mv [source] [destination]` | Moves or renames a file or directory. | `mv oldname.txt newname.txt` |

### 1.2 File Permissions & Ownership
| Command | Description | Example |
|---------|-------------|---------|
| `chmod [permissions] [file]` | Changes file permissions. | `chmod 755 script.sh` |
| `chown [user]:[group] [file]` | Changes ownership of a file or directory. | `chown user:user file.txt` |
| `ls -l` | Lists files with detailed information including permissions. | `ls -l /home/user/` |

### 1.3 Package Management (APT)
| Command | Description | Example |
|---------|-------------|---------|
| `apt update` | Updates the package lists. | `sudo apt update` |
| `apt upgrade` | Upgrades all installed packages. | `sudo apt upgrade -y` |
| `apt install [package]` | Installs a package. | `sudo apt install vim` |
| `apt remove [package]` | Removes a package. | `sudo apt remove firefox` |
| `dpkg -i [package.deb]` | Installs a `.deb` package manually. | `sudo dpkg -i software.deb` |

---

## 2. Intermediate Commands
### 2.1 Process Management
| Command | Description | Example |
|---------|-------------|---------|
| `ps aux` | Displays running processes. | `ps aux | grep apache` |
| `kill [PID]` | Terminates a process by Process ID. | `kill 1234` |
| `top` / `htop` | Shows real-time system processes and resource usage. | `top` or `htop` |
| `jobs` | Lists background jobs. | `jobs` |
| `fg [job_id]` | Brings a background job to the foreground. | `fg %1` |

### 2.2 Disk & Storage Management
| Command | Description | Example |
|---------|-------------|---------|
| `df -h` | Shows disk space usage. | `df -h` |
| `du -sh [dir]` | Displays the size of a directory. | `du -sh /var/log` |
| `fdisk -l` | Lists available storage devices and partitions. | `sudo fdisk -l` |
| `mount [device] [dir]` | Mounts a filesystem. | `sudo mount /dev/sdb1 /mnt/usb` |
| `umount [device]` | Unmounts a filesystem. | `sudo umount /mnt/usb` |

### 2.3 Networking
| Command | Description | Example |
|---------|-------------|---------|
| `ip a` | Displays IP addresses and interfaces. | `ip a` |
| `ping [host]` | Checks connectivity to a host. | `ping google.com` |
| `wget [URL]` | Downloads files from the internet. | `wget http://example.com/file.zip` |
| `curl -O [URL]` | Fetches files from the web. | `curl -O http://example.com/file.zip` |
| `netstat -tulnp` | Shows active network connections. | `sudo netstat -tulnp` |
| `nmap [IP]` | Scans a target IP for open ports. | `nmap 192.168.1.1` |

---

## 3. Advanced Commands
### 3.1 Shell Scripting Basics
```bash
#!/bin/bash
echo "Hello, World!"
```
| Concept | Example |
|---------|---------|
| Variables | `name="Linux"; echo $name` |
| Conditional | `if [ -f file ]; then echo "File exists"; fi` |
| Looping | `for i in {1..5}; do echo $i; done` |

### 3.2 System Monitoring
| Command | Description | Example |
|---------|-------------|---------|
| `vmstat` | Shows system performance statistics. | `vmstat 2 5` (updates every 2 seconds, 5 times) |
| `iostat` | Displays CPU and disk usage statistics. | `iostat -x 2` (shows extended statistics every 2 seconds) |
| `sar -u 5 10` | Monitors CPU usage every 5 seconds, 10 times. | `sar -u 5 10` |

### 3.3 Security & Firewalls
| Command | Description | Example |
|---------|-------------|---------|
| `ufw enable` | Enables the Uncomplicated Firewall (UFW). | `sudo ufw enable` |
| `ufw allow [port]` | Allows a specific port through the firewall. | `sudo ufw allow 22/tcp` |
| `iptables -L` | Lists firewall rules. | `sudo iptables -L -v -n` |
| `fail2ban-client status` | Checks the status of Fail2Ban (prevents brute force attacks). | `sudo fail2ban-client status sshd` |

---

## Conclusion
Mastering Linux commands improves your efficiency as a system administrator or security engineer. Keep practicing and exploring new commands. 

🚀 **Happy Learning!**
