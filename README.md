## NLP-Erowid

# Project Overview
In the field of cognitive sciences, understanding the subjective experiences of individuals is paramount in comprehending the effects of psychoactive drugs. Traditional approaches often focus on objective measures such as physical effects and brain activity, neglecting the rich insights available through first-hand accounts. The NLP-Erowid project seeks to bridge this gap by employing Natural Language Processing (NLP) methods on Erowid experience reports to systematically characterize the subjective effects of psychoactive drugs.

This research, led by Miranda Shen in collaboration with Sean Noah, a UC Berkeley Postdoctoral Researcher, aims to contribute to the goals of cognitive science by exploring the relationship between biological processes in the brain and psychological phenomena. By analyzing narratives shared by users, the project strives to expand our understanding of the diverse range of experiences induced by different classes of drugs, including psychedelics, stimulants, and sedatives.

# Contents
2023-11-Log-GPT-Model-Final.ipynb: This Jupyter Notebook contains reports for 25 drugs scraped from Erowid.org. The reports underwent cleaning, and UMAP was applied to the TF-IDF dataframe to create a 2-dimensional graph. K-Means clustering was then utilized to categorize drugs into six distinct clusters. The project also leveraged the GPT API to classify each report on a sentence-by-sentence level, providing distinctions between clusters, individual drugs, and their relevant subjective effects. From there, a logistic regression model was utilized to predict sentences describing subjective effects from their vector representations. The same methodology was utilized to predict positive and negative mental health outcomes from these narrative self-reports.

# Analysis

# UMAP and K-Means Clustering
Upon cleaning and TF-IDF processing, the application of UMAP and the elbow method for K-Means clustering resulted in six distinct clusters, each associated with specific classes of drugs. Here's a summary:

Cluster 1: Alcohol, Meth, Ketamine, Cocaine
Cluster 2: 5-MeO-DMT, Cannabis, Datura, Nitrous, Opiates, DPT, 2C-T-2, 2C-T-7
Cluster 3: LSD, Psilocybin, DMT
Cluster 4: MDMA, Amphetamine
Cluster 5: MDA, 5-MeO-MIPT, 5-MeO-DIPT, 2C-E
Cluster 6: Salvia, Ayahuasca, 2C-B, 25I-NBOMe
Logistic Regression and GPT-4 Language Model

A two-step process integrating logistic regression and vector embeddings was employed to identify sentences depicting subjective effects. The OpenAI GPT-4 language model API call was used to label sentences related to subjective effects, resulting in insightful findings.

<img width="635" alt="image" src="https://github.com/mirandalshen/NLP-Erowid/assets/86203932/db3d72ca-590a-4608-b0f5-752c78354a39">

Positive Mental Health Outcomes: <img width="634" alt="image" src="https://github.com/mirandalshen/NLP-Erowid/assets/86203932/4be1a10f-0806-4c0f-ac30-d699d17453f0">

Negative Mental Health Outcomes: <img width="647" alt="image" src="https://github.com/mirandalshen/NLP-Erowid/assets/86203932/745e04f3-35ef-45f8-bf5d-c3416883c8ca">

# Acknowledgments
We appreciate the support and collaboration of Earth and Fire Erowid for generously providing access to the narrative reports and engaging in discussions that greatly enriched this study.
