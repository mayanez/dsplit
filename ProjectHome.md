Simple python script designed to be a helper to k3b/growisofs. If you have a large directory you want backed up to CD/DVD, then **dsplit** splits the directory into multiple CD/DVD sized directories. (The output of **dsplit** consists of directories named `vol-%2d`, which are _hard linked_ to portions of the source directory. Thus your precious source is left untouched, and the **dsplit** output consumes almost no space.

## USAGE ##
**dsplit** `[options]` _src_ _dst_

Splits _src_ into CD/DVD sized sub-directories. Output is in `vol-%2d` subdirs of _dst_, and by default the files are hard-linked to the source (so they consume no space).

### OPTIONS ###
> `-s` _size_, `--volume-size=`_size_
> > Size of each volume in MB (default 4400MB)

> `--for-dvd`
> > Set volume size for DVD (4400MB)

> `--for-dvd2`
> > Set volume size for double layer DVD (8080MB)

> `--for-cd`
> > Set volume size for CD (680MB)

> `-v`
> > Verbose (print all subdirectories included in volumes)

> `-V`
> > Very verbose (print all files included too)