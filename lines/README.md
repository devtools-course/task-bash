# Line counter

> Points: 30 \
> File: `line-counter.sh`

You have to implement a script which calculates the LOC metric of a project. (LOC is `Lines Of Code`) 

## Synopsis

```text
line-counter.sh PROJECT_ROOT [OPTIONS]...

OPTIONS:
    -i, --include FILE      Calculate LOC only for the files whose extensions are
                            declared in FILE. FILE must follow the CSV format

    -e, --exclude FILE      Exclude files whose extension are declared in FILE.
                            FILE must follow the CSV format

When both options are used, -e excludes files from the set selected by -i.
```

Since the CSV format allows different separators, your script must automatically detect which one is used. It is guaranteed that the extensions consist of alphanumeric characters and maybe dots.

## Example

`./line-counter.sh -i a.csv`
* stdout: `12`
* stderr: ``

a.csv:
```csv
cpp,cc,cxx
hpp,hh,hxx
```

## Error handling
No error handling is required

---
+ What is the CSV format?
+ How to get a file extension?
+ How to safely pass data in a pipeline (`... | ...`)?
+ Why is `\n` important at the end of a file?
