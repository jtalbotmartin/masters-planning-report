
### Mutational Signatures and HRDetect

A 2012 study analysing whole genome sequences of 21 breast cancers introduced the concept of mutational signatures[46]. The analysis of this study demonstrated consistent mutagenic patterns across the sequenced tumour. The statistical power of thousands of accumulated somatic mutations in the tumour's sequence enables the discernment of patterns of base substitution, indel, rearrangement and copy number mutations caused by specific mutagenic processes. This enables inference of the causal mechanisms of a cancer's development (considered as such after validation of the causal - rather than associative - effect of an established signature) from the whole genome sequence (WGS) of the cancer itself. [12]
Since this initial finding, many more studies have been conducted, using larger and more diverse sets of somatic mutation data across tissue and cancer types [{}]. This has enabled the expansion of the number of identified signatures, our understanding of the underlying biological processes at play, and the development of sophisticated tools and frameworks for mutational signature analysis. [{mutational signature review - look at reference notes}].

As detailed in {intro}, the causal mechanisms of cancer development can lead to specific vulnerabilities in the cancer to which it gives rise - as is the case in BRCA-deficient tumours and PARP inhibitor sensitivity [43-45 landscape]. Mutational signatures can thus - as a result of facilitating the identification of causal mechanisms conferring treatment-sensitivity - be robust biomarkers of drug responsiveness used to stratify or diagnose patients. [47]
For this reason, clinical applications of mutational signatures require robust classification on which to base intervention decisions. HRDetect, a probabilistic classifier of BRCA-deficient cancers introduced in section {} was developed for this reason [1]. 

In this research, BRCA-deficient features were quantitatively defined using an initial training set contraining 22 BRCA-null tumours. The distinguishing genomic profile of these mutations were defined as "over-representation of base-substitution signature 3 or 8, an excess of large deletions (>3 bp) with microhomology at the junction of the deletion, rearrangement signature 5 and copy number profiles associated with the widespread loss of heterozygosity. Additionally, BRCA1-null tumors mainly had an excess of rearrangement signature 3 mutations (characterized by short <10-kb tandem duplications) and a lesser contribution of rearrangement signature 1 mutations (typified by long >100-kb tandem duplications)" [1]. These signatures and their respective generative mechanisms are shown in figure {} (taken from [12]), and details of these signatures on a DNA level can be explored using COSMIC [48]

![[Pasted image 20230111050314.png]]
caption: Distinctive signatures of BRCA1 deficiency, and the corresponding generative mechanisms (taken from [12]) - acronyms: HRD, homologous recombination deficiency; ID, insertion or deletion signature; LOH, loss of heterozygosity; MMBIR: microhomology-mediated break-induced replication; POLQ, DNA polymerase-θ; RS, rearrangement signature; ssDNA, single-stranded DNA; TD, tandem duplication; TMEJ: DNA polymerase-θ-mediated end joining

Through robust phases of training, model parameters were identified, selected and weighted - leading to the use of five distinguishing parameters for use in the model in order to best segregate BRCA-deficient and sporadic cancers: "microhomologymediated indels, the HRD index, base-substitution signature 3, rearrangement signature 3 and rearrangement signature 5" [1], with the later edition of base-substitution 8 after further genetic diagnoses were uncovered.

When applying this predictive model to a cohort of 560 breast cancer patients [1], HRDetect displayed a 98.7% detection sensitivity of BRCA-deficient tumours - demonstrating clear distinctive capabilities in the separating of high and low probabilities of BRCA-deficiency[1]. In addition, HRDetect identified 20% of patients in this cohort as having a high level of BRCA-deficiency - representing a significant shift in the expected incidence of this type of breast cancer. Of these identified patients, no somatic or germline BRCA1 or BRCA2 mutations could be identified in 47 - forming the cohort of interest for this project. A caveat in this statistic is that for 37/47 of these patients, data needed to infer BRCA1 or BRCA2 silencing via the presence of promoter hypermethylation was not available - a key fact to take into account when interpreting my findings to infer biallelic BRCA1 or BRCA2 inactivation. These results are illustrated in figure {}, taken from [1].

