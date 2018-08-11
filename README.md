# Antibody NGS Pipeline

Bulk antibody sequence preprocessing, annotation with abstar, upload to MongoDB and S3.  
This is based on the AbStar analysis pipeline: (www.github.com/briney/abstar)

### install  
`pip install antibody-ngs-pipeline`


### use  

To run antibody_ngs_pipeline:  
`antibody_ngs_pipeline`

To run antibody_ngs_pipeline with FASTQC report on raw data:  
`antibody_ngs_pipeline -f`
  
To run antibody_ngs_pipeline with adapter trimming by CutAdapt:  
`antibody_ngs_pipeline -t <path-to-adapters.fasta>`

To run antibody_ngs_pipeline with adapter trimming by CutAdapt, quality trimming 
with sickle and get a FASTQC report on both raw data and processed data:  
`antibody_ngs_pipeline -f -t <path-to-adapters.fasta>`




### requirements  
Python 3.5+  
abstar  
abutils  
cutadapt  
pymongo  
  

Merging paired sequences requires PANDAseq: https://github.com/neufeld/pandaseq  
batch_mongoimport (from Abstar) requires MongoDB: http://www.mongodb.org/  
Downloading from BaseSpace requires Basemount: https://basemount.basespace.illumina.com/  
