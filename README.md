# Natural Language Processing Assignment 1

This repository contains the implementation report and code for a complete Natural Language Processing pipeline.

## Project Overview

This project covers four main parts:

1. Text preprocessing and linguistic analysis  
2. N-gram language models and smoothing  
3. Byte Pair Encoding for Urdu text  
4. Embedding models and downstream evaluation  

## Part 1: NLP Preprocessing

This part focuses on cleaning and analyzing text collected from a webpage.

### Tasks Covered

- HTML to plain text conversion
- Regex extraction
- Sentence tokenization
- Word tokenization
- Text normalization
- Stopword removal
- Corpus statistics
- POS tagging
- Stemming vs lemmatization
- Named Entity Recognition

### Key Results

- Total sentences: 19
- Total tokens: 1051
- Tokens before stopword removal: 1156
- Tokens after stopword removal: 774
- Vocabulary before stopword removal: 355
- Vocabulary after stopword removal: 299

## Part 2: Language Models and Smoothing

This part implements unigram and bigram language models with and without smoothing.

### Models Implemented

- Unigram without smoothing
- Unigram with Laplace smoothing
- Bigram without smoothing
- Bigram with linear interpolation smoothing

### Perplexity Results

| Model | In-domain Perplexity | Out-of-domain Perplexity |
|---|---:|---:|
| Unigram Unsmooth | 725.90 | 945.00 |
| Unigram Laplace | 728.50 | 943.83 |
| Bigram Unsmooth | Infinity | Infinity |
| Bigram Linear Interpolation | 275.44 | 666.99 |

## Part 3: Byte Pair Encoding for Urdu

This part implements BPE for Urdu word segmentation and calculates average Unicode characters per token.

### Key Results

- Dictionary words: 5691
- Urdu sentences segmented: 50
- BPE merges learned: 500
- Total Urdu corpus tokens: 12,654
- Average Unicode characters per token: 3.637

## Part 4: Embedding Models

This part covers TF-IDF, count-based embeddings, neural word embeddings, intrinsic evaluation, sentence embeddings, and extrinsic evaluation.

### TF-IDF Results

| Method | Vocabulary | Sparsity | OOV | Average Cosine Similarity |
|---|---:|---:|---:|---:|
| Word-level TF-IDF | 15000 | 0.9817 | 0.0343 | 0.1651 |
| BPE-based TF-IDF | 186 | 0.1067 | 0.0 | 0.8419 |

### Neural Word Embeddings

- Method: SGNS / Word2Vec-style training
- Vocabulary: 6000
- Training pairs: 40000
- Epoch 1 loss: 4.1631
- Training time: 0.61 seconds

### Sentence Embedding Results

- Mean pooling accuracy: 0.51
- TF-IDF weighted accuracy: 0.5183

### Extrinsic Evaluation: AG News Classification

| Method | Accuracy | Macro-F1 |
|---|---:|---:|
| TF-IDF | 0.8307 | 0.8282 |
| Sentence Mean Embedding | 0.4473 | 0.4407 |

## Tools and Technologies

- Python
- NLTK
- BeautifulSoup
- Regex
- TF-IDF
- BPE
- PPMI
- SGNS
- Word Embeddings
- Sentence Embeddings
- AG News Dataset
- Reuters Corpus
- Brown Corpus

## Conclusion

This project demonstrates a complete NLP workflow, starting from text collection and preprocessing and moving toward language modeling, Urdu segmentation, word embeddings, sentence embeddings, and downstream text classification.
