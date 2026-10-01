Reference genome:
GRCh38

Short-read aligner:
STAR v2.7.x

Input:
paired-end RNA-seq

Minimum sequencing depth:
70 million paired-end reads

Minimum mapping rate:
90%

Quantification:
exon-level and splice-junction quantification

PSI:
junction-based exon inclusion measurement

Filtering:
>=50 junction reads
>=80% sample support
PSI CI width <=0.25

Batch correction:
variance-preserving normalization

Exact STAR command:
NOT RECOVERED

Exact STAR parameters:
--twopassMode
--outFilterMismatchNoverLmax
--alignSJoverhangMin
--alignSJDBoverhangMin
--outFilterMultimapNmax
--quantMode

Exact preprocessing scripts:
NOT RECOVERED
