# Project Goal
- Using <b>classification model</b> help people to distinguish tweets are reliable or not.  
- In nowadays, tweets information spread very fast and sometimes it even faster than news. However, not like journalist posts a news need a supervisor’s agreement. when people post tweets, they don’t think too much, or check is it a reliable source or not. They just re-tweet what they saw even it is fake news.
Therefore, the fake news would propagate very fast and people will hard tell which is reliable news which is not.

# Methods
- <b>Machine Learning Models</b> (Logistic Regression, SVM)  

1. Vectorize each tweet using <b>Tfidf</b>.  
2. Build <b>Logistic Regression</b> and <b>SVM</b> to classify tweets and get preliminary accuracy rate.  
3. Use <b>NLTK</b> module to paraphrase and expand tweets amount 5 times. And use <b>POS</b> for each word's part of speech and check <b>synonyms</b> exist or not. If there has synonyms words, then randomly choose words to build new sentences.  
4. Build new Logistic Regression and SVM models to check accuracy rate. Logistic Regression enhances from 81.2% to <b>83.9%</b> and SVM raises from 82% to <b>91%</b>.  
5. Build a <b>pipeline</b> in SVM model to automate words vectorization and classify reliable/unreliable tweets to estimate classification accuracy.  

- <b>CNN Model</b>

1. Use Keras Tokenizer to vetorize these tweets samples into a 2D integer tensor using Keras Tokenizer.  
2. Initial padding of 0s, until vector's size is MAX_SEQUENCE_LENGTH.  
3. split the training data into a training set and a validation set.    
4. Embedding each tweet to vector using 'glove.6B.100d.txt' (source: https://nlp.stanford.edu/projects/glove/).  
5. Run 3 times <b>convilution and subsampling</b> (Feature Maps). (Filter size = 5; maxpooling size = 5)  
6. Training accuracy is 92.35%; Testing accuracy is 73.21%.  
7. After expanding dataset, training accuracy is 96.74%; testing accuracy is 78.3%.  

# Result
Our model's accuracy rate enhance a little after we paraphrase our tweets. However, both models' accuracy rate doesn't enhance big. The reason may because of paraphrasing sentences
features too similar with original sentences, so the training model can't get great improve on prediction. In the future, we may want to try another paraphrase method to enhance
accuracy rate. Try to paraphrase the sentence using different sturcture because our method get same sentence structure and only change the vocabulary. If we can change to different
sentence structure, it might get better result.

# Poster
![poster](https://user-images.githubusercontent.com/67025904/134560543-6999d371-7f92-402f-b3b3-826a6d18903c.jpg)
