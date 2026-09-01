# 🔐 File Permissions & User Management

## 🛡️ File Permissions (chmod)

Shows perms like `-rwxr-xr--` (owner/group/other)

```bash
ls -l file.txt
```

Add execute permission for everyone

```bash
chmod +x script.sh
```

Remove execute permission

```bash
chmod -x script.sh
```

Add execute for owner (user) only

```bash
chmod u+x script.sh
```

Add write for group only

```bash
chmod g+w file.txt
```

Remove read for others

```bash
chmod o-r file.txt
```

Owner: rwx, group: r-x, other: r-x

```bash
chmod 755 script.sh
```

Owner: rw-, group: r--, other: r--

```bash
chmod 644 file.txt
```

Apply recursively to all files/dirs inside

```bash
chmod -R 755 folder
```

> Numeric permission values: read=4, write=2, execute=1 (add them up per owner/group/other).

## 👤 Ownership (chown / chgrp)

Change file owner to "ratul"

```bash
chown ratul file.txt
```

Change owner and group together

```bash
chown ratul:ratul file.txt
```

Change ownership recursively

```bash
chown -R ratul:ratul folder
```

Change group only

```bash
chgrp ratul file.txt
```

## 👥 Users & Groups

Create a new user

```bash
sudo useradd ratul
```

Set/change password for user

```bash
sudo passwd ratul
```

Delete a user

```bash
sudo userdel ratul
```

Delete a user and their home directory

```bash
sudo userdel -r ratul
```

Create a new group

```bash
sudo groupadd ratul
```

Delete a group

```bash
sudo groupdel ratul
```

Add user "admin" to group "ratul" (append, don't replace)

```bash
sudo usermod -aG ratul admin
```

Show groups a user belongs to

```bash
groups ratul
```

Show current logged-in user

```bash
whoami
```

Show current user's uid/gid and groups

```bash
id
```

Show who is logged in

```bash
who
```

Switch to user "ratul" (login shell)

```bash
su - ratul
```

Switch to root

```bash
sudo su -
```

## 🔑 Elevated Privileges

Run a single command as root

```bash
sudo command
```

Start an interactive root shell

```bash
sudo -i
```

List what the current user is allowed to run with sudo

```bash
sudo -l
```
