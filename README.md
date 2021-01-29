# NLP


### Glossary

***NLP***

*Natual Language Processing*: A broad category of algorithms/models dedicated to using text/audio/video and other non-numeric/unstructured signals to predict outputs.

***NLU***

*Natural Language Understanding*: A subdivision of **NLP**, this particular study discipline involves comprehension of written text or audio - often in the form of summary extraction or association.

***NLG***

*Natural Language Generation*: The inverse of **NLU**, this subdivision of **NLP** seeks to create text or audio that has the properties of real text. 

**Levels of Analysis NLP**

- Discourse: inference

- Semantic: meanings

- Syntactical: grammar

- Lexical: words


***Morphology***: study of the structure and formation of words

***Inflections***: syntactic differences between words

***Stemming***: reducing a word to its root form

***Lemmatization***: uses lexical knowledge bases such as WordNet to obtain word base forms

***POS Tagging***: breaks a document into chunks and assigns a tag (ADJ, N, NP etc) to each word **AMBIGUITY is a problem (see notes)**

***Taxonomy Seach***:
Hierarchical organization of entities.
Parent-child “is-a” relationships

***Onotology Search***:
Arbitrary complex relationships between entities. 
Is-a, has-a, uses-a .. non-hierarchical relationships

***Shallow Parsing***: gets down to the word and sentence structure level. semantic types (e.g., location, org, person), semantic roles (e.g., agents, theme), sense distinctions (e.g., WordNet, OntoNotes), entity resolution

***Feature Engineering:***
the process of using domain knowledge to extract ”hand crafted” features from raw data via data mining techniques. These features can be used to improve the performance of machine learning algorithms. 

***Feature Learning:***
set of techniques that allows a system to automatically discover the representations needed for feature detection or classification from raw data. 

***Top down NLP***: high level concepts and categories

***Bottom up NLP***: works of off groups of smaller text (hypernyms etc)

***Sentence Segmentation***: Process of deciding where sentences end and begin is not always straightforward, do not assume it is.

***Word tokenization***: convert a string of characters into a sequence of tokens (usually based on a separator: , | ' ')

***Stop Words***: Extremely common “function” words that are of little value in helping select documents matching a user need  

***Lexical Knowledge Bases***: 

***Synonym/antonym***: a word or phrase that means exactly or nearly the same as another word or phrase in the same language.

***Hyponym/hypernym***: Hyponymy shows the relationship between a generic term (hypernym) and a specific instance of it (hyponym).

***Holonym/meronym***: the relationship between a term denoting the whole and a term denoting a part of, or a member of, the whole.

***Knowledge Graphs***:

- Entity
- Edge
- Attribute
- Ontology (basically XML with specific relation types)

***Grammar***: defines the syntax and structure of language. 

- Dependency grammar (word-based grammars): A word has a relation or depends on another word based on the positioning of the words in the sentence

- Directed acyclic graph (DAG): Every node in the tree has at most one incoming edge, except the root node.

- Constituency Grammars (phrase structure grammars): Syntax and rules that govern the hierarchy and ordering of the various constituents in the sentences.


***Unigram Tagging***: no context taken when considering POS.

***N-gram Tagging***: context of N words taken into account when creating POS tag.

***Stochastic taggers***: models that incorporate frequency and/or probability 

- Frequency-based: assign tag that occurs most frequently with the word in the training data. 

- Probability-based: calculate the probability of occurrences of a given sequence of tags;  best tag for a word is determined by the probability that it occurs with the n previous tags (context, n-gram)

- Hidden Markov Models: combines frequency and probability based approaches

***POS Tagging***: shallowest – POS tags only

***Shallow Parsing/Chunking***: grouping POS tags into “phrases”, obtain semantically meaningful phrases and relations 

***Chinking***: syntax elements not part of chunks

***Full Parsing***: complete internal syntax (expensive) 

***Distributional hypothesis***: Words which are similar in meaning occur in similar contexts

***Term/Word Similarity***: similarity between individual tokens or words.

***Jaccard/Cosine Similarity***: statistical measurements of similarity
- Jaccard similarity is good for cases where duplication does not matter
- Cosine similarity is good for cases where duplication does matter

**PMI – pointwise mutual information***

***Word2Vec*** 
Complexity of neural network language models comes with non-linear hidden layers. Word2Vec models are simpler (probably not as accurate) but more scalable

- SkipGram: 
 - Focus word is the single input vector, and the target context words are the output layer

- CBOW: maximize the conditional probability of observing the actual output word (the focus word) given the input context words, with regard to the weights
  - Sliding window of context words 
  - Each word is coded in one-hot form
  - Single hidden layer and single output layer
  
**Skip-gram: works well with small amount of training data, is able to represent well rare words and phrases well. CBOW: several times faster to train than skip-gram, slightly better accuracy for frequent words**


***Document Clustering***: Unsupervised machine learning 
Organize a corpus of documents into various groups based on some features/attributes/properties of the documents.


***k-Means - algo***:
- Randomly pick k-centroids in d-space (algorithms exist for initializing centroids that converge more effectively, e.g., kmeans++)
- Assign each data point to the closest centroid (using a nearness measure such as Euclidean distance)
- Move centroid to the average location of all data points.

**k-means / issues**
- Final cluster configuration depends on initial centroid allocation
- Need to choose the value of k (use cross validation, elbow method, et al)
- Convergence issues: algorithm can fall into a loop, bouncing back and forth between two solutions (in most practical situations, kmeans converges but can be stuck at a local minima)
- Interpretability can be a problem: sometimes the answer isn’t useful


***Latent Semantic Analysis (LSA)***
-  A form os SVD
- Uncovers latent hidden terms which correlate semantically to form topics.
- Words that are close in meaning will occur in similar pieces of text (hence topics are unlikely to share words)

***Latent Dirichlet  (LDA)***
- Generative probabilistic model – each item of a collection (document) is modelled as a finite mixture over an underlying set of topic probabilities; each topic is modelled as an infinite mixture over an underlying set of word probabilities.
- Probability distributions over words vs topic-topic matrix (LSA) – different topics can share keywords

***Semantic Topic Modeling***
- Find common topics in queries to get deeper insights
- Queries are short-text, sparse, and don’t provide enough word counts for models to learn how words are related and to disambiguate multiple meanings of a single word. (e.g., see LDA output with words in incorrect categories)

***Sentiment Analysis (SA)***
- Also known as opinion mining, opinion analysis, 
- Unstructured textual data has facts (objective) and opinions (subjective)
- Computational study of opinions, sentiments and emotions expressed in text. 
- Extract subjective and opinion such as emotions, attitude, mood, modality, et al to compute the polarity of a document
- Polarity: positive, negative, or a neutral sentiment. 
- Advanced analysis: complex emotions such as sadness, happiness, anger, and sarcasm. 

