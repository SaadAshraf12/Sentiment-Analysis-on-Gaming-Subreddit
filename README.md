# Sentiment-Analysis-on-Gaming-Subreddit
This Jupyter Notebook performs sentiment analysis on Reddit data using BERT embeddings and a Random Forest classifier. It includes data preprocessing, feature extraction, and visualization of sentiment distribution and model performance through confusion matrices.

The Jupyter Notebook implements a comprehensive sentiment analysis pipeline that includes multiple phases involving data collection, preprocessing, feature extraction, and classification. Here’s a detailed summary:

1. **Reddit Data Collection**:
   - Reddit submissions are scraped, and data is saved to a CSV file for further processing. This dataset comprises user comments and headlines, which form the basis for sentiment analysis.

2. **Text Preprocessing**:
   - Text from Reddit data is cleaned by removing unnecessary elements such as URLs, user mentions, hashtags, punctuation, and converting it to lowercase. Tokenization is performed, and common stopwords are filtered out. The cleaned data is stored in a new CSV file.

3. **Topic Modeling with LDA**:
   - Latent Dirichlet Allocation (LDA) is employed for topic modeling, extracting latent themes from the cleaned text.

4. **Feature Extraction**:
   - The notebook employs **BERT** models for feature extraction, generating text embeddings. These embeddings are used for sentiment analysis. Specifically, the `nlptown/bert-base-multilingual-uncased-sentiment` model is applied for sentiment classification, predicting sentiments (positive, neutral, negative) for the Reddit data.
   - These BERT-based embeddings are saved into a new dataset (`embedding_reddit_data.csv`), which contains both headline and comment sentiments.

5. **Sentiment Classification**:
   - A **Random Forest Classifier** is trained on the BERT-based embeddings to classify sentiments. Both comments and headlines undergo classification into categories like "negative," "neutral," and "positive."
   
6. **Confusion Matrix and Distribution Plots**:
   - To evaluate the performance of the classifier, a **confusion matrix** is plotted, showing how well the model has predicted the sentiments.
   - The distribution of sentiment predictions is also visualized using bar plots for both headline and comment sentiments, giving insights into the frequency of each sentiment class.

7. **Evaluation and Testing**:
   - The Random Forest model is tested, and predictions are compared against the true labels, followed by confusion matrix analysis and sentiment distribution evaluation.

This notebook builds a sophisticated sentiment analysis pipeline that leverages BERT embeddings and machine learning models for accurate classification of sentiment within the Reddit data.


**CONFUSION MATRIX**
![image](https://github.com/user-attachments/assets/f859be83-80d3-4dc1-accd-fe711766a4b9)


**DISTRIBUTION OF HEADLINE SENTIMENT**
![image](https://github.com/user-attachments/assets/1aaec1b7-ea82-410e-8c12-e0fdf67ff485)


**DISTRIBUTION OF COMMENTS SENTIMENT**
![image](https://github.com/user-attachments/assets/856d05e8-29f2-4746-adf1-bbb681d2aa7a)


**Visualiztion Of Top 25 Most Common Words For Both Positive And Negative Sentiments in Dataset**
![image](https://github.com/user-attachments/assets/6104565f-5511-4a63-9131-c3f7f39cbd33)
![image](https://github.com/user-attachments/assets/8bc6a6b0-af17-4927-9559-d995cdbc2860)


**Correlation Heatmap Of Top 10 Most impactful words of both positive and negative sentiment with impact score**
![image](https://github.com/user-attachments/assets/583e2a27-b860-4d5f-b3af-35bd773e31c1)



