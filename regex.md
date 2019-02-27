# Regular Expressions / regex

## Remove duplicate lines in a sorted file

Per <https://stackoverflow.com/a/45829605/384316>

* search for `^(.*)(\n\1)+$`
* replace with `$1`