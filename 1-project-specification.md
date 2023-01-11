**The central hypothesis of this project is that pathogenic genetic variants in the near-coding regions of the BRCA1 and BRCA2 genes may be responsible for a proportion of unexplained breast cancer cases, in which BRCA-deficiency has been identified through mutational signature analysis as the causal mechanism of disease progression. Uncovering and interpreting these variants would enable familial screening to identify variant carriers and implement downstream clinical interventions, and could provide novel mechanistic insights into relevant disease biology.

The following sections will articulate the biological background of this project, and clarify the aims and objectives of the work.

### project overview
- BRCA1 and BRCA2 are tumour suppressor genes.[10,11] The proteins encoded by BRCA1 and BRCA2 have numerous roles in the maintenance of genomic integrity[8]. Of particular relevance, are the roles of these proteins in a biological pathway for the high-fidelity repair of DNA double strand breaks (DSBs) - a particularly cytotoxic class of genetic mutation, owing to it's propensity to modify genomic architecture via chromosomal rearrangements. [5,6,7, 9]
- In the loss of functional BRCA proteins due to the biallelic inactivation of BRCA genes, this pathway of double-strand break repair - homologous recombination (HR, or HR-DSB) - ceases to function correctly.
	- In healthy cells, this mechanism of HR-DSB - in which a homologous DNA molecule template is used for repair - exists in a complementary partnership with a distinct DSB pathway named non-homologous end joining (NHEJ) to maintain genomic integrity in the face of exogenous threats, and genomic stability during the DNA replication process. [37]
	- Although used preferentially by cells when HR is not required, NHEJ has disruptive or toxic effects when utilised in scenarios for which it cannot correctly repair DNA lesions - leading to destabilising genomic alterations. The abrogation of BRCA1 or BRCA2 leads to the breakdown of HR, disrupting the complementary HR-NHEJ partnership needed to safely repair DSBs. This leads to the loss of genomic integrity due to the accumulation of lesions introduced by NHEJ, or other mutagenic DBS pathways. [38]
	- For this reason, heterozygous germline BRCA variants are associated with significantly higher risk of cancer development - particularly breast and ovarian cancers. [{HRDetect 4 and 5}], in which tumorigenesis is initiated when the wild-type allele is lost [8].
	- ...incidence in population
	- ...incidence in BRCA carriers


- Cancer development is driven by clonal proliferation, fuelled by 'driver' mutations. These mutations undergo positive selection to confer growth advantage, and thus are causally implicated in tumorigenesis [39,40]. 
- uncontrolled growth caused by {} leads to tumour development.
- As a cancer develops, it accumulates {} mutations that confer {drivers and non drivers, hallmarks etc..}. 
- When cancers are caused by mutagenic processes such as the breakdown of HR, patterns of base substitution, indel, rearrangement and copy number mutations emerge across the collection of somatic mutations contained within the genome of the tumour - termed mutational signatures. By analysing a cancer's whole genome sequence, these patterns can be analysed, and signatures extracted, giving insights about the underlying mutagenic process that gave rise to the cancer regardless of whether a causal mutation has been discovered.
- Understanding the underlying mutagenic process driving the development of a cancer can have powerful implications for optimal treatment of a patient. Thus, gleaning these insights of underlying processes driving cancer development from mutational signature analysis is able to guide clinical decisions, and improve patient outcomes. {PARP inhibitors - selective cell death by putting more pressure on HR}

- Although mutational signatures can empower clinical decisions regardless of whether a causal mutation has been found, genetic diagnoses are still of vast significance. These diagnoses enable screening in a patient's family members, making it possible for them to understand their own risk of disease, and facilitating the implementation of preventative clinical interventions. In addition, genetic diagnoses can contain novel insights into disease biology, with downstream implications for future interpretation and treatment of a disease.
- {introduction to expanding field of variant searching / demonstrations of significant impact of non-coding regions, utilising this methodology in the project}


### research question
- In 2017, HRDetect was developed [1]. HRDetect is a highly sensitive mutational signature analysis algorithm, designed to classify tumours as being caused by BRCA-deficiency - or, the breakdown in HR-DSB caused by BRCA-deficiency - on the basis of the whole genome sequence of the cancer.
- The results of a study applying this algorithm to a cohort of 560 cancer patients yielded surprising results: 
- Previous to this study, BRCA-deficiency was thought to account for 1-5% of breast cancer cases, based on rates of genetic attribution to germline mutations in these genes [1-3 HRPaper]. However, HRDetect found this value to significantly greater, with the proportion of breast cancers caused by BRCA-deficiency to up to 22%, based on the proportions of patients displaying an algorithmic score suggesting BRCA-deficiency as a causal cancer development mechanism.
- Furthermore, a particularly interesting result is that in 41/124 (33%) of these BRCA-deficient cases, BRCA inactivation could not be elucidated through genetic and/or epigenetic analysis.
- This key finding is the starting point for this research, the aims and objectives of which are the following:

### aims and objectives

- This project seeks in the first instance to investigate whether a proportion of the aforementioned undiagnosed BRCA-deficient cancer cases can be explained by pathogenic genetic variants in the near-coding regions of the BRCA1 and BRCA2 genes. I have defined these near-coding regions as Promoter, 5'UTR (untranslated regions), Intronic and 3'UTR regions of these genes, and am using the Genomics England 100,000 Genomes Project (GEL) dataset for my analysis.
- In order to achieve this central aim, my objectives are:
	- To curate an unbiased set of high-confidence likely pathogenic variants in near-coding regions of BRCA genes in all consenting GEL participants. This requires variant extraction in near-coding BRCA1 and BRCA2 regions, with subsequent filtering on the basis of allele frequencies and a combination of applied variant annotations - using SpliceAI, CADD, PhyloP, RNA Binding Protein Data, UTRannotator and PolyA signals. 
	- To conduct burden testing of curated variants. Using analysis from [1] provided by Nik-Zainal group (responsible for HRDetect), I will compare variant incidence with those in control cohorts to understand whether curated variants are enriched in individuals with an HRDetect score sufficient to enable a BRCA-deficient classification.
	- To conduct variant interpretation where variants of interest have been uncovered.
- Further aims in subsequent work (if time allows), will be guided by initial findings - using results to formulate and select the most interesting questions to explore. However, some possible directions for the work are:
	- investigating specific mechanisms of near-coding gene activation if interesting variants, or seemingly important mechanisms are discovered
	- using analogous methodology to identify near-coding mechanisms of other undiagnosed cancer participants - for example, searching for variants causing DNA mismatch repair deficiency in Lynch Syndrome patients. [2,3,4]

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