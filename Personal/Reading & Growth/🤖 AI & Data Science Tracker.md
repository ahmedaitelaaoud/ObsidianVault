# 🤖 AI & Data Science Learning Tracker

> From Mathematics to Machine Learning to AI Engineering

---

## 🎯 Overall Progress

**Start Date:** {{date:YYYY-MM-DD}}
**Target:** AI/ML Engineer + Data Scientist
**Current Level:** Beginner

**Overall Completion:** ████░░░░░░░░░░░░░░░░ 0%

---

## 📊 Skill Categories

| Category | Progress | Status | Priority |
|----------|----------|--------|----------|
| Mathematics & Statistics | 0% | 🔴 Not Started | 🔥 Critical |
| Python for Data Science | 0% | 🔴 Not Started | 🔥 Critical |
| Data Analysis | 0% | 🔴 Not Started | 🔥 High |
| Machine Learning | 0% | 🔴 Not Started | ⭐ High |
| Deep Learning | 0% | 🔴 Not Started | ⭐ Medium |
| NLP | 0% | 🔴 Not Started | 💡 Low |
| Computer Vision | 0% | 🔴 Not Started | 💡 Low |
| MLOps | 0% | 🔴 Not Started | 💡 Low |

---

## 📚 PHASE 1: FOUNDATIONS (Months 1-3)

### Mathematics & Statistics 📐
**Priority:** 🔥 ESSENTIAL - Can't skip this!

#### Statistics Basics
- [ ] Descriptive statistics (mean, median, mode, variance, std dev)
- [ ] Probability basics (events, conditional probability)
- [ ] Distributions (normal, binomial, poisson)
- [ ] Central Limit Theorem (CLT)
- [ ] Hypothesis testing (null hypothesis, p-value)
- [ ] Confidence intervals
- [ ] Correlation vs causation
- [ ] Sampling techniques

**Resources:**
- [ ] Khan Academy Statistics
- [ ] StatQuest (YouTube) - HIGHLY RECOMMENDED
- [ ] Coursera: Introduction to Statistics

**Practice:**
- [ ] Calculate stats for real datasets
- [ ] Interpret statistical results
- [ ] Design simple experiments

---

#### Linear Algebra
- [ ] Vectors and matrices
- [ ] Matrix operations (addition, multiplication)
- [ ] Dot product and cross product
- [ ] Matrix determinant and inverse
- [ ] Eigenvalues and eigenvectors
- [ ] Matrix decomposition (SVD)

**Why Important:** Neural networks are just matrix operations!

**Resources:**
- [ ] 3Blue1Brown - Essence of Linear Algebra (YouTube)
- [ ] Khan Academy Linear Algebra

---

#### Calculus (Basic)
- [ ] Derivatives (rates of change)
- [ ] Chain rule
- [ ] Partial derivatives
- [ ] Gradient (direction of steepest ascent)
- [ ] Integration basics

**Why Important:** Gradient descent uses derivatives!

**Resources:**
- [ ] 3Blue1Brown - Essence of Calculus
- [ ] Khan Academy Calculus

---

### Python for Data Science 🐍
**Prerequisite:** Complete [[🐍 Python Learning Tracker]] basics first

#### NumPy Mastery
- [ ] Arrays (1D, 2D, 3D)
- [ ] Array creation (zeros, ones, arange, linspace)
- [ ] Indexing and slicing
- [ ] Array operations (arithmetic, broadcasting)
- [ ] Universal functions (ufuncs)
- [ ] Aggregations (sum, mean, std, min, max)
- [ ] Reshaping and transposing
- [ ] Random number generation

**Practice Projects:**
- [ ] Matrix calculator
- [ ] Statistical analysis with NumPy
- [ ] Image processing basics

---

#### Pandas Proficiency
- [ ] Series and DataFrames
- [ ] Reading data (CSV, Excel, JSON, SQL)
- [ ] Data inspection (head, info, describe)
- [ ] Indexing (loc, iloc, boolean indexing)
- [ ] Data cleaning:
  - Handling missing values (dropna, fillna)
  - Removing duplicates
  - Data type conversion
- [ ] Data transformation:
  - Sorting
  - Filtering
  - GroupBy operations
  - Merge, join, concatenate
  - Pivot tables
- [ ] Apply and map functions
- [ ] Time series basics

**Practice Projects:**
- [ ] Clean messy dataset
- [ ] Sales data analysis
- [ ] Customer data exploration

---

#### Data Visualization 📊
**Matplotlib:**
- [ ] Basic plots (line, scatter, bar, histogram)
- [ ] Subplots and figure layout
- [ ] Customization (colors, labels, titles, legends)
- [ ] Saving figures

