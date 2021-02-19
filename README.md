##Predominant Sites and Signals
Predominant polyA sites and signals were derived from the polyA site 2.0 database. PolyA sites were filtered for protein coding genes.  The predominant polyA site was defined as the polyA site that is used in more than 50% of a gene’s transcripts. For each site, predominant polyA signals were selected depending on the strength of the candidate hexamer as well as the distance of the candidate hexamer to the -21 position from representative polyA site. Both files are available in hg38 and hg19. For additional details on how polyA sites and signals were selected, check <Paper>.

###Predominant PolyA Site Bed file columns
    1)  Chromosome 
    2)  polyA site start
    3)  polyA site stop
    4)  Representative site 
    5)  Gene symbol
    6)  Strand
    7)  Representative site position
    8)  Percent of Samples supporting polyA site
    9)  Number of Protocols supporting polyA site
    10) Annotated location
    11) Candidate Hexamers
    12) Average TPM of PolyA Site
    13) Total average TPM of sites found in Gene
    14) polyA site Usage


###PolyA Signal Bed file columns
    1)  Chromosome 
    2)  polyA signal start
    3)  polyA signal stop
    4)  Representative site
    5)  Gene name
    6)  Strand
    7)  Hexamer

##Constraint Analysis Bed files
In order to assess the tolerance for variation in our predominant polyA signals compared to similar regions in the gene, we compared gnomAD allele frequencies between predominant polyA signals and control regions. Predominant polyA signals were limited to AATAAA and ATTAAA hexamers. Upstream control regions consist of 6 A and T bases found in the 3’ UTR, upstream of the predominant polyA signal. The makeup of the A and T bases depend on the downstream polyA signal. For example, if the predominant signal of the gene was AATAAA, we captured 5 A’s and 1 T in any order, upstream of the predominant polyA signal. PolyA signal and control intervals have been filtered out if they overlapped known repetitive regions or regions of low complexity. See <paper> for details.

###Control bed file columns
    1)  Chromosome 
    2)  Control base start
    3)  Control base stop
    4)  Gene Symbol
    5)  Base
    6)  Strand


##Clinical Genes
In order to better understand which polyA signal variants are in genes with known clinical significance, we first produced a union of known clinically significant genes found in OMIM, CGD (Clinical Genomics Database), and HGMD. For HGMD, only genes with DM assertion were included. To prevent ambiguity of gene symbols across databases, all gene names were first converted to HGNC IDs before being intersected. 

###Clinical Genes table columns
    1)  HGNC ID
    2)  Found in OMIM?
    3)  Found in HGMD?
    4)  Found in CGD?
    5)  Has predominant polyA signal?

