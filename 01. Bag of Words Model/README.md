<h1> Sentiment Analysis of Reviews </h1>

This is my attempt to train a BoW model. In this model, we will use <a href="https://www.kaggle.com/marklvl/sentiment-labelled-sentences-data-set">Sentiment Labelled Sentences Data Set</a>
from <a href="https://www.kaggle.com/">Kaggle</a>.
<br>

<h2> Built With </h2>
<ul>
  <li> JupyterLab </li>
  <li> Python3 </li>
  <li> NumPy </li>
  <li> Pandas </li>
  <li> nltk </li>
  <li> Scikit Learn </li>
</ul>

<h2> Bag of Words Model </h2>

The BoW model is one of the simplest NLP models, which is really easy to implement and works well with document classification.
<br>
<br>
A major challenge with raw texts is that ML algorithms can not work with them directly. They need a vector of numbers for each record. Converting human language to a computer interpretable form is a hard task.
<br>
<br>
<h3> Cleaning Data </h3>
The first step of this algorithm is cleaning the documents within a corpus. This is done in 5 major steps.
<ol>
  <li> Converting all characters to lower case </li>
  <li> Removing any possible link </li>
  <li> Removing punctuation</li>
  <li> Stemming, i.e process of reducing inflected words to their root form </li>
  <li> Removing <emph>Stopwords</emph>. Stop words are a set of commonly used words in a language. </li>
</ol>

<h3> Creating Feature Matrix </h3>
After each document has been cleaned, we will need a neat dataset to train any ML model. a simple idea to obtain a dataset from documents is as follows.
<ol>
  <li> Extract a vocabulary list. Containing of each unique word in the corpus </li>
  <li> Create a matrix with rows corresponding to documents and columns corresponding to extracted vocabulary. The <i>(i, j)th</i> element of this matrix is set to one if and only if the <i>ith</i> document of corpus contain the <i>jth</i> word of vocabulary.</li>
  <br>
  After this step, we will have a neat dataset with binary features and binary labels. Now we can use any machine language model we want, to classify this data =).
  <br>
  <br>
  In this code, i used to different models, <b>Random Forest Classifier</b> and <b>Naive Bayes Classifier</b>. The result of training this two models is showed in the notebook. You can also try giving manual reviews and ask each of two models to classify the type of given review.
</ol>


<h2> Resources </h2>
[1] Dimitrios Kotzias, Misha Denil, Nando de Freitas, and Padhraic Smyth.
From group to individual labels using deep features. In Proceedings of
the 21th ACM SIGKDD International Conference on Knowledge Dis-
covery and Data Mining, KDD ’15, page 597–606, New York, NY, USA,
2015. Association for Computing Machinery.
