# Process & Job Control

## Viewing Processes

ps                        // show processes running in current shell
ps aux                    // show ALL processes, all users, detailed
ps -ef                    // similar to ps aux, System V style
top                       // live view of processes, CPU/memory usage (q to quit)
htop                      // nicer interactive version of top (may need install)
pgrep nginx               // find PID(s) of processes matching "nginx"

## Killing / Signaling Processes

kill 1234                 // send TERM signal to process with PID 1234 (graceful stop)
kill -9 1234               // force kill (SIGKILL), can't be ignored
killall nginx              // kill all processes by name
pkill nginx                 // kill processes matching a name pattern

## Jobs & Background Tasks

command &                  // run command in background
jobs                        // list background jobs in current shell
fg                          // bring last background job to foreground
fg %1                       // bring job number 1 to foreground
bg                           // resume a stopped job in background
Ctrl+Z                       // suspend (pause) current foreground job
nohup command &              // run command immune to hangups (survives terminal close)
disown                        // detach a background job from the shell

## Priority

nice -n 10 command          // start command with lower priority (higher niceness = lower priority)
renice 10 -p 1234            // change priority of an already-running process
