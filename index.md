% Replicathon 2020 (IQ BIO REU, UPR-RP)

## Getting Started

Check out the [**introduction slides**](https://speakerdeck.com/pkimes/20200626-iqbio-intro) to review the goals and context for the event! If you're interested in learning more, links to relevant papers are included in the [Useful Links](#useful-links) section below. There are a couple ways that you can get started.

1. **If you have R already installed and ready to go**, clone or download [this repository](https://github.com/pkimes/PR2020replicathon) to your computer and open the `.Rmd` files with [RStudio](https://rstudio.com/) or any other editor that you're comfortable using.
2. **If you don't have R installed on your computer**, create a free account with [RStudio Cloud](https://rstudio.cloud/), click the blue dropdown arrow next to **[New Project]**, select **[New Project from Git Repo]**, and enter this GitHub repo URL: https://github.com/pkimes/PR2020replicathon 

Free accounts on RStudio Cloud have unlimited access to cloud computing until August 3, 2020! Unfortunately, after that, free accounts will be limited to 15 hours per month.

## Reinforcement Questions

After going over the introductory slides and presentation, work through these *reinforcement questions* to make sure you and your team has a good understanding of replicability and the problem.

- [`reinforcement questions`](tutorials/00_reinforcement_questions.html)

## Main Analysis Template

* `analysis_template` [(Rmd)](https://github.com/pkimes/PR2020replicathon/blob/master/analysis_template.Rmd) [(html)](analysis_template.html) : R markdown template which each team will use to create a fully reproducible analysis with the goal of assessing and interpreting the replicability of two pharmacogenomic experiments. This document will contain all of the text and code of their analyses, which are quided by a series of questions. The tools and concepts needed to answer the questions are explored in the tutorials.

## Datasets

Data files are included under the `data` folder.

* `rawPharmacoData.rds` : raw data file generated by `downloadData.R` that contains drug response data at every dose for each cell line and drug used in both studies. 

* `summarizedPharmacoData.rds` : summarized data file generated by `downloadData.R` that contains drug response data (combined over all doses) for each cell line and drug used in both studies.

* `modelSummarizedPharmacoData.rds` : summarized data file generated in the `supplement_dose_response.Rmd` tutorial that contains recomputed drug response data (combined over all doses) for each cell line and drug used in both studies.

## Tutorials

Tutorials are included under the `tutorial` folder.

Each tutorial contains text and code that explores various aspects of data science, replicability, and reproducibility. Tutorial `0a` provides a gentle introduction to R for those with limited programming experience, and Tutorial `0b` introduces some of the main functions in the `dplyr` and `tidyr` packages. Tutorials `1a` and `1b` get us started with exploring the two original datasets from the CCLE and GDSC studies, `rawPharmacoData.rds` and `summarizedPharmacoData.rds`. Tutorials `2a` and `2b` dig deeper into specific issues that can impact replicability and provide ideas for things to look into for this Replicathon. Finally, the Supplementary Tutorials provide more details that are useful but not immediately necessary for getting started.

* `0a` [(Rmd)](https://github.com/pkimes/PR2020replicathon/blob/master/tutorials/0a_R_basics.Rmd) [(html)](tutorials/0a_R_basics.html) : "Introduction to R Basics"

* `0b` [(Rmd)](https://github.com/pkimes/PR2020replicathon/blob/master/tutorials/0b_R_tidyverse.Rmd) [(html)](tutorials/0b_R_tidyverse.html) : "Introduction to the Tidyverse"

* `1a` [(Rmd)](https://github.com/pkimes/PR2020replicathon/blob/master/tutorials/1a_explore_rawData.Rmd) [(html)](tutorials/1a_explore_rawData.html) : "Exploring Pharmacological Data with the `rawPharmacoData` Dataset"

* `1b` [(Rmd)](https://github.com/pkimes/PR2020replicathon/blob/master/tutorials/1b_explore_summarizedData.Rmd) [(html)](tutorials/1b_explore_summarizedData.html) : "Exploring Replicability with the `summarizedPharmacoData` Dataset"

* `2a` [(Rmd)](https://github.com/pkimes/PR2020replicathon/blob/master/tutorials/2a_deeper_subgroups.Rmd) [(html)](tutorials/2a_deeper_subgroups.html) : "Digging Deeper with Cell Line and Drug Subgroups"

* `2b` [(Rmd)](https://github.com/pkimes/PR2020replicathon/blob/master/tutorials/2b_deeper_summarization.Rmd) [(html)](tutorials/2b_deeper_summarization.html) : "Digging Deeper with Drug Response Summarization"

**Supplementary Tutorials**

* `supplement` [(Rmd)](https://github.com/pkimes/PR2020replicathon/blob/master/tutorials/supplement_correlation.Rmd) [(html)](tutorials/supplement_correlation.html) : "Correlation Measures"

* `supplement` [(Rmd)](https://github.com/pkimes/PR2020replicathon/blob/master/tutorials/supplement_dose_response.Rmd) [(html)](tutorials/supplement_dose_response.html) : "Dose-Response Modeling"

* `supplement` [(Rmd)](https://github.com/pkimes/PR2020replicathon/blob/master/tutorials/supplement_PCA_clustering.Rmd) [(html)](tutorials/supplement_PCA_clustering.html) : "Exploring High Dimensional Data with PCA and Clustering"

## Code to generate data files (You do not need to use this)

For full reproducibility, this is the script to generate the `RDS` files. This step has already been done for you, and the data files should be available as part of this repository without running the script.

* [`downloadData.R`](https://github.com/pkimes/PR2020replicathon/blob/master/downloadData.R) : a script that uses the [PharmacoGx](http://bioconductor.org/packages/PharmacoGx/) package to format two datasets (raw and summary level) and save them as `RDS` files. 

## Mentors

- Luli Zou
- Ana Betty Villaseñor-Altamirano
- Kelly Street
- Mercedeh Movassagh
- Jill Lundell
- Patrick Kimes

<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vQSSj927ztwderiUqJdz-mBYKhwPxWl7F_wM6B9iu7w92LdXWWTRFG1gqNnwtzerBUrLwXfC-fB32bl/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false" width="650" height="400"></iframe>

## Useful Links

* [CCLE (Cancer Cell Line Encyclopedia) Study](https://www.ncbi.nlm.nih.gov/pubmed/22460905) from March 2012

* [GDSC (Genomics of Drug Sensitivity in Cancer) Study](https://www.ncbi.nlm.nih.gov/pubmed/22460902) from March 2012

* [Reanalysis of CCLE and GDSC](https://www.ncbi.nlm.nih.gov/pubmed/24284626) from December 2013

* [Commentary 1 on the reanalysis](https://www.ncbi.nlm.nih.gov/pubmed/27905415) from December 2016

* [Commentary 2 on the reanalysis](https://www.ncbi.nlm.nih.gov/pubmed/27905421) from December 2016

* [Commentary 3 on the reanalysis](https://www.ncbi.nlm.nih.gov/pubmed/27905419) from December 2016

* [Revisiting the reanalysis](https://www.ncbi.nlm.nih.gov/pubmed/28928933) from August 2017

## Code of Conduct

To ensure a safe, enjoyable, and friendly experience for everyone who participates, we have a strict [code of conduct](code_of_conduct.html) that all participants are expected to follow.


