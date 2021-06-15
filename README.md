16S-arc_vertebrate_paper
========================

Code associated with the manuscript:

Youngblut et al. Strong influence of vertebrate host phylogeny on gut archaeal diversity.

# Citation

> Youngblut, Nicholas D., Georg H. Reischer, Silke Dauser, Chris Walzer, Gabrielle Stalder, Andreas H. Farnleitner, and Ruth E. Ley. 2020. "Strong Influence of Vertebrate Host Phylogeny on Gut Archaeal Diversity." bioRxiv. https://doi.org/10.1101/2020.11.10.376293.

# Notebooks

* 00_misc
  * Initial, miscellaneous assessments of the data
    * eg., PCR & sequencing pass/fail
    * eg., Sequence dataset submission
* 01_LLA
  * Ley Lab Amplicon (LLA) pipeline run on all 16S-arc MiSeq sequencing data
  * The pipeline consists of:
    * Read filtering via trimmomatic
    * ASV generation via DADA2   
    * Phylogeny inference via fasttree on an MSA generated via MAFFT
    * Taxonomic classification via the Qiime2 q2-feature-classifier
      * SILVA v119 used for classification
  * The ASV count table and associated data (metadata, taxonomy, & phylogeny)
    were combined into a phyloseq object
    * The phyloseq object was split into one with all samples ('IndD', 1 sample per individual)
      and just one randomly selected sample per species ('SpecD')
    * Compositional data (CoDa) transformations were assessed
    * Rarefaction analysis via phyloseq & iNEXT
    * Closest type strain via BLASTn against the All Species Living Tree database
* 02_dataset_explore
  * Initial dataset exploration
* 03_modulating_factors
  * Which factors explain archaeal diversity?
  * Analyses performed on total archaeal diversity (eg., MRM) and individual archaeal taxa
    (eg., RRPP on ASVs)
* 04_cophylo
  * Host-Archaea co-phylogeny analyses
* 05_cooccur
  * Archaea-Archaea taxon co-occurrence analyses
* 06_ancestral_state
  * Ancestral state reconstruction of archaeal taxa
* 07_arc-bac
  * Archaea-Bacteria community diversity correlation
  * Archaea-Bacteria co-occurence analyses
  * Bacteria obtained from [Youngblut et al., 2019](https://doi.org/10.1038/s41467-019-10191-3)
* 08_metagenomes
  * metagenome data from [Youngblut et al., 2020](https://pubmed.ncbi.nlm.nih.gov/33144315/)
  * Methanothermobacter contigs can be found at [FigShare](https://figshare.com/s/4c6ceb4ba8be4bab659f)

# Raw data

* Sample metadata
  * Available as Table S1 in the manuscript
* MiSeq sequence data
  * Available from the European Nucleotide Archive under the study accession number PRJEB40672
* Shotgun metagenome data
  * Available from the European Nucleotide Archive under the study accession number PRJEB38078

# Contact

Nick Youngblut (`nyoungblut@tuebingen.mpg.de`) 