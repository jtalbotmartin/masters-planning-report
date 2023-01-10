
### Mutational Signatures and HRDetect

As described in [12], a 2012 study analysing whole genome sequences of 21 breast cancers introduced the concept of mutational signatures. The analysis of this study demonstrated consistent mutagenic patterns across the sequenced tumour [{}]. The statistical power of thousands of accumulated somatic mutations in the tumour's sequence enables the discernment of patterns of base substitution, indel, rearrangement and copy number mutations caused by specific mutagenic processes. This enables inference of the causal mechanisms of a cancer's development (considered as such after validation of the causal - rather than associative - effect of an established signature) from the sequence of the cancer itself.
SInce this intial finding, many more studies have been conducted, using larger and more diverse sets of somatic mutation data across tissue and cancer types [{}]. This has enabled the expansion of the number of identified signatures, our understanding of the underlying biological processes at play, and the development of sophisticated tools and frameworks for mutational signature analysis. [{mutational signature review - look at reference notes}].

- difficulty in signature fititing (leads into action of HRDetect)
	- figure 3a and 3b 
- signatures present in breast cancer
- brca signatures / HR
	- figure
- HRDetect - USE MUTATIONAL SIGNATURES REVIEW
	- Overview of Action
	- combination of signatures
	- Results
	- Prognostic Benefit
	- 
	- undiagnosed patients + methylation
	- 
	- concurrence with chord 
	- critique: methylation - implications for this study
- 

### Computational Genomics and Near-Coding Regions

As described in [13], the last three decades have seen huge technological development and advances in the analysis of human genetic variation, and understanding of the genetic basis of human disease. [HGP, gmomAD...]However, the majority of efforts have been centered around sequencing and analysing variation within protein-coding regions of the genome. The enrichment of these regions for causal effects enables a very successful means of discovery of disease-linked genes. However, this restriction to regions that directly encode proteins ignores the vast majority of the human genome; doing so disregards genetic variation that contributes to disease aetiology contained within key functional elements on the non-coding genome, and leaves many instances of rare disease without a genetic diagnosis [26,15,16]. An overview of these non-coding function elements, taken from [14] is shown in figure 1.

With WGS becoming commonplace, in addition to other facilitatory technologies, diagnostic yields have improved, and the importance of variation in these functional non-coding regions is being increasingly demonstrated [16,17,18,19, 22]. The rare disease field continues to reveal disease mechanisms pertaining to variants in these regions - "acting through affecting splicing[], transcription[], translation[], RNA processing and stability [] and chromatin interactions" [21]. One such study found that, in the case of MEF2C, loss-of-function caused by upstream non-coding variation accounts for a quarter of likely diagnoses of MEF2C-linked Developmental Disorders [20]. 

The wealth of work done in this field has enabled the hypothesis generation in this study, and have been the foundation on which the formulation of this project is built. These studies have guided:
- the data, methodology and frameworks I will use in the extraction and interpretation of variants uncovered. In this project [23, 21, 20, 24, 25, 27]
- the tools I will use for variant annotation and analysis (described below)
- the regions of BRCA defined within the scope of my search for novel mechanisms of BRCA-deficiency - defining a set of near-coding regulatory regions comprising of 5' and 3' UTRs, Promoter and Intronic regions.

In this instance, the regions of BRCA in which I will analyse are chosen in light of the annotations available, in order to interpret the findings I will generate. These annotations I will utilise are as follows:
- Combined Annotation–Dependent Depletion (CADD) Scores [28] - a measure of deleteriousness used to estimate variant pathogenicity.
- PhyloP (Phylogenic P-values) [29]- a measure of evolutionary conservation at individual alignment sites [30] {tells me}
- SpliceAI
- UTRannotator [31] - a plugin to Ensembl's variant effect preductor [33] tool to annotate upstream open reading frame-creating or disrupting 5'UTR variants [32] {these variants are}
- PolyA Signals

- extrapolate mechanisms 
**Regions**

**Tools**

**Frameworks and Methodology**

Figure 2, taken from [21] illustrates disruptive mechanisms of disease in regulatory elements.


Increasingly, the importance of variation in these regions is being demonstrated, 

![[Pasted image 20230110205028.png]]caption: taken from[14]
"Chromosomes are partitioned into topologically associating domains (TADs) corresponding to domains of highly interacting chromatin. In TADs, DNA is complexed with histones to form nucleosomes (orange circles); active promoters (orange rectangles) and enhancer (pink rectangles) or silencer (dark blue rectangles) elements can form chromatin loops, mediated by protein effectors [transcription factor (TF)1, TF2]. Transcription of protein-coding genes (green blocks) or noncoding RNA genes (lncRNA; purple blocks) is shown as colored arrows. The generic protein-coding gene structure includes the flanking untranslated regions (UTRs) and alternating regions of introns (noncoding sequences) and exons (coding sequences). Transposable elements (aqua ovals) and tandem repeats (dark blue ovals) are repetitive DNA sequences that constitute ~50% of the human genome."

![[Pasted image 20230110213420.png]]
captionL taken from [21]
"Gene and protein expression are tightly controlled processes mediated by a multitude of regulatory elements. Transcription of a gene into RNA is mediated by a promoter element directly upstream of the gene [], along with more distal enhancer and repressor elements (collectively referred to as cis‑regulatory elements, or CREs) to which transcription factors bind []. CREs may be within their target gene or in other intragenic or intergenic space either 3′ or 5′ of the transcription unit they influence. Within the gene itself, intronic regions contain specific sequences that control their removal through splicing to form the mature RNA (mRNA) transcript, and untranslated regions (UTRs) regulate RNA stability, trafficking, and the rate at which it is translated into protein []. Each gene also sits within a wider regulatory context, or topologically associated domain (TAD), flanked by boundary/insulator elements which restrict the action of CREs to within specific TADs []."


In recent years ... {}
Figure 1 gives an overview of these functional 
...

- Overview
	- 50% 
	- non-coding regions
	- recent expansion of non-coding
- key studies
	- LoF
	- MEF2C
	- Neurodevelopment disorders
- interpretation - clinical interpretation
- annotations
	- SpliceAI
	- PhyloP
	- CADD
	- UTRannotator
	- RNA Binding Protein
	- PolyA Signals