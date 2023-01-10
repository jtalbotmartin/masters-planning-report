### project overview

- BRCA1 and BRCA2 are tumour suppressor genes. The proteins encoded by BRCA1 and BRCA2 are fundamental to a biological pathway for the high-fidelity repair of DNA double strand breaks - a particularly harmful type of genetic mutation.
- When BRCA proteins become dysfunctional {?} due to the inactivation of BRCA genes, this pathway of double-strand break repair - Homologous-Recombination HR-DSB - ceases to function correctly. This leads to genomic instability {...e} caused by reliance on an unsuitable mechanism of DNA double-strand break repair in the place of HR.
- Downstream, the consequences for the breakdown of this pathway are the development of cancer.
- {tumorigenesis}
- Inheriting a pathogenic germline BRCA mutation confers a significant increase in the lifetime risk of breast cancer.


- In cancer development, uncontrolled growth caused by {} leads to tumour development.
- As a cancer develops, it accumulates {} mutations that confer {drivers and non drivers, hallmarks etc..}. 
- When cancers are caused by mutagenic processes such as the breakdown of HR, patterns emerge across the collection of somatic mutations contained within the genome of the tumour - termed mutational signatures. By analysing a cancer's whole genome sequence, these patterns can be analysed, and signatures extracted, giving insights about the underlying mutagenic process that gave rise to the cancer regardless of whether a causal mutation has been discovered.
- Understanding the underlying mutagenic process driving the development of a cancer can have powerful implications for optimal treatment of a patient. Thus, gleaning these insights of underlying processes driving cancer development from mutational signature analysis is able to guide clinical decisions, and improve patient outcomes.

- However, although mutational signatures can empower clinical decisions regardless of whether a causal mutation has been found, genetic diagnoses are still of vast significance. These diagnoses enable screening in a patient's family members, making it possible for them to understand their own risk of disease, and facilitating the implementation of preventative clinical interventions. In addition, genetic diagnoses can contain novel insights into disease biology, with downstream implications for future interpretation and treatment of a disease.


### research question
- in {}, HRDetect was developed. HRDetect is a mutational signature analysis algorithm, designed to classify tumours as being caused by BRCA-deficiency - or, a breakdown in HR-DSB caused by BRCA-deficiency - on the basis of the whole genome sequence of the cancer. The results of a study applying this algorithm to a cohort of cancer patients yielded surprising results: 
- previous to this study, BRCA-deficiency was thought to account for {}% of cases, based on rates of genetic diagnosis. However, HRDetect found this value to be in the range of {}%, based on the proportions of patients displaying an algorithmic score suggesting BRCA-deficiency as a causal cancer development mechanism.

- Furthermore, a particularly interesting finding is that in a high number of these cases, a mutation in BRCA1 or BRCA2 was not observed. {}

- This key finding is the starting point for this research, the aims and objectives of which are the following:
- 

### aims and objectives

- This project seeks in the first instance to investigate whether a proportion of the aforementioned undiagnosed BRCA-deficient cancer cases can be explained by pathogenic genetic variants in the near-coding regions of the BRCA1 and BRCA2 genes. - I have defined these as Promoter, 5'UTR (untranslated regions), Intronic and 3'UTR regions of these genes, and am using the Genomics England 100,000 Genomes Project (GEL) dataset.
- In order to achieve this central aim, my objectives are:
	- To curate an unbiased set of high-confidence likely pathogenic variants in near-coding regions of BRCA genes in all consenting GEL participants. This requires variant extraction in near-coding BRCA1 and BRCA2 regions, with subsequent filtering on the basis of allele frequencies and a combination of applied variant annotations - using SpliceAI, CADD, PhyloP, RNA Binding Protein Data, UTRannotator and PolyA signals. 
	- To conduct burden testing of curated variants. Using data from {} provided by Nik-Zainal group (responsible for HRDetect), I will compare variant incidence with control cohorts to understand whether curated variants are enriched in individuals with an HRDetect score sufficient to enable a BRCA-deficient classification.
	- To conduct variant interpretation where variants of interest have been uncovered.
- Further aims in subsequent work (if time allows), will be guided by initial findings - using results to formulate and select the most interesting questions to explore. However, some possible directions for the work are:
	- investigating specific mechanisms of near-coding gene activation if interesting variants, or seemingly important mechanisms are discovered
	- using analogous methodology to identify near-coding mechanisms of other undiagnosed cancer participants - for example, searching for variants causing DNA mismatch repair deficiency in Lynch Syndrome patients. 

### hypotheses

### BRCA, DSB Repair and Cancer Development

- DSBs impact
- Repair Pathways
- BRCA and HR
	-  figure
- Tumorigenesis

- potentially unclear
	- biallelic inactivation
	- but inherited makes this likely
	- so non-coding could cause biallelic
	- but this isn't proven
	- may need to check for promoter hypermethylation . LoF assay
- 
- , in which I will apply analytical methods utilised in recent rare disease studies 
- 
- of BRCA1 and BRCA2, representating a novel way
- Use results from this mutational signature analysis to identify a point in which to deploy a rare disease genomics toolkit
-  results from mutational signature analysis with novel the aims and objectives of which are the following:
- 