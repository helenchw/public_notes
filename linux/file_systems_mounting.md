# Notes on File System Mounting

## Davfs2 

(Ubuntu Linux, 22.04)

`mount.davfs2` creates a cache file under `/var/cache/davfs2/` or `~/.davfs2/cache` by default.
Thus, one needs to make sure the folders have sufficient space for caching the *whole* file to upload.
The cache directory paths are configurable in `/etc/davfs2/davfs.conf` and `~/.davfs/davfs.conf`  through the option `cache_dir`.

(Reference: https://linux.die.net/man/8/mount.davfs)
