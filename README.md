---
type: "project" 
date: "2020-06-15" # Date you first upload your project.
title: "An Exploration into the Dual-Route Model of Word Processing"
names: [Yi-Wen Huang]
github_repo: 
website:
tags: [fmri, language, dual-route model, connectivity]
summary: "This is a project where I explored the processing of fMRI data. The dataset in use is ds003481, which involved the task of reading different words. I attempted to replicate the study's findings and also complete a functional conncectivity map per condition in this project."
image: ""
---
<!-- This is an html comment and this won't appear in the rendered page. You are now editing the "content" area, the core of your description. Everything that you can do in markdown is allowed below. We added a couple of comments to guide your through documenting your progress. -->

## Project definition

### Background

Coltheart and others have proposed "The Dual-Route Model" to explain how humans process words -- The ventral pathway primarily handles visual word recognition and semantic processing, while the dorsal pathway specializes in grapheme-to-phoneme conversion and phonological processing, including the resolution of phonological output. These two distinctions have been found in past fMRI scannings, and I wanted to use this opportunity to replicate this finding. In this project, particiapnts were asked to read the following categories: motion verbs, mental verbs, pseudo words, and symbols. Initially, I attempted to plot the brain activation pattern by regressing the brain data to a GLM. I also tried to create the functional connectivity map to look into the effects reported by the original study. Lastly, I planned on looking into training a classification model based on the brain responses, though I could not complete the last part due to the constraints of time. 

### Tools

The project used the following tools: 
* data acquisition: datalad
* preprocessing: fmriprep
* fmri data processing in python: nibabel, nilearn, nltools

### Data

Dataset: [The Pragmatic Language Dataset](https://openneuro.org/datasets/ds003481/versions/1.0.3)
Files: sub-123, run-01

### Deliverables

At the end of this project, we will have:
 - An analysis notebook
 - The final presentation slides

## Results

### Progress overview

1. I recreated the brain activation patterns of each condition visually.
2. I chose 2 brain regions as the seed for the calculation of functiona connectivity: the Left Inferior Temporal Gyrus (LITG) as the ventral pathway representative, and the Left Superior Temporal Gyrus (LSTG) as the dorsal pathway representative.
3. I calculated the whole-brain connectivity by pairwise correlation and generated 4 clusters from the correlation matrix. 

### Tools I learned during this project

* **docker** for data and environment management
* **fmriprep** for fMRI data preprocessing
* **nilearn**, **nibabel**, and **nltools** for fmri data analysis

### Results

#### Deliverable 1: An analysis notebook

The notebook where I completed my analysis. 

## Conclusion and acknowledgement

From the most surface level, I think I have successfully complted my goal, which was to get hands-on experience with fMRI data and go through the rough steps of processing and analysis. I got a great overview of how fMRI datasets could be run, and it has given me great confidence for future projects if I plan on looking into the brain again. 

I have observed the following: 
- The brain activation pattern for all the contrasts looked slightly off, possibly due to fault preprocessing steps. 
- The activated areas for the ventral and dorsal representatives (LITG and LSTG) seem to be non-overlapping, so it could be that they form two separated networks in language processing? However, the areas seemed to be swapped, so further inspection was needed.

I faced a lot of challenges during this project, and many questions, presumably more than the beginning, confuse me. For example, I still feel lost about how preprocessing works, because each step still feels like a mystery to me. I still have questions regarding the design matrices. I did not have sufficient statistical tools so I couldn't decide how to interpret the results. 

The learning process has been heavily AI based, while also referring to the tutorials of DartBrain. Modules that I learned from the most in BHS include Docker and environment settings, Introduction to open data resources, and Functional connectivity. 

References: 
Jobard G, Crivello F, Tzourio-Mazoyer N. Evaluation of the dual route theory of reading: a metanalysis of 35 neuroimaging studies. Neuroimage. 2003 Oct;20(2):693-712. doi: 10.1016/S1053-8119(03)00343-4. PMID: 14568445.
Reyes-Aguilar A, Licea-Haquet G, Arce BI, Giordano M (2023) Contribution and functional connectivity between cerebrum and cerebellum on sub-lexical and lexical-semantic processing of verbs. PLoS ONE 18(9): e0291558. https://doi.org/ 10.1371/journal.pone.0291558
