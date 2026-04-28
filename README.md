# cds-motif-extractor
Python tool to extract CDS sequences from GFF3 files based on DNA or protein motif matches.

## Requirements
- Python 3
- biopython
- gffutils

Install dependencies:
```bash
pip install -r requirements.txt

Example usage using query of DNA sequence:

python extract_cds_by_motif.py \
  --input-dir "Genome_KP" \
  --query "ATGCGT" \
  --output extracted_cds.fasta \
  --search-in dna \
  --padding 400

Example usage using query of protein sequence:

python extract_cds_by_motif.py \
  --input-dir "Genome_KP" \
  --query "MKTIIALSY" \
  --output extracted_protein_motif_hits.fasta \
  --search-in protein
