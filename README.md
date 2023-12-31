CSCE5310_Project
CSCE 5310 Methods in Empirical Analysis - Project - Loan Delinquencies Prediction

Notebook Code flow:
Download dataset from G-Drive

Pre-processing: duplicate and null check

EDA: understand relation by analysing a) univariate b) bivariate c) correlation d) all charts

Model Building / Predictive Analysis:

a) Data transform: delete columns like ID, batch etc after EDA

b) SPSS: analysis for PCA, which columns can be removed

c) Model Iter - 1: Test few models with all columns: different set of columns and compare with all columns; which gives better results

d) Model Iter - 2: Test again after removing some columns with less Eigen values suggested by SPSS

e) Model Iter - 3: Test again after removing few more columns

f) Compare Iter 1, 2 & 3: as no model is giving some significant results, use resampling and try again

Model Training with Resampling

Hyperparameter tuning for best model from resampling: Model which are giving better results with resampling

Phase 2:
Try two more models (Logistic Regression & SVM)

Tune hyperparameters for optimum performance

Try scaling on best model with resampling and tuned hyperparameter try scaling for columns with large variance and conclude whether scaling is useful or not

Summarization and conclusion

Required Libraries:
import numpy as np

import pandas as pd

import seaborn as sns

import matplotlib.pyplot as plt

from sklearn.model_selection import train_test_split, GridSearchCV

from sklearn.linear_model import SGDClassifier

from sklearn.metrics import confusion_matrix, ConfusionMatrixDisplay, classification_report, accuracy_score

from sklearn.metrics import log_loss, f1_score, roc_auc_score, roc_curve, auc

from sklearn.tree import DecisionTreeClassifier

from sklearn.preprocessing import StandardScaler

from sklearn.neighbors import KNeighborsClassifier

from sklearn.ensemble import RandomForestClassifier

from xgboost import XGBClassifier

import imblearn

from imblearn.over_sampling import RandomOverSampler

from sklearn.linear_model import LogisticRegression

from sklearn.naive_bayes import GaussianNB

from sklearn.svm import SVC
