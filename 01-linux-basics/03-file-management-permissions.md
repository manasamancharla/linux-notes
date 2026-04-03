# File Management and Permissions
## File and Directory Management

- **`cp file1.txt file2.txt`** – Copies a file.
- **`cp -r dir1 dir2`** – Copies a directory recursively.
- **`mv old_name new_name`** – Moves or renames a file or directory.

## File Viewing and Editing

- **`more file.txt`** – Reads long text files page by page.
- **`head -n 10 file.txt`** – Displays the first 10 lines of a file.
- **`tail -n 10 file.txt`** – Displays the last 10 lines of a file.
- **`echo 'Hello' > file.txt`** – Writes text to a file, overwriting existing content.
- **`echo 'Hello' >> file.txt`** – Appends text to a file without overwriting.

## File and Directory Permissions
Each file and directory has three levels of permission:
- **Owner (User)**: The creator of the file.
- **Group**: Users belonging to the assigned group.
- **Others**: All other users on the system.

Permissions are represented as:
- **Read (`r` or `4`)** – View file contents.
- **Write (`w` or `2`)** – Modify file contents.
- **Execute (`x` or `1`)** – Run scripts or programs.

**For directories, execute (x) means the ability to enter (cd) the directory.**

### Modify permissions using symbols:
- Add (`+`), remove (`-`), or set (`=`) permissions.

Set full access for user, read/execute for group, and no access for others
```bash
chmod u=rwx,g=rx,o= filename
```

### Using Numeric (Octal) Mode
Each permission has a value.Their sum is the overall permission for a category
- Read (`4`), Write (`2`), Execute (`1`).

User (rwx), Group (r-x), Others (r-x)
```bash
chmod 755 filename  
```
**`ls -l` lists files and directories in long (detailed) format.**

### Default Permissions: `umask`
- It controls the default permissions for new files and directories.
- Files default = 666, directories default = 777
- `umask` is subtracted from default permissions to give the actual permission a file or dir for a category.

Check current umask:
```bash
umask #0022
```
Now
```
New file: 666-022 = 644 (rw-r--r--)
New dir:  777-022 = 755 (rwxr-xr-x)
```

Set a new umask:
```bash
umask 022  # Default: 755 for directories, 644 for files
```

### Changing Ownership with `chown`
```bash
chown user filename  
```


### Changing Group Ownership with `chgrp`
```bash
chgrp group filename 
```
## Archiving and Compression
- `tar` is used for creating and extracting archives.

| Option | Description |
|-----|-------------|
| `c` | create archive |
| `v` | verbose |
| `f` | filename of archive |
| `x` | extract archive |
| `z` | gzip compression |
| `j` | bzip2 compression |
| `J` | xz compression |

Naming conventions for easy understanding, not rules enforced by the system.

### Archiving and extracting with `tar`
```bash
tar -cvf archive.tar filename_or_directory 
tar -xvf archive.tar 
```

### Archiving and extracting with `tar` and gzip compression
```bash
tar -czvf archive.tar.gz filename_or_directory 
tar -xzvf archive.tar.gz 
```

### gzip and gunzip
Compresses and decompresses individual files (not directories)

| Option | Description |
|-----|-------------|
| `k` | Keep the original file |

```bash
gzip -k file.txt # file.txt.gz
gunzip file.txt.gz
```

### bzip2 and bunzip2
Provides better compression than gzip, but slower.

| Option | Description |
|-----|-------------|
| `k` | Keep the original file |

```bash
bzip2 file.txt # file.txt.bz2
bunzip2 file.txt.bz2
```

### xz and unxz
Provides highest compression ratio, but slowest compression speed.

| Option | Description |
|-----|-------------|
| `k` | Keep the original file |

```bash
xz file.txt # file.txt.xz
unxz file.txt.xz
```

### zip and unzip
Zip is a cross-platform format

| Option | Description |
|-----|-------------|
| `r` | recursive (used for directories) |
| `d` | destination path (unzip) |


```bash
zip -r archive.zip directory/
unzip archive.zip -d .
```