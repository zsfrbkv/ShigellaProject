# Data
This directory contains all data used in **1. Structure of the phylogenetic tree of _E. coli_ and _Shigella_ spp.**

### Genomes_faa/
Protein data of the 414 strains. These files include full genomes and were used for the construction of orthologous groups. 
The amino acid sequences of all protein-coding genes were aligned using **ProteinOrtho V5.13** with parameters `cov=67` (min. 
coverage of best blast alignments in per cent) and `identity=50` (min. per cent identity of best blast alignments).

### universal_singlecopy_orthologs.csv
This table is the output of **ProteinOrtho**. Rows represent a genome and columns represent 238 universal single-copy 
orthologous groups.

### Genomes_fna/
Nucleotide sequences of all protein-coding genes of the 414 strains. This data and `universal_singlecopy_orthologs.csv` 
were used to make files with nucleotide sequences of orthologs from each orthologous group. 

### Orthologs/
Each `.fa` file represents an orthologous group and includes nucleotide sequences of orthologs from 
the 414 strains. The names of the files correspond to columns in `universal_singlecopy_orthologs.csv`. These files were 
then aligned using **Mafft** in the linsi mode. After that we concatenated the obtained alignments and constructed a 
phylogenetic using **RAxML** with the GTR+Gamma model and 100 bootstrap replicates.

### Alignments_nt/
Each `.fa.o` file represents a nucleotide alignment of the corresponding orthologous group obtained by using 
**Mafft** in the linsi mode. The dir also includes the cancatenated alignment.

### Alignments_codons/
Each `.fa` file represents a codon (nucleotide) alignment of the corresponding orthologous group obtained by using 
**MACSE**. All frameshifts were treated as recommended by the tool tutorial. The dir also includes the cancatenated alignment.

### total_stats.csv
In this project we analysed 414 complete genomes including 35 _Shigella_ spp. genomes, 41 STEC genomes, 31 ExPEC genomes, 
8 APEC genomes, 7 ETEC genomes, 3 EPEC and AIEC genomes each, 2 EAEC genomes, and 1 EIEC genome. This table gives more detail.

### excluded_strains.csv
We excluded clones and closely related _E. coli_ strains that formed plateaus in the phylognetic tree from further analysis.
This table gives more detail on the excluded strains.

