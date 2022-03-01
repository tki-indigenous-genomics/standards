---
Title: Data Storage Standards
Authors: Sam Buckberry, Jimmy Breen
---


# Data storage standards
A collection of documents on data storage standards for the TKI Indigenous Genomics Group

**Authors:** Sam Buckberry, Jimmy Breen

## Definitions

**File type:** This is the file format to be typically denoted by the file extension.  
**Description:** A brief description of the file format.  
**Compression:** The algorithm and/or method used to compress the file.  
**Permissions:** What groups and users have access to the data   
**Access frequency:** How often this data type may require access. These descriptions are based on a subset of the [Google Cloud storage class descriptors](https://cloud.google.com/storage/docs/storage-classes#classes)

- **Standard:** Standard Storage is for data that is frequently accessed and/or stored for only brief periods of time. Standard data files should be able to be regenerated from Nearline or Archive data files without too much time or effort.
- **Nearline:** Nearline Storage is ideal for data you plan to read or modify on average once per month or less. Nearline Storage is appropriate for data backup and short-term archiving.
- **Archive:** highly durable storage for data archiving, backup, and disaster recovery. Only used for infrequently accessed data.

**Community access:** Are their community custodians for this data? If so, who are they?  
**Identifiable:** Could this data be used to identify an individual (YES/NO).  
**Location:** Location(s) where the data should be stored.  
**Notes:** Any additional information that would assist users of the data.

---
## Whole genome sequencing (WGS)

**File type:** CRAM  
**Description:**  
**Compression:**  
**Permissions:**  
**Community access:**  
**Location:**

**File type:** VCF  
**Description:**  
**Compression:**  
**Permissions:**  
**Access frequency:**
**Community access:**  
**Location:**


---
## DNA methylation

### Raw data

**File type:** FASTQ   
**Description:**  
**Compression:**  
**Permissions:**  
**Community access:**  
**Location:**

### Mapped data

**File type:** CRAM
**Description:**  
**Compression:**  
**Permissions:**  
**Community access:**  
**Location:**

### Processed data  

**File type:** CGmap   
**Description:**  
**Compression:**  
**Permissions:**  
**Community access:**  
**Location:**

**File type:** ATCGmap  
**Description:**  
**Compression:**  
**Permissions:**  
**Community access:**  
**Location:**

---
## Gene expression
