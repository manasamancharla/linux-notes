# System Monitoring

## CPU and Memory Monitoring

`top` – To view real-time CPU and memory usage

`vmstat` - To check CPU, memory, and I/O stats
```bash
vmstat
```
```bash
vmstat 2 5 # Update every 2 sec, show 5 updates. Both are optional
```

`free -m` - Shows free and used memory in mb.

## Disk Monitoring

`df -h` - Shows filesystem level disk usage

`du -sh /path` - Show size of a directory

`lsblk` - Shows disk and partition structure









