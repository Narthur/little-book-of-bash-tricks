# Miscellaneous Tricks

## Use Terminal as a stop watch

To start stopwatch:

    time cat

To stop stopwatch:

    ctrl+c

## Send email attachment to multiple recipients using Mutt

    a="address1@gmail.com, address2@gmail.com"
    mutt -s "subject" -a file.pdf -- $a

## Search file contents recursively

    grep -r "needle" /path/to/search/
