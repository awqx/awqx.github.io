---
title: "fastFMM extension to concurrent functional linear mixed models"
collection: publications
category: manuscripts
permalink: /publication/2026-03-18-fastFMM
excerpt: 'Functional LMMs allow modeling associations between photometry traces and trial-specific scalar values like behavioral summaries and session number, while also accounting for between-animal heterogeneity. Here, we extend the method to concurrent FLMMs (cFLMMs), a method that can fit the instantaneous relationship between functional outcomes and functional covariates. (Reviewed Preprint).'
date: 2026-03-18
venue: 'eLife'
paperurl: 'http://awqx.github.io/files/xin2026-fastFMM.pdf'
citation: 'Xin AW, Cui E, Pereira F, Loewinger G. Capturing instantaneous neural signal-behavior relationships with concurrent functional mixed models. eLife. 2026 Mar 18;15. doi: 10.7554/eLife.109428.1'
---

The full text with reviewer comment and our Provisional Author Response is available on [eLife](https://doi.org/10.7554/eLife.109428.1). 

This is a Reviewed Preprint, which reflects a single round of peer review. The revised preprint and Complete Author Response will be released by the end of 2026. 

## Abstract

We previously proposed an analysis framework for fiber photometry data based on functional linear mixed models (FLMMs). Functional LMMs allow modeling associations between photometry traces and trial-specific scalar values like behavioral summaries and session number, while also accounting for between-animal heterogeneity. Here, we extend the method to concurrent FLMMs (cFLMMs), a method that can fit the instantaneous relationship between functional outcomes and functional covariates. Concurrent FLMMs enable testing of how the photometry signal is associated with, for example, a behavioral variable that evolves across within-trial timepoints (e.g. animal speed). cFLMMs can also model the relationship between the photometry signal and covariates in experiments with variable trial lengths (e.g., in studies where trials end when an animal responds). We illustrate the application of cFLMMs on two published studies and show the method can identify signal–behavior associations in analyses not possible with FLMMs. We find that analyzing photometry–behavior associations based on behavioral summaries (e.g., latency-to-response, average lick rate) can lead to misleading conclusions. We published our method in the fastFMM package, available as an R package through GitHub ([https://github.com/awqx/fastFMM](https://github.com/awqx/fastFMM)).