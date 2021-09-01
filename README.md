# filter-combine-reads
This script accepts two required input files.
1) a fasta file of an OTU from Pacbio post-ccs/demultiplexing,
2) a fasta file containing a genus of interest downloaded from NCBI database. 

Output is a combined file of the Pacbio and NCBI sequences filtered to only contain reads where more than one identical read was found (Pacbio only).
The Pacbio fasta file must contain this "size" information in the header. 
This threshold can be changed depending on your data. 
An identifier is also added, either "pacbio" or "ncbi" so read's origin can be easily known for subsequent analysis.

Lastly, a tsv file is created ("all_reads_info.tsv") which contains all of the reads information. This is formatted to be used with ggtree package in Rstudio.