**Seaborn:**
- [ ] Statistical plots (distribution, regression)
- [ ] Categorical plots (box, violin, swarm)
- [ ] Heatmaps and correlation matrices
- [ ] FacetGrid for multiple plots
- [ ] Styling and themes

**Plotly (Optional but cool):**
- [ ] Interactive plots
- [ ] 3D visualizations
- [ ] Dashboards

**Practice:**
- [ ] Create 20+ different visualizations
- [ ] Tell stories with data
- [ ] Presentation-ready charts

---

## 📚 PHASE 2: DATA ANALYSIS (Months 2-4)

### Exploratory Data Analysis (EDA) 🔍

**Process:**
1. **Understand the data**
   - [ ] What is each column?
   - [ ] Data types correct?
   - [ ] How much data?

2. **Clean the data**
   - [ ] Missing values strategy
   - [ ] Outliers detection
   - [ ] Data validation

3. **Explore relationships**
   - [ ] Correlation analysis
   - [ ] Distributions
   - [ ] Patterns and trends

4. **Visualize insights**
   - [ ] Key findings in charts
   - [ ] Comparative analysis

5. **Document findings**
   - [ ] Insights summary
   - [ ] Data quality notes

**Practice Datasets:**
- [ ] Titanic (Kaggle)
- [ ] Iris dataset
- [ ] House prices
- [ ] Customer data
- [ ] Financial data

**Projects:**
- [ ] Complete 5+ EDA notebooks
- [ ] Share findings as blog posts

---

### Data Collection & Cleaning 🧹

**Data Sources:**
- [ ] CSV files
- [ ] APIs (requests library)
- [ ] Web scraping (BeautifulSoup, Scrapy)
- [ ] Databases (SQL)
- [ ] Excel files

**Cleaning Techniques:**
- [ ] Dealing with missing data
- [ ] Handling duplicates
- [ ] Outlier treatment
- [ ] Data normalization/standardization
- [ ] Feature engineering basics
- [ ] Data type conversion
- [ ] String manipulation

**Projects:**
- [ ] Scrape website and clean data
- [ ] API data pipeline
- [ ] Database to clean CSV

---

## 📚 PHASE 3: MACHINE LEARNING (Months 4-8)

### ML Fundamentals 🤖

#### Supervised Learning
**Regression:**
- [ ] Linear Regression
  - Theory (y = mx + b)
  - Cost function (MSE)
  - Gradient descent
  - Implementation from scratch
  - Using scikit-learn
- [ ] Polynomial Regression
- [ ] Ridge and Lasso (regularization)
- [ ] Metrics (R², MAE, RMSE)

**Classification:**
- [ ] Logistic Regression
  - Binary classification
  - Sigmoid function
  - Decision boundary
- [ ] Decision Trees
  - How they split
  - Entropy and information gain
  - Overfitting issues
- [ ] Random Forest
  - Ensemble method
  - Bagging
  - Feature importance
- [ ] Support Vector Machines (SVM)
  - Hyperplane concept
  - Kernels
- [ ] K-Nearest Neighbors (KNN)
  - Distance metrics
  - K selection
- [ ] Naive Bayes
  - Probability-based
  - Text classification
- [ ] Metrics (Accuracy, Precision, Recall, F1, ROC-AUC, Confusion Matrix)

**Practice:**
- [ ] Implement each algorithm from scratch (at least once)
- [ ] Apply to real datasets
- [ ] Understand when to use each

---

#### Unsupervised Learning
**Clustering:**
- [ ] K-Means
  - How it works
  - Elbow method
  - Limitations
- [ ] Hierarchical Clustering
  - Dendrograms
  - Linkage methods
- [ ] DBSCAN
  - Density-based
  - Good for irregular shapes

**Dimensionality Reduction:**
- [ ] PCA (Principal Component Analysis)
  - Variance explanation
  - Feature extraction
  - Visualization
- [ ] t-SNE
  - For visualization
  - Non-linear reduction

**Practice:**
- [ ] Customer segmentation
- [ ] Anomaly detection
- [ ] High-dimensional data visualization

---

### Scikit-learn Mastery 🛠️

**Essential Workflow:**
```python
# 1. Prepare data
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

# 2. Feature scaling
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)

# 3. Train model
from sklearn.linear_model import LogisticRegression
model = LogisticRegression()
model.fit(X_train, y_train)

# 4. Evaluate
y_pred = model.predict(X_test)
from sklearn.metrics import accuracy_score
accuracy = accuracy_score(y_test, y_pred)

# 5. Tune (GridSearch, RandomSearch)
from sklearn.model_selection import GridSearchCV
```

