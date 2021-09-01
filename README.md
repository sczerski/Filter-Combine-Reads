# filter-combine-reads
Required Input:
1) a fasta file of an OTU from Pacbio post-ccs/demultiplexing,
2) a fasta file containing a genus of interest downloaded from NCBI database. 

Output:
1) "all_filtered_seqs_w_id.fasta" = a combined file of the Pacbio and NCBI sequences filtered to only contain reads where more than one identical read was found (Pacbio only).
2) "all_reads_info.tsv = contains all of the reads information. This is formatted to be used as annotations for a tree build with the ggtree package in Rstudio.

Note:
1) The Pacbio fasta file must contain this "size" information in the header. 
2) This threshold can be changed depending on your data. 
3) An identifier is also added, either "pacbio" or "ncbi" so read's origin can be easily known for subsequent analysis.
4) Extra files are created during intermediate steps that are likely not of much use (will consolidate or remove later).
