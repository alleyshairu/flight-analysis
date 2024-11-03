# Predicting Airplane Delays

## Context

Using machine learning techniques to identify whether the flight will be delayed due to weather.

## Dataset

The provided dataset contains scheduled and actual departure and arrival times reported by certified US air carriers that account for at least 1 percent of domestic scheduled passenger revenues. The data was collected by the Office of Airline Information, Bureau of Transportation Statistics (BTS). The dataset contains date, time, origin, destination, airline, distance, and delay status of flights for flights between 2014 and 2018.
The data are in 60 compressed files, where each file contains a CSV for the flight details in a month for the five years (from 2014 - 2018). The data can be downloaded from this link: [https://ucstaff-my.sharepoint.com/:f:/g/personal/ibrahim_radwan_canberra_edu_au/Er0nVreXmihEmtMz5qC5kVIB81-ugSusExPYdcyQTglfLg?e=bNO312]. Please download the data files and place them on a relative path. Dataset(s) used in this assignment were compiled by the Office of Airline Information, Bureau of Transportation Statistics (BTS), Airline On-Time Performance Data, available with the following link: [https://www.transtats.bts.gov/Fields.asp?gnoyr_VQ=FGJ]. 

## Two Notebooks 
1.  onpremises.ipynb (run on local machine) 
2.  cloud.ipynb (run using SageMaker on Amazon Cloud)

## Requirements
* Python >= 3.12 
* Jupyter 
* Git 
* Amazon SageMaker 

## Libraries / Dependencies 
```
pip install numpy
pip install seaborn 
pip install geopandas
pip install matplotlib
pip install scikit-learn 
pip install category_encoders 
pip install boto3
pip install sagemaker 
```

## On Premise Model Comparison

| Metric                  | Model 1       | Model 2 (Enhanced)|
|-------------------------|---------------|-----------------|
| **Accuracy**            | 0.79          | 0.62           |
| **Precision (Class 1)** | 0.52          | 0.29           |
| **Recall (Class 1)**    | 0.00          | 0.58           |
| **Specificity (Class 0)** | 1.00        | 0.62           |
| **F1-Score (Class 1)**  | 0.00          | 0.39           |

#### Confusion Matrix Comparison

| **Confusion Matrix**                  | Model 1       | Model 2 (Enhanced)|
|---------------------------------------|---------------|-----------------|
| True Negatives (TN)                   | 258462        | 161483         |
| False Positives (FP)                  | 70            | 97049          |
| False Negatives (FN)                  | 68511         | 28841          |
| True Positives (TP)                   | 75            | 39745          |

## License
This project is licensed under the MIT License - see the [LICENSE.md](./LICENSE) file for details.
