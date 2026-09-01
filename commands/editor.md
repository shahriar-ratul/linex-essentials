# ✏️ Vi / Vim Editor

Open (or create) file in vi

```bash
vi server.txt
```

Open (or create) file in vim (vi improved)

```bash
vim server.txt
```

## 🔀 Modes

Insert mode before cursor (start typing/editing)

```text
i
```

Insert mode after cursor

```text
a
```

Open a new line below and insert

```text
o
```

Back to normal mode from insert mode

```text
Esc
```

## 💾 Save & Quit (from normal mode)

Save (write) without quitting

```text
:w
```

Quit (fails if there are unsaved changes)

```text
:q
```

Force quit, discard unsaved changes

```text
:q!
```

Save and quit

```text
:wq
```

Save and quit, only writes if file was changed

```text
:x
```

Save and quit (normal mode shortcut, same as `:wq`)

```text
ZZ
```

Quit without saving (same as `:q!`)

```text
ZQ
```

Quit all open files/buffers

```text
:qa
```

Force quit all open files, discard changes

```text
:qa!
```

Quit and exit with error code (useful to abort a git commit/rebase)

```text
:cq
```

## 🧭 Moving Around

Left, down, up, right

```text
h j k l
```

Go to first line of file

```text
gg
```

Go to last line of file

```text
G
```

Go to line 42

```text
:42
```

Go to start of line

```text
0
```

Go to end of line

```text
$
```

Jump forward one word

```text
w
```

Jump backward one word

```text
b
```

## ✂️ Editing

Delete (cut) current line

```text
dd
```

Yank (copy) current line

```text
yy
```

Paste after cursor

```text
p
```

Paste before cursor

```text
P
```

Delete character under cursor

```text
x
```

Undo

```text
u
```

Redo

```text
Ctrl+r
```

Search forward for "text" (`n` = next match, `N` = previous)

```text
/text
```

Replace all "old" with "new" in whole file

```text
:%s/old/new/g
```

Same as above but confirm each replacement

```text
:%s/old/new/gc
```

## 📝 Notes

- git uses vi/vim by default for commit messages, rebase, etc.
- `:cq` is handy to abort a git commit/rebase cleanly without saving.
