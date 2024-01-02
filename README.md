# usenetBackup

## Q: why not simply use the usenet to store backups?

A: because everyone will be able to read the data in the next 5000d+

* you could use a 7z-password (secure? - no!)
* you could encrypt it with gpg (secure? - better, but how long does it take to break it in 5000d+?)
* you could post it in a way nobody is able to find it without a suitable nzb-file (secure? - dont know!)

***Dont use usenetBackup for any information you wouldnt write on a postcard!***

## requirements

* usenet provider allowing you to post
* ngPost (cli version is fine) installed in $HOME/bin

## install

* copy usenetBackup into any $PATH directory, f.e. $HOME/bin or /usr/local/bin

## use

```
export NZB_DIR=/mnt/data/usenetBackup/
usenetBackup <FileOrDirectoryToBackup>
```

now you **have to backup** the newly created .nzb in /mnt/data/usenetBackup/ to some safe place. **Without this .nzb you wont be able to restore your data!**

## restore

In case your data get damaged.

* restore the .nzb from your (real) backup solution
* use any usenet client to download your files again
* a good (sabnzbd) usenet client will read the (random) password from the .nzb, if not - use your favorite texteditor to get it.
* unpack the 7z archive
* your files are back.
