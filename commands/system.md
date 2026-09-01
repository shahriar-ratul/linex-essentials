# 🖥️ System, Disk & Package Management

## 💽 Disk & Memory

Show disk space usage per mounted filesystem, human-readable

```bash
df -h
```

Show total size of a folder, human-readable

```bash
du -sh folder
```

Show size of each item in current dir

```bash
du -sh *
```

Show RAM/swap usage, human-readable

```bash
free -h
```

List mounted filesystems

```bash
mount
```

List block devices (disks/partitions)

```bash
lsblk
```

## 🕐 System Info & Time

How long the system has been running + load average

```bash
uptime
```

Show current date and time

```bash
date
```

Show current user

```bash
whoami
```

Kernel/system info

```bash
uname -a
```

Show Linux distro info

```bash
cat /etc/os-release
```

Manual page for a command (`q` to quit)

```bash
man command
```

Quick help/usage for a command

```bash
command --help
```

## 🔧 Services (systemd)

Check status of a service

```bash
systemctl status nginx
```

Start a service

```bash
systemctl start nginx
```

Stop a service

```bash
systemctl stop nginx
```

Restart a service

```bash
systemctl restart nginx
```

Start service automatically on boot

```bash
systemctl enable nginx
```

Stop auto-start on boot

```bash
systemctl disable nginx
```

View logs for a specific service

```bash
journalctl -u nginx
```

Follow system logs live

```bash
journalctl -f
```

## 📦 Package Management

Refresh package list (Debian/Ubuntu)

```bash
sudo apt update
```

Upgrade installed packages (Debian/Ubuntu)

```bash
sudo apt upgrade
```

Install a package (Debian/Ubuntu)

```bash
sudo apt install package
```

Remove a package (Debian/Ubuntu)

```bash
sudo apt remove package
```

Install a package (RHEL/CentOS, older)

```bash
sudo yum install package
```

Install a package (RHEL/Fedora, newer)

```bash
sudo dnf install package
```

## 🗜️ Archiving & Compression

Create a tar archive

```bash
tar -cvf archive.tar folder/
```

Extract a tar archive

```bash
tar -xvf archive.tar
```

Create a gzip-compressed tar archive

```bash
tar -czvf archive.tar.gz folder/
```

Extract a gzip-compressed tar archive

```bash
tar -xzvf archive.tar.gz
```

Create a zip archive

```bash
zip -r archive.zip folder/
```

Extract a zip archive

```bash
unzip archive.zip
```

Compress a file (creates `file.txt.gz`)

```bash
gzip file.txt
```

Decompress a `.gz` file

```bash
gunzip file.txt.gz
```

## 🌱 Environment & Shell

Print text

```bash
echo "hello"
```

Print an environment variable

```bash
echo $PATH
```

Set an environment variable for this shell session

```bash
export VAR=value
```

Create a shortcut command

```bash
alias ll='ls -la'
```

List all environment variables

```bash
env
```

Show which binary would run for a command

```bash
which command
```
