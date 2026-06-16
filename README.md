

## Course Information
- **Course:** Course 2 - Natural Language Processing (Probabilistic Models)
- **Platform:** DeepLearning.AI
- **Assignment:** #3 - Language Models & Auto-Complete Systems

## 📌 Overview
In this assignment, I built an **auto-complete system** – a feature we encounter daily:
- **Google Search:** Suggestions that help complete your search query
- **Email Writing:** Predictions for possible endings to your sentences

By the end of this project, I developed a functional prototype of an auto-complete system using probabilistic language models.

## 🎯 What I Learned
- **Language Model Fundamentals:** Understood how to compute probabilities of word sequences using n-grams.
- **Auto-Complete Logic:** Implemented the core logic that suggests the most likely next word given a starting context.
- **Smoothing Techniques:** Applied smoothing methods to handle unseen n-grams and avoid zero probabilities.
- **Perplexity Evaluation:** Used perplexity as a metric to evaluate the quality of language models.
- **N-gram Implementation:** Built and trained unigram, bigram, and trigram models from scratch.

## ⚙️ Key Skills Practiced
- N-gram language modeling
- Probability estimation for word sequences
- Backoff and smoothing (Laplace smoothing, etc.)
- Auto-complete algorithm design
- Text preprocessing for language models

## 🚧 Challenges Faced
1. **Handling Unseen N-grams:** Figuring out how to gracefully handle n-grams that never appeared in the training data without breaking the model.
2. **Smoothing Implementation:** Deciding which smoothing technique to use and implementing it correctly to maintain reasonable probability distributions.
3. **Efficiency with Large Vocabularies:** Ensuring the auto-complete suggestions remained fast even with thousands of possible next words.
4. **Balancing Context Length:** Finding the right balance between using longer contexts (more accurate but sparser) and shorter contexts (less accurate but more reliable).

## 📋 Important Submission Notes (AutoGrader)
To avoid `Grader Error: Grader feedback not found` or similar unexpected errors from the DeepLearning.AI AutoGrader, I made sure NOT to:
- Add any extra `print` statements in the assignment
- Add any extra code cells
- Change any of the function parameters
- Use global variables inside graded exercises (unless specifically instructed)
- Change the assignment code where not required (like creating extra variables)

> 💡 **Tip:** If you run into unexpected grader errors, check the above points first. You can always get a fresh copy of the assignment by following the workspace refresh instructions on DeepLearning.AI.

## 🛠️ Technologies & Tools
- Python
- NumPy
- Collections (Counter, defaultdict)
- Jupyter Notebook / VS Code
- NLTK (for text preprocessing, if used)

## 📈 Results
- Successfully built a working auto-complete prototype.
- Implemented n-gram models (unigram, bigram, trigram) with proper smoothing.
- Generated relevant next-word predictions given partial sentences.
- Evaluated model performance using perplexity scores.

## 🔗 Related Concepts
- N-gram language models
- Markov assumption
- Laplace (add-one) smoothing
- Good-Turing estimation
- Stupid backoff
- Perplexity as an evaluation metric

## 📚 Acknowledgments
This assignment was completed as part of the Natural Language Processing specialization on **DeepLearning.AI**. The auto-complete system follows classical n-gram language modeling approaches widely used in early NLP systems.

---