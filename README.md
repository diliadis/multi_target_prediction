# Repository for mulit-target prediction datasets
This is a repository for datasets that fall under the umbrella of multi-target prediction. More specifically, the 
repository contains datasets from the following problem settings:

* Multi-label classification
* Multivariate (Multi-target) regression
* Hierarchical Multi-label classification
* Dyadic prediction
* Matrix Completion

## Multi-label classification
The following datasets were collected from the [Extreme Classification Repository](http://manikvarma.org/downloads/XC/XMLRepository.html)

General information about the datasets:

| Dataset | Instance Dim. | Label Dim. | Training Set size | Test Set size | 
| --- | :---: | :---: | :---: | :---: | 
| `Bibtex` | 1836 | 159 | 4880 | 2515 | 
| `Delicious` | 500 | 983 | 12920 | 3185 | 

### 1) Bibtex

The dataset was first introduced by [Katakis et al.](http://lpis.csd.auth.gr/publications/katakis_ecmlpkdd08_challenge.pdf) 
and is concerned with the automated tag recommendation problem.

### 2) Delicious
The dataset was first introduced by [Tsoumakas et al.](http://lpis.csd.auth.gr/publications/tsoumakas-mmd08.pdf)
and is also concerned with automated tag suggestion problem. The dataset was extracted from the del.icio.us social 
bookmarking site on the 1st of April 2007. 


The features for the instances are in the form of Bag-of-word representations.


## Multivariate(Multi-target) regression

The following datasets were collected from the [Mulan](http://mulan.sourceforge.net/datasets-mtr.html) repository.

General information about the datasets:

| Dataset | Instance Dim. | Label Dim. | examples | 
| --- | :---: | :---: | :---: | 
| `osales` | 413 | 12 | 639 |
| `scm1d` | 280 | 16 | 9803 |

### 1) Osales
The dataset was originally used in Kaggle's ["Online Product Sales"](https://www.kaggle.com/c/online-sales) competition
and is concernedwith the prediction of the online sales of consumer products. The rows correspond to products and the 
columns(targets) correspond to the monthly sales for the first 12 months after the product launches.

### 2) scm1d
The dataset is derived from the Trading Agent Competition in Supply Chain Management (TAC SCM) tournament from 2010.
A row corresponds to an observation day in the tournament. The instace features are the observed prices for a specific
tournament day as well as 4 time-delayed observations for each observed product and component (1, 2, 4 and 8 days of
delay). Each of the 16 targets correspond to the next day mean price.
