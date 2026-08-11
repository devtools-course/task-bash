# Symmetric difference

> Points: 15 \
> File: `sym-diff.sh`

You have to provide a function `sym-diff` that takes two arguments (the names of two arrays) and calculates their symmetric difference.

Each array represents a set of numbers so its element uniqueness is guaranteed.

The result (stdout) must be sorted in descending order.

> **Important! You cannot access arrays elements directly, use other commands that manipulate the data to achieve the goal.** You are allowed only to use `${_[@]}` at the beginning of your function to retrieve the data.

## Example

```bash
ar=(1 2)
ra=(1 3)

val=()
while read -r line; do val+=("$line"); done < <(sym-diff ar ra)
```

`val` is expected to be equal to `(3 2)`

## Error handling
No error handling is required

---
+ How to find all unique numbers? How to remove all other numbers?
+ How to sort numbers?
+ Can it be solved with a single pipeline (`... | ...`)?
