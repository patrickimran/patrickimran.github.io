# Circulating Tumor DNA: NGS approaches to Cancer Diagnostics
1. [Introduction to Cancer Diagnostics](#1)
2. [Liquid Biopsy](#2)
3. [Identification of Allele Variants](#3)<br>
    3.1. [Whole Genome Sequencing](#31)<br>
    3.2. [Whole Exome Sequencing](#32)<br>
    3.3. [Targeted Sequencing](#33)
4. [Significance and Future](#4)




## 1. Introduction to Cancer Diagnostics<a name="1"></a>

Cancer diagnostics is a critical and fast-growing area of research as there is the need to develop cheaper, faster, and more accurate diagnostic tests. Early detection is critical. It can give patients better outlook on treatment, and many studies have shown that survival rates are 5-10X higher for patients diagnosed at early stages of cancer. [1]

Traditional methods of cancer detection include: [2]
- __Endoscopy__: Inserting a tube-like instrument with a camera into the body, e.g. colonoscopy
- __Radiology__: Irradiating patients to produce imagery such as x-rays (mammograms), CT scans, MRI
- __Tissue Biopsy__: Analysis of tissue or cell samples, e.g. Pap smear, needle biopsy, surgical biopsy

Many of these techniques are invasive, painful, tissue specific, and/or have potential to harm patients. And for those same reasons, they aren't feasible for monitoring real-time tumor dynamics or response to treatment. Let's look at an emerging technology, __liquid biopsy__, and the principles and technologies that enable it. 

## 2. Liquid Biopsy<a name="2"></a>

The principle behind liquid biopsy is the discovery in 1977 by Leon et al. [3] of an increased concentration of cell-free DNA circulating in the blood of cancer patients. Circulating tumor DNA, or __ctDNA__, is the circulating DNA in the blood which comes from tumors. By detecting ctDNA in blood, we can use it as a biomarker for cancer. Compared to tissue biopsy, it is less invasive, available even when there might not be enough tumor tissue to sample (or when tissue is hard to reach), and requires little blood draw (10ml is typical [4]). As a result, tests can be done frequently allowing for _real-time monitoring_: showing current tumor dynamics, tracking response to treatment of specific mutations, etc. 

This diagram shows the types of information we can get from ctDNA: 

![CTCs vs ctDNA 1](http://cancerdiscovery.aacrjournals.org/content/candisc/4/6/650/F1.large.jpg)


#### What about circulating tumor cells?
CTCs, or circulating tumor cells, are intact cells from tumors that circulate in the DNA. While appealing, as it would allow similar analyses to traditional tissue biopsies, there are still many technological challenges in isolating CTCs among an abundance of normal blood cells. As a result, they are not as reliable as a diagnostic tool in terms of sensitivity, which is critical for early detection. [6]

## 3. Identification of Allele Variants<a name="233"></a>

For analyzing ctDNA and the cancer genome, we can do so at three different levels of NGS:

1. __Whole Genome Sequencing__ - very high level view

2. __Whole Exome Sequencing__ - high level view

3. __Targeted Sequencing__ - detailed view

The differences between the three can be summarized in the following table from a study identifying genetic causes of primary immunodeficiencies (PID), i.e. allele variants associated with PID [7]. For cancer diagnostics, the technology and advantages, etc. are the same but for cancer-associated allele variants. 

![](https://www.frontiersin.org/files/Articles/264192/fimmu-08-00847-HTML/image_m/fimmu-08-00847-t001.jpg)

Each level of NGS offers its own advantages and limitations. We find that targeted sequencing is the best approach for the diagnostic solution described earlier: one that is cheap, sensitive, and real-time. However, note the first two limitations in the above table: it would be impossible without prior and continuous research using WGS or WES.

### 3.1 Whole Genome Sequencing<a name="31"></a>

The main benefit to WGS is that it can identify _de novo_ mutations (indels, inversion, virus integration, translocation, etc.) that are associated with cancer. This is essential to mapping the cancer genome and identifying the regions of interest which will then be interrogated in targeted sequencing. 

From study of whole genome sequencing to find copy number changes in ctDNA of prostate cancer patients:
>We performed whole-genome sequencing from plasma at a shallow sequencing depth to establish a genome-wide copy number profile of the tumor at low costs within 2 days. [9]

Their methodology is as follows:

![](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3707016/bin/gm434-2.jpg)

WGS has been successful at identifying and profiling variants, however WGS becomes prohibitively expensive at the high resolutions necessary to detect ctDNA fragments, and especially so in early stages of cancer. [8]

### 3.2 Whole Exome Sequencing<a name="32"></a>

Whole exome sequencing (which sequences only protein-coding DNA) is a more cost effective method that can be used for routine analysis of de novo mutations. It is a kind of middle-ground with some of the cost-effectiveness and routine-ness of targeted sequencing, and some of abilities of WGS in identifying de novo mutations. 

In a very highly cited _Nature_ paper fron 2013 titled "Non-invasive analysis of acquired resistance to cancer therapy by sequencing of plasma DNA",  Murtaza et. al. demonstrated as a proof of concept how WES can be used to detect new cancer-associated variants over time. The authors collected and sequenced blood samples at the beginning of treatment and after. By comparing the relative representation of variants between the two timepoints, they were able to see where some allele variants increased or decreased in response to therapy. This allows identification of cancer allele variants that are associated with acquired drug resistance. [9]

Their workflow can be seen below:

>![](https://media.springernature.com/m685/nature-assets/nature/journal/v497/n7447/images/nature12065-f1.2.jpg)
>1. Collect plasma samples: once before and at multiple time steps during treatment and follow up.
>2. Perform whole exome sequencing on ctDNA in samples from select time points, and on germline DNA for comparison.
>3. Variant-calling algorithms to identify mutations, and then calculate allele fraction (relative frequency of an >allele) of mutant alleles. 
>4. Comparing allele fraction of mutant alleles across time can identify if alleles rose in frequency due to some selective pressure from the treatment.

#### Another type of exome sequencing: CAPP-Seq
Cancer Personalized Profiling by Deep Sequencing (__CAPP-Seq__) is a method for _quantifying ctDNA levels_ in blood. Increases in the amount of ctDNA have been shown to be associated with cancer progression. In one study, ctDNA was detected in 94% of lung cancer patients experiencing relapse in their first blood sample post-treatment. ctDNA could be detected on average 5.2 months before relapse was detected by radiographic techniques. ctDNA analysis is promising as an early detector of relapse, which could facilitate treatment when it is easiest to treat. [10]



### 3.3 Targeted Sequencing<a name="33"></a>

WGS can identify genes that are associated with cancers, and WES can further identify mutations that are associated with treatment progression. With such knowledge, we are enabled to perform targeted _sequencing_ of those known genes of interest and track cancers much more frequently, and inexpensively, than WES. 

Tagged Amplicon Deep Sequencing, or __TAm-seq__, is a method for detecting and quantifying _known_ cancer mutations in ctDNA.
It has a couple advantages that make it a good diagnostic tool [11] :
* Reduced noise from sequencing
* Increased sensitivity (true positive rate)
* Fast and inexpensive
* Allows __frequent and real-time monitoring of specific mutations__

It is limited in that, unline WES or WGS, it is unable to identify de novo mutations - instead it relies on a "panel" of genes of interest, hence _targeted_. 

An example of a TAm-seq panel used by the biotech startup Inivata (spun off from the original ctDNA TAm-seq paper by its authors), showing genes/regions of interest [12] :

![](https://i.imgur.com/gQZMWud.png)

#### TAm-seq's workflow
1. Design PCR primers to cover each gene of interest in overlapping short amplicons (See figure)
2. Perform an intial pre-amplification of all regions in parallel to preserve representation of all alleles (both wild-type and mutantt). 
3. Selectively re-amplify those genes or regions of interest in the pre-amplified material in single-plex PCR.
4. Add sequencing adaptors and sample-specific barcodes in additional PCR. 
5. Sequence!

It is summarized in the following figure: [11]

![](https://i.imgur.com/HmwpbsJ.jpg)

Analysis of TAm-seq data usually involves plotting mutant allele percentage over time, in addition to treatment progression. The following figure shows the reduction in a specific mutantation, BRAF V600E, throughout treatment  [15] :

![](https://i.imgur.com/FzsOkty.png) 

Another figure of TAm-seq analysis demonstrates the ability of TAm-seq to track response to treatment across multiple genes, in more than one patient, over time [14] :

![](http://i.imgur.com/3kGJ5JR.jpg)

## 4. Significance and Future<a name="4"></a>

Liquid biopsy has the promise of being a cheap and inexpensive cancer diagnostic, one that is non-invasive and easy on patients. It has the potential to diagnose cancer early with early ctDNA detection, which would mean improved odds of successful treatment. It would also allow real time, fine-grained monitoring of mutations over time to both track patient progress, but also prove a powerful tool in the evaluation of new therapeutics and improve our understanding of how mutations change in response to these treatments. This also has implications for personalized medicine. For example, finding a therapeutic that is known to reduce the frequency of a mutant allele that we know a patient has, allows us to find them the most effective treatment.

Many new biotech companies and startups have begun to bring this technology to reality, such as Grail [1] and Freenome [15], in the race to bring these tests to patients. At iGEM 2018, the second-place winning project was a liquid biopsy diagnostic device, algorithm, and application for the detection and frequent tracking of methylation profiles in ctDNA. While it will be many more years before we see liquid biopsy diagnostics that are patient-ready, the technology is an area of intense growth and competition.




_article by Patrick McGrath, pmcgrath@ucsd.edu_
# References
[1] https://grail.com/<br>

[2] https://www.cancer.org/healthy/find-cancer-early/tests-to-find-and-diagnose-cancer.html<br>

[3] Leon, S. A., Shapiro, B., Sklaroff, D. M., & Yaros, M. J. (1977). Free DNA in the serum of cancer patients and the effect of therapy. Cancer research, 37(3), 646-650.

[4] https://www.liquidbiopsy.com/sample-collection-guidelines/

[5] https://www.sciencedirect.com/science/article/pii/S1672022917300487#b0285

[6] Alix-Panabières, C., & Pantel, K. (2016). Clinical applications of circulating tumor cells and circulating tumor DNA as liquid biopsy. Cancer discovery, 6(5), 479-491.

[7] Seleman, Michael, et al. "Uses of Next-Generation Sequencing Technologies for the Diagnosis of Primary Immunodeficiencies." Frontiers in Immunology 8 (2017).

[8] Ma, M., Zhu, H., Zhang, C., Sun, X., Gao, X., & Chen, G. (2015). “Liquid biopsy”—ctDNA detection with great potential and challenges. Annals of translational medicine, 3(16).

[9] Murtaza, Muhammed, et al. "Non-invasive analysis of acquired resistance to cancer therapy by sequencing of plasma DNA." Nature 497.7447 (2013): 108.

[10] Chaudhuri, A. A., Chabon, J. J., Lovejoy, A. F., Newman, A. M., Stehr, H., Azad, T. D., ... & Scherer, F. (2017). Early detection of molecular residual disease in localized lung cancer by circulating tumor DNA profiling. Cancer discovery.

[11] Forshew, T., Murtaza, M., Parkinson, C., Gale, D., Tsui, D. W., Kaper, F., ... & Hadfield, J. (2012). Noninvasive identification and monitoring of cancer mutations by targeted deep sequencing of plasma DNA. Science translational medicine, 4(136), 136ra68-136ra68.

[12] https://www.inivata.com/wp-content/uploads/2016/11/inivata-ncri-poster.pdf

[13] https://www.inivata.com/wp-content/uploads/2016/06/InivataPoster_MolecularTargets_November_2015.pdf

[14] https://www.inivata.com/wp-content/uploads/2016/06/InivataPoster_IASLC_September_2015.pdf

[15] https://www.wired.com/story/startups-race-to-create-cancer-screens-from-dna/

[16] http://2018.igem.org/Team:UC_San_Diego
