# Forum Discussion Classification

This project was done for our neural network course. The goal is to classify text into five categories using deep learning models and a transformer. NLP techniques were applied to clean and preprocess the text data before training the models.

## 1. Data Overview

### 1.1 Loading the Dataset
The dataset consists of two columns:
- **Discussion**: The text of the discussion.
- **Category**: The label representing the category of the discussion.

### 1.2 Category Distribution
We visualize the distribution of categories in the training dataset using a bar plot. This helps us ensure no category is undersampled or oversampled.

### 1.3 Missing Values
We check for missing values in the training and testing datasets and we fill the missing values in the **Discussion** column with empty strings.

## 2. Preprocessing

### 2.1 Remove Duplicates
Duplicate entries in the **Discussion** column are removed from the training dataset.

### 2.2 Drop Unnecessary Columns
We drop the **SampleID** column from the training dataset because it does not contribute to model training.

### 2.3 Text Preprocessing
Several text cleaning and preprocessing techniques are applied to ensure the data is ready for deep learning models:

- #### Contraction Expansion

- #### Removing URLs, Emails, and Mentions

- #### Removing Extra Whitespaces

- #### Removing Non-Alphanumeric Characters

- #### Normalizing Repeated Characters

- #### Lemmatization

- #### Stopwords Removal


### 2.4 Encoding Labels

### 2.5 Train-Test Split
We split the dataset into training and testing sets:
- 80% of the data is used for training.
- 20% is used for testing.

## 3. Tokenization and Embedding

After preprocessing the text, we used a **tokenizer** to tokenize the discussions.

For the word embeddings, we experimented with three pretrained embeddings:
1. **FastText**
2. **Word2Vec**
3. **GloVe**

Among these, **GloVe** performed the best and was selected for the final model training. 

## 4. Models

We trained and evaluated the following models:

1. **Simple RNN**
2. **RNN using LSTM**
3. **CNN**
4. **Transformer**

<p align="center">
  <strong>The performance results for each model:</strong>
</p>

<div align="center">

| Model                | Training Accuracy | Validation Accuracy |
|----------------------|-------------------|---------------------|
| Simple RNN           | 0.7044            | 0.7006              |
| RNN using LSTM       | 0.7225            | 0.7234              |
| CNN                  | 0.7191            | 0.7233              |
| Transformer          | 0.7126            | 0.7139              |

</div>


## Team Members:
 
- [@SalmaNasrEldin](https://github.com/SalmaNasrEldin)
- [@marwa-ehab](https://github.com/marwa-ehab)
- [@SmaherNabil](https://github.com/SmaherNabil)
- [@zeinabsakran77](https://github.com/zeinabsakran77)
- [@sa10ma](https://github.com/sa10ma)

## Thank You

We have put a lot of effort into this project, and this [report](https://github.com/monaya37/Forums/blob/5ea3419166a2de0a95cac1a3ea56fc4c2abe269e/Neural%20Networks%20Project%20Documentation.pdf) summarizes the details of the work we have done. We would like to sincerely thank **TA Yomna Ahmed** for her support throughout this course. We reached out to her with countless questions, and she was always there to help us.




