# NLP-Sentiment-Analysis-Topic-Modelling
-----------------------------------------------------------------------------------------------------------------------------------------------------

## Project Overview
This project conducts an in-depth analysis of customer reviews for McDonald's fast food restaurants in the United States. The goal is to identify and understand the main issues related to their service using advanced NLP techniques.

## Techniques Used
1. **Sentiment Analysis**: Using Recurrent Neural Networks (RNN) and Long Short-Term Memory (LSTM) models
2. **Topic Modeling**: Using Latent Dirichlet Allocation (LDA)

## Usage
To use this project, follow these steps:
1. Upload the dataset 'McDonald_s_Reviews.csv'.
2. Run 'sentimentAnalysis.ipynb' it will create a 'pred_negative_reviews.csv' that we use for topic modelling.
3. Upload 'pred_negative_reviews.csv' i.e. the csv file containing the negative reviews predicted by the LSTM model. 
4. Run 'LDA.ipynb' 
**Note:** If you run "sentimentAnalysis.ipynb" the file "pred_negative_reviews.csv" will be overwrited, so it may cause slightly different results.

## Dataset
- Over 33,000 anonymized Google reviews of McDonald's stores in the United States 
- Focused on review content and ratings

## Methodology

### 1. Data Pre-processing
- Normalization
- Tokenization
- Lemmatization
- Stopwords Removal

### 2. Sentiment Analysis
- Conversion of ratings to numeric values
- Sentiment classification (positive, neutral, negative)
- Tokenization and sequence padding
- Data splitting into training and test sets
- Model comparison: RNN vs LSTM

### 3. Topic Modeling
- Focus on negative reviews identified by sentiment analysis
- POS Tagging
- Noun and Adjective Filtering
- Frequent and Rare Terms Removal
- LDA model with 3 topics

## Results

### Sentiment Analysis
- Both RNN and LSTM models struggled with neutral sentiments
- LSTM showed superior performance overall
- Performance metrics:

  | Model | Accuracy | Precision | Recall | F1 score |
  |-------|----------|-----------|--------|----------|
  | RNN   | 70.28%   | 0.74      | 0.70   | 0.68     |
  | LSTM  | 80.11%   | 0.81      | 0.80   | 0.77     |

### Topic Modeling
Three main topics identified in negative reviews:
1. Waiting Time (44.2% of tokens)
2. Location and Food Quality (30% of tokens)
3. Staff (26% of tokens)

## Conclusions
This analysis provides valuable insights into customer experiences at McDonald's, highlighting key areas of concern:
1. Long waiting times, especially at drive-throughs
2. Issues with food quality and restaurant cleanliness
3. Staff behavior and service quality

These findings can guide McDonald's in improving their service quality and enhancing customer satisfaction.

## References
1. Bengio, Y., Goodfellow, I., & Courville, A. (2017). Deep learning (Vol. 1). MIT press Cambridge, MA, USA.
2. Blei, D. M., Ng, A. Y., & Jordan, M. I. (2003). Latent dirichlet allocation. Journal of machine Learning research, 3(Jan), 993-1022.
