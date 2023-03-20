---
title: Trends in Explainable AI (XAI) Literature
tags: Paper
abbrlink: 1906
date: 2023-03-19 21:08:54
cover:
---

1. Title: Trends in Explainable AI (XAI) Literature

2. Authors: Alon Jacovi

3. Affiliation: Bar Ilan University, Israel

4. Keywords: Explainable AI (XAI), machine learning, research trends, multidisciplinary collaboration 

5. Urls: 
- Paper: https://arxiv.org/abs/2301.05433v1 
- Github Code: https://github.com/alonjacovi/XAI-Scholar 

6. Summary: 
- (1): The article addresses the challenges of observing the whole landscape of Explainable AI (XAI) research, considering XAI as a multidisciplinary field with a decentralized terminology and publication venues. The authors aim to analyze and report the trends and features in the XAI research conducted to date.
 
- (2): The past methods are difficult to generalize owing to the multidisciplinary nature of XAI research. Current studies investigate different methods that focus on the development, implementation, and practice of AI systems' explanations and interpretations. The authors argue that there is an absence of a clear, unique terminology used to identify XAI research leading to a lack of precise and standardized terminology. The proposed approach is comprehensive and dataset-driven, which aims to present an ambitious dataset of XAI papers available to other researchers to use. 

- (3): The authors used the SemanticScholar API and manual curation to collect the XAI literature. They observed and analyzed the trends and patterns of the XAI research landscape, size, and scope of the literature, citation trends, cross-field trends, and collaboration trends. They developed a XAI-Scholar dataset which can be used as a paper discovery engine to retrieve XAI literature that is most cited according to specific constraints. 

- (4): The authors found that the XAI research collection is becoming increasingly multidisciplinary, with relative growth in papers belonging to increasingly diverse scientific fields. The authors affirmed that the dataset provided in this article will facilitate future research and provide a comprehensive understanding of the current state of XAI research.
7. Methods:

- (1): The authors conducted a keyword-based search using a set of manually derived keywords to maximize recall while maintaining near-perfect precision. The search yielded a total of 3101 papers, and only those that matched at least two keywords were collected. 

- (2): The authors also collected titles of papers from various curated XAI collections and matched them using the SemanticScholar API. This step added 766 papers to the original set, bringing the total number of papers to 3867. 

- (3): The authors expanded the search through citation tree expansion, selecting XAI papers from the 2000 most cited papers by the previously collected papers. Manual filtering was used. This step added 648 papers, bringing the total to 4515. 

- (4): The authors further expanded the search through citation tree expansion using the citations and references of all collected papers. Automatic filtering was used, and the 2-keyword-match method from step 1 was applied. This step added 709 papers, bringing the total to 5224. 

- (5): Finally, the authors conducted a manual quality check and removed 25 incorrectly-attributed papers from the collection. The resulting dataset, XAI-Scholar, is comprehensive and dataset-driven, providing a paper discovery engine for researchers to retrieve XAI literature that is most cited according to specific constraints.





8. Conclusion: 

- (1): This article is significant in providing a comprehensive dataset of Explainable AI (XAI) research and analyzing the trends and features to facilitate future research and provide a better understanding of the current state of XAI research. The authors have addressed the challenges of understanding the whole landscape of XAI research due to the multidisciplinary nature of the field and the lack of standardized terminology. 

- (2): Innovation point: The authors' approach of collecting XAI literature using a dataset-driven methodology and providing a comprehensive dataset, XAI-Scholar, is innovative and serves as a paper discovery engine for researchers. Performance: The authors have conducted a thorough analysis of the XAI research landscape, trends, and patterns. However, it could have been helpful to have additional analysis of the quality of the papers collected in XAI-Scholar. Workload: Although the authors have used both manual and automatic methods for collecting the XAI literature, the workload of manual filtering and quality check could have been time-consuming.




