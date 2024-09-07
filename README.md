# Enriched-BC7-LitCovid
Enriched BC7-LitCovid Corpus

The [LitCovid dataset] (https://www.ncbi.nlm.nih.gov/research/coronavirus/) was established from PubMed database to collect COVID-19-related articles. The dataset is updated daily and the articles are organized into seven research topics: *treatment*, *mechanism*, *prevention*, *case report*, *diagnosis*, *transmission*, and *epidemic forecasting*. For the purpose of automatically annotating the resulting topics, the [LitCovid Track for COVID-19 literature topic annotations in BioCreative VII] (https://biocreative.bioinformatics.udel.edu/tasks/biocreative-vii/track-5/) called for a community effort. 

This challenge is actually a multi-label classification task that aims at assigning one or more topic labels to each article. In the *BC7-LitCovid* corpus released by this challenge, only titles, abstracts, keywords, journal names, PMID (PubMed Identifier), and DOI (Digital Object Identifier) are available. Though many other fields, including full texts, biological entities, and MeSH (Medical Subject Heading), are also available via PubMed/LitCovid, these fields are seldom utilized by participating teams. We argue that one of main reasons is that it is not trivial to directly retrieve these fields from PubMed/LitCovid, since many fields are actually missed due to copyright restrictions. For this purpose, the *BC7-LitCovid* corpus is enriched with the procedure in Xu et al. (2024). This novel corpus is named as enriched version of the BC7-LitCovid corpus.  
## 1. Introduction  
The official BioCreative LitCovid dataset could be found at: https://biocreative.bioinformatics.udel.edu/tasks/biocreative-vii/track-5/
## 2. Tables
The enriched BC7_LitCovid_corpus comprises the following tables: article, descriptor, journal, keyword, label, language, qualifier, article_annotation, article_descriptor, article_descriptor_qualifier, article_keyword, article_label, article_passage, descriptor_tree_number, and qualifier_tree_number

## 3. Various Fields
### 3.1 Metadata
Metadata can be found in the following tables: ```article```, ```journal```, ```keyword```, and ```article_keyword```.
### 3.2 Biological Entities
Biological entities can be found in the following table: ```article_annotation```.
### 3.3 MeSH 
MeSH can be found in the following tables: ```article_descriptor```, ```article_descriptor_qualifier```, ```descriptor```, ```descriptor_tree_number```, ```qualifier```, and ```qualifier_tree_number```.
### 3.4 Full Texts
Full texts can be found in the following tables: ```article``` and ```article_passage```.
### 3.5 Topic Labels
Topic labels can be found in the following tables: ```article_label``` and ```label```.

## 3. References
[1] Shuo Xu, Yuefu Zhang, Liang Chen, and Xin An, 2024. Is Metadata of Articles about COVID-19 enough for Multi-Label Topic Classification Task? *Database*.
[2] Shuo Xu, Yuefu Zhang, and Xin An, 2021. [Team BJUT-BJFU at BioCreative VII LitCovid Track: A Deep Learning based Method for Multi-label Topic Classification in COVID-19 Literature](https://biocreative.bioinformatics.udel.edu/media/store/files/2021/TRACK5_pos_3_BC7_submission_217.pdf). *Proceedings of teh BioCreative VII Challenge Evaluation Workshop*, pp. 275-277.
