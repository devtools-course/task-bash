# Directory stack

> Points: 15 \
> File: `stackd.sh`

You have to reimplement `pushd`-`popd`-`dirs` utils in bash. The script must provide a function `stackd` which can be used to replace `pushd`-`popd`-`dirs`.

> **You CANNOT use any of those commands!** To switch directories use `cd`.

## Synopsis

```text
stackd CMD

CMD:
    init          Initialise the directory stack with PWD as the first element
    
    list          Display the entire stack (dirs).
                  Example: 'top middle bottom'
    
    pop           Pop a dir from the stack and switch to the new top directory.
                  The second directory must be displayed (popd)
    
    push DIR      Push DIR onto the stack and switch to it (pushd)
```

## Error handling

When exiting due to an error, you must provide a description.
The description must be clear and concise.

### Invalid number of arguments
* `push`: exit code 11
* `pop`: exit code 21
* `list`: exit code 31
* `init`: exit code 41

### Invalid CMD
Exit code: 6

### DIR in push is not a directory
Exit code: 12

### Not enough elements to pop
Exit code: 22

### The directory does not exist when pop
Exit code: 23

---
+ Why do we use different exit codes?
+ How to store the stack? _You must choose the most optimal way!_
+ Why is your script executed with `source`? Try executing a script, which runs `cd` directly, and see the `PWD` afterwards. Why does it happen?
