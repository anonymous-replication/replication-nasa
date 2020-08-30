
# Replication Package for NASA project

This project is able to effectively predict the defects in selected projects from the NASA data program. The dataset is mostly composed of Halstead and McCabe software quality metrics.

## Getting Started

These instructions get you a copy of the project up and running on your local machine for testing and further explorations of the data.

### Prerequisites

You need to install some packages to use our replication package. The *requirements.txt* file in the root directory stores all the necessary packages. We strongly recommend using either Linux or Mac to execute this package. Windows is not supported by default, but you may get it working there too.

<h4>1) Requirements Installation</h4>

Practical example assuming you are in the root project:

```shell
virtualenv -p python3 venv
source venv/bin/activate
python3 install -r requirements.txt
```

<h4>2) Data</h4>

We make available both versions of the NASA data. The raw data in which can be downloaded from [PROMISE](http://promise.site.uottawa.ca/SERepository/), and the processed data.

<h5>2.1) Raw Data</h5>

This folder contains the raw data of the nine NASA projects.

<h5>2.2) Processed Data</h5>

This folder contains the processed data of the nine NASA projects.

<h4>3) RS-XGB</h4>

Our implementation of XGBoost using the random space of features is available under the **src** folder. The algorithm can be executed as follows (using CM1 project):

```shell
python3 src/exploration.py data/processed/CM1-processed.csv
```

In this version, we serialize each model in a file called **models.pkl**.
