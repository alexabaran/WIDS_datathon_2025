# ADHD Brain Activity Patterns:


### What the question asks:

- Brain activity patterns associated with ADHD.

- How these patterns might differ between males and females.

- The focus is on MRI data — the key dataset seems to be the functional MRI connectome matrices, which represent brain activity.



### Understanding the Core of the Task:

The challenge is to find brain activity patterns that are associated with ADHD and sex differences. 

The MRI (functional brain imaging) data is central to this task, and the goal is to analyze how these brain activity patterns differ in individuals with ADHD and how those patterns might differ between males and females.


### Challenge Question and Task:

### *“What brain activity patterns are associated with ADHD; are they different between males and females, and, if so, how?”*

The goal is to build a model to predict both an individual’s sex and their ADHD diagnosis using functional brain imaging data of children and adolescents and their socio-demographic, emotions, and parenting information.



## 📁 Project Structure

```
ADHD-Female-Brain-Detection/
│
│
├── notebooks/
│   ├── 01_eda.ipynb            # exploratory data analysis
│   ├── 02_preprocessing.ipynb  # feature engineering / cleaning
│   ├── 03_modeling.ipynb       # baseline + better models
│   ├── 04_evaluation.ipynb     # final models evaluation
│   ├── submission_LR.csv       # submission for logistic regression
│   ├── submission_nn1.csv      # submission for neural network 1
│   └── submission_nn2.csv      # submission for neural network 2
│
├── reports/
│   ├── data_description.md     # dataset + feature explanation
│   └── model_notes.md          # decisions made about models
│
├── README.md
└── requirements.txt
```
