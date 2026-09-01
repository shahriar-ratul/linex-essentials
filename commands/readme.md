# File & Directory Basics

## Navigation

pwd                     // print current working directory
cd test                 // go into "test" folder
cd ..                   // go up one folder
cd ~ or cd              // go to home directory
cd -                    // go to previous directory
ls                      // list files in current dir
ls -a                   // list all files, including hidden (dotfiles)
ls -l                   // long listing (permissions, owner, size, date)
ls -la                  // long listing + hidden files
ls -lh                  // long listing with human-readable sizes (K/M/G)
ls -lr                  // alphabetic reverse order
ls -lt                  // order by modified time, newest on top
ls -ltr                 // order by modified time, oldest on top
tree                    // show directory structure as a tree (may need install)
clear                   // clear current terminal window
history                 // show command history
uname                   // print system/kernel name
uname -a                // print all system info (kernel, hostname, arch)

## Create / Remove

mkdir test              // create a directory
mkdir -p a/b/c          // create nested directories in one go
touch linex.txt         // create a new empty file (or update its timestamp)
touch shell.txt
rmdir test              // remove an EMPTY directory
rm test                 // remove a file
rm -rf test             // remove a folder and everything inside it (no confirm, careful!)
rm *.txt                // remove all .txt files in current dir
ln -s target linkname   // create a symbolic (soft) link

## Copy / Move / Rename

cp info.txt server_new.txt   // copy a file
cp -r dir1 dir2               // copy a directory recursively
mv aws.txt server.txt         // rename a file
mv server.txt folder          // move a file into "folder"

## Viewing File Content

cat server.txt               // print whole file content
cat info.txt                 // all file content
cat -n server.txt            // print with line numbers
cat > server.txt             // create/overwrite file, type content, Ctrl+D to save
welcome to server
cat >> server.txt            // append content to file, Ctrl+D to save
server info aws
cat info.txt server.txt > server.txt   // concatenate two files into one (overwrites target)
tac info.txt                 // print file content in reverse line order
rev info.txt                 // reverse each line's characters
head info.txt                // first 10 lines
head -n 4 info.txt            // first 4 lines
tail info.txt                // last 10 lines
tail -n 5 info.txt            // last 5 lines
tail -f server.log            // follow file live as it grows (logs)
less server.txt               // page through a file (q to quit, / to search)
more server.txt               // page through a file, simpler than less
wc server.txt                 // count lines, words, bytes
wc -l server.txt              // count lines only

## Searching & Filtering

grep "test" server.txt        // print lines containing "test"
grep -v "test" server.txt     // print lines NOT containing "test"
grep -i "test" server.txt     // case-insensitive search
grep -c "test" server.txt     // count matching lines
grep -r "test" .              // search recursively in all files under current dir
grep -n "test" server.txt     // show line numbers with matches
find . -name "*.txt"          // find files by name under current dir
find . -type d -name "test"   // find directories by name
locate filename                // fast filename search (needs updatedb / mlocate installed)
which bash                    // show full path of a command
whereis bash                  // show binary/source/man locations of a command
sort server.txt               // sort lines alphabetically
sort -n numbers.txt           // sort lines numerically
uniq server.txt               // remove adjacent duplicate lines (sort first for full dedup)
diff server.txt info.txt      // show differences between two files
