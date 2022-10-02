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
The first step of this algorithm is cleaning the documents within a corpus. This is done in 4 major steps.
<ol>
  <li> Converting all characters to lower case. </li>
  <li> Removing punctuation.</li>
  <li> Stemming, i.e process of reducing inflected words to their root form. </li>
  <li> Removing <emph>Stopwords</emph>. Stopwords are a set of commonly used words in a language. </li>
</ol>

<h3> Creating Feature Matrix </h3>
After each document has been cleaned, we will need a neat dataset to train any ML model. a simple idea to obtain a dataset from documents is as follows.
<ol>
  <li> Extract a vocabulary list, Containing of each unique word in the corpus </li>
  <li> Create a matrix with rows corresponding to documents and columns corresponding to extracted vocabulary.</li>
  <li> The <i>(i, j)th</i> element of this matrix is set to $TF-IDF(i, j)$. Which is defined as below:</li>
  <br>
  $TF-IDF(i, j) = TF(d_i^j) \times IDF(d_i^j)$
  <br>
  <br>
  $TF(d_i^j) = \frac{Frequency \: of \: jth \: word \: of \: ith \: document}{Total \: number \: of \: words \: in \: ith \: document}$
  <br>
  <br>
  $IDF(d_i^j) = log (\frac{Total \: number \: of \: documents \: in \: the \: corpus}{Number \: of \: documents \: which \: contain \: jth \: word \: of \: ith \: document})$
  
  </ol>
 After this step, we will have a neat dataset with numeric features and binary labels. Now we can use any machine learning model we want, to classify this data =)

<h3> Classifying </h3>
  In this code, i used two different models, <b>Random Forest Classifier</b> and <b>Naive Bayes Classifier</b>. The result of training this two models is showed in the notebook. You can also try giving manual reviews and ask each of two models to classify the type of given review.


<h2> Resources </h2>
[1] Dimitrios Kotzias, Misha Denil, Nando de Freitas, and Padhraic Smyth.
From group to individual labels using deep features. In Proceedings of
the 21th ACM SIGKDD International Conference on Knowledge Dis-
covery and Data Mining, KDD ’15, page 597–606, New York, NY, USA,
2015. Association for Computing Machinery.
