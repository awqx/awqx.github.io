---
layout: archive
title: Projects
permalink: /projects/
author_profile: false
---
## Projects and past research

My list of publications can also be found on [ORCID](https://orcid.org/0000-0002-7954-8049).

### Concurrent functional linear mixed models for photometry analysis

PI: Dr. Francisco Pereira. Mentor: Dr. Gabe Loewinger. Collaborators: Dr. Erjia Cui. 

I extended the existing R package `fastFMM` to include procedures for fitting concurrent functional linear models.

### Labeling nuanced outcomes of depression with large language models

PI: Dr. Francisco Pereira. Mentors: Dr. Dylan Nielson, Dr. Juan Antonio Lossio-Ventura. 

Associated publication: Xin AW, Nielson DM, Krause KR, Fiorini G, Midgley N, Pereira F, et al. Using large language models to detect outcomes in qualitative studies of adolescent depression. Journal of the American Medical Informatics Association. 2024 Dec 11;ocae298. [https://doi.org/10.1093/jamia/ocae298](https://doi.org/10.1093/jamia/ocae298).

I led work to create models that could detect the presence of nuanced features of depression within patient interviews. Our target features were previously described in a coding framework developed by our collaborators. Clinical studies commonly only track diagnostic features of major depressive disorder (MDD) to monitor participant progress. Drs. Krause KR, Fiorini G, and Midgley N performed a qualitative analysis of interviews with adolescent patients in a clinical study of depression, creating a new coding framework that captured features outside of symptoms, including relationships, self-perception, and feeling of family support. 

I processed patient interviews and embedded text with a variety of large language models (LLMs), including BERT, MentalBERT, MentalLongformer, Llama 2-7B, and Llama 3-7B. I tuned logistic regression models on the embeddings and performed post hoc analyses comparing model performance.  

### Efficient calculation of coefficient variance in functional concurrent mixed models

PI: Dr. Francisco Pereira. Mentor: Gabe Loewinger.

I am working on a scalable, interpretable implementation of functional mixed models to analyze longitudinal high-dimensional data. I am improving the fastFMM R package previously published by Drs. Loewinger and Erjia Cui (latter is currently at UMN). 

  
I diagnosed and fixed an issue with undercoverage of random coefficient confidence intervals when modeling nested effects. I discovered that the flaw arose due to a hard-coded cross-product formula that applied in simple, non-nested cases, and addressed the error by adding a full cross-product function. Due to the additional computational load, I also integrated a code speed-up for our method of moments estimator. 

I have completed beta code for fitting concurrent functional mixed models ([awxin/fastFMMconc on GitHub](https://github.com/awxin/fastFMMconc)), and we are running test simulations for an upcoming methods paper. Concurrent models will allow for fitting time-varying functional covariates. I am currently working with labs at the NIMH and University of Alabama-Birmingham on implementing these models. Furthermore, I am testing coverage on simulated data. 

### Observing changes in mood and expectation during a gambling task.

PI: Dr. Francisco Pereira. Mentor: Dr. Charles Zheng. 

Previously, our team and collaborators recruited MTurk workers to perform a task where they tracked their mood and expectation of future reward in a gambling task with predetermined losing and winning streaks. I created a bespoke quality metric combining non-response rates, correlation of mood to recorded events, and reaction time. 

### Tuberculosis mGWAS with conditioning and recursive feature elimination

PI: Prof. Megan Murray. Mentor: Dr. Chuan-Chin Huang. 

Senior thesis in Statistics, recommended for High Honors. 

I performed microbial genome-wide association studies (GWAS) of tuberculosis for my senior thesis in Statistics (recommended for High Honors). The project aimed to identify new causal SNPs that may affect the virulence of tuberculosis. As a sub-goal, the project compared the performance of several GWAS techniques. My direct mentor, Dr. Chuan-Chin Huang, organized raw genomic sequencing data from patient sputum samples. 

My work included standard methods for mGWAS, such as linear mixed models, generalized linear models, and PCA population correction. I also implemented recursive feature elimination (RFE) to capture additional non-linear interactions. Additionally, I used conditional mGWAS based on work from Dr. Kevin Ma, Dr. Murray’s former PhD student. By conditioning on drug susceptibility tests, we hoped to better detect signals from compensatory mutations. We did not find strong candidate SNPs for verification through microbiological testing or external validation data.

### Quantitative structure-activity relationship models for small molecule binding to cyclodextrin

PI: Prof. Horst von Recum. Mentor: Dr. Edgardo Rivera-Delgado.

Xin AW, Rivera-Delgado E, von Recum HA. Using QSAR to predict polymer-drug interactions for drug delivery. Front Soft Matter [Internet]. 2024 Jul 29 [cited 2024 Aug 30];4. Available from: https://www.frontiersin.org/journals/soft-matter/articles/10.3389/frsfm.2024.1402702/full

I developed a suite of quantitative structure activity relationship (QSAR) models to predict the binding of small molecules to cyclodextrin. I used R to implement a variety of modeling techniques, including generalized linear models, support vector machines, random forest, multivariate adaptive regression splines. Originally, predictors were generated using the software PaDEL-Descriptor, but I eventually integrated chemical descriptor generation into an R-only pipeline and eventual R Shiny app. The project repository is [here](https://github.com/awqx/cyclodextrin-qsarr). The accompanying R package is [here](https://github.com/awqx/qsarr).

Documentation of this project is, unfortunately, a bit of a mess due to the self-taught nature. 

Presented at ISEF 2018 and 2019. 2018: Fourth Place Grand Prize Award in Chemistry, Air Force First Place Award in Chemistry, Runner-up for American Chemical Society. 2019: First Place from the American Statistical Association, King Abdul-Aziz and his Companions Foundation (Mawhiba) Award in the category of Intelligence-based Solutions in Cyber-security, STEMCloud Award in Engineering Mechanics.
