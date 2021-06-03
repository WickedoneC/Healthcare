## Using NLP to Predict Drug Effectiveness

Given patient comments on treatment, can we predict the effectiveness of the treatment/drug?

### Exploring the Text

* tokenize the words
* remove stop words
* lemmatize the text

### Processing the Text

* can create a matrix with a token for each word
* can use tf-idf with CountVectorizer of TfidVectorizer

### Text Classification

* change labels to 1 and 0
* remove stop words and punctuation
* lemmatize the text
* explore word statistics and frequency plots / word clouds
* use tfidf to transform the data
* Random Forest and GradientBoost results
    * Acc: .90 and F1: .94 
    * Acc: .86 and F1: .92
    * Baseline accuracy of guessing all as Effective: .86


### Predicting on the Test Dataset

* change labels to 1 and 0
* remove stop words and punctuation
* lemmatize the text
* use tfidf to transform the data
* Random Forest and GradientBoost Test Dataset results
    * Acc: .88 and F1: .93 
    * Acc: .86 and F1: .92

### Results and Takeaways

The models predicted as equally well on the Test Dataset as they did on testing data used to evaluate the model.

In both the Training Dataset and the Testing Data, the two most common words were the same:
   * Effective: 'pain' and 'taking'
   * Non-effective: 'benefits' and 'none'
   

The 'Non-effective' class was a relatively small percentage in both datasets. Although the F1 score came back high, tuning should take into account the class imbalance.
