Jimmy Breen
Chief Data Scientist, Indigenous Genomics, TKI
(jimmymbreen@gmail.com)
#datamanagement #server #infrastructure

## Genomics data process
- Raw instrument data (image files and signal intensities, BCL files) 
- Sequencing-associated files (log files, quality metrics, setup information) 
- Sequence-calls ([FASTQ](https://en.wikipedia.org/wiki/FASTQ_format), [FASTA](https://en.wikipedia.org/wiki/FASTA), [SAM/BAM/CRAM format](https://samtools.github.io/hts-specs/SAMv1.pdf), etc.) 
- Reference genome alignments ([SAM/BAM/CRAM format](https://samtools.github.io/hts-specs/SAMv1.pdf)) 
- Coverage files ([bigWigs](https://genome.ucsc.edu/goldenpath/help/bigWig.html))
- Variant calls ([VCF](https://en.wikipedia.org/wiki/Variant_Call_Format)) & genome VCF files ([gVCF](https://support.illumina.com/help/BS_App_TSA_help/Content/Vault/Informatics/Sequencing_Analysis/BS/swSEQ_mBS_gVCF.htm#:~:text=gVCF%20is%20a%20text%20file,single%20'block'%20VCF%20records.))
- Quality control metrics
	- Alignment statistics
	- Coverage statistics
	- Pairing orientation
	- Fragment sizes
	- Sequence composition (GC%)
	- Over-represented sequences
	- Approach-specific statistics (Transcriptome representation, DNA methylation conversion efficiency)
- Customised report for distribution (TXT, DOC, PDF, etc.) 
- Data-specific Analytical pipeline record (details of analysis sufficient for an exact reanalysis, including software versions, database versions, etc.)

## Genomics storage
### Raw sequencing data types (i.e. Large data files)
1. Whole Genome Sequencing (WGS)
	- Sequencing (or resequencing) of a patient sample from blood
	- Large raw sequencing files in FASTQ or unmapped CRAM format
	- ~120GB (30X coverage) per sample (FASTQ) depending on exact coverage
	- Highly accessed initially for data processing then infrequently indefinitely
	- Can be transitioned to cold storage after 3 months
	- Reanalysis of these data files are rare but may occur 
	- Processing using the [bcbio-nextgen germline workflow](https://github.com/bcbio/bcbio-nextgen)

2. Transcriptome sequencing (RNA-seq)
	- Sequencing of the RNA fraction of a patient sample (blood in our case, but can be other tissues when required)
	- Small raw sequencing files in FASTQ
	- ~8GB/6M reads per sample (FASTQ)
	- Accessed initially for data processing then infrequently indefinitely
	- Can be transitioned to cold storage after 3 months
	- Reanalysis of these data files are rare but may occur
	- Processing using the SAGC RNA-seq analysis

3. DNA methylation (WGBS)
	- Sequencing of bisulfite-converted DNA from patient sample (blood in our case, but can be other tissues when required)
	- Large raw sequencing files in FASTQ
	- ~150GB (30X+ coverage) per sample (FASTQ) depending on exact coverage
	- Accessed initially for data processing then infrequently indefinitely
	- Can be transitioned to cold storage after 3 months
	- Reanalysis of these data files are rare but may occur
	- Processing using the SAGC DNA WGBS analysis

## Data Standards
1. Whole genome sequencing
2. DNA methylation
3. RNA sequencing
4. 

## User permission profiles
1. Category 1 (Highest): Lead PI (Alex Brown) and Chief Data Scientist (Jimmy Breen)
2. Category 2: Lead PI, Chief Data Scientist and Data Science team
3. Category 3: Lead PI, Chief Data Scientist, Data Science team and TKI IT Team
4. Category 4 (Lowest): Public
