# Downloading large datasets

To download a large dataset from our cloud you need to have installed the package "rclone". If you're downloading on DRAC clusters, rclone is already installed.

Next steps will guide you in the downloading process using a command line:

## 1. If you're not downloading in DRAC clusters, install rclone:
```
sudo apt  install rclone
```

## 2. Setup rclone configuration (you will need your NeuroVIP user name and your password)

Run next command to setup rclone configuration. Make this whether you have a local installation of rclone, or if you are going to download on DRAC clusters.
```
rclone config
```

Chose or type next options for the different parameters:
```
Chose "n"  #for new remote

Enter name for new remote --> neurovip

Type of storage to configure --> <number> / WebDAV

URL of http host to connect to --> https://206-12-88-239.cloud.computecanada.ca/nextcloud/remote.php/dav/files/<your NeuroVIP username>

Name of the WebDAV site/service/software you are using --> <number> / Nextcloud

User name --> <your NeuroVIP username>

chose "y" to enter password

Password --> <your password>

Leave "Option bearer_token" empty

choose "no" for "Edit advanced config"

choose "yes" for "Keep this 'nextcloud' remote"

choose "q" to quit config
```

## 3. Go to your download folder and create a folder that will receive the data:
```
cd <download folder>
mkdir <destination folder name>
```

## 4. Run next command to begin downloading
```
rclone sync -v neurovip:/path/file <destination folder name> 2>&1|tee -a nexcloud_download.log
```

## Notes:
If downloading gets interrupted the same command will resume the download.
The log file contains all information about the download.
If you're on a Compute Canada server, you may want run this command within an "screen" created with the "screen" command.






