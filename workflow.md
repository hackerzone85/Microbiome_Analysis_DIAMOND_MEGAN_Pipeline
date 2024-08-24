1. Required Software
1. DIAMOND (http://www.diamondsearch.org)
2. MEGAN (http://megan.husonlab.org)
3. Unicycler (https://github.com/rrwick/Unicycler#installation)
4. Medaka (https://github.com/nanoporetech/medaka)

2. Download required files
aria2c -c -s 16 -x 16 https://ftp.ncbi.nlm.nih.gov/blast/db/FASTA/nr.gz
aria2c -c -x 16 -s 16 https://ftp.ncbi.nlm.nih.gov/pub/taxonomy/accession2taxid/prot.accession2taxid.gz
aria2c -c -s 16 -x 16 https://ftp.ncbi.nlm.nih.gov/pub/taxonomy/taxdump.tar.gz
tar -xvzf taxdump.tar.gz
