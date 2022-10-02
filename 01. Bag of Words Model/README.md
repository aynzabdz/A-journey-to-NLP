<h2> Bag of words model </h2>

This is my attempt to train a BoW model. In this model, we will use <a href="https://www.kaggle.com/marklvl/sentiment-labelled-sentences-data-set">Sentiment Labelled Sentences Data Set</a>
from <a href="https://www.kaggle.com/">Kaggle</a>.


<h2> Resources </h2>
@inproceedings{10.1145/2783258.2783380,
author = {Kotzias, Dimitrios and Denil, Misha and de Freitas, Nando and Smyth, Padhraic},
title = {From Group to Individual Labels Using Deep Features},
year = {2015},
isbn = {9781450336642},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/2783258.2783380},
doi = {10.1145/2783258.2783380},
abstract = {In many classification problems labels are relatively scarce. One context in which this occurs is where we have labels for groups of instances but not for the instances themselves, as in multi-instance learning. Past work on this problem has typically focused on learning classifiers to make predictions at the group level. In this paper we focus on the problem of learning classifiers to make predictions at the instance level. To achieve this we propose a new objective function that encourages smoothness of inferred instance-level labels based on instance-level similarity, while at the same time respecting group-level label constraints. We apply this approach to the problem of predicting labels for sentences given labels for reviews, using a convolutional neural network to infer sentence similarity. The approach is evaluated using three large review data sets from IMDB, Yelp, and Amazon, and we demonstrate the proposed approach is both accurate and scalable compared to various alternatives.},
booktitle = {Proceedings of the 21th ACM SIGKDD International Conference on Knowledge Discovery and Data Mining},
pages = {597–606},
numpages = {10},
keywords = {multi-instance learning, unsupervised learning, sentiment analysis, deep learning},
location = {Sydney, NSW, Australia},
series = {KDD '15}
}
