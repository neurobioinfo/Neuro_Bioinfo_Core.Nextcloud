# Welcome to the Neuro_Bioinfo_Core Nextcloud Server Wiki!


## Neuro_Bioinfo_Core data storage platform
As part of the NeuroVIP project, the Neuro Bioinfo Core group is offering a platform for all Neuro PIs who wish to store their data.  
&nbsp;  
This storage platform is intended for:
* Long-term storage of large amounts of data, especially raw data
* Files which are accessed only infrequently
* MNI groups with storage needs greater than the default offered by the DRAC, but who do not wish to write yearly computing grants to secure it.
* MNI groups who would prefer a more intuitive graphical way to manage their raw data, backed by experienced in-house informatics support.
* All types of data, **excluding the fundamental MRI/PET imaging that is routinely stored on the Neuro BIC server**

## Front end: Nextcloud server
We have mounted a Nextcloud server as the portal for Neuro PIs to manage their data. Nextcloud is an open-source data sharing platform similar to Dropbox.

Click here to access the [Neuro_Bioinfo_Core Nextcloud server](https://neurobioinfo.github.io/Neuro_Bioinfo_Core.Nextcloud)

See the [official Nextcloud documentation](https://docs.nextcloud.com/server/latest/user_manual/en/webinterface.html) for general instructions on how to use the Nextcloud web interface.  

**Note: we have not implemented all features from the above link. For example, we do not support using Nextcloud as an email client, nor do we support multi-factor authentication at this time.**

## Back end: DRAC cloud infrastructure
Behind the scenes, the Nextcloud server provides a bridge to a large cloud storage resource allocated to the Neuro Bioinfo Core by the Digital Research Alliance of Canada (DRAC). This cloud storage, very similar in structure to Amazon's Simple Storage Service (AWS S3), is managed and operated entirely by the Neuro Bioinfo Core. 

The Nextcloud front-end server provides the access control necessary for multiple groups to manage their data in this common space, without risking unwanted access between groups.

## Questions or comments
Please direct any questions, comments or general support requests to neurobioinfo@mcgill.ca

 - - - -

## Contents
- [Getting Started](getting_started.md)
- [Upload data](upload_data.md)
- [Redundant Backups](redundant_backups.md)
- [Best Practices for Data Storage](bpds.md)
- [Download data](download_data.md)
