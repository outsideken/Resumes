# Resume Clustering

This unsupervised machine learning study used natural language processing and clustering techniques to evaluate a small set of 73 resumes.  Resumes are a unique subset of unstructured data because of the inherent, if lazy, structure that is embedded in the typical resume. 

A number of unsupervised machine learning methods were evaluated with the data set with different results.

* Distance using multple metrics (cosine, euclidean, manhattan, cityblock) and the sklearn CountVectorizer and TfidfVectorizer methods
* KMeans()
* Gensim Word2Vec

#### Document Similarity

The `nltk` and `sklearn` libraries were used to tokenize and process the cleaned and anonymized resume text.  CountVectorizer and TfidfVectorizer were used to determine a simple document similarity using different metrics--Euclidean, Cosine, Manhattan--to evaluate the best performing method.  

Initial observations indicate that CountVectorizer produced more accurately grouped clusters than TfidfVectorizer.  This is likely an artifact of the market sector and small number of resumes in the corpus (73).  The Euclidean metric was the best performing metric followed by Manhattan.  


The and the business sector from which the of resumes came.from a small number of job advertisements and therefore were somewhat similar in language, which was 

#### Topic Modeling
