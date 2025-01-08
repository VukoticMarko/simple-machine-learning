# Sentiment Analysis using NLTK and Scikit-Learn

## Overview
This project demonstrates how to perform sentiment analysis on movie reviews using the Natural Language Toolkit (NLTK) and Scikit-Learn. The code processes movie review data, extracts features, trains a Support Vector Machine (SVM) classifier, and evaluates its accuracy.

---

## Key Features
- **Dataset**: Uses the `movie_reviews` dataset from the NLTK library, which contains labeled positive and negative movie reviews.
- **Feature Extraction**: Extracts the 4000 most common words as features for classification.
- **Model Training**: Implements a Support Vector Machine (SVM) classifier using Scikit-Learn integrated with NLTK.
- **Performance Evaluation**: Measures the accuracy of the model on a test dataset.

---

## Workflow
1. **Import Libraries and Dataset**:
   - Use `nltk.corpus.movie_reviews` for labeled movie review data.
   - Shuffle the dataset for randomness.

2. **Feature Extraction**:
   - Calculate the frequency of all words in the dataset.
   - Select the top 4000 words as features.
   - Create a function `find_features()` to map features to reviews.

3. **Prepare Training and Testing Sets**:
   - Use Scikit-Learn's `train_test_split` to split data into training (75%) and testing (25%) sets.

4. **Model Training and Testing**:
   - Train an SVM classifier on the training data using `SklearnClassifier`.
   - Evaluate the model's performance using NLTK's `accuracy()` function.

---

## Key Outputs
- **Most Common Words**: Displays the 15 most frequent words in the dataset.
- **Feature Example**: Shows the features extracted from a sample negative review.
- **SVM Model Accuracy**: Prints the accuracy of the classifier on the test dataset.

## Notes
- Ensure NLTK and required Scikit-Learn libraries are installed.
- The dataset is preloaded in NLTK but may need to be downloaded via nltk.download().

## License
This project is provided under the MIT License. Feel free to use and modify it for personal or educational purposes.
