# geneyx.analysis.api
This repository holds the scripts and manuals for Geneyx Analysis API
You can review Geneyx products at https://geneyx.com

You can get access to geneyx analysis at https://analysis.geneyx.com

# Who needs geneyx anlysis API?
If you are Geneyx Analysis user that want to automate your data flow, for example:
- Integrate your sequencing machine and automatically send FASTQ to Geneyx Analysis
- Integrate with your LIMS and automatically create VCF samples or download reports
- Integrate with your EMR and uploading clinical data to the patient record

# Examples
## Uploading sample to Geneyx Analysis
For automating the process of uploading VCFs to Geneyx Analysis you can use the two files
scripts/ga.config.yml  			- request api key and user key from Geneyx Support edit the file and enter to the right places
scripts/ga_uploadSamples.py		- A python script that does the upload processing together with sample and patient data. please run it and check the command line arguments.
You can read more at docs/geneyx.analysis.api.pdf

## Unifying Dragen SV/CNV/Repeat files
Illumina' Dragen pipeline creates by default 4 types of VCF files
* SNVs
* SV/CNV/Repeat
for uploading those files to Geneyx Analysis it is required to merge the SV/CNV/Repeat files and upload the merged file as unified SV.
For doing so one can use scripts/UnifiedVcf.py
The script takes as parameters the three VCF files created by DRAGEN SV/CNV/Repeats and creates a unified SV file. 

Running prerequisites:
1.	Python 3.9.
2.	bgzip



