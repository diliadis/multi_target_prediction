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

| Dataset | Instance features | Label Dim. | Training examples | Test examples | 
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


## Hierarchical Multi-label classification

The following datasets were collected from the PASCAL Visual Object Classes (VOC) challenge of 2006 and 2007
and are considered as benchmarks in the fields of visual object category recognition and detection. 


| Dataset | Instance features | Label Dim. | examples |
| --- | :---: | :---: | :---: | 
| `VOC2006` |  | 10 | 5304 | 
| `VOC2007` |  | 20 | 9963 | 


### 1) VOC2006
The dataset was introduced as a benchmark for the [PASCAL VOC challenge of 2006](http://host.robots.ox.ac.uk/pascal/VOC/voc2006/index.html). The goal of this challenge is to 
recognize objects from a number of visual object classes in realistic scenes. The ten object classes that have been 
selected are:

* bicycle, bus, car, motorbike
* cat, cow, dog, horse, sheep
* person

The data has been split into 50% for training/validation and 50% for testing. The distributions of images and objects 
by class are approximately equal across the training/validation and test sets. In total there are 5304 images, 
containing 9507 annotated objects.

### 2) VOC2007 
The dataset was introduced as a benchmark for the [PASCAL VOC challenge of 2007](http://host.robots.ox.ac.uk/pascal/VOC/voc2007/). The goal of the challenge is again to 
recognize objects from a number of visual object classes in realistic scenes. The twenty object classes that have been
selected are:

* bottle, chair, dining table, potted plant, sofa, tv/monitor
* aeroplane, bicycle, boat, bus, car, motorbike, train
* bird, cat, cow, dog, horse, sheep
* person

The data has been split into 50% for training/validation and 50% for testing. The distributions of images and objects 
by class are approximately equal across the training/validation and test sets. In total there are 9,963 images, 
containing 24,640 annotated objects.

We consider these two datasets as instances of a hierarchical multi-label classification problem because :
* multiple objects can be present in an image at once (hence multi-label)
* there is a known hierarchy of the labels available

<p align="center">
  <img src="https://github.com/diliadis/multi_target_prediction/blob/master/images/hierarchy.png">
</p>

## Multivariate(Multi-target) regression

The following datasets were collected from the [Mulan](http://mulan.sourceforge.net/datasets-mtr.html) repository.

General information about the datasets:

| Dataset | Instance features | Label Dim. | examples | 
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


## Dyadic prediction
The two datasets were collected from [Tornede et al.](https://arxiv.org/pdf/2001.10741.pdf) and the [ExCAPE database](https://solr.ideaconsult.net/search/excape/)

| Dataset | Instance features | Label Dim. | Label features | examples | 
| --- | :---: | :---: | :---: | :---: | 
| `EAS dataset` | 45 | 1270 | 153 | 68 |
| `ExCAPE` | 29,413 | 526 | - | 955,386 |


### 1) EAS dataset
The dataset was introduced by [Tornede et al.](https://arxiv.org/pdf/2001.10741.pdf) as a potential benchmark for the
extreme algorithm selection (EAS) problem. Benchmark datasets for regular algorithm selection (AS) usually contain tens 
of algorithms. However, in combined algorithm selection and hyperparameter optimization problems, the number of 
candidate configurations explodes, something that compromises the efficiency of learning algorithms. Therefore, the 
dataset proposed by Tornede et al. considers thousands configurations of cancidate algorithms, in order to facilitate 
meta learning. 

The dataset contains 1270 algorithms which represent the labels as well as 68 benchmarking datasets that
correspond to the labels. Each one of the 68 benchmarking datasets is represented by a 45 dimensional feature vector
while each one of the 1270 algorithms is represented by 153 dimensional feature vector.

### ExCAPE dataset
This dataset is available in the ExCAPE database. It is a large scale quantitative structure activity relationship
(QSAR) benchmark dataset that was built upon public resources (ChEMBL and PubChem databases). The database contains 
70.8 million data points covering about one million compounds and 1667 protein targets. The compound structures are
standardized, the targets have official gene symbols and the activity values are log-transformed into pXC50 values.
The dataset can be binarized to two classes, active and inactive by using a threshold (usually active if pXC50 > 6).
Every protein target used has at least 300 SAR data points, 75 active compounds and 75 inactive compounds. This 
filtering yields 955,386 compounds, 526 protein targets, and 49,316,517 SAR data points (90% sparse).


## Matrix completion

The two datasets were collected from the [Netflix price Challenge](https://www.netflixprize.com/index.html) and the
[GroupLens research lab](https://grouplens.org/about/what-is-grouplens/).


| Dataset | Instance Dim. | Label Dim. | examples | 
| --- | :---: | :---: | :---: | 
| `netflix` | - | 4499 | 470758 |
| `movielens` | - | 3952 | 6040 |

### 1) Netflix prize
The dataset was offered by Netflix for the Netflix prize competition. This movie rating dataset has been used 
extensively to evaluate collaborative filtering algorithms.The dataset contains 24 million ratings, 4499 movies and 
470758 costumers. The ratings are made on a 5-star scale (whole-star ratings only).


### 2) MovieLens 1M
This movie rating dataset has also been used extensively as a benchmark for collaborative filtering algorithms.
The dataset contains 1,000,209 anonymous ratings of approximately 3952 movies made by 6040 MovieLens users who joined 
MovieLens 2000. The ratings are made on a 5-star scale (whole-star ratings only). Each user has at least 20 ratings.

| problem setting | datasets | novel instances | novel targets | side-info instances | side-info targets | missing values in label matrix | type of target variable |
|----------|----------|----------|----------|----------|----------|----------|----------|
| Multi-label| Bibtex | yes | no | yes| no | no | binary |
| Classification | Delicious | yes | no | yes| no | no | binary |
|----------|----------|----------|----------|----------|----------|----------|----------|
| Multivariate| Osales | yes | no | yes| no | no | continuous |
| Regression | scm1d | yes | no | yes| no | no | continuous |
|----------|----------|----------|----------|----------|----------|----------|----------|
| Dyadic | EAS | yes | no | yes| yes | yes | continuous |
| Prediction | ExCAPE | yes | no | yes| yes | yes | real/continuous |
|----------|----------|----------|----------|----------|----------|----------|----------|
| Matrix | Netflix | no | no | no| no | yes | continuous |
| Completion | MovieLens1M | no | no | no| no | yes | continuous |
|----------|----------|----------|----------|----------|----------|----------|----------|
| Hierarchical | Netflix | yes | no | yes| hierarchical | no | binary |
| Multi-label Classification | MovieLens1M | yes | no | yes| hierarchical | no | binary |

