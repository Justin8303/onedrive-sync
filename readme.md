# OneDrive-Sync

# Installation

## When to use?
If you have a drive with you, that you want to sync with any directory on your computer (e.g. OneDrive) and you need a backup or an offline version, this tool is for you.

## How to use?

1. Download the latest version of the [OneDrive-Sync](https://github.com/Justin8303/onedrive-sync/releases) from the release page.
2. Save the main.exe to any folder (that is persistent)
3. Install nssm.exe from [nssm.cc](https://nssm.cc/download)
4. Open a command prompt as administrator and run the following command:
```
nssm.exe install OneDrive-Sync
```
5. In the NSSM GUI, set the following:
```
Path: <path to main.exe>
Startup directory: <path to main.exe>
Arguments: --sync-programm <path to FreeFileSync.exe>
```
FFS Location is probably: C:\PROGRA~1\FreeFileSync\FreeFileSync.exe\
(note: you need to use PROGRA~1 instead of Program Files, because nssm does not support spaces in the path)

6. Click on Install Service
7. Open the Windows Services and start the OneDrive-Sync service
8. The drive you want to sync with and create a new FreeFileSync configuration with the name .sync.ffs_batch

### How to configure?
You need to create a file called .sync.ffs_batch in the root of the drive you want to sync with.\
If you plug in a drive with this file, the service will automatically start the sync process.

# Faq

### Why does this exist?
I have a drive with me, that I want to sync with my OneDrive.\

### Why is it called OneDrive-Sync?
Because I use it to sync my OneDrive with a drive.

### Issues
If you have any issues, please create an issue on the [issue page](https://github.com/Justin8303/onedrive-sync/issues).

### How to contribute?
If you want to contribute, please create a pull request on the [pull request page](https://github.com/Justin8303/onedrive-sync/pulls).

# References
- [NSSM](https://nssm.cc/)
- [FreeFileSync](https://freefilesync.org/)
- [Abdus](https://abdus.dev/posts/python-monitor-usb/)

(I've used the code from Abdus to monitor the USB drives)