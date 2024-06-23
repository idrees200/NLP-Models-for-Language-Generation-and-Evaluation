# NLP Models for Language Generation and Evaluation

This Python script demonstrates the implementation and evaluation of various NLP models for language generation and evaluation. It includes Unigram, Smoothed Unigram, Bigram, and Smoothed Bigram models, along with methods to calculate perplexity and generate sentences.

## Overview

The script performs the following tasks:

1. **Data Preprocessing**
   - Reads data from files (`train.txt`, `pos_test.txt`, `neg_test.txt`).
   - Preprocesses each sentence by adding start `<s>` and end `</s>` tokens.
   - Identifies and replaces rare words (words with frequency less than or equal to a threshold) with `<UNK>`.

2. **Language Models**
   - **Unigram Model**: 
     - Calculates frequency of each word.
     - Generates sentences randomly based on unigram probabilities.
     - Computes sentence probability using unigram frequencies.

   - **Smoothed Unigram Model**: 
     - Similar to Unigram Model but applies Laplace smoothing.
     - Handles unseen words by assigning them a small probability.

   - **Bigram Model**: 
     - Builds frequency counts for each bigram (pair of consecutive words).
     - Generates sentences based on the most likely next word given the previous word.
     - Computes sentence probability using bigram frequencies.

   - **Smoothed Bigram Model**:
     - Extends Bigram Model with Laplace smoothing.
     - Handles unseen bigrams by smoothing the probability estimates.

3. **Sentence Generation**
   - Generates 20 sentences for each model and writes them to output files (`unigram_output.txt`, `smooth_unigram_output.txt`, `bigram_output.txt`, `smooth_bigram_output.txt`).

4. **Perplexity Calculation**
   - Calculates perplexity of each model on positive (`pos_test.txt`) and negative (`neg_test.txt`) test data.
   - Perplexity is a measure of how well a probability model predicts a sample.

5. **Analysis and Comparison**
   - Provides insights into sentence generation differences between Unigram and Bigram models.
   - Discusses the impact of smoothing techniques on probability distribution and sentence generation.
   - Compares perplexity values across different models and test datasets.

## Dependencies

- Python 3.x
- Libraries: `random`, `math`, `collections.Counter`

## Usage

1. **Setup**: Ensure Python and required libraries are installed.
2. **Execution**: Run the script. It will preprocess data, build models, generate sentences, and calculate perplexity.
3. **Output**: Review generated sentences in output files and perplexity values in the console.

## Further Improvements

- Explore more advanced smoothing techniques (like Good-Turing or Kneser-Ney) for better language modeling.
- Implement higher-order n-gram models (trigrams, etc.) for capturing more complex dependencies in text.
- Extend the evaluation to larger datasets and diverse text corpora for robust model assessment.


