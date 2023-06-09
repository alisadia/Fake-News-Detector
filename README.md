# Fake-News-Detector
Fake news is a serious problem that has been on the rise in recent years. It can hurt society, leading to misinformation, distrust, and even violence. There are several different ways to detect fake news, and one of the most promising approaches is to use Deep learning.
News detection and prediction are two important aspects of news analytics. News detection involves identifying and categorizing news articles based on their topic, sentiment, source, and other relevant factors. News prediction involves forecasting future events based on the analysis of past news articles.

In this Project, We have used various natural language processing techniques and Deep learning algorithms to classify Pakistan Political news as Real or Fake and predict the probability of News being authentic shortly using Keras and TensorFlow libraries in Python.

## Problem Statement
To develop a technique through a web portal that can detect news as Fake or Real and predict the analytical part.
## Motivation
A survey conducted by the Digital Rights Foundation in 2022 that 73% of Pakistanis had encountered fake news. Misinformation has had a significant impact in Pakistan over the last four to five years, and there is currently no system in place to detect misinformation and predict the analytical part.
## Getting Started
These instructions will get a copy of the project up and running on your local machine for development and testing.
### Prerequisites
Things you need to install:

1. Python 3.10
 * This setup requires Python 3.10 to be installed on your machine. Python can be downloaded from https://www.python.org/downloads/. Once you've downloaded and installed Python, you'll need to configure PATH variables and set a virtual environment on your VS Code. 
2. You will also need to download and install the below packages after you install the python 
 * keras
 * TensorFlow
 * sklearn
 * flask
3. Xampp
 * You also need to install xampp for the database. Xampp Can be downloaded from https://www.apachefriends.org/.
## Dataset
### Detection:
Because there was no dataset of Pakistan political news, we manually collected 5k text-based datasets related to Pakistan politics from various platforms, news channels, websites, and social media. We provided a total of 5K news, of which 4K are Real and 1K are fake News. The dataset has 18 columns in total, which are as follows:
 * Column 1: The ID of news
 * Column 2: News Title
 * Column 3: News Text which contains the claims and statement of the News
 * Column 4: Published Date of news
 * Column 5: Source (channel Name) on which news was published
 * Column 6: Source URL
 * Column 7: Author of news who published
 * Column 8: Country (Pakistan)
 * Column 9: Language (English)
 * Column 10: Other Source (Another channel) which published news
 * Column 11: Other Source URL
 * Column 12: News Type (Website, Social Media)
 * Column 13: Party Affiliation to which party the news is associated
 * Column 14: Location of the speech or statement
 * Column 15: Region of the speech or statement
 * Column 16: Subject ( Categories: Cultural, Democratic, Educational, Economical, International Politics)
 * Column 17: Header Image URL (Image Related to news)
 * Column 18: Label (Label class contains: Real, Fake)
The dataset used for this project was in CSV format named Detection_Real_4k_.csv and can be found in the repo.
### Prediction:
Predicting the probability of news being authentic shortly is a challenging task, but it is becoming increasingly important. With the rise of social media and the ease with which fake news can be spread, it is more important than ever to be able to distinguish between real and fake news.

We created a dataset of 300 news questions to predict news articles and check the probability of news. For example, 
 * Will Pakistan's economy grow in 2026?
 * Who will be the next prime minister of Pakistan? 
 * Who will be the next army chief of Pakistan?
 * or Will Pakistan's sports infrastructure improve in the future?
The dataset used for this project was in CSV format named prediction_questions (1).csv and can be found in the repo.

## Tools
### Frontend
 * HTML5
 * CSS3
 * Javascript
