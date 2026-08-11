# Scalar product

> Points: 10 \
> File: `prod.sh`

You have to calculate the scalar product of two vectors.

## Synopsis

```text
prod.sh 
```

The input consists of two lines (two vectors) with a space as a separator. 

## Example

`./prod.sh`
* stdin:
    ```
  1 2 3 4
  1 1 1 1
  ```
* stdout: `10`
* stderr: ``

## Error handling

When exiting due to an error, you must provide a description.
The description must be clear and concise.

### Non-numeric symbols
Exit code: 11

### Mismatched number of elements
Exit code: 10

---
+ How to read a line from stdin and split it?
+ How to test whether a string is a number?
