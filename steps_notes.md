# Bactopia uptade to Nextflow DSL2

## 1 Step: Learning how Bactopia uses channels and process
### Channels emitted by bactopia:
 FASTQ_PE_STATUS , ESTIMATE_GENOME_SIZE , QC_READS, QC_ORIGINAL_SUMMARY, COUNT_31MERS, ARIBA_DATABASES, ARIBA_ANALYSIS, MINMER_SKETCH, CALL_VARIANTS, MAPPING_QUERY, ASSEMBLY, QC_FINAL_SUMMARY, MAKE_BLASTDB, ANNOTATION, ASSEMBLY_QC, BLAST_GENES, BLAST_PRIMERS, BLAST_PROTEINS, ANTIMICROBIAL_RESISTANCE, PLASMID_BLAST, PRODIGAL_TF, PROKKA_PROTEINS, SEQUENCE_TYPE, MLST_DATABASES, MINMER_SKETCH, MINMER_QUERY, MINMER_DATABASES, REFERENCES, DOWNLOAD_REFERENCES, REFSEQ_SKETCH, CALL_VARIANTS_AUTO, AMR_DATABASES, PLASMID_BLASTDB, BLAST_GENES, BLAST_GENES_FASTAS, BLAST_PRIMERS, BLAST_PRIMERS_FASTAS, BLAST_PROTEINS, BLAST_PROTEINS_FASTAS, MAPPING_QUERY, MAPPING_QUERY_FASTAS.

 OBS: Channels can be used twice on DSL2, and are automatically forked, so all channels need to be revised and explicit forks need to be removed.

 I'm using sample fastq from NCBI SRA of[Escherichia coli](https://www.ncbi.nlm.nih.gov/sra/SRX10122872[accn]) to test the Bactopia pipeline, i'll run with the -with-dag to generate dag files and analyse the whole data process inside bactopia workflow.

 I've created dag.dot files to understand better how Bactopia works. The flowchart contains a lot of useful information.

## 2 step: Adding Stubs to process
Adding stubs is an important step on pipeline engineering process, because you can separate nextflow process to other tools process(scripts, shell commands or tools like fastqc).

Current Status = (24/24) stubs added to process

I've runned the main.nf using -stub-run parameter and had a complete run, with no error messages (all the processes were called on this run) and the pull request for adding stubs were finished

## 3 Step: Update modules

I'll start to turn processes into modules to make the main.nf more redable and the process will be called as modules.

Current Status = (1/24) process modules added


## 4 Step: Update all process
There are 24 process on the pipeline.\
Current Status = (0/24) processes updated

## 5 Step: Modifying Workflow scope to ensure process usage
