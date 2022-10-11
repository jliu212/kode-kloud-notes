# Working with Shell II

## Fire Compression and Archival

### `DU` disk usage

`du -sk` show size of the file
`du -sh` prints the size as human readable format
`ls -lh` shows file with size

### `tar` Tape Archive

`tar -c` create archive
`tar -f` specify the name
`tar -tf` to see content
`tar -xf` to extract content
`tar -zcf` to compress

### Compressing

Compression algroithm and compression level

`bzip2` add .bz2
`bunzip2` decompressing
`bzcat` to show content without uncompressing

`gzip` add .gz
`gunzip` decompressing
`zcat`

`xz` add .sz
`unxz` decompressing
`xzcat`

## Searching for Files and directories

`locate` find files quickly, depends mlocate.db, which may not be updated
`updatedb` to update mlocate.db

`find /path/to/di -name` find the file within the directory

`grep` search files that contains a string
`grep -i` case insensitive
`grep -r` recursive
`grep -v` inverse pattern matching
`grep -w` to search for whold words
`grep -A` print line below the matching pattern
`grep -B` print line above the mathcing pattern

### IO Redirection

standard input
standard output
standard error

redirect stdout
`>` new file
`>>` append to existing file

redirect stderr
`2>` error
`2>>` to append to existing file
/dev/null the bit bucket

### Command line pipes

Allwo linking of muiltiple commands
`command 1 | command 2`

`echo $SHELL | tee shell.txt`
