# Dataset

The datasets for manually annotated atypical aspects for restaurant, hotel, and hair salon domains available in this directory. The table below shows details of the columns in the dataset.

| Column                    | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| name                      | Business name of the item.                                                  |
| business_id               | Yelp business ID of the item.                                               |
| review                    | The user review text for the domain.                                        |
| decomposed_review         | Processed review text by Extraction Step 1.                                      |
| split_decomposed_review   | Aspect sentence from the processed review.                                  |
| manual_ata_classification | Manual annotated classification of aspect sentence, values are between <pos> & <neg>. |
| manual_ata_extractive     | Extractive annotation for atypical aspects.                                 |
