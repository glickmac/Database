# Database

![Python](https://img.shields.io/badge/python-v2.7%20%2F%20v3.6-blue.svg)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)


## Table of Contents
[Database Information](#intro)     
[Database Creation](#workflow)   
   

## <a name="intro"></a>Database Information

The following repository contains three gene nucleotide databases that contain mycobacterial species level information. The procedure to generate the databases is explained in greater detailed below. The BLAST Databases are found under the Databases folder.


## <a name="workflow"></a>Database Creation

### rpoB and HSP65

The rpoB and HSP65 databases are taken from sequences from the [NCBI](https://www.ncbi.nlm.nih.gov/nuccore). The size of the gene and the genus name were used to filter the query results. The data was download on May 1st, 2018. Additional filtering steps were performed using jupyter notebook scripts under the scripts directory. 

#### Overview of Filtering Steps

- Removed sequences that did not align using [Seaview](http://doua.prabi.fr/software/seaview)

- Subsampled 2 sequences by species (if available) with an emphasis on selecting sequences from established cultures. 

- Selected conserved region of gene amongst all subsampled sequences

- Created nucleotide BLAST database

#### Species Information

A phylogenetic tree was created using [PhyML](http://www.atgc-montpellier.fr/phyml/) in the SeaView program with default settings. The resulting trees are located under data/Tree_of_Database_Sequences. The subsampled sequences had to be further refined to only one sample per species to create the tree.

A complete list of the species included in the databases are listed in the Count_of_Species.xlsx excel file. 

### 16S RNA

The small subunit rna 16S gene data for all Mycobacterium was downloaded from [Silva](https://www.arb-silva.de/) on July 18th, 2018. The data was filtered by the species present in the HSP65 and rpoB database. The data was also length filtered to allow for proper alignment. The data was subsampled by species to include one record per species. 

- [NCBI](https://www.ncbi.nlm.nih.gov/nuccore)

- [Silva](https://www.arb-silva.de/)





