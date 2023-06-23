# Overview: NLP-Analysis-of-Erowid-Self-Reports

In the field of cognitive sciences, the subjective experience of individuals has often been overlooked in favor of objective measures. However, the subjective experience holds significant potential in the study of drugs. While empirical measures such as physical effects and brain activity are commonly used to analyze drug effects, first-hand accounts of users are rarely collected or comprehensively interpreted. This gap can be addressed by systematically characterizing the subjective effects of psychoactive drugs through the use of natural language processing (NLP) methods applied to Erowid experience reports.

Understanding the subjective effects of psychoactive drugs is crucial for advancing the goals of cognitive science, which aim to explore the relationship between biological processes in the brain and psychological phenomena. Incorporating first-hand accounts of psychoactive drug experiences can provide valuable insights into the categorization and quantification of unique subjective effects. By analyzing the narratives shared by users, we can expand our understanding of the diverse range of experiences induced by different classes of drugs, including psychedelics, stimulants, and sedatives.

Overall, this research allows for the creation of a taxonomy based on quantified subjective effects to organize different types of drugs within data-driven subcategories.

This project was headed by Miranda Shen in collaboration with Sean Noah, UC Berkeley Postdoctoral Researcher.

## Contents:

- Clustering_and_Distances.ipynb: This file contains reports for 25 drugs scraped from Erowid.org. 100 reports were randomly sampled from each drug and cleaned. UMAP was applied to the TF-IDF dataframe from the reports and K-Means was utilized to create 6 distinct clusters. Having used the GPT API to classify each report on a sentence-by-sentence level from a list of subjective effects inspired by Effect Index, the clusters were broken down by most to least common classification to provide distinctions between clusters, individual drugs, and their relevant subjective effects.
