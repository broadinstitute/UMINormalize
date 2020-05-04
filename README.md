## Description
UMINormalize contains code for normalization of read counts of AllSeq data (UMI stands for unique molecular identifier). This uses a specialized out of memory k-way merge sort of the data based on the UMI barcode, coordinates of the aligned reads (mainly bacterial reads), boundary of the features/genes (mainly for eukaryotic host reads) and strand specificity of the alignments. After sorting is done, the UMINormalize segments and collapses the reads based on a heuristic to obtain reads of mRNA transcripts without any PCR duplicates. Out of memory sort allows unlimited number of reads accompanied by fast C++ code.

## Running UMINormalize
After compiling the way to run UMINormalize is

umi_norm -i <infile> -o <outdir> -p <prefix> -c <collapse_type>

where, 

infile contains the input sam/bam file containing aligned reads.
outdir points to the path of the output directory.
prefix is a string used as a prefix of output files.
collapse_type is used to specify if the umi collapse is based on coordinates (for bacterial reads) or feature boundaries (used for eukaryotic host reads).


 
