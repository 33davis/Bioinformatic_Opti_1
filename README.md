# Bioinformatic optimization for capture of rare sequences in marine metagenomic data #
 ## subgoals include : 
  ## (1) understanding how relative parameter important in post-processing ancient metgenomic analyses 
  ## (2) how to utilze post-processing tools for samples to see when more targeted deep sequencing is needed 
  ## (3) compare relative outputs of current tools for shotgun metagenomic data
  ## (4) increase the identification and validation of rare marine species in sediment records with sedaDNA
  
### Intial goals of project 
1. identify current bioninformatic standards and methods
2. create synthetic test data
   - created database of 20 COI partial sequenences for Nototheniideae and Sphenisciformes from NCBI
   - I chose COI sequenences based on availability, as well as hoping to utilize new MARES COI barcode database pipeline that was recently published.
    2a. MARES pipeline: for intial testing the precompiled database from [https://osf.io/8rdqk/] was used, which was downloaded 20.02.2024.
    2b. after proof of concept testing with Armbrecht pipeline, the MARES custom database pipeline will be used to construct a custom COI databse [33davis/MARES_database_pipeline]
    2c. create a combined MARES + PR2v5 database to simulate a complex eukaryotic database to map published data against
    2d. understand utility and proof of concept using this database
3. create "fishing" dataset combining empirical and synthetic data
   - utilizing gargammel to simulate sedaDNA fragments [add link to code]
   - for COI sequence "syntheic" sequences, utilize the bioconda::gargammel-slim package to create random fragemetns and simulate damage on partial gene sequences (no gaps)
   - create different "damage level" sequences by subsampling created files [add link to code]
   - run gargammel on targeted files (all deamination files, and subsampled files [add link to code]
   - merge fasta files + combined files back together prior to running through pipelein [add link to code]
   - these different datasets will then be run through target pipelines by themselves, and then also merged with published dataset to quantify and compare ability to be "fished" back out. This will help provide reference if simulated ancient Nototheniideae and Sphenisciformes sequences can be identified with current pipeline and settings, espeically in complex metagenomic samples
   - will also highlight the importance of database choice 
4. test data with Linda pipeline (Armbrecht et al., 2020) [https://onlinelibrary.wiley.com/doi/10.1111/1755-0998.13162]
   #### it is noted that MALT/ HOPS has not had an updated with NCBI since 2022. Most likely it will not be updated in the future. 
     - beginning with U1538 site data
     - will begin with U1538 sample data, that is already been collapsed + adapterremoval + intial FastQC/MultiQC qaulity control
       (6a) create conda environment for testing data [link to code] available here
       (6b) databases were merged with code [add link to code]
       (6c) malt-build with [add link to code] for MARES preload database, and merged MARES + PR2 v5 database
       (6d) run Komplexity - bbtools/dedupe - MALT - blast2RMA [add link to code] 
       (6e) Visualize and quanitify runs in MEGAN v. against built databases // previously published data.
       (6f) run for all datasets: IODP Exp. U1538, 
  5. 

### Chapter 1 Methodology ### 
#### Pre-procesing #### 
#### synthetic and IODP + synthetic dataset construction ####
#### dataset processing in bioinformatic pipeline ####
#### HOPS + percent damage ####
#### Basic identities + statistics #### 
#### synthetic extraction + visualization ####
#### Precision, Sensitivity, and F1 Scores ####
#### Shannon Diversity + visualization #### 
