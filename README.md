
# 🏡 Airbnb Property Unlisting Prediction (Text Mining Project)

Academic group project for the **Text Mining (2023/24)** course, part of the Master’s in **Data Science and Advanced Analytics**.  
The goal was to apply **Natural Language Processing (NLP)** to predict whether an Airbnb property will be **unlisted in the next quarter**, using textual data from descriptions, host profiles, and guest reviews.

## Objectives
- **Binary Classification** – Predict if a property will be unlisted (1) or remain listed (0).  
- Explore the predictive power of different text sources: *description*, *host_about*, *reviews*.  
- Compare classical ML models with deep learning and transformer-based approaches.  

## Dataset
- **Train set**: 6,248 properties  
- **Reviews**: 361,281 guest comments (multi-language, later translated to English)  
- **Test set**: 695 properties (evaluation set, no target provided)  
- **Test reviews**: 41,866 guest comments  

Main features: property description, host description, reviews, insurance code, diagnosis, admission details, etc.

## Preprocessing
- Language detection + translation of all text to English  
- Text cleaning, Stopword removal, stemming and lemmatization  
- Merge of property/host dataset with reviews
- Train/validation split with **stratified sampling**  

## 🛠Feature Engineering
- **Bag of Words (BoW)**  
- **TF-IDF (1-gram and n-grams up to 3)**  
- **BERT Tokenizer** for transformer-based models  

## Models Tested
- **Classical ML**: Logistic Regression, K-Nearest Neighbors (KNN)  
- **Neural networks**: Multi-Layer Perceptron (MLP)  
- **Deep learning**: Long Short-Term Memory (LSTM)  
- **Transformers**: BERT-based architectures  

Hyperparameter tuning with **RandomizedSearchCV**.  
Evaluation metrics: **Accuracy, Precision, Recall, Weighted F1-Score**.

## Results
- Best overall model → **Logistic Regression with TF-IDF (1-Gram)**  

## Learnings
- **Preprocessing multilingual data** was critical (translation to English improved performance).  
- **TF-IDF (1-gram)** was surprisingly strong, outperforming more complex setups.  
- Logistic Regression + TF-IDF offered the best trade-off between performance and interpretability.  
- Future improvements: train LSTM/Transformers for more epochs, include sentiment analysis and topic modeling.

## Team
Group 19 – Text Mining 2023/24
