# The enriched version of BC7-LitCovid corpus
## 1. Introduction  
The [LitCovid dataset](https://www.ncbi.nlm.nih.gov/research/coronavirus/) was established from PubMed database to collect COVID-19-related articles. The dataset is updated daily and the articles are organized into seven research topics: *treatment*, *mechanism*, *prevention*, *case report*, *diagnosis*, *transmission*, and *epidemic forecasting*. For the purpose of automatically annotating the resulting topics, the [LitCovid Track for COVID-19 literature topic annotations in BioCreative VII](https://biocreative.bioinformatics.udel.edu/tasks/biocreative-vii/track-5/) called for a community effort. 

This challenge is actually a multi-label classification task (Xu et al., 2019, 2024a) that aims at assigning one or more topic labels to each article. In the *BC7-LitCovid* corpus released by this challenge, only titles, abstracts, keywords, journal names, PMID (PubMed Identifier), and DOI (Digital Object Identifier) are available. Though many other fields, including full texts, biological entities, and MeSH (Medical Subject Heading), are also available via PubMed/LitCovid, these fields are seldom utilized by participating teams (Chen et al., 2022). We argue that one of main reasons is that it is not trivial to directly retrieve these fields from PubMed/LitCovid, since many fields are actually missed due to copyright restrictions or the other reasons. For this purpose, the *BC7-LitCovid* corpus is enriched with the procedure in Xu et al. (2021, 2024b). This novel corpus is named as the enriched version of BC7-LitCovid corpus. 

## 2. Tables
The enriched version of BC7-LitCovid corpus comprises the following tables: ```article```, ```descriptor```, ```journal```, ```keyword```, ```label```, ```language```, ```qualifier```, ```article_annotation```, ```article_descriptor```, ```article_descriptor_qualifier```, ```article_keyword```, ```article_label```, ```article_passage```, ```descriptor_tree_number```, and ```qualifier_tree_number```

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

## 4. Usage
The compressed files (*bc7_lit_covid_enriched.zip.001*, *bc7_lit_covid_enriched.zip.002*, *bc7_lit_covid_enriched.zip.003*, and *bc7_lit_covid_enriched.zip.004*) are downloaded from this repository, and uncompressed to get a file named *bc7_lit_covid_enriched.sql*. Then, after a new MySQL database named *bc7_lit_covid_enriched* is created, the file *bc7_lit_covid_enriched.sql* can be directly imported into the *bc7_lit_covid_enriched* database. Thus, our enriched version of BC7-LitCovid corpus can be fully loaded into a local MySQL database. 

## 5. References
[1] Shuo Xu, Yuefu Zhang, Liang Chen, and Xin An, 2024b. Is Metadata of Articles about COVID-19 enough for Multi-Label Topic Classification Task? *Database*.

[2] Shuo Xu, Yuefu Zhang, Xin An, and Sainan Pi, 2024a. [Performance Evaluation of Seven Multi-Label Classification Methods on Real-World Patent and Publication Datasets](https://doi.org/10.2478/jdis-2024-0014). *Journal of Data and Information Science*, Vol. 9, No. 2, pp. 81-103.

[3] Qingyu Chen, Alexis Allot, Robert Leaman, Rezarta Islamaj, Jingcheng Du, Li Fang, Kai Wang, Shuo Xu, Yuefu Zhang, Parsa Bagherzadeh, Sabine Bergler, Aakash Bhatnagar, Nidhir Bhavsar, Yung-Chun Chang, Sheng-Jie Lin, Wentai Tang, Hongtong Zhang, Ilija Tavchioski, Senja Pollak, Shubo Tian, Jinfeng Zhang, Yulia Otmakhova, Antonio Jimeno Yepes, Hang Dong, Honghan Wu, Richard Dufour, Yanis Labrak, Niladri Chatterjee, Kushagri Tandon, Fréjus A. A. Laleye, Loïc Rakotoson, Emmanuele Chersoni, Jinghang Gu, Annemarie Friedrich, Subhash Chandra Pujari, Mariia Chizhikova, Naveen Sivadasan, Saipradeep VG, and Zhiyong Lu, 2022. [Multi-Label Classification for Biomedical Literature: An Overview of the BioCreative VII LitCovid Track for COVID-19 Literature Topic Annotations](https://doi.org/10.1093/database/baac069). *Database*, Vol. 2022, pp. baac069.

[4] Shuo Xu, Yuefu Zhang, and Xin An, 2021. [Team BJUT-BJFU at BioCreative VII LitCovid Track: A Deep Learning based Method for Multi-label Topic Classification in COVID-19 Literature](https://biocreative.bioinformatics.udel.edu/media/store/files/2021/TRACK5_pos_3_BC7_submission_217.pdf). *Proceedings of the BioCreative VII Challenge Evaluation Workshop*, pp. 275-277.

[5] Shuo Xu and Xin An, 2019. [ML<sup>2</sup>S-SVM: Multi-Label Least-Squares Support Vector Machine Classifiers](https://doi.org/10.1108/EL-09-2019-0207). *The Electronic Library*, Vol. 37, No. 6, pp. 1040-1058.