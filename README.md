Naive Bayes — Effect of Laplace Smoothing on Rare Events
Overview

This repository contains the code and experimental materials for a university-level Machine Learning coursework assignment analysing how Laplace smoothing influences rare-event handling in Naive Bayes classifiers. The project focuses on the smoothing parameter as an internal probabilistic mechanism and examines its impact on probability estimation, classification performance, and robustness in sparse text data.

Project Objective

The objective of this project is to investigate how different levels of Laplace smoothing affect the behaviour of a Multinomial Naive Bayes classifier when rare features are present. Rather than comparing multiple models, the study isolates the smoothing parameter and analyses how it governs the trade-off between sensitivity to rare events and stability of probability estimates.

Key questions addressed include:

How do zero-frequency features affect Naive Bayes predictions?

How does smoothing improve robustness for documents containing rare tokens?

At what point does excessive smoothing increase bias?

Repository Structure

notebooks/
Jupyter notebook containing all experiments, evaluations, and figure generation.

figures/
Output plots used in the written report, including performance trends and rare-event analysis.

report/
Final written tutorial submitted as a PDF or web page.

data/
No external datasets are stored. The dataset is fetched programmatically using scikit-learn.

Dataset

The experiments use a subset of the 20 Newsgroups text corpus, restricted to two categories. Documents are represented using a bag-of-words model with raw term counts, resulting in a sparse, high-dimensional feature space with a heavy-tailed frequency distribution.

Experimental Methodology

A Multinomial Naive Bayes classifier is trained using varying values of the Laplace smoothing parameter. Model performance is evaluated using accuracy, macro-averaged F1 score, and log loss. Additional evaluation is performed on a subset of documents containing rare tokens to directly assess rare-event robustness.

Reproducibility

All experiments are fully reproducible. Running the provided notebook from start to finish will regenerate all figures and quantitative results reported in the tutorial. Random seeds are fixed, and no manual preprocessing steps are required.

Requirements

The implementation relies on standard Python libraries for machine learning and data analysis, including NumPy, Matplotlib, and scikit-learn. No specialised hardware or proprietary software is required.

Usage

Open and run the Jupyter notebook in the notebooks/ directory.

Inspect the generated figures and evaluation outputs.

Read the written report in the report/ directory to follow the theoretical explanation and experimental analysis.

License

This repository is provided for educational use. Refer to the LICENSE file for usage and redistribution conditions.
