# Natural Language Processing

## Intro to NLP

Data comes in many different forms: time stamps, sensor readings, images, categorical labels, and so much more. But text is still some of the most valuable data out there for those who know how to use it.

In this course about Natural Language Processing (NLP), you will use the leading NLP library (spaCy) to take on some of the most important tasks in working with text.

By the end, you will be able to use spaCy for:

* Basic text processing and pattern matching
* Building machine learning models with text
* Representing text with word embeddings that numerically capture the meaning of words and documents

spaCy is the leading library for NLP, and it has quickly become one of the most popular Python frameworks. Most people find it intuitive, and it has excellent documentation.

spaCy relies on **models** that are language-specific and come in different sizes. You can load a spaCy model with `spacy.load()`.

### Text preprocessing

There are a few types of preprocessing to improve how we model with words. The first is "lemmatizing." The "lemma" of a word is its base form. For example, "walk" is the lemma of the word "walking". So, when you lemmatize the word walking, you would convert it to walk.

It's also common to remove stopwords. Stopwords are words that occur frequently in the language and don't contain much information. English stopwords include "the", "is", "and", "but", "not".

With a spaCy token, `token.lemma_` returns the lemma, while `token.is_stop` returns a boolean `True` if the token is a stopword (and `False` otherwise).

#### Why are lemmas and identifying stopwords important?

Language data has a lot of noise mixed in with informative content. In the sentence above, the important words are tea, healthy and calming. Removing stop words might help the predictive model focus on relevant words. Lemmatizing similarly helps by combining multiple forms of the same word into one base form ("calming", "calms", "calmed" would all change to "calm").

    However, lemmatizing and dropping stopwords might result in your models performing worse. So you should treat this preprocessing as part of your hyperparameter optimization process.

### Pattern Matching

Another common NLP task is matching tokens or phrases within chunks of text or whole documents. You can do pattern matching with regular expressions, but spaCy's matching capabilities tend to be easier to use.

To match individual tokens, you create a `Matcher`. When you want to match a list of terms, it's easier and more efficient to use `PhraseMatcher`.

## Text Classification

A common task in NLP is **text classification**. This is "classification" in the conventional machine learning sense, and it is applied to text. Examples include spam detection, sentiment analysis, and tagging customer queries.

### Bag of Words

Machine learning models don't learn from raw text data. Instead, you need to convert the text to something numeric.

The simplest common representation is a variation of one-hot encoding. You represent each document as a vector of term frequencies for each term in the vocabulary. The vocabulary is built from all the tokens (terms) in the corpus (the collection of documents).

As an example, take the sentences *"Tea is life. Tea is love."* and *"Tea is healthy, calming, and delicious."* as our corpus. The vocabulary then is `{"tea", "is", "life", "love", "healthy", "calming", "and", "delicious"}` (ignoring punctuation).

For each document, count up how many times a term occurs, and place that count in the appropriate element of a vector. The first sentence has "tea" twice and that is the first position in our vocabulary, so we put the number 2 in the first element of the vector. Our sentences as vectors then look like

v1=[22110000]

v2=[11001111]

This is called the bag of words representation. You can see that documents with similar terms will have similar vectors. Vocabularies frequently have tens of thousands of terms, so these vectors can be very large.

Another common representation is **TF-IDF (Term Frequency - Inverse Document Frequency)**. TF-IDF is similar to bag of words except that each term count is scaled by the term's frequency in the corpus. Using TF-IDF can potentially improve your models.

## Word Embeddings

You know at this point that machine learning on text requires that you first represent the text numerically. So far, you've done this with bag of words representations. But you can usually do better with word embeddings.

**Word embeddings** (also called word vectors) represent each word numerically in such a way that the vector corresponds to how that word is used or what it means. Vector encodings are learned by considering the context in which the words appear. Words that appear in similar contexts will have similar vectors. For example, vectors for "leopard", "lion", and "tiger" will be close together, while they'll be far away from "planet" and "castle".

Even cooler, relations between words can be examined with mathematical operations. Subtracting the vectors for "man" and "woman" will return another vector. If you add that to the vector for "king" the result is close to the vector for "queen."

![Word Embeddings](https://www.tensorflow.org/images/linear-relationships.png)

These vectors can be used as features for machine learning models. Word vectors will typically improve the performance of your models above bag of words encoding. spaCy provides embeddings learned from a model called Word2Vec. You can access them by loading a large language model like `en_core_web_lg`. Then they will be available on tokens from the `.vector` attribute.

### Classification Models

With the document vectors, you can train scikit-learn models, xgboost models, or any other standard approach to modeling.

### Document Similarity

Documents with similar content generally have similar vectors. So you can find similar documents by measuring the similarity between the vectors. A common metric for this is the **cosine similarity** which measures the angle between two vectors,  **a**  and  **b** .

cosθ=a⋅b\∥a∥∥b∥

This is the dot product of  **a**  and  **b** , divided by the magnitudes of each vector. The cosine similarity can vary between -1 and 1, corresponding complete opposite to perfect similarity, respectively.
