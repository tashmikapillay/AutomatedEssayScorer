📝 Automated Essay Scoring

An NLP-based machine learning project that automatically evaluates and scores student essays.
Group Project 

👥 Team
Tashmika Pillay, Jeryn Naidoo, Tahsheel Briglal. 

📌 About the Project
Automated Essay Scoring (AES) is an application of Natural Language Processing that evaluates and scores written essays based on a machine learning model. Traditionally, essay grading requires significant human effort, time, and subjectivity — AES emerges as a promising solution to address these challenges.
This project explores the use of machine learning to predict essay scores based on linguistic features extracted from text, with significant implications for education technology, standardised testing, and personalised learning.

🎯 Project Objective
Develop and compare three machine learning models for essay scoring and evaluate their performance using F1 Score and Cohen's Kappa:

Logistic Regression
Random Forest
Multinomial Naïve Bayes


🧠 NLP Techniques Used
TechniqueDescriptionTokenizationSplit essay text into individual word tokens using NLTK's word_tokenizeStopword RemovalRemoved common English stopwords using NLTK's stopword corpusLemmatizationReduced words to root forms using NLTK's WordNetLemmatizerTF-IDF VectorizationWeighted words by frequency using unigrams and bigrams (ngram_range=(1,2), max_features=5000)Label EncodingConverted categorical scores to numerical format using sklearn's LabelEncoder

🛠️ Built With
ToolPurposePythonCore languageNLTKText preprocessingscikit-learnML models, TF-IDF, evaluationpandas & numpyData handlingmatplotlib & seabornVisualisationGoogle ColabDevelopment environment
Dataset: Learning Agency Lab — Automated Essay Scoring 2.0 (Kaggle)

⚙️ Methodology

Load dataset — essays with scores ranging from 1 to 6
Preprocess text — tokenize, remove stopwords, lemmatize
Vectorize — TF-IDF with unigrams and bigrams
Split data — 80% training / 20% testing (random_state=42)
Train models — Logistic Regression, Random Forest, Naïve Bayes
Evaluate — F1 Score and Cohen's Kappa
Compare — confusion matrices and bar plots


📊 Results
ModelF1 ScoreCohen's KappaLogistic Regression0.3260.286Random Forest0.2830.289Naïve Bayes0.2520.137
Key Findings

Logistic Regression achieved the highest F1 score, handling TF-IDF sparse features best due to its linear structure and multinomial classification
Random Forest slightly outperformed on Cohen's Kappa, showing better alignment with true score distributions, but was less consistent across all classes
Naïve Bayes underperformed on both metrics — its independence assumption proved unsuitable for capturing complex essay language patterns


🚀 How to Run
Option 1 — Google Colab (Recommended)
Show Image

Click the badge above
Go to Runtime → Run All
Upload the dataset CSV when prompted

Option 2 — Run Locally
bashgit clone https://github.com/tashmikapillay/AutomatedEssayScorer.git
cd AutomatedEssayScorer
pip install -r requirements.txt
jupyter notebook AutomatedEssayScorer.ipynb
Requirements
nltk
scikit-learn
pandas
numpy
matplotlib
seaborn

📁 Repository Structure
AutomatedEssayScorer/
├── AutomatedEssayScorer.ipynb   # Main notebook
├── notes/                        # Project report & research notes PDF
├── requirements.txt
└── README.md

⚠️ Limitations & Future Work

Classic ML models with TF-IDF ignore essay structure and argument coherence
Small sample sizes for scores 1 & 6 caused class imbalance
Future improvements:

Transformer-based embeddings like BERT
Improved grammar and coherence feature extraction
Ordinal regression to better capture score scales




📚 References

Breiman, L. (2001). Random forests. Machine Learning, 45(1), 5–32.
Cohen, J. (1960). A coefficient of agreement for nominal scales. Educational and Psychological Measurement, 20(1), 37–46.
Jurafsky, D., & Martin, J. H. (2021). Speech and language processing (3rd ed.).
The Learning Agency Lab. (2024). Automated Essay Scoring 2.0 Dataset. Kaggle.
Pedregosa et al. (2011). Scikit-learn: Machine learning in Python. JMLR, 12, 2825–2830.