**Master These:**
- [ ] train_test_split, cross_val_score
- [ ] StandardScaler, MinMaxScaler
- [ ] Pipeline (chaining steps)
- [ ] GridSearchCV, RandomizedSearchCV
- [ ] All metrics (classification_report, confusion_matrix)

---

## 📚 PHASE 4: DEEP LEARNING (Months 6-10)

### Neural Networks Basics 🧠

**Fundamentals:**
- [ ] Perceptron (single neuron)
- [ ] Multi-layer perceptron (MLP)
- [ ] Activation functions (ReLU, Sigmoid, Tanh, Softmax)
- [ ] Forward propagation
- [ ] Backpropagation (how neural nets learn)
- [ ] Loss functions (MSE, Cross-Entropy)
- [ ] Optimizers (SGD, Adam, RMSprop)
- [ ] Learning rate
- [ ] Batch size and epochs

**Common Issues:**
- [ ] Overfitting (model memorizes training data)
  - Solution: Dropout, Regularization, More data
- [ ] Underfitting (model too simple)
  - Solution: More complex model, more features
- [ ] Vanishing/Exploding gradients
  - Solution: Batch normalization, better initialization

---

### TensorFlow / Keras 🔧

**Keras Basics:**
```python
from tensorflow import keras

model = keras.Sequential([
    keras.layers.Dense(64, activation='relu'),
    keras.layers.Dense(32, activation='relu'),
    keras.layers.Dense(10, activation='softmax')
])

model.compile(
    optimizer='adam',
    loss='categorical_crossentropy',
    metrics=['accuracy']
)

model.fit(X_train, y_train, epochs=10, batch_size=32)
```

**Master These:**
- [ ] Sequential vs Functional API
- [ ] Common layers (Dense, Conv2D, LSTM)
- [ ] Model compilation and training
- [ ] Callbacks (EarlyStopping, ModelCheckpoint)
- [ ] Model evaluation and prediction
- [ ] Save and load models

**Or PyTorch (Alternative):**
- [ ] Tensors
- [ ] Autograd
- [ ] nn.Module
- [ ] Training loop

---

### Convolutional Neural Networks (CNN) 📷
**For Image Tasks**

**Concepts:**
- [ ] Convolution operation
- [ ] Filters/Kernels
- [ ] Pooling (Max, Average)
- [ ] Flatten layer
- [ ] Common architectures (LeNet, AlexNet, VGG, ResNet)

**Practice:**
- [ ] MNIST digit classification
- [ ] CIFAR-10 image classification
- [ ] Cat vs Dog classifier
- [ ] Build custom image classifier

---

### Recurrent Neural Networks (RNN) 🔁
**For Sequence Data**

**Concepts:**
- [ ] Vanilla RNN
- [ ] LSTM (Long Short-Term Memory)
- [ ] GRU (Gated Recurrent Unit)
- [ ] Sequence to sequence
- [ ] Attention mechanism (basics)

**Applications:**
- [ ] Time series prediction
- [ ] Text generation
- [ ] Sentiment analysis
- [ ] Language translation (simple)

---

## 📚 PHASE 5: SPECIALIZATION (Months 8+)

### Natural Language Processing (NLP) 💬

**Text Processing:**
- [ ] Tokenization
- [ ] Stemming and Lemmatization
- [ ] Stop words removal
- [ ] TF-IDF
- [ ] Word embeddings (Word2Vec, GloVe)

**Models:**
- [ ] Bag of Words
- [ ] N-grams
- [ ] RNN for text
- [ ] Transformer basics (BERT, GPT concepts)

**Projects:**
- [ ] Spam classifier
- [ ] Sentiment analysis
- [ ] Text summarization
- [ ] Chatbot (simple)

---

### Computer Vision (Advanced) 👁️

**Techniques:**
- [ ] Object detection (YOLO, R-CNN concepts)
- [ ] Image segmentation
- [ ] Transfer learning (using pre-trained models)
- [ ] Data augmentation

**Projects:**
- [ ] Face recognition
- [ ] Object detector
- [ ] Style transfer
- [ ] OCR (text from images)

---

### MLOps & Deployment 🚀

**Model Deployment:**
- [ ] Save models (pickle, joblib, SavedModel)
- [ ] Flask/FastAPI for model serving
- [ ] Docker basics for ML
- [ ] Cloud deployment (Heroku, AWS, GCP basics)

**Experiment Tracking:**
- [ ] MLflow basics
- [ ] Weights & Biases (W&B)

**Version Control for ML:**
- [ ] DVC (Data Version Control)
- [ ] Model versioning

---

## 📊 Practice & Projects

### Kaggle Competitions 🏆

