##CAGPM Lab Reading List
-------------------------------------------

Collection of folders containing methods and papers related to CAGPM laboratory practices.  Links to source should be included where available.

###Background on qPCR

Authors worth reviewing: [Michael W. Pfaffl](http://www.researchgate.net/profile/Michael_Pfaffl "Pfaffl"), [Stephen A. Bustin](http://www.researchgate.net/profile/Stephen_Bustin2 "Bustin"), [Jo Vandesompele](http://www.researchgate.net/profile/Jo_Vandesompele "Vandesompele"), [Jan Hellemans](http://www.researchgate.net/profile/Jan_Hellemans "Hellemans")

* [How to do successful gene expression analysis using real-time PCR](http://www.sciencedirect.com/science/article/pii/S1046202309002461 "Vandesompele") - This is a great introduction and overview for qPCR method and Experimental Design.
* [MIQE Guidelines](http://www.clinchem.org/content/55/4/611.long "MIQE") -  Minimum Information for Publication of Quantitative Real-Time PCR Experiments.  In an effort to increase the reproducibility of Real-Time PCR, Bustin *et al* produced a comprehensive list of requirements (and recommendations) for the publication of qPCR data.  These include everything from Experimental Design considerations to Primer locations and sequences.
	* [MIQE Practical Implementation](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC2955025/ "MIQE Practical") - Recommendations around adoption of MIQE guidelines in a laboratory setting
* [qBase relative quantification framework](http://genomebiology.com/content/8/2/R19 "qBase+") - Too broad ranging to fit in anything but background; this summarizes the PCR experimentation process (GeNorm and Relative Expression Analysis included) used in qBase+ software.  The recommendations in this publication are extremely important to the implementation of PCR protocols whether using qBase+ or not.
* [BioRAD Real-Time PCR Reference](http://www.bio-rad.com/en-us/applications-technologies/qpcr-real-time-pcr "BioRAD") - Consider this and it's equivalent guides from [Life Technologies](http://www.lifetechnologies.com/us/en/home/global/forms/real-time-pcr-handbook-lt.html "LifeTech") & [QIAgen](http://www.qiagen.com/us/resources/molecular-biology-methods/pcr/ "QIAgen") the Encyclopedic references for qPCR work.  If you have a specific question about a particular process related to qPCR; the answer can most likely be found here with a little digging through website trees.  I prefer the BioRAD reference since it relies more heavily on the MIQE guidelines and RDML standards than the other sources; but for general information, all will be sufficient.

###qPCR Technical

* [Quantification of mRNA using real-time RT-PCR](http://www.nature.com/nprot/journal/v1/n3/full/nprot.2006.236.html "Nature Protocols") - Detailed experimental overview with optimization recommendations.  It's dense, but worth the read if there's a large amount of PCR in your future.
* [Amplification Efficiency of TaqMan Assays](http://www3.appliedbiosystems.com/cms/groups/mcb_marketing/documents/generaldocuments/cms_040377.pdf "TaqMan Amp Efficiency") - I see this as Life Technologies' counter argument to the Efficiency correction and Efficiency Publication requirements in MIQE.  It's important to know this information even if you don't completely agree with it.  My efficiencies with TaqMan assays are typically 80-95% regardless of tissue.  I prefer to correct for efficiency when possible.  This note is especially important for TLDA experiments where assay specific efficiency data is difficult to obtain.

###qPCR Math


* [Accurate Normalization of qPCR by geometric averaging of multiple internal controls](http://genomebiology.com/2002/3/7/research/0034/ "GeNorm") - Selection of and Normalization math around reference assay selection for qPCR.  This addresses why multiple stable internal controls are better than one, and provides all of the equations necessary to perform the calculations.
* [A new mathematical model for relative quantification in real-time RT–PCR](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC55695/ "Pfaffl Method") - Pfaffl's elaboration on PCR normalization math and efficiency correction.  This is a precursor to the qBase+ methods referenced above.  Pfaffl does a great job explaining the reasoning behind the math while qBase is a great consolidation of the equations required.
* [2^(-ddCt) Method](http://www.sciencedirect.com/science/article/pii/S1046202301912629 "ddCt") - It's not congruent with the most current methods, but it's always good to know what the newer methods were developed from.

####Links
* [Array Conversion to PCR](https://github.com/MNic/CAGPM_LabReadingList/blob/master/ArraytoPCR/ArraytoPCR.md "ArrayConvert")
* [Primer Design](https://github.com/MNic/CAGPM_LabReadingList/blob/master/PrimerDesign/PrimerDesign.md "Primer Design")