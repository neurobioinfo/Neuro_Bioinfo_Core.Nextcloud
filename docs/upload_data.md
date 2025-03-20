# Moving Data onto Neuro_Bioinfo_Core Nextcloud Server

## From your local machine

This option is most appropriate for smaller datasets, usually hosted on your local machine or an external drive

1. Log into [the Neuro_Bioinfo_Core Nextcloud server](https://neurobioinfo.github.io/Neuro_Bioinfo_Core.Nextcloud) and click the "Files" icon on the top-left

2. Navigate to your group's data folder (hint: name most likely will be "[PI's last name]Lab")

3. Click on the "+" button and choose "Upload file"
> Create local folders as needed to organize your data

![nextcloud howto2-optimized](https://github.com/neurobioinfo/Neuro_Bioinfo_Core.Nextcloud/assets/35270039/b06522fc-beb5-493a-9dd4-83e148de8919)

## From Digital Alliance HPC:

This option is most appropriate for larger datasets, in particular those which are already stored on some HPC server hosted by the Digital Alliance

1. Copy data to your group's sub-folder within /lustre04/scratch/spiegelm/Neuro_Bioinfo_Core.Nextcloud/transfer_tmp on beluga.computecanada.ca
> Connect to beluga by your preferred method (filezilla, globus, terminal command-line, etc.)
> > If a folder for your group doesn't already exist, please ask the Neuro Bioinfo Core to create it for you
* you MUST set your linux permissions so the "other" user can read all files, and read + execute all folders you wish to upload. i.e. in your upload folder, run the following commands:
```
find -type f -exec chmod o+r {} \;
find -type d -exec chmod o+rx {} \;
```
* don't worry, once they are on nextcloud, these permissions will no longer apply; it's just to manage the upload

&nbsp;&nbsp;&nbsp;&nbsp;**__Wait at least 6 hours before going to the next step. The data has to migrate behind the scenes__**

&nbsp;&nbsp;&nbsp;&nbsp;**__If you want to move in more than 5TB of data at a time, please contact neurobioinfo@mcgill.ca to co-ordinate before you begin__**

2. Log into [the Neuro_Bioinfo_Core Nextcloud server](https://neurobioinfo.github.io/Neuro_Bioinfo_Core.Nextcloud) and click the "Files" icon on the top-left 

3. Navigate to your group's data folder (name will be something like "[PI's last name]Lab")

4. If the transfer has completed successfully, all the folders you copied in step 1 should be there.

5. If your data does not appear where it should  
&nbsp;&nbsp;&nbsp;&nbsp;- *Try again in a few hours (especially if there is a large data transfer underway)*  
&nbsp;&nbsp;&nbsp;&nbsp;- *Contact the NeuroBioinfo Core at neurobioinfo@mcgill.ca for support*

### 