# Purpose/Principle
Best practice for archiving of essential data is that it should exist in multiple independent copies.  
This is meant to serve as a hedge against accidental deletion (human error) or equipment failure.  
The Neuro_Bioinfo_Core storage platform applies this principle to key data for each participating research group.

# Requirements and Limitations
### This backup policy is intended to be applied to raw data only.  
Any files which can be re-generated are not meant to be included.  
* Data to be backed up must be contained within your group's main folder, i.e. the one named [PIname]Lab, with a folder-and-arrow icon 
(<img src="https://github.com/neurobioinfo/Neuro_Bioinfo_Core.Nextcloud/assets/35270039/6f51436c-75b1-49f0-9aae-25e02a51a69e" width=25>)  
* Within that parent folder, data to be backed up will be the entire contents of the sub-folder named "raw.data". Only data in this folder will be backed up  
* Users are on their honour to put only essential raw data in this folder. We may occasionally audit the space to ensure this practise is being respected  
* Please consult our [best practices for data storage](https://github.com/neurobioinfo/Neuro_Bioinfo_Core.Nextcloud/wiki/Best-Practices-for-Data-Storage)

# How it Works
* On scheduled intervals, server admins will create a second copy of all data contained in each group's [PIname]/raw.data folder.
* This copy will reside in a separate s3 bucket owned by the Neuro_Bioinfo_Core storage project. It will be accessible only to Neuro Bioinfo Core staff.

# Restoring Accidentally Deleted Data
* First, always look in your nextcloud trash folder; smaller and/or just-deleted files will often be retained there and can be restored without administrator action
* If you cannot restore the data yourself from the trash, please send a message to neurobioinfo@mcgill.ca that includes the full directory path(s) of the data to be restored, whenever possible

# Disclaimer
This backup policy will be in place until we approach the ultimate limits of our storage capacity (350TB for 2023, 400TB for 2024, 500TB for 2025).  
Should we ever reach the point where ongoing backups will hamper our ability to host new data, this backup policy may be changed.