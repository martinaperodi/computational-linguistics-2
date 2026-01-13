# computational-linguistics-2

# Project Goal
This project focuses on text classification for authorship attribution: identifying the author of a paragraph among a set of known authors. The aim is to implement and compare multiple models and document the methodology and results.

# Dataset
Three authors selected from Project Gutenberg

Texts split into paragraphs (50–100 tokens each)

Data split into:

- Training set: ≥1000 paragraphs per author
- Validation set: ≥100 paragraphs per author
- Test set: ≥100 paragraphs per author

Books in training set do not appear in validation or test sets.

# Models:
1. SVM with non-lexical features (Profiling-UD)

  - 5-fold cross-validation on training set
  - Evaluation on validation and test sets
  - Top 20 relevant features reported

2. SVM with n-grams (characters, words, POS)

  - Multiple n-gram configurations tested
  - Best model evaluated on test set

3. SVM with word embeddings

  - Word embeddings combined using different strategies
  - Best model selected via validation set and tested


4. Neural Language Model fine-tuning
  - Fine-tuning for 6 epochs
  - Track training and validation loss
  - Final evaluation on test set
