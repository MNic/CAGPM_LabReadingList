##Primer Design


###Useful Resources:
* [UCSC Genome Browser - In Silico PCR](http://genome.ucsc.edu/cgi-bin/hgPcr?command=start "InSilicoPCR")
* [UCSC Genome Browser - Genome Browser Gateway](http://genome.ucsc.edu/cgi-bin/hgGateway?hgsid=400136405_nE61bEUVeZ7ZJkeTyG8GUBj5aUeZ "Genome Browser")
* [NCBI GenBank](http://www.ncbi.nlm.nih.gov/genbank/ "GenBank")
* [Ensembl.org](http://useast.ensembl.org/index.html "Ensembl")
* [Primer3](http://bioinfo.ut.ee/primer3/ "Primer3Web") or [Primer3Plus](http://www.bioinformatics.nl/cgi-bin/primer3plus/primer3plus.cgi/ "P3Plus")
* [Blastn](http://blast.ncbi.nlm.nih.gov/blast/Blast.cgi?PROGRAM=blastn&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome "Blast")
* [mFold - DNAFold](http://mfold.rna.albany.edu/?q=mfold/dna-folding-form "DNA Fold")

###General Design Overview

Selection:

1. Select Targets of Interest
2. Explore the Gene/Transcript of interest
3. Choose region(s) on targets of interest to amplify
4. Find best Forward Primer, Reverse Primer, and (if needed) Probe locations
5. Order Oligos

Receiving Oligos

1. LabReady vs Lyophillized 
2. Dilution from Stock
3. Primer Balance
4. Standard Curve Efficiency Testing 
5. Assay creation

* Note: We'll be using [Human RUNX1](http://www.ncbi.nlm.nih.gov/gene/861 "RUNX1") in any examples below.

###Selection

1. Select Targets of Interest:
	* Targets are typically provided from other experiments (downsizing from Microarray or mRNASeq), other investigators, or area-of-interest specific literature.  When introduced to a new target of interest be sure to take note of the Gene name (Runt-related transcription factor 1), Gene ID (861), Official Symbol (RUNX1), Oraganism and 'Also Known As' from NCBI's GenBank.  Other names for a transcript can help in literature searches for previously successful experiments.
	
2. Explore the Gene/Transcript:  
	* UCSC and Ensembl are great for this.  Take note of the structure of the gene, how many exons, how many isoforms.  
		* Are any exons skipped in alternate isoforms?  
		* Are there exon junctions unique to each isoform?
	
	

