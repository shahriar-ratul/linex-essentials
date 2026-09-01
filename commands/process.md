# ⚙️ Process & Job Control

## 🔍 Viewing Processes

Show processes running in current shell

```bash
ps
```

Show ALL processes, all users, detailed

```bash
ps aux
```

Similar to `ps aux`, System V style

```bash
ps -ef
```

Live view of processes, CPU/memory usage (`q` to quit)

```bash
top
```

Nicer interactive version of top (may need install)

```bash
htop
```

Find PID(s) of processes matching "nginx"

```bash
pgrep nginx
```

## 💀 Killing / Signaling Processes

Send TERM signal to process with PID 1234 (graceful stop)

```bash
kill 1234
```

Force kill (SIGKILL), can't be ignored

```bash
kill -9 1234
```

Kill all processes by name

```bash
killall nginx
```

Kill processes matching a name pattern

```bash
pkill nginx
```

## 🧳 Jobs & Background Tasks

Run command in background

```bash
command &
```

List background jobs in current shell

```bash
jobs
```

Bring last background job to foreground

```bash
fg
```

Bring job number 1 to foreground

```bash
fg %1
```

Resume a stopped job in background

```bash
bg
```

Run command immune to hangups (survives terminal close)

```bash
nohup command &
```

Detach a background job from the shell

```bash
disown
```

> `Ctrl+Z` suspends (pauses) the current foreground job.

## ⏱️ Priority

Start command with lower priority (higher niceness = lower priority)

```bash
nice -n 10 command
```

Change priority of an already-running process

```bash
renice 10 -p 1234
```
