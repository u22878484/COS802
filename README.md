# COS802 Project - eCommerce Text Classification

## Project Objective
- To develop an efficient and starighforward classification model with the term frequency-inverse document frequency (TF-IDF and Word2Vec algorithms)
- To use the techniques and findings from this project for application to South African eCommerce data, thereby gaining insights into the South African consumer sprend trend market.

## Data
Original source: https://doi.org/10.5281/zenodo.3355823

The data file 'ecommerceDataset.csv is text data from an Indian e-commerce platform.

## Data Pre-processing
Category frequencies, character and word counts and average word length analysis was performed on the dataset.

Text normalization techniques employed on the data included:
- Lowercase conversion.
- Whitespace, punctuation and Unicode character removal.
- Substitution of contractoin words.
- Stop word removal.
- Substitution of acronyms.

## Text Vectorization
**TF-IDF** - is a method that solves the challange with Bag-of-Words(BoW) approach where no specific preference is given to words regardless of theors frequency in the sentence or document. TF-IDF scores words in relation to ts usage or frequency and thus can highlight the word's relevance in the document.

**Word2Vec** - This algorithm differs from TF-IDF in that it is able to identify the context of a word in relation to other words, It is achieved via two methods: Skip-Gram and Continuous Bag of Words (CBOW).

## Classification
Three classifiers were used specifically, with the highest performing model (In terms of F1-score) being chosen to perform the final classification of the test subset. The chosen classification models are XGBoost, Linear SVM and Random Forest.

## Result
Based on the Validation F1-scores, the pretrained Google News Word2Vec model + XGBoost classifier produced the best result. This was then applied to the Test subset to produce a final F1-score of **0.940309**.

## Expansion and Future Work
In addition to apply such techniques and models to South African data, specific extensions of this project will include:
- A next transaction predictor, based on transaction dates, amounts, description and categories.
- Proactive fraud prevention.
- Loyalty and rewards incentives based on consumer spend behaviour.
- Life-stage trigger modelling - E.g. Proposing forex to clients if international air tickets are purchased or the option of car and household cover if a vehicle finance or home loan transaction is identified.
