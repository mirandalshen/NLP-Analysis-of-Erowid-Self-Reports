# Overview: NLP-Erowid

In the field of cognitive sciences, the subjective experience of individuals has often been overlooked in favor of objective measures. However, the subjective experience holds significant potential in the study of drugs. While empirical measures such as physical effects and brain activity are commonly used to analyze drug effects, first-hand accounts of users are rarely collected or comprehensively interpreted. This gap can be addressed by systematically characterizing the subjective effects of psychoactive drugs through the use of natural language processing (NLP) methods applied to Erowid experience reports.

Understanding the subjective effects of psychoactive drugs is crucial for advancing the goals of cognitive science, which aim to explore the relationship between biological processes in the brain and psychological phenomena. Incorporating first-hand accounts of psychoactive drug experiences can provide valuable insights into the categorization and quantification of unique subjective effects. By analyzing the narratives shared by users, we can expand our understanding of the diverse range of experiences induced by different classes of drugs, including psychedelics, stimulants, and sedatives.

Overall, this research allows for the creation of a taxonomy based on quantified subjective effects to organize different types of drugs within data-driven subcategories.

This project was headed by Miranda Shen in collaboration with Sean Noah, UC Berkeley Postdoctoral Researcher.

## Contents:

- Clustering_and_Distances.ipynb: This file contains reports for 25 drugs scraped from Erowid.org. 100 reports were randomly sampled from each drug and cleaned. UMAP was applied to the term frequency-inverse document frequency (TF-IDF) dataframe from the reports and K-Means was utilized to create 6 distinct clusters. Having used the GPT API to classify each report on a sentence-by-sentence level from a list of subjective effects inspired by Effect Index, the clusters were broken down by most to least common classification to provide distinctions between clusters, individual drugs, and their relevant subjective effects.

## Analysis:

Upon cleaning the 100 randomly sampled reports and applying TF-IDF, UMAP was applied to create the 2-dimensional graph below.

<img width="635" alt="image" src="https://github.com/mirandalshen/NLP-Erowid/assets/86203932/db3d72ca-590a-4608-b0f5-752c78354a39">

Using the elbow method to produce an optimal number of clusters, K-means was then applied to create 6 clusters of drugs.

This revealed the following:

- Cluster 1 contains the following classes: ['Alcohol' 'Meth' 'Ketamine' 'Cocaine']
- Cluster 2 contains the following classes: ['5-MeO-DMT' 'Cannabis' 'Datura' 'Nitrous' 'Opiates' 'DPT' '2C-T-2' '2C-T-7']
- Cluster 3 contains the following classes: ['LSD' 'Psilocybin' 'DMT']
- Cluster 4 contains the following classes: ['MDMA' 'Amphetamine']
- Cluster 5 contains the following classes: ['MDA' '5-MeO-MIPT' '5-MeO-DIPT' '2C-E']
- Cluster 6 contains the following classes: ['Salvia' 'Ayahuasca' '2C-B' '25I-NBOMe']

We utilized a two-step process integrating logistic regression and vector embeddings. First, we created the logistic regression model designed to identify sentences that depict subjective effects by utilizing vector embeddings. Then, we employed an OpenAI GPT-4 language model API call for each sentence, specifically designed to label sentences related to subjective effects. This model resulted in the following findings.

<img width="624" alt="image" src="https://github.com/mirandalshen/NLP-Erowid/assets/86203932/d13776b3-123a-4a68-bf7a-731327890fdc">

## Findings:

From there, we performed an OpenAI GPT-4 language model API call for each sentence to label subjective effect sentences by categories inspired by the Effect Index. Below, we display the rates of different categories of subjective effect sentences across psychoactive drugs as a heatmap.

<img width="653" alt="image" src="https://github.com/mirandalshen/NLP-Erowid/assets/86203932/7fff2d7d-7d87-4857-8674-e020369ceac1">

This analysis has been extended to analyze correlations between common mental health outcomes and substance use, as seen in the two figures below.

Positive mental health outcomes:

<img width="634" alt="image" src="https://github.com/mirandalshen/NLP-Erowid/assets/86203932/4be1a10f-0806-4c0f-ac30-d699d17453f0">

Negative mental health outcomes:

<img width="647" alt="image" src="https://github.com/mirandalshen/NLP-Erowid/assets/86203932/745e04f3-35ef-45f8-bf5d-c3416883c8ca">
