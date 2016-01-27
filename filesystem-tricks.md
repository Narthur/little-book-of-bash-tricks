# Filesystem Tricks

## Get size of a directory in Unix terminal

    du -sh directory_name
    
[Source](http://unix.stackexchange.com/a/3021/138212)

## Compare two directories recursively 

    diff --recursive --brief /tmp/dir1 /tmp/dir2
    
[Source](http://www.unixtutorial.org/2008/06/how-to-compare-directories-in-unix/)

## Find largest files

### In single directory

    ls -lhS

Option | Effect
-------|---------------------------
`-l`   | long listing
`-h`   | human readable file sizes
`-S`   | sort by file size

Pipe output to `tail` to see only the top ten results:

    ls -lhS | tail

Advantages:

- Incredibly fast.
- Elegant.
- Outputs human-readable size.

### Recursively

    sudo find /path/to/search/ -size +15M -printf "%s - %p\n" | sort -n | tail

Advantages:

- Outputs path to each file.
- Correctly sorts files while doing a full recursive search.
