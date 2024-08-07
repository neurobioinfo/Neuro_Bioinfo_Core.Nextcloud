# Primary Data: Raw
These should be exclusively the primary "big data" generated by sequencers, genotypers, light-sheet, EM etc.  
In other words, this data cannot be regenerated without repeating the initial experiment.  
&nbsp;  
**This - and ONLY this data - will be backed up in duplicate copies following our [backup policy](https://github.com/neurobioinfo/Neuro_Bioinfo_Core.Nextcloud/wiki/Policy:-Redundant-Backups).**  
&nbsp;  
NOTE: this platform is not intended to support the very large amounts of fundamental imaging (human MRI/PET) that Neuro PIs currently store on the BIC server.  
&nbsp;  
If you wish this data to be backed up, its parent directory **must** be named "raw.data" (lowercase), found within your group's main data folder, i.e. the one named [PIname]Lab, with a folder-and-arrow icon 
(<img src="https://github.com/neurobioinfo/Neuro_Bioinfo_Core.Nextcloud/assets/35270039/6f51436c-75b1-49f0-9aae-25e02a51a69e" width=25>).  
&nbsp;  
Within this "raw.data" folder, your data may have any structure you like. However it is good practice to have directory structures that are as informative as possible. For example this might include:
* Having sub-folders by data type, e.g. genotyping, dnaseq, bulk Rnaseq, single-cell RNAseq, ATAC-seq, light-sheet, EM, microscopy etc.
* Having sub-folders by project name
&nbsp;  

Common raw data file types include: fastq/bam/cram (for sequence data), jpg/idat/txt (for genotyping data)

# Secondary and Tertiary Data: Analyzed
These are the data generated from computationally-intensive analyses of your primary data.  
Users should apply discretion when deciding whether or not to store non-primary data on the Neuro_Bioinfo_Core storage platform.  
&nbsp;  
Reasons to store non-primary data include:  
* It is the product of very large amounts of computation and would be very costly/time-consuming to replace. (e.g. joint-called vcf for a large cohort)  
* It is a valuable project deliverable in itself  
* It is a common input for many downstream analyses (e.g. RNAseq gene count matrices)  
* You are required to keep it by university policy/publication requirement/grant mandate etc.  

We strongly discourage users from simply stockpiling all the files generated by their analyses with no curation.  
Practices to avoid include:
* Preserving intermediary files, i.e. those used only to generate final outputs. e.g.:
    * Alignment bam files produced by post-processing steps in dnaseq/rnaseq analyses
    * Single-sample dnaseq variant vcf files
    * Genotype files in various stages of filtration
* Preserving files which are easy/quick/inexpensive to regenerate
* Preserving extremely verbose analysis logs, core dumps, or files of unknown use/provenance

# Personal or Non-Data files
* Should ideally be stored outside of your group's main data folder, i.e. not in the one named [PIname]Lab, with a folder-and-arrow icon 
(<img src="https://github.com/neurobioinfo/Neuro_Bioinfo_Core.Nextcloud/assets/35270039/6f51436c-75b1-49f0-9aae-25e02a51a69e" width=25>).  
* You can create any number of private folders in Nextcloud. You can name and organize them any way you like.  

# Common Considerations
* Data compression should be used whenever possible to save space. In particular, large plain-text formats such as fastq should be compressed with a utility like gzip.
* Large collections of small files should be packaged whenever possible into archive formats such as tar/dar or zip.  
* Data stored on this platform are not intended to be accessed frequently. Consider using a resource like the Digital Research Alliance of Canada (DRAC) server /project space for files that your group will re-use often.
* Sharing files with external users via this platform is possible, but not optimal for large datasets. If you wish to share large amounts of data to a user outside this platform, please contact neurobioinfo@mcgill.ca for assistance.

# Additional Resources
[Digital Research Alliance of Canada - Data Management Best Practices](https://alliancecan.ca/sites/default/files/2022-05/Portage_Webinar_2020Sept16_SomeRDMBestPractices.pdf)  
[Digital Research Alliance of Canada - Building Documentation and Metadata](https://alliancecan.ca/sites/default/files/2022-05/Portage_Webinar_2020Sept29_BeginningWithTheEndInMind.pdf)