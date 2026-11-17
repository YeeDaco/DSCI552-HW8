# DSCI 552 — Homework 8

Supervised, semi-supervised and unsupervised learning on the UCI Breast Cancer Wisconsin (Diagnostic) data (a 30-run Monte-Carlo comparison of an L1-penalized linear SVM tuned by 5-fold cross-validation, self-training of an L1 SVM from 50% labeled training data, k-means with k = 2 used as a classifier through a majority poll of the 30 points closest to each center, and spectral clustering with an RBF kernel whose gamma gives the same cluster balance as the classes; accuracy, precision, recall, F1-score and AUC on the training and test sets, ROC curves and confusion matrices), and active versus passive learning with L1 linear SVMs on the UCI banknote authentication data (learning curves of 90 incrementally trained SVMs averaged over 50 Monte-Carlo runs).

## Structure

```
.
├── README.md
├── .gitignore
├── data
│   ├── banknote
│   │   └── data_banknote_authentication.txt
│   └── wdbc
│       ├── wdbc.data
│       └── wdbc.names
├── notebook
│   └── Lu_Yiming_HW8.ipynb
└── requirements.txt
```

## Run

```bash
pip install -r requirements.txt
cd notebook
jupyter notebook Lu_Yiming_HW8.ipynb   # then Kernel -> Restart & Run All
```

The notebook loads data with the relative paths `../data/wdbc/` and `../data/banknote/`. The ID column of `wdbc.data` is an identifier and is not used as a feature. A full run (30 Monte-Carlo runs of the four methods in problem 1, and 2 x 50 learning curves of 90 cross-validated L1 SVMs each in problem 2) takes about 30 minutes on an 8-thread machine, almost all of it in problem 2.
