# Bactopia uptade to Nextflow DSL2

## 1 Step: Learning how Bactopia uses channels and process
### Channels emitted by bactopia:
 FASTQ_PE_STATUS , ESTIMATE_GENOME_SIZE , QC_READS, QC_ORIGINAL_SUMMARY, COUNT_31MERS, ARIBA_DATABASES, ARIBA_ANALYSIS, MINMER_SKETCH, CALL_VARIANTS, MAPPING_QUERY, ASSEMBLY, QC_FINAL_SUMMARY, MAKE_BLASTDB, ANNOTATION, ASSEMBLY_QC, BLAST_GENES, BLAST_PRIMERS, BLAST_PROTEINS, ANTIMICROBIAL_RESISTANCE, PLASMID_BLAST, PRODIGAL_TF, PROKKA_PROTEINS, SEQUENCE_TYPE, MLST_DATABASES, MINMER_SKETCH, MINMER_QUERY, MINMER_DATABASES, REFERENCES, DOWNLOAD_REFERENCES, REFSEQ_SKETCH, CALL_VARIANTS_AUTO, AMR_DATABASES, PLASMID_BLASTDB, BLAST_GENES, BLAST_GENES_FASTAS, BLAST_PRIMERS, BLAST_PRIMERS_FASTAS, BLAST_PROTEINS, BLAST_PROTEINS_FASTAS, MAPPING_QUERY, MAPPING_QUERY_FASTAS.

 OBS: Channels can be used twice on DSL2, and are automatically forked, so all channels need to be revised and explicit forks need to be removed.

 Executing process:






## 2 Step: Update all modules inclusion
## 3 Step: Update all process
There are 24 process on the pipeline.\
Current Status = (0/24) processes updated

## 4 Step: Modifying Workflow scope to ensure process usage
