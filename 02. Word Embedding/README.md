<h1> Word Embedding</h1>

In Natural Language Processing, Word Embedding refers to the procces of representing each word in the form of a real valued vector. 
These vectors encode the meaning of the word such that the words that are closer in the vector space are expected to be similar in meaning. 
For example, if we produce vectors for words like <i>Queen</i>, <i>Girl</i>, <i>Boy</i> and <i>King</i>, we expect a diagram like below:
<br>
<p align="center">
<img src="https://github.com/aynzabdz/A-journey-to-NLP/blob/main/02.%20Word%20Embedding/Images/Visualizing_vectors.png"  width="400" />
</p>
This diagram is an interesting one. It shows the vertical axis has a sense of masculinity and the horizontal axis has a sense of authorization.
Also it confirms the famous equation
<p align="center"> $Queen - Girl + Boy = King$ </p>


There are two ways to get a word embedding module.
<ol>
  <li>Word2Vec</li>
  <li>GloVe</li>
</ol>

<h2>Word2Vec</h2>
This module is a thecnique for word embedding published in 2013. <a href="https://arxiv.org/abs/1301.3781">See paper</a>
<br>
This model sees the local property of each word. The main idea here is as follows: "In a huge corpus of documentation, the context words
(words close to a specific target word) have impact on its meaning." A support for this idea is that you can actually estimate the meaning of a word
which is used repeatedly in a book, using the adjacent words.
<br>
There are two wayd to train a Word2Vec Model. <b>CBoW</b> tends to estimate the target word vector using context words and <b>Skipgram</b> estimates the 
context words using target word vector. In the notebook, the word2vec model is downloaded and explored.

<h2>GloVe</h2>
GloVe stand for Global Vectors [for Word Representation]. This model sees the global property of each word. <a href="https://nlp.stanford.edu/pubs/glove.pdf">See paper</a>
<br>
It builds a co-occurence table (or simply count table) from the words in corpus. Then calculates the number
of times that words have been in each others context (i.e. they have been close) and puts the calculated numbers in the corresponding elements of table.
An interesting property of this table is that it is symmetric. This meand the number of times that <i>word_i</i> has been in context of <i>word_j</i> is 
the same as the number of times <i>word_j</i> has been in context of <i>word_i</i>. After the calculation of count table, we can actually proceed and
calculate following probability.
<p align="center"> $P(i | j) = P(word_i \: is \: in \: context \: of \: word_j) =  \frac{X_{i, j}}{X_i}$ </p>

In this equation $X$ refers to the count table and $X_i = \sum_k{X_{i, k}}$.
