# Resume Clustering

Resumes are an important way to convey professional experience, academic background, and other skills to prospective employers.  However, when a single job advertisement garners several hundred (or several thousand) resumes, how does a program manager efficiently evaluate hundreds (or thousands) of resumes to find the best candidates for the position?  This study investigates the use of unsupervised machine learning and natural language pocessing to cluster resumes of similar professional backgrounds and experience levels.

This unsupervised machine learning study used natural language processing to evaluate a small set of 73 resumes from the same market sector.  Resumes are a unique subset of unstructured data because of the inherent, if lazy, structure that is embedded in the typical resume.  The most interpretable results came from a simple document distance model using CountVectorizer using the 'euclidean' metric.  

Overall, a number of unsupervised machine learning methods were evaluated with the data set with different results.  iPython notebooks in this repository cover each of these methods.

* Distance
* KMeans
* Gensim Word2Vec
* Hierarchical Clustering / Agglomerative Clustering

#### Distance

The `nltk` and `sklearn` libraries were used to tokenize and process the cleaned and anonymized resume text.  CountVectorizer and TfidfVectorizer were used to determine a simple document similarity using different metrics--Euclidean, Cosine, Manhattan--to evaluate the best performing method.  

Initial observations indicate that CountVectorizer produced more interpretable clusters (experience and skills) than TfidfVectorizer .  This is likely an artifact of the market sector and small number of resumes in the corpus (73).  The Euclidean distance metric was the best performing metric followed by Manhattan.

#### KMeans

* [k-means clustering](https://en.wikipedia.org/wiki/K-means_clustering)
* [sklearn Clustering: KMeans](http://scikit-learn.org/stable/modules/clustering.html#k-means)

KMeans produced some interesting clustering results and plots of the clusters appeared to be centered on job advertisements for which the resumes were submitted.  Only one job advertisement was available for the resumes collected for this study so this observation could not be validated.

#### Gensim Word2Vec

* [Word2Vec](https://en.wikipedia.org/wiki/Word2vec)
* [Gensim Word2Vec](https://radimrehurek.com/gensim/models/word2vec.html)

Word2Vec produced some very interesting results, but the corpus size was insufficient to utilize the results confidently.  Word2Vec is certainly worth evaluating with a much larger resume corpus.

#### Agglomerative Clustering

* [Hierarchical clustering](https://en.wikipedia.org/wiki/Hierarchical_clustering)
* [sklearn.cluster.AgglomerativeClustering](http://scikit-learn.org/stable/modules/generated/sklearn.cluster.AgglomerativeClustering.html#sklearn.cluster.AgglomerativeClustering)
* [Example: Agglomerative clustering with and without structure](http://scikit-learn.org/stable/auto_examples/cluster/plot_agglomerative_clustering.html)

Agglomerative Clustering produced an interesting clusterig series, but insuffienct time prevented a thorough interpretation of the results to evaluate the methods effectiveness in clustering resumes.

#### Conclusions

This study found a number of interesting results that are being developed in a follow-on evaluation incorporating some supervised learning to build an 'expert' system for evaluating resumes within the market sector.  KMeans, Word2Vec, and Agglomerative Clustering will both be re-evaluated once a much larger corpus of resumes is obtained.

