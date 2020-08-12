# Stock-Machine-Learning
Utilized Machine Learning to predict stock performance

Stock investment has always been my personal interest, in this project, I want to try to ingetrage Data Science with Stock investment to see whether I can get any meaningful insight, or if I can apply any machine learning techniques to predict whether the stock can outperform SP500 index fund.


 
## Data Gathering
#### Stock market data
http://theautomatic.net/yahoo_fin-documentation/
pip install yahoo_fin
pip install requests_html
from yahoo_fin.stock_info import *
#library for the sector information
pip install datapackage

*get sp500 list
tickers = tickers_sp500()

#### Stock Sector information
import datapackage
import pandas as pd

data_url = 'https://datahub.io/core/s-and-p-500-companies/datapackage.json'

*to load Data Package into storage
package = datapackage.Package(data_url)

*to load only tabular data
resources = package.resources
for resource in resources:
    if resource.tabular:
        data = pd.read_csv(resource.descriptor['path'])
        print (data)
        
        
        
## Data Exploration
#### Univariate
Continuous Variable 
Categorical Variable
#### Correlation

#### Cleaning Missing Values

#### Encoding: convert categorical features to values


## Feature Importance
#### SelectKBest

#### RFE

#### Random Forest

#### Decision Tree

## Machine Learning
#### Logistic Regression
#### KNN
#### Gaussian Naive Bayes
#### Stochastic Gradient Descent

