# Essential Linux Commands for DevOps Engineers

This cheat sheet covers must-know Linux commands for any DevOps engineer, categorized for easy access.

---

## 1. **File and Directory Management**
```bash
ls -l           # List files in long format
cd /path        # Change directory
pwd             # Print current working directory
mkdir newdir    # Create a new directory
rm file         # Remove file
rm -r dir       # Remove directory recursively
cp file1 file2  # Copy file
mv old new      # Move or rename file
find / -name "file.txt"  # Search for a file
```

## 2. **Permissions and Ownership**
```bash
chmod 755 script.sh         # Change permissions
chown user:group file       # Change ownership
ls -l                       # Check current permissions and ownership
```

## 3. **User and Group Management**
```bash
useradd newuser             # Add new user
passwd newuser              # Set password for user
usermod -aG group user      # Add user to group
groupadd devops             # Create new group
id user                     # Check groups of a user
```

## 4. **Process and Service Management**
```bash
top                        # Monitor system resources
htop                       # Interactive process viewer
ps aux                     # Show all processes
kill -9 PID                # Force kill a process
systemctl status nginx     # Check service status
systemctl start nginx      # Start a service
systemctl stop nginx       # Stop a service
```

## 5. **Networking**
```bash
ip a                       # Show IP addresses
ifconfig                   # View network config (older)
ip route                   # Show routing table
ping 8.8.8.8               # Ping a host
traceroute google.com      # Trace route to host
netstat -tulnp             # List listening ports and services
ss -tulwn                  # Faster netstat alternative
```

## 6. **Disk and File System**
```bash
df -h                      # Disk usage in human readable
du -sh *                   # Directory sizes in current path
mount /dev/sdb1 /mnt       # Mount a device
umount /mnt                # Unmount a device
lsblk                      # List block devices
```

## 7. **Archiving and Compression**
```bash
tar -czvf archive.tar.gz dir/   # Create compressed archive
tar -xzvf archive.tar.gz        # Extract archive
zip -r file.zip folder/         # Zip folder
unzip file.zip                  # Unzip file
```

## 8. **Package Management**
```bash
apt update && apt upgrade     # Update system (Debian/Ubuntu)
yum update                    # Update system (RHEL/CentOS)
apt install nginx             # Install package
apt remove nginx              # Remove package
```

## 9. **Crontab (Scheduling Jobs)**
```bash
crontab -e                    # Edit current user's crontab
crontab -l                    # List cron jobs
```

## 10. **SSH and Remote Access**
```bash
ssh user@ip_address           # Connect to remote machine
scp file user@ip:/path        # Secure copy
ssh-keygen                    # Generate SSH key
ssh-copy-id user@ip           # Copy public key to remote
```

## 11. **Log and Monitoring**
```bash
tail -f /var/log/syslog       # Monitor log file
journalctl -xe                # View system logs
uptime                        # Show system uptime
dstat                        # Real-time resource stats
```

## 12. **System Info and Debugging**
```bash
uname -a                      # Kernel and OS info
hostname                      # Show hostname
free -h                       # Show memory usage
strace ./script.sh            # Debug system calls
```

---

### Tip:
Practice these regularly in a sandbox VM or cloud lab. Real-world familiarity builds confidence for troubleshooting and automation tasks.

