# Column

> Points: 15 \
> File: `column.sh`

You have to reimplement `column` util in bash. 

> **You CANNOT use `column` in your implementation!**

## Synopsis

```text
column.sh [-s SEPARATOR] 

OPTIONS:
    -s SEPARATOR      The character used to split the rows.
                      The default value is ' ' (a space)
```

The semantics of your script must be the same as that of `column -s SEPARATOR -t` from `utils-linux`, except for the last column: it must not be followed by spaces.

## Example

`./column.sh -s ','`
* stdin:
    ```
  aq,s,fp
  e,rtu,t
  ```
* stdout:
    ```
  aq  s    fp
  e   rtu  t
  ```
* stderr: ``

## Error handling

When exiting due to an error, you must provide a description.
The description must be clear and concise.

### Invalid option
Exit code: 1

### Missing the value for `-s`
Exit code: 2

### Non-matching number of elements
Exit code: 3

---
+ How to print something to stderr?
+ How to split data by a separator without reading the string char-by-char?
+ How to parse the options with default values?
