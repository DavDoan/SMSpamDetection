# SMSpamDetection

Dependencies: Libraries utilized are mentioned at the beginning of the SMSpamDetect.ipynb file.

This project utilizes the dataset gathered by UC Irvine's Machine Learning Repository (available through a Creative Commons Attribution 4.0 International license) and analyzes the data from both a supervised and unsupervised machine learning perspective. 

Naive-Bayes was the supervised algorithm used to classify SMS messages and a K-Means clustering technique was the unsupervised method used. First, the extracted data was normalized by removing stopwords and stemming them. With this, I used Term Frequency-Inverse Document Frequency (TF-IDF) to weigh and vectorized each of these words based on their appearance rate in spam and ham messages. With these weighted vectors, I ran the data through several Naive-Bayes algorithms and discovered Bernoulli's algorithm was the most accurate, reaching 98.549% accuracy. 

I also used a K-Nearest Neighbor (K-NN) algorithm as an alternative supervised model. After the model was trained on the vectorized training data, the algorithm determined which spam or ham datapoint was closest to the inputted testing data, calculated using a Minkowski metric. The training data is then labeled as spam or ham depending on the closest training datapoints. The accuracy of the K-NN algorithm was also high, reaching 95.164%. 

In the unsupervised approach, I reduced the dimensionality of the vectors using principal component analysis (PCA) which still retains the important patterns and relationships in the vectorized data. With this, I was able to use the K-Means model to separate the data into two different clusters, each representing ham or spam. Under this model, inputted messages would be classified based on their proximity to either the ham or spam cluster, and the accuracy reached 90.135%. While the accuracy provided by the K-Means model was less accurate than Bernoulli's Naive-Bayes algorithm, the accuracy is still high for an unsupervised algorithm.

Post-Analysis: Overall, the Naive-Bayes and K-NN algorithms performed better than K-Means due to their nature as supervised machine learning algorithms, meaning the algorithms will perform better on trained SMS message data. On the other hand, I expect the unsupervised K-Means model to perform better on other kinds of spam data, like email or social media spam. 

A more detailed write-up is provided throughout the SMSpamDetect.ipynb file.
