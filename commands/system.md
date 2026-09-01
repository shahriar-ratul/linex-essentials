# System, Disk & Package Management

## Disk & Memory

df -h                        // show disk space usage per mounted filesystem, human-readable
du -sh folder                // show total size of a folder, human-readable
du -sh *                     // show size of each item in current dir
free -h                       // show RAM/swap usage, human-readable
mount                          // list mounted filesystems
lsblk                          // list block devices (disks/partitions)

## System Info & Time

uptime                         // how long the system has been running + load average
date                             // show current date and time
whoami                            // show current user
uname -a                          // kernel/system info
cat /etc/os-release                // show Linux distro info
man command                        // manual page for a command (q to quit)
command --help                      // quick help/usage for a command

## Services (systemd)

systemctl status nginx          // check status of a service
systemctl start nginx           // start a service
systemctl stop nginx            // stop a service
systemctl restart nginx         // restart a service
systemctl enable nginx          // start service automatically on boot
systemctl disable nginx         // stop auto-start on boot
journalctl -u nginx              // view logs for a specific service
journalctl -f                     // follow system logs live

## Package Management

sudo apt update                  // refresh package list (Debian/Ubuntu)
sudo apt upgrade                 // upgrade installed packages (Debian/Ubuntu)
sudo apt install package         // install a package (Debian/Ubuntu)
sudo apt remove package          // remove a package (Debian/Ubuntu)
sudo yum install package         // install a package (RHEL/CentOS, older)
sudo dnf install package         // install a package (RHEL/Fedora, newer)

## Archiving & Compression

tar -cvf archive.tar folder/       // create a tar archive
tar -xvf archive.tar               // extract a tar archive
tar -czvf archive.tar.gz folder/   // create a gzip-compressed tar archive
tar -xzvf archive.tar.gz           // extract a gzip-compressed tar archive
zip -r archive.zip folder/          // create a zip archive
unzip archive.zip                    // extract a zip archive
gzip file.txt                         // compress a file (creates file.txt.gz)
gunzip file.txt.gz                    // decompress a .gz file

## Environment & Shell

echo "hello"                    // print text
echo $PATH                       // print an environment variable
export VAR=value                  // set an environment variable for this shell session
alias ll='ls -la'                  // create a shortcut command
env                                 // list all environment variables
which command                       // show which binary would run for a command
