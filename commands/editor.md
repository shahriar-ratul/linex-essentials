# Vi / Vim Editor

vi server.txt           // open (or create) file in vi
vim server.txt          // open (or create) file in vim (vi improved)

## Modes

i                        // insert mode before cursor (start typing/editing)
a                        // insert mode after cursor
o                        // open a new line below and insert
Esc                      // back to normal mode from insert mode

## Save & Quit (from normal mode)

:w                       // save (write) without quitting
:q                       // quit (fails if there are unsaved changes)
:q!                      // force quit, discard unsaved changes
:wq                      // save and quit
:x                       // save and quit, only writes if file was changed
ZZ                       // save and quit (normal mode shortcut, same as :wq)
ZQ                       // quit without saving (same as :q!)
:qa                      // quit all open files/buffers
:qa!                     // force quit all open files, discard changes
:cq                      // quit and exit with error code (useful to abort git commit/rebase)

## Moving Around

h j k l                  // left, down, up, right
gg                       // go to first line of file
G                        // go to last line of file
:42                      // go to line 42
0                        // go to start of line
$                        // go to end of line
w / b                    // jump forward / backward one word

## Editing

dd                       // delete (cut) current line
yy                       // yank (copy) current line
p                        // paste after cursor
P                        // paste before cursor
x                        // delete character under cursor
u                        // undo
Ctrl+r                   // redo
/text                    // search forward for "text" (n = next match, N = previous)
:%s/old/new/g            // replace all "old" with "new" in whole file
:%s/old/new/gc           // same as above but confirm each replacement

## Notes

- git uses vi/vim by default for commit messages, rebase, etc.
- ":cq" is handy to abort a git commit/rebase cleanly without saving.
