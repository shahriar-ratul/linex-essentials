# 📁 File & Directory Basics

## 🧭 Navigation

Print current working directory

```bash
pwd
```

Go into "test" folder

```bash
cd test
```

Go up one folder

```bash
cd ..
```

Go to home directory

```bash
cd ~
```

Go to previous directory

```bash
cd -
```

List files in current dir

```bash
ls
```

List all files, including hidden (dotfiles)

```bash
ls -a
```

Long listing (permissions, owner, size, date)

```bash
ls -l
```

Long listing + hidden files

```bash
ls -la
```

Long listing with human-readable sizes (K/M/G)

```bash
ls -lh
```

Alphabetic reverse order

```bash
ls -lr
```

Order by modified time, newest on top

```bash
ls -lt
```

Order by modified time, oldest on top

```bash
ls -ltr
```

Show directory structure as a tree (may need install)

```bash
tree
```

Clear current terminal window

```bash
clear
```

Show command history

```bash
history
```

Print system/kernel name

```bash
uname
```

Print all system info (kernel, hostname, arch)

```bash
uname -a
```

## 🆕 Create / Remove

Create a directory

```bash
mkdir test
```

Create nested directories in one go

```bash
mkdir -p a/b/c
```

Create a new empty file (or update its timestamp)

```bash
touch linex.txt
```

Remove an EMPTY directory

```bash
rmdir test
```

Remove a file

```bash
rm test
```

Remove a folder and everything inside it (no confirm, careful!)

```bash
rm -rf test
```

Remove all `.txt` files in current dir

```bash
rm *.txt
```

Create a symbolic (soft) link

```bash
ln -s target linkname
```

## 🔁 Copy / Move / Rename

Copy a file

```bash
cp info.txt server_new.txt
```

Copy a directory recursively

```bash
cp -r dir1 dir2
```

Rename a file

```bash
mv aws.txt server.txt
```

Move a file into "folder"

```bash
mv server.txt folder
```

## 👀 Viewing File Content

Print whole file content

```bash
cat server.txt
```

Print with line numbers

```bash
cat -n server.txt
```

Create/overwrite file, type content, then `Ctrl+D` to save

```bash
cat > server.txt
```

Append content to file, then `Ctrl+D` to save

```bash
cat >> server.txt
```

Concatenate two files into one (overwrites target)

```bash
cat info.txt server.txt > server.txt
```

Print file content in reverse line order

```bash
tac info.txt
```

Reverse each line's characters

```bash
rev info.txt
```

First 10 lines

```bash
head info.txt
```

First 4 lines

```bash
head -n 4 info.txt
```

Last 10 lines

```bash
tail info.txt
```

Last 5 lines

```bash
tail -n 5 info.txt
```

Follow file live as it grows (logs)

```bash
tail -f server.log
```

Page through a file (`q` to quit, `/` to search)

```bash
less server.txt
```

Page through a file, simpler than `less`

```bash
more server.txt
```

Count lines, words, bytes

```bash
wc server.txt
```

Count lines only

```bash
wc -l server.txt
```

## 🔎 Searching & Filtering

Print lines containing "test"

```bash
grep "test" server.txt
```

Print lines NOT containing "test"

```bash
grep -v "test" server.txt
```

Case-insensitive search

```bash
grep -i "test" server.txt
```

Count matching lines

```bash
grep -c "test" server.txt
```

Search recursively in all files under current dir

```bash
grep -r "test" .
```

Show line numbers with matches

```bash
grep -n "test" server.txt
```

Find files by name under current dir

```bash
find . -name "*.txt"
```

Find directories by name

```bash
find . -type d -name "test"
```

Fast filename search (needs `updatedb` / `mlocate` installed)

```bash
locate filename
```

Show full path of a command

```bash
which bash
```

Show binary/source/man locations of a command

```bash
whereis bash
```

Sort lines alphabetically

```bash
sort server.txt
```

Sort lines numerically

```bash
sort -n numbers.txt
```

Remove adjacent duplicate lines (sort first for full dedup)

```bash
uniq server.txt
```

Show differences between two files

```bash
diff server.txt info.txt
```