**Beginner:**
- [ ] Titanic (getting started)
- [ ] House Prices
- [ ] Digit Recognizer (MNIST)

**Intermediate:**
- [ ] Participate in 3+ active competitions
- [ ] Study winning solutions
- [ ] Improve ranking

**Goal:** Reach Kaggle Expert level

---

### Portfolio Projects (Build These) 🚀

**Must-Have Projects:**

1. [ ] **Data Analysis Project**
   - EDA on interesting dataset
   - Insights and visualizations
   - Blog post about findings

2. [ ] **Regression Project**
   - House price prediction
   - Stock price prediction
   - Sales forecasting

3. [ ] **Classification Project**
   - Customer churn prediction
   - Fraud detection
   - Disease prediction

4. [ ] **Image Classification**
   - CNN for image recognition
   - Transfer learning
   - Custom dataset

5. [ ] **NLP Project**
   - Sentiment analysis
   - Text classification
   - Chatbot or text generator

6. [ ] **Time Series**
   - Sales forecasting
   - Stock prediction
   - Anomaly detection

7. [ ] **Clustering Project**
   - Customer segmentation
   - Document clustering

8. [ ] **End-to-End ML Pipeline**
   - Data collection
   - Preprocessing
   - Model training
   - Deployment (API)
   - Frontend (optional)

9. [ ] **Recommendation System**
   - Movie recommender
   - Product recommender

10. [ ] **Deep Learning Project**
    - Image generation
    - Style transfer
    - Advanced NLP

**Target:** 10+ complete ML projects

---

## 📚 Learning Resources

### Online Courses (Best Ones) 🎓

**Beginner:**
- [ ] **Google Machine Learning Crash Course** (free)
- [ ] **Fast.ai - Practical Deep Learning** (free, top-down approach)
- [ ] **Andrew Ng - Machine Learning** (Coursera)

**Intermediate/Advanced:**
- [ ] **Andrew Ng - Deep Learning Specialization** (Coursera)
- [ ] **Kaggle Learn** (free micro-courses)
- [ ] **DeepLearning.AI TensorFlow Developer**

### Books 📖

- [ ] "Hands-On Machine Learning" - Aurélien Géron ⭐⭐⭐⭐⭐
- [ ] "Deep Learning with Python" - François Chollet
- [ ] "Pattern Recognition and Machine Learning" - Bishop (advanced)

### YouTube Channels 📺

- **StatQuest** - Statistics explained simply ⭐⭐⭐⭐⭐
- **3Blue1Brown** - Math visualizations
- **Sentdex** - Python for ML
- **Two Minute Papers** - Latest AI research
- **Yannic Kilcher** - Paper reviews

### Websites & Blogs

- Kaggle Learn
- Towards Data Science (Medium)
- Machine Learning Mastery
- Papers with Code
- Distill.pub (amazing visualizations)

---

## 📊 Weekly Progress Log

### Week of {{date:YYYY-MM-DD}}

**Hours Studied:** ___ hours (target: 4-6h)

**Main Focus:**


**Completed:**
- [ ] 
- [ ] 

**Courses/Tutorials:**


**Projects Worked On:**


**Kaggle Activity:**
- Competitions entered: ___
- Notebooks created: ___

**Papers Read:**


**Code Committed:** ___ commits

**Next Week:**
1. 
2. 
3. 

**Challenges:**


---

## 🎯 Monthly Goals

### {{date:MMMM YYYY}}

**Primary Focus:** 

**Specific Targets:**
- [ ] Complete ___ course modules
- [ ] Build ___ projects
- [ ] Kaggle: ___ notebooks, ___ rank improvement
- [ ] Study ___ hours
- [ ] Read ___ papers/articles

**Projects:**
1. [ ] 
2. [ ] 

**Status:** On Track / Ahead / Behind

---

## 🏆 Milestones & Achievements

- [ ] First NumPy array manipulated
- [ ] First Pandas DataFrame cleaned
- [ ] First data visualization created
- [ ] First ML model trained
- [ ] First Kaggle competition entered
- [ ] First neural network built
- [ ] First deep learning model deployed
- [ ] Kaggle competition top 10%
- [ ] Contributed to ML open source
- [ ] Published ML blog post
- [ ] 10 complete ML projects

---

*Last updated: {{date:YYYY-MM-DD}}*
*Review: Weekly in [[📊 Weekly Review Template]]*

**Remember:**
- Mathematics is your foundation - don't skip it
- Start with small datasets
- Understand the theory before libraries
- Visualize everything
- Always validate your models
- Document your experiments
- Share your learnings

**"Data is the new oil, but you need to refine it first!"** 🛢️➡️💎