### Backend
 * PHP 7.4
 * Python 3.10
 * Flask

 ## Software Development Methodology
 We used Scrum Methodology, and in product backlog the project features include a text box where the user entersthe newss andd two buttons detectionn and prediction where the news is detected as real or fake and the probability of the news is predicted, as well as feedback of the website .Every week a corner meeting is conducted to discuss the modules and updation of features.
 ![image](https://user-images.githubusercontent.com/129365210/234193820-4b9153ab-b120-413e-98fb-d869ca44eaca.png)

## Architecture Diagram
1. Dataset Generation
  * Data from Diversified Sources (Social Media, Websites, News Channels)
  * Data Extraction ( News Text, Date, Author, etc)
  * Labeled Corpus (Collection of text data that has been manually annotated with labels )
2. Dataset Preprocessing using NLP(Natural Language Processing)
  * Redundancy (Removing Duplicates)
  * Normalize  <br>
    Data into a consistent and meaningful format so that it can be easily processed and analyzed. 
    For Example, the sentence "Imran Khan criticized for the defense of Pakistan blasphemy laws" is normalized to " Imran Khan was criticized for defending           Pakistan's blasphemy laws" 
  * Tokenize <br>
    Breaking down a piece of text into smaller units
    For example ['Imran', 'Khan', 'criticized', 'for', 'defense', 'of', 'Pakistan', 'blasphemy', 'laws']
  * Special Characters Removal <br>
    Removing special characters from a string of text. Special characters are characters that are not letters, numbers, or spaces. They can include               punctuation marks, and symbols For example Imran Khan criticized for their defense of Pakistan's blasphemy law
  * TF-IDF <br>
    term frequency-inverse document frequency which is used to evaluate the importance of a word in a document. The term frequency is the number of times a       word appears in a document. The inverse document frequency is a measure of whether a term is common or rare in a given document corpus. Here are the TF-     IDF scores for the words in the sentence "Imran Khan criticized for the defense of Pakistan blasphemy law":
    | Word | TF | IDF | TF-IDF |
    |---|---|---|---|
    | Imran | 0.042 | 0.309 | 0.129 |
    | Khan | 0.042 | 0.309 | 0.129 |
    | criticized | 0.063 | 0.725 | 0.451 |
    | for | 0.094 | 0.518 | 0.489 |
    | defense | 0.063 | 0.649 | 0.411 |
    | of | 0.094 | 0.518 | 0.489 |
    | Pakistan | 0.042 | 0.309 | 0.129 |
    | blasphemy | 0.063 | 0.725 | 0.451 |
    | law | 0.063 | 0.649 | 0.411 |

The word "criticized" has the highest TF-IDF score because it is the most frequent word in the sentence and it also appears in a relatively small number of documents. The word "blasphemy" has the second highest TF-IDF score because it is a less common word, but it is still relevant to the topic of the sentence.<br>
3. Feature Extraction <br>
Feature extraction is a process of transforming raw data into features that can be used for machine learning. Features are typically numerical values that represent some aspect of the data.
  * Lexical analysis and Token Separation <br>
    Lexical analysis is the process of breaking down a stream of characters into tokens.Tokenization is the process of identifying and separating tokens in a     stream of characters. This is typically done using a lexical analyzer, which is a program that is specifically designed to perform lexical analysis.
    Here is the lexical analysis and token separation of the sentence "Imran Khan criticized for defense of Pakistan blasphemy law":
    | Token | Type |
    |---|---|
    | Imran | Proper noun |
    | Khan | Proper noun |
    | criticized | Verb |
    | for | Preposition |
    | defense | Noun |
    | of | Preposition |
    | Pakistan | Proper noun |
    | blasphemy | Noun |
    | law | Noun |
  * Embeddings <br>
      An embedding is a vector of numbers that represents the meaning of a word. Here is the embedding of the sentence "Imran Khan was criticized for his           defense of Pakistan's blasphemy law":
    [-0.036, -0.008007, 0.010, 0.0057,...]
4. Detection
  * RNN  (Recurrent Neural Network) <br>
    A recurrent neural network (RNN) is a type of artificial neural network that is commonly used to process sequential data. This type of neural network has a feedback loop that allows it to remember previous states, which makes it well-suited for tasks such as natural language processing and speech recognition. 
    Limitation: incapable of handling such “long-term dependencies”.
    For the RNN architecture Diagram See,https://miro.medium.com/v2/resize:fit:651/1*6xj691fPWf3S-mWUCbxSJg.jpeg
  * LSTM ( Long Short-Term Memory ) <br>
    Long short-term memory (LSTM) is a type of recurrent neural network (RNN) that is commonly used to process sequential data. LSTMs can learn long-term dependencies, which makes them well-suited for tasks such as natural language processing and speech recognition.
    Limitation: LSTMs take longer to train, and LSTMs require more memory to train.
    For the LSTM architecture Diagram See,https://databasecamp.de/wp-content/uploads/lstm-architecture-1024x709.png
  * BI-LSTM ( Bidirectional LSTM ) <br>
    A bidirectional long short-term memory (BiLSTM) is a type of RNN that can process sequences in both directions, forward and backward. This makes it well-suited for tasks such as natural language processing, where it can be used to understand the context of a word or phrase by looking at both the words that come before it and the words that come after it.
    Limitation: Since BiLSTM has double LSTM cells so it is costly, BiLSTM is a much slower model, Requires more time for training
    For the BI-LSTM architecture Diagram See,https://production-media.paperswithcode.com/methods/Screen_Shot_2020-05-25_at_8.54.27_PM.png
  * ENSEMBLE DNN
    An ensemble deep neural network (DNN) is a type of DNN that is made up of multiple individual DNNs. The individual DNNs are trained on the same dataset,     but they are trained independently of each other. The outputs of the individual DNNs are then combined to produce a single output.
    Here are some of the advantages of using an ensemble DNN:<br>
     * Improved performance: Ensemble DNNs are often able to achieve better performance than any of the individual models on their own. This is because ensemble DNNs can learn from the strengths of each model and avoid the weaknesses of each model.
     * Reduced variance: Ensemble DNNs are less likely to overfit the training data than any of the individual models on their own. This is because ensemble        DNNs can learn from the different perspectives of the individual models.
     * Increased robustness: Ensemble DNNs are more robust to noise in the training data than any of the individual models on their own. This is because ensemble DNNs can learn from the different perspectives of the individual models.
    There are many different ways to ensemble models and the one we used is: <br>
    **Stacking**: <br>
    Stacking is a technique for creating an ensemble of models where we train a meta-model to combine the predictions of multiple base models. The meta-model is trained on the predictions of the base models, and it learns how to combine these predictions to get a more accurate prediction.
    The three models RNN, LSTM, and BILSTM were independently trained on the same detection dataset and then we trained a meta-model Logistic Regression to combine the predictions of individual models which were then combined to produce a more accurate result.
5. Prediction
  * Deep Hybrid Model <br>
    A deep hybrid model is a machine learning model that combines two or more different types of machine learning algorithms. This can be done to improve the performance of the model on a particular task or to make the model more robust to changes in the data.<br>
    For predicting the probability of news, we used neural networks, word2vec, and NLP and combined these models to get more accurate results.
    * NLP (Natural Language Processing) <br>
      Natural language processing (NLP) is a field of computer science that deals with the interaction between computers and human (natural) languages, in particular, the ability of computers to understand and generate human language. <br>
      Question answering: NLP is used to answer questions about text <br>
      Text summarization: NLP is used to summarize text into a shorter, more concise version.
    * Word 2 Vector <br>
      Word2vec is a method of representing words as vectors in a high-dimensional space. These vectors are learned from a corpus of text, and they can be used to represent the meaning of words, their relationships to other words, and their usage patterns.
    * Neural Network <br>
      A neural network is a type of machine-learning algorithm that is inspired by the human brain. It is made up of a network of nodes, or neurons, that are connected. Each neuron receives input from other neurons and produces an output. The output of each neuron is then used as the input to other neurons.
  * Cosine Similarity <br>
    Cosine similarity is a measure of similarity between two non-zero vectors defined in an inner product space. Cosine similarity is the cosine of the angle between the vectors; that is, it is the dot product of the vectors divided by the product of their lengths. It follows that the cosine similarity does not depend on the magnitudes of the vectors, but only on their angle. The cosine similarity always belongs to the interval [-1, 1].<br>
    We found the probability using cosine similarity between the input question and the generated answer. Below is the formula of cosine similarity.<br>
    <center>
    Cosine Similarity = ( A . B ) / ( || A || * || B || )<br>
    </center>
    <br>
    Where:

    * A is the vector representation of the question
    * B is the vector representation of the answer
    * ||A|| is the length of the vector A
    * ||B|| is the length of the vector B


![Final Architecture Diagram-page0001](https://user-images.githubusercontent.com/129365210/234273584-e94dfb17-93cf-4673-9b3c-1ad7c272064d.jpg)




