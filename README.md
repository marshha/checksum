# checksum
This utility generates or verifies checksums for each file in a specified file or directory.

## Generating checksum files
```
usage: checksum generate [-h] [--type {md5,sha1,sha256}] [--suffix SUFFIX]
                         filepath [filepath ...]

positional arguments:
  filepath              Filename or directory to checksum

optional arguments:
  -h, --help            show this help message and exit
  --type {md5,sha1,sha256}
                        Select a checksum algorithm
  --suffix SUFFIX       Select the checksum file suffix. Default is the
                        checksum algorithm
```

For a directory structure like this:
```
test1/
test1/testfile.txt
test1/subdir
test1/subdir/subfile2.txt
test1/subdir/subfile1.txt
```

These checksum files will be generated:
```
test1/
test1/testfile.txt.sha1
test1/subdir
test1/subdir/subfile1.txt.sha1
test1/subdir/subfile2.txt.sha1
```

The content of one checksum file:
```
$ cat test1/testfile.txt.sha1 
bdc37c074ec4ee6050d68bc133c6b912f36474df
```
