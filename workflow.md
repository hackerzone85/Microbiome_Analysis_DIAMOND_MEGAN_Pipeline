# Required Software
1. DIAMOND (http://www.diamondsearch.org)
2. MEGAN (http://megan.husonlab.org)
3. Unicycler (https://github.com/rrwick/Unicycler)
4. metaSPAdes (https://github.com/ablab/spades)
5. Medaka (https://github.com/nanoporetech/medaka)
6. ea-utils (https://github.com/ExpressionAnalysis/ea-utils)
7. SRA Tools

# Download required files
```
aria2c -c -s 16 -x 16 https://ftp.ncbi.nlm.nih.gov/blast/db/FASTA/nr.gz
aria2c -c -x 16 -s 16 https://ftp.ncbi.nlm.nih.gov/pub/taxonomy/accession2taxid/prot.accession2taxid.gz
aria2c -c -s 16 -x 16 https://ftp.ncbi.nlm.nih.gov/pub/taxonomy/taxdump.tar.gz
tar -xvzf taxdump.tar.gz
aria2c -c -s 16 -x 16 https://software-ab.cs.uni-tuebingen.de/download/megan6/megan-map-Feb2022.db.zip #The current version is megan-map-Feb2022.db
unzip megan-map-Feb2022.db.zip -d destination_folder
```
# Download and install all the required software
1. DIAMOND
```
mamba create -n diamond diamond
```
2. MEGAN
To download MEGAN Linux binaries and extract them, go to the directory in which you wish SPAdes to be installed and run:
```
aria2c -c -s 16 -x 16 https://software-ab.cs.uni-tuebingen.de/download/megan6/MEGAN_Community_unix_6_25_10.sh
sh MEGAN_Community_unix_6_25_10.sh
```
4. SPAdes (Includes metaSPAdes)
To download SPAdes Linux binaries and extract them, go to the directory in which you wish SPAdes to be installed and run:
```
wget http://cab.spbu.ru/files/release3.15.3/SPAdes-3.15.3-Linux.tar.gz
tar -xzf SPAdes-3.15.3-Linux.tar.gz
cd SPAdes-3.15.3-Linux/bin/
```
In this case, you do not need to run any installation scripts – SPAdes is ready to use. We also suggest adding the SPAdes installation directory to the PATH variable. 
Note that pre-build binaries do not work on new Linux kernels. 
5. Unicycler
```
git clone https://github.com/rrwick/Unicycler.git
cd Unicycler
pip install -t /home/<usr_name>/Unicycler .
```



