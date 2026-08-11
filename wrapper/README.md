# Wrapper

> Points: 25 \
> File: `wrapper.sh`

Spoiler alert! _You are going to find and study some new information yourself during this task._

Create a custom wrapper script which can be used as a shebang.

## What your wrapper must do
### Handle `SIGTERM` signal

Print `No no no, mr fish!` to stdout and log `SIGTERM detected` in `WARN` mode. You must prevent the script from termination.

### Track the inner script execution

* Log each command that is executed in `DEBUG` mode
* When the command is `echo`, it must be logged in `ERROR` mode and the wrapper must prevent `echo` from being executed.

### Logging

Log format: `MODE TIMESTAMP MESSAGE`
* `MODE` - find some information about log modes yourself
* `TIMESTAMP` - the timestamp of the log. Format: `YYYY-MM-DD HH:MM:SS`

All logs must be written to the file `$LOG_FILE` (passed as an env variable)


## Example

Inner script:
```bash
#! wrapper.sh

echo 3 4 5 6
ls -l | grep total | cut -f1 -d' '
```

stdout: `total`
stderr: ``

`$LOG_FILE`:
```log
ERROR 2026-02-26 11:14:51 echo 3 4 5 6
DEBUG 2026-02-26 11:14:51 ls -l
DEBUG 2026-02-26 11:14:51 grep total
DEBUG 2026-02-26 11:14:51 cut -f1 -d' '
```

> **Important!** Tests might fail if you run them at 23:59:_ (The date might change)

> **Important!** Use `fenrir rund` if your system's language is not English!

---
+ How to handle signals in bash?
+ Read about special signals in bash for tracking the execution.
+ You might need to use `set` and `shopt` commands to set up the execution.
+ How to get current datetime in bash?
