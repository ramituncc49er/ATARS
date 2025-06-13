# Atypical Aspect-Based Recommender System (ATARS)
This repository contains the source code and datasets for Atypical Aspect-Based Recommender System (ATARS) as described in the paper. ["Engineering Serendipity through Recommendations of Items with Atypical Aspects"](https://arxiv.org/pdf/2505.23580) currently under review at ACM Transactions on Recommender Systems.

<p align="center">
  <img src="figs/atars_interaction.png" height="250">
</p>

Hypothetical interaction with the proposed recommender system, where items with atypical aspects relevant to the user are promoted at the top of the ranking (before), in order to engineer a serendipitous experience (after).

The task of extracting atypical aspects was originally introduced in the paper ["Extraction of Atypical Aspects from Customer Reviews"](https://arxiv.org/abs/2311.02702) with the repository of the paper at [https://github.com/smitanannaware/XtrAtA](https://github.com/smitanannaware/XtrAtA).

# Datasets

## Extracted Atypical Aspects from Reviews

The datasets for manually annotated atypical aspects for restaurant, hotel, and hair salon domains available in this directory. The table below shows details of the columns in the datasets.

| Column                    | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| name                      | Business name of the item.                                                  |
| business_id               | Yelp business ID of the item.                                               |
| review                    | The user review text for the domain.                                        |
| decomposed_review         | Processed review text by Extraction Step 1.                                      |
| split_decomposed_review   | Aspect sentence from the processed review.                                  |
| manual_ata_classification | Manual annotated classification of aspect sentence, values are between <pos> & <neg>. |
| manual_ata_extractive     | Extractive annotation for atypical aspects.                                 |

## Synthetic User Profiles

The datasets for LLM generated synthetic user profiles for restaurant, hotel, and hair salon domains, available in this directory. Each dataset has a train_test and dev directory. The table below shows details of the columns in the datasets.

| Column                 | Description                                                              |
|------------------------|--------------------------------------------------------------------------|
| atypical_aspects       | List of atypical aspects integrated as personal attributes of the user profile. |
| narrative_user_profile | LLM generated user profile.                                              |

## Mapped User Profiles to Atypical Aspects

The datasets for crowdsourced annotations of user-aspect utility values for restaurant, hotel, and hair salon domains, available in this directory. The table below shows details of the columns in the datasets.

| Column                      | Description                                                                                   |
|-----------------------------|-----------------------------------------------------------------------------------------------|
| doc_id                      | ID for document, used for RAG                                                                 |
| chunk_id                    | ID for chunking, used for RAG                                                                 |
| user_profile                | Synthetic user profile                                                                        |
| name                        | Business name of the item.                                                                    |
| business_id                 | Yelp business ID of the item.                                                                 |
| reformulated_review_sentence| Aspect sentence from the processed review.                                                    |
| reformulated_review         | Processed review text by Extraction Step 1.                                                   |
| whole_review                | The user review text for the domain.                                                          |
| true_strong_weak            | Extractive primary and secondary atypical aspects are combined.                               |
| abs_true_strong_weak        | Abstractive primary and secondary atypical aspects are combined.                              |
| GroundTruthCategorical      | Crowdsourced annotation of utility value for atypical aspect with respect to user profile.    |
| A_prime                     | Combined atypical aspect with its crowdsourced annotation of utility value included for interpretability |

For any questions please contact [raditya@charlotte.edu](mailto:raditya@charlotte.edu).
