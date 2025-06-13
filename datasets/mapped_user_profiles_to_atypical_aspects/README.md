# Dataset

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
