# Machine-Learning
To categorize news articles into their respective categories, I implemented a multi-step process involving data preprocessing, model training, and evaluation. Here's a breakdown of the steps:

1. Data Loading and Preprocessing:
   - I loaded the news articles dataset from JSON files, which contained information such as headlines, articles, abstracts, and captions.
   - Text preprocessing techniques were applied to clean and tokenize the textual data. This involved removing non-alphanumeric characters, converting text to lowercase, removing stopwords, and lemmatizing the words.

2. Data Exploration:
   - I visualized the distribution of different categories (sections) within the dataset to understand the class distribution and potential class imbalances.
   - Identified the top words for each section to gain insights into the most common terms associated with each category.

3. Handling Class Imbalance:
   - Checked for class imbalances in the dataset to ensure that each category was adequately represented.
   - Applied oversampling or undersampling techniques to balance the class distribution, ensuring that the model was not biased towards dominant categories.

4. Model Training (Naive Bayes):
   - Utilized the CountVectorizer to convert text data into numerical feature vectors.
   - Trained a Multinomial Naive Bayes classifier using the transformed features to predict the category labels.

5. Model Training (BiLSTM):
   - Tokenized the preprocessed text data and performed padding to ensure uniform sequence lengths.
   - Constructed a Bidirectional LSTM model using Keras, consisting of embedding layers, bidirectional LSTM layers, and a dense output layer with softmax activation.
   - Compiled and trained the model on the padded sequences, validating the performance using a validation split.

6. Model Evaluation:
   - Evaluated the trained models using a separate testing dataset.
   - Calculated accuracy scores, generated classification reports, and visualized confusion matrices to assess the model's performance in categorizing news articles.
   
By following these steps, I successfully developed and evaluated two models for categorizing news articles into their corresponding categories. The Naive Bayes model provided a simple and efficient solution, while the Bidirectional LSTM model offered a more sophisticated approach leveraging deep learning techniques. These models can be further optimized and deployed to automate the categorization of news articles, providing valuable insights for information retrieval and analysis tasks.
