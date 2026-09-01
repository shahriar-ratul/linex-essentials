# File Permissions & User Management

## File Permissions (chmod)

ls -l file.txt                 // shows perms like -rwxr-xr--  (owner/group/other)
chmod +x script.sh             // add execute permission for everyone
chmod -x script.sh             // remove execute permission
chmod u+x script.sh            // add execute for owner (user) only
chmod g+w file.txt             // add write for group only
chmod o-r file.txt             // remove read for others
chmod 755 script.sh            // owner: rwx, group: r-x, other: r-x
chmod 644 file.txt             // owner: rw-, group: r--, other: r--
chmod -R 755 folder            // apply recursively to all files/dirs inside

Numeric permission values: read=4, write=2, execute=1 (add them up per owner/group/other).

## Ownership (chown / chgrp)

chown ratul file.txt           // change file owner to "ratul"
chown ratul:ratul file.txt     // change owner and group together
chown -R ratul:ratul folder    // change ownership recursively
chgrp ratul file.txt           // change group only

## Users & Groups

sudo useradd ratul             // create a new user
sudo passwd ratul              // set/change password for user
sudo userdel ratul             // delete a user
sudo userdel -r ratul          // delete a user and their home directory
sudo groupadd ratul            // create a new group
sudo groupdel ratul            // delete a group
sudo usermod -aG ratul admin   // add user "admin" to group "ratul" (append, don't replace)
groups ratul                   // show groups a user belongs to
whoami                         // show current logged-in user
id                              // show current user's uid/gid and groups
who                             // show who is logged in
su - ratul                      // switch to user "ratul" (login shell)
sudo su -                       // switch to root

## Elevated Privileges

sudo command                   // run a single command as root
sudo -i                         // start an interactive root shell
sudo -l                         // list what the current user is allowed to run with sudo