![[Pasted image 20230111060345.png]]

caption: 

### Computational Genomics and Near-Coding Regions

As described in [13], the last three decades have seen huge technological development and advances in the analysis of human genetic variation, and understanding of the genetic basis of human disease. However, the majority of efforts have been centered around sequencing and analysing variation within protein-coding regions of the genome. The enrichment of these regions for causal effects enables a very successful means of discovery of disease-linked genes. However, this restriction to regions that directly encode proteins ignores the vast majority of the human genome; doing so disregards genetic variation that contributes to disease aetiology contained within key functional elements of the non-coding genome, and leaves many instances of rare disease without a genetic diagnosis [26,15,16]. An overview of these non-coding function elements, taken from [14] is shown in figure 1.

With WGS becoming commonplace, in addition to other facilitatory technologies, diagnostic yields have improved, and the importance of variation in these functional non-coding regions is being increasingly demonstrated [16,17,18,19, 22]. The rare disease field continues to reveal disease mechanisms pertaining to variants in these regions - "acting through affecting splicing[], transcription[], translation[], RNA processing and stability [] and chromatin interactions" [21]. One such study found that, in the case of MEF2C, loss-of-function caused by upstream non-coding variation accounts for a quarter of likely diagnoses of MEF2C-linked Developmental Disorders [20]. 

The wealth of work done in this field has enabled the hypothesis generation in this study, and have been the foundation on which the formulation of this project is built. These studies have guided:
- the data, methodology and frameworks I will use in the extraction and interpretation of variants uncovered. In this project [23, 21, 20, 24, 25, 27]
- the tools I will use for variant annotation and analysis (described below)
- the BRCA1 and BRCA2 regions defined within the scope of my search for novel mechanisms of BRCA-deficiency - defining a set of near-coding regulatory regions [49] comprising of:
	-  5' and 3' UTRs - sequences immediately adjacent to a gene's coding sequence, with key regulatory roles through interactions with RNA-binding proteins and miRNAs, including in mRNA stability and translation [14]. Various mechanisms of rare disease caused by UTR variants have been demonstrated - for example, the creation of upstream start codons (uAUGs) or upstream open reading frames (oORFs) disrupts translation, resulting in phenotypes including severe developmental disorders [20].
	- Promoter Regions - regions that regulate transcription, found upstream of the coding region. Promoters comprise an open chromatin region spanning either side of the transcription start site, initiating transcription via the recruitment of transcription factors and RNA polymerase II [14]. Promoter variants alter methylation patterns, or impact transcription factor binding, disrupting transcription - illustrated in the case of OVOL2, where this mechanism caused corneal endothelial dystrophies [49, 55]
	- Intronic regions - regions between protein coding exons, subject to removal during pre-RNA splicing. Donor and acceptor splice sites, and branch points are examples of signals suggesting a critical role of introns in pre-RNA splicing. Mutations impacting splicing make significant rare disease contributions, including in the case of retinal disease [57]

These annotations I will utilise are as follows:
- Combined Annotation–Dependent Depletion (CADD) Scores [28] - a measure of deleteriousness used to estimate variant pathogenicity.
- PhyloP (Phylogenic P-values) [29]- a measure of evolutionary conservation at individual alignment sites [30], an inference measure of tolerance to mutation at a particular site.
- SpliceAI [34] - a best-in-class [35] deep neural network for the prediction of splicing variants. {tells me}
- UTRannotator [31] - a plugin to Ensembl's variant effect predictor [33] tool, used to annotate upstream open reading frame-creating or disrupting 5'UTR variants [32].
- Omni-PolyA [51] - a tool for poly(A) signal recognition, a key structure in the polyadenylation stage of RNA processing.
- Data on RNA-Binding Proteins - key components in RNA regulation, forming interactions with UTRs  [52-54].

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