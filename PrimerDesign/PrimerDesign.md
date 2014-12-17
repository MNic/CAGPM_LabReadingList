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
	* UCSC and Ensembl are great for this.  Take note of the structure of the gene, 
		* How many exons?
			- For [RUNX1](http://genome.ucsc.edu/cgi-bin/hgTracks?db=hg19&position=chr21%3A36054043-36508047&hgsid=400289563_IQQWwCeeSlqllGDWh7dsybaGOKZm "RUNX1"): Up to 8 Exons
		* How many isoforms?  
			- RefSeq isoforms = 3
		* Are any exons skipped in alternate isoforms?  
			- One transcript has 2 exons the other two don't have.  One isoform is truncated early
		* Are there exon junctions unique to each isoform?
			- Ex1-2 & Ex2-3 junctions are unique to the long isoform
			- Ex4-5 is unique to the truncated isoform
			- At this level the 3rd transcript appears to have no unique properties differentiating it from the other two transcripts.
			- Also worth noting, exons 3-6 are shared by all isoforms.  Amplifying any of these should yield combined results for all isoforms.
		* Are there any unique, potentially complicating properties of the transcript (see [MYL9](http://genome.ucsc.edu/cgi-bin/hgTracks?db=hg19&position=chr20%3A35161547-35186566&hgsid=400289563_IQQWwCeeSlqllGDWh7dsybaGOKZm "MYL9")

3. Choose region(s) on target to amplify:
	* Identifying regions of interest is a fairly simple decision tree.  An assay developed where one primer spans the junction between two exons is prefered above all other arrangements.  This is followed closely by any assay having each primer in adjacent exons spanning the junction.  Finally having both primers within the same exon is used as a last resort.
		- Primer Spanning Exon Junction > Amplicon Spanning exon junction >>> Amplicon in a single exon.
		- The reason for this priority list is primarily the default exclusion of genomic DNA by the first two assays.  Assays spanning an exon juction have sequences unique to RNA since intron between the exons (present in the DNA) has been removed.  The amplicon in a single exon has the same sequence in both gDNA and RNA.
		
	* In a scenario in which we'd like to assess the expression of RUNX1 and its isoforms we would need to:
		- Identify differentiating exon junctions:
			* [RUNX1 transcript variant 1](http://genome.ucsc.edu/cgi-bin/hgc?hgsid=400289563_IQQWwCeeSlqllGDWh7dsybaGOKZm&c=chr21&o=36160097&t=36421595&g=refGene&i=NM_001754) has 2 unique exons
			* [RUNX1 transcript variant 2](http://genome.ucsc.edu/cgi-bin/hgc?hgsid=400289563_IQQWwCeeSlqllGDWh7dsybaGOKZm&c=chr21&o=36160097&t=36260987&g=refGene&i=NM_001001890) appears to have no distinguishing junctions
			* [RUNX1 transcript variant 3](http://genome.ucsc.edu/cgi-bin/hgc?hgsid=400289563_IQQWwCeeSlqllGDWh7dsybaGOKZm&c=chr21&o=36193573&t=36260987&g=refGene&i=NM_001122607) has a unique final exon.
		- Select regions around the differentiating junctions and pull their cDNA sequence from [Ensembl](http://useast.ensembl.org/index.html "Ensembl"):
			* [RUNX1 transcript variant 1 - Exons](http://useast.ensembl.org/Homo_sapiens/Transcript/Exons?db=core;g=ENSG00000159216;r=21:34787801-36004667;t=ENST00000437180) Note the nomenclature difference between UCSC Genome Browser and Ensembl.  There will be ambiguities like these that will require more investigation to get correct.  Ensembl has provided a link to the RefSeq NM_001754 for the long transcript.  So we'll choose to use RUNX1-201 over RUNX1-002 in this scenario.
			* The linked Exon page provides the sequences of each exon (Capital letters) with the beginning and end of each intron (lowercase letters).  Untranslated regions are indicated in Blue while translated are black.  RNA should contain both blue and black capital letters; but selection of translated regions is generally preferred unless there's an experimental or technical reason to favor untranslated.


	
	

