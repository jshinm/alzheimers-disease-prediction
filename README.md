<img src='img/20200423_Final_project_poster.png'>

## Title
Predicting Alzheimer’s disease risk factors from the variant fingerprints of non-AD genes

## Introduction
Alzheimer’s Disease (AD) is a progressive neurodegenerative disease that is characterized by impaired cognitive domain of brain function. As of 2017, it is a 6th leading cause of death in the U.S., and the typical life expectancy after diagnosis is only about 4 to 8 years.[1] The worst part lies in the fact that there still has not been any effective treatments developed for this disease that has been known for over 100 years. This is partly due to its complex genetic components involved in AD.[2] As a result, despite numerous speculations, a clear mechanism of AD has yet to be discovered. Nonetheless, many studies have suggested multiple genes associated with the disease phenotypes.[3] This project aims to further expend the list of relevant genes/variants most prevalent in people with high number of genetic risk factors. Also, using the analyzed dataset, the risk scores, a combined number of AD risk factors, were predicted using machine learning algorithms.

## Methods
A total of 862 samples were acquired from either openSNP and Personal Genome Project. The dataset was first analyzed and annotated by openCRAVAT using 8 annotators.[4] Subsequently, the genomic variants associated with AD in accordance with the ClinVar database were labeled as risk factors for AD. Annotated results were reorganized to extract information with respect to these risk factors. Initially, a list of genetic variants co-occurred with the risk factors was generated.[5] Those genetic variants were converted into their corresponding genes. Using these metrics, frequencies of the variant occurrence within the gene was measured. After removal of AD variants from the analysis, the finalized training set was fed into two machine learning algorithms, namely support vector regression and stochastic gradient descent classifier, for regression and classification, respectively. 

## Results
Of the 17761 distinct variants that could be found in ClinVar database, 32 AD variants were identified and used as risk factors. These are variants of the following genes: APOE, PSEN1/2, APP, PRNP, A2M, TNF, NOS3, HFE, TF, ADAM10, LRRK2.[6] After screening for AD risk factors, 659 samples that carried at least one AD variant were selected for analysis. As expected, there were substantially high number of variants in some genes that are common in most of the samples, which is described as “background.” Top 10 common variants were subtracted from the analysis which consisted of APC, SYNE1, TTN, RYR2, etc. Subsequently, samples with 5 risk factors and higher were selected as a high risk group. 352 and 307 samples were found to be high and low risk groups respectively. Next, parsed dataset was transformed into a training set for SVR and SGD predictors. SVR compared to SGD performed much better in every aspect. Lastly, the list of genes highly associated with high risk users was visualized by Manhattan plot. Here, in order to present at optimal scale of y-axis, threshold was readjusted to 8.

## Implications
It is evident there are many genes associated with genetic risk factors of AD. More than 10 highly prevalent genes could be found in Manhattan plot. CHST3, for instance, is known for its correlation with AD related hearing loss.[7] Though this analysis must follow further exploration, it is interesting to see a stark difference in number of genetic variants between high and low risk groups. Even at higher and lower threshold, the pattern was not different. Only the range of y-axis was affected by the change of threshold. Also, despite the simplicity of features being trained by ML algorithms, the performance by SVR was surprisingly excellent. This further corroborates the main hypothesis of certain patterns of variants associated with AD risk factors. 

## Reference
1.	Heron, M., Deaths: Leading Causes for 2016. Natl Vital Stat Rep, 2018. 67(6): p. 1-77.
2.	Poblador-Plou, B., et al., Comorbidity of dementia: a cross-sectional study of primary care older patients. BMC Psychiatry, 2014. 14: p. 84.
3.	Giri, M., M. Zhang, and Y. Lu, Genes associated with Alzheimer's disease: an overview and current status. Clin Interv Aging, 2016. 11: p. 665-81.
4.	Pagel, K.A., et al., Integrated Informatics Analysis of Cancer-Related Variants. JCO Clin Cancer Inform, 2020. 4: p. 310-317.
5.	Reitz, C., et al., A summary risk score for the prediction of Alzheimer disease in elderly persons. Arch Neurol, 2010. 67(7): p. 835-41.
6.	Lanoiselee, H.M., et al., APP, PSEN1, and PSEN2 mutations in early-onset Alzheimer disease: A genetic screening study of familial and sporadic cases. PLoS Med, 2017. 14(3): p. e1002270.
7.	Loughrey, D.G., M.A. Parra, and B.A. Lawlor, Visual short-term memory binding deficit with age-related hearing loss in cognitively normal older adults. Sci Rep, 2019. 9(1): p. 12600.
