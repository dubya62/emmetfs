# EmmetFs
* An emmet-like tool to quickly create nested directories and files.

## TODO
* Grouping
* Multiplying and auto numbering

## Syntax
```
emmetfs <emmetfs_string>
```
* emmetfs_string is a string that uses the following syntax
```
directoryName>_fileName{file contents}+_anotherFile^anotherDirectory
```
* > = nested file or directory
    * You may only nest files or directories in directories
* _ = indicate that this is a file (only if at the beginning of a name)
* {} = Insert this text into the file (TODO: add escape character handling to be able to insert right curly brace)
    * Files without this are initialized as empty
* + = sibling file/directory
* ^ = move back up a directory
    * You may not move above the starting working directory

## Usage
```
usage: emmetfs [-h] [-d WORKING_DIRECTORY] [-p] [-o] emmetfs_string

positional arguments:
  emmetfs_string

options:
  -h, --help            show this help message and exit
  -d, --working-directory WORKING_DIRECTORY
                        Directory to perform operations from
  -p, --print-tree      Print the parsed file structure and exit.
  -o, --overwrite       Overwrite existing files/directories with
                        naming conflicts instead of throwing an
                        error.
```

