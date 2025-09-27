# Election-prediction-using-sentimental-analysis

### Details:
Scrapes tweets related to political parties (BJP, Congress).
Cleans raw tweet text (removes stopwords, punctuation, emojis).
Uses NLTK for tokenization and TextBlob for sentiment analysis, generating polarity and subjectivity scores.
Labels tweets as positive (1) or negative (0) based on polarity.
Saves processed datasets for use in model training.

## 2. Model1-GloVe.ipynb

### Purpose: 
Build and evaluate a sentiment classification model using GloVe embeddings and a simple architecture.

### Details:
Loads processed data.
Uses pre-trained GloVe word vectors for embedding tweets.
Trains a neural network (using Keras/TensorFlow) for sentiment classification.
Evaluates model accuracy and loss.

## 3. Model2-LSTM.ipynb

### Purpose: 
Build and evaluate a more advanced Bi-Directional LSTM model for sentiment classification.

### Details:
Loads and preprocesses tweet data.
Uses GloVe embeddings.
Builds a Bidirectional LSTM network in Keras for improved sequence understanding.
Trains and evaluates the model (reports validation loss and accuracy, e.g., ~97% accuracy).
Saves the trained model and weights for testing.

## 4. testing.ipynb

### Purpose: 
Load the best-performing model and test it on new (unseen) tweet data.

### Details:
Loads previously saved model architecture and weights.
Processes new tweet datasets for BJP and Congress (using the same pipeline).
Predicts sentiment (positive/negative) on new tweets.
Outputs the number of positive tweets for each party as a proxy for public sentiment/potential election outcome.

## How to Run

miniproj3.ipynb: Run notebook to preprocess data.

Model1-GloVe.ipynb & Model2-LSTM.ipynb: Train and evaluate models. Compare performance.

testing.ipynb: Use the best model (from Model2-LSTM by default) to predict sentiment on fresh data.



