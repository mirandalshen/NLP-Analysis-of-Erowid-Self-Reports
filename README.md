# Overview: NLP-Erowid

In the field of cognitive sciences, the subjective experience of individuals has often been overlooked in favor of objective measures. However, the subjective experience holds significant potential in the study of drugs. While empirical measures such as physical effects and brain activity are commonly used to analyze drug effects, first-hand accounts of users are rarely collected or comprehensively interpreted. This gap can be addressed by systematically characterizing the subjective effects of psychoactive drugs through the use of natural language processing (NLP) methods applied to Erowid experience reports.

Understanding the subjective effects of psychoactive drugs is crucial for advancing the goals of cognitive science, which aim to explore the relationship between biological processes in the brain and psychological phenomena. Incorporating first-hand accounts of psychoactive drug experiences can provide valuable insights into the categorization and quantification of unique subjective effects. By analyzing the narratives shared by users, we can expand our understanding of the diverse range of experiences induced by different classes of drugs, including psychedelics, stimulants, and sedatives.

Overall, this research allows for the creation of a taxonomy based on quantified subjective effects to organize different types of drugs within data-driven subcategories.

This project was headed by Miranda Shen in collaboration with Sean Noah, UC Berkeley Postdoctoral Researcher.

## Contents:

- Clustering_and_Distances.ipynb: This file contains reports for 25 drugs scraped from Erowid.org. 100 reports were randomly sampled from each drug and cleaned. UMAP was applied to the term frequency-inverse document frequency (TF-IDF) dataframe from the reports and K-Means was utilized to create 6 distinct clusters. Having used the GPT API to classify each report on a sentence-by-sentence level from a list of subjective effects inspired by Effect Index, the clusters were broken down by most to least common classification to provide distinctions between clusters, individual drugs, and their relevant subjective effects.

## Analysis:

Upon cleaning the 100 randomly sampled reports and applying TF-IDF, UMAP was applied to create the 2-dimensional graph below.

![image](https://github.com/mirandalshen/NLP-Analysis-of-Erowid-Self-Reports/assets/86203932/06ae0f59-ccc8-4752-b3d8-2bec5b609e7a)

Using the elbow method to produce an optimal number of clusters, K-means was then applied to create 6 clusters of drugs.

![image](https://github.com/mirandalshen/NLP-Analysis-of-Erowid-Self-Reports/assets/86203932/7d64ff85-f786-4e40-b883-b88c940660e0)

This revealed the following:

- Cluster 1 contains the following classes: ['Alcohol' 'Meth' 'Ketamine' 'Cocaine']
- Cluster 2 contains the following classes: ['5-MeO-DMT' 'Cannabis' 'Datura' 'Nitrous' 'Opiates' 'DPT' '2C-T-2' '2C-T-7']
- Cluster 3 contains the following classes: ['LSD' 'Psilocybin' 'DMT']
- Cluster 4 contains the following classes: ['MDMA' 'Amphetamine']
- Cluster 5 contains the following classes: ['MDA' '5-MeO-MIPT' '5-MeO-DIPT' '2C-E']
- Cluster 6 contains the following classes: ['Salvia' 'Ayahuasca' '2C-B' '25I-NBOMe']

Combining the GPT API dataframe of subjective effect classifications showed how each cluster varies in subjective effects.

**Cluster 1:**
- cognitive distortion: 13.58%
- visual distortion: 12.29%
- euphoria: 10.14%
- ego dissolution: 8.68%
- cognitive enhancement: 8.67%

**Cluster 2:**
- cognitive distortion: 13.93%
- visual distortion: 12.49%
- cognitive enhancement: 9.18%
- euphoria: 9.11%
- ego dissolution: 6.00%

**Cluster 3:**
- visual distortion: 16.31%
- cognitive distortion: 12.24%
- ego dissolution: 11.90%
- insight: 9.27%
- cognitive enhancement: 6.77%

**Cluster 4:**
- cognitive enhancement: 17.35%
- euphoria: 12.96%
- cognitive distortion: 12.67%
- sociability enhancement: 10.09%
- dysphoria: 6.13%

**Cluster 5:**
- visual distortion: 13.45%
- cognitive distortion: 13.37%
- cognitive enhancement: 11.30%
- euphoria: 10.08%
- visual enhancement: 6.34%

**Cluster 6:**
- visual distortion: 12.74%
- cognitive distortion: 12.35%
- ego dissolution: 10.25%
- insight: 9.03%
- cognitive enhancement: 7.37%
