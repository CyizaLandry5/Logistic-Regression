# Logistic Regression

## Course Information
- **Course:** Course 1 - Natural Language Processing (Classification & Vector Spaces)
- **Platform:** DeepLearning.AI
- **Assignment:** #1 - Logistic Regression for Sentiment Analysis

## 📌 Overview
This assignment introduced the fundamentals of **logistic regression** for **sentiment analysis** on tweets. Given a tweet, the model determines whether it expresses a positive or negative sentiment. This is a foundational NLP classification task that demonstrates how simple models can achieve impressive results when combined with effective feature engineering.

## 🎯 What I Learned
- **Feature Extraction:** Learned how to represent text data numerically by counting positive and negative word frequencies in tweets.
- **Sigmoid Function:** Implemented the sigmoid activation function that maps logits to probabilities between 0 and 1.
- **Logistic Regression from Scratch:** Built the entire logistic regression model including:
  - Cost function (log loss / binary cross-entropy)
  - Gradient descent for parameter optimization
  - Vectorized implementation for efficiency
- **Text Preprocessing:** Used the `process_tweet` function to tokenize, remove stopwords, and apply stemming to tweets.
- **Model Evaluation:** Calculated accuracy on a test set and performed error analysis on misclassified examples.
- **Training vs. Test Performance:** Observed how a simple logistic regression model can achieve ~99.5% accuracy on this dataset.

## ⚙️ Key Skills Practiced
- Implementing logistic regression from scratch with NumPy
- Vectorized operations for gradient descent
- Text preprocessing (tokenization, stopword removal, stemming)
- Feature engineering for NLP (frequency-based features)
- Model evaluation and error analysis
- Probability interpretation of model outputs

## 🚧 Challenges Faced
1. **Understanding Vectorized Operations:** Translating the gradient descent update rule into vectorized form: `θ = θ - (α/m) * X^T · (h - y)` required careful attention to matrix dimensions.
2. **Cost Function Implementation:** Ensuring the log loss handled edge cases (predictions exactly 0 or 1) and that the -1/m factor was applied correctly.
3. **Feature Extraction:** Building the `extract_features` function to count positive and negative word frequencies from the `freqs` dictionary, handling missing keys with `.get()`.
4. **Bias Term Handling:** Remembering to add the bias term (x0 = 1) to the feature vector for the intercept parameter θ0.
5. **Prediction Threshold:** Deciding the classification threshold (0.5) and applying it correctly to convert probabilities to discrete labels.
6. **Data Splitting:** Understanding the train/test split (80/20) and ensuring labels aligned correctly with tweets.

## 📋 Important Submission Notes (AutoGrader)
To avoid `Grader Error: Grader feedback not found` or similar unexpected errors from the DeepLearning.AI AutoGrader, I made sure NOT to:
- Add any extra `print` statements in the assignment
- Add any extra code cells
- Change any of the function parameters
- Use global variables inside graded exercises (unless specifically instructed)
- Change the assignment code where not required (like creating extra variables)

> 💡 **Tip:** If you run into unexpected grader errors, check the above points first. You can always get a fresh copy of the assignment by following the workspace refresh instructions on DeepLearning.AI.

## 🛠️ Technologies & Tools
- Python 3
- NumPy (linear algebra)
- NLTK (twitter_samples, stopwords)
- Pandas (optional data handling)
- Custom utilities (process_tweet, build_freqs)

## 📈 Results
- **Training Accuracy:** Achieved excellent performance on the training set.
- **Test Accuracy:** **~99.65%** accuracy on 2,000 test tweets (1,000 positive, 1,000 negative).
- **Model Performance:** The model correctly classified the vast majority of tweets, with only a few misclassifications (shown in error analysis).

### Sample Predictions

I am happy -> 0.519258
I am bad -> 0.494338
great -> 0.516051
great great great -> 0.548021
great great great great -> 0.563876


### Cost Convergence

The cost after training is 0.22525459.
The resulting vector of weights is [6e-08, 0.00053785, -0.00055884]


### Classification Logic
- **Positive sentiment:** Prediction > 0.5
- **Negative sentiment:** Prediction ≤ 0.5

## 🔗 Key Concepts & Formulas
- **Sigmoid Function:** `h(z) = 1 / (1 + e^(-z))`
- **Log Loss (Binary Cross-Entropy):** `J(θ) = -1/m * [y·log(h) + (1-y)·log(1-h)]`
- **Gradient Descent Update:** `θ = θ - (α/m) * X^T · (h - y)`
- **Prediction:** `y_pred = sigmoid(x · θ)`
- **Feature Vector:** `[bias=1, positive_word_count, negative_word_count]`

## 🧪 Error Analysis Observations
The model occasionally misclassified tweets that:
- Contained mixed sentiment expressions (e.g., "good" and "bad" in same tweet)
- Used ambiguous or sarcastic language
- Had neutral statements that didn't strongly indicate either sentiment
- Contained emojis or special characters that weren't captured in preprocessing

## 📚 Acknowledgments
This assignment was completed as part of the Natural Language Processing specialization on **DeepLearning.AI**. The logistic regression implementation follows the classical approach to binary classification, with NLP-specific adaptations for text feature extraction from tweets.

---
