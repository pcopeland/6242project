# 6242project

## Description:
This package undertakes a comprehensive analysis of traffic congestion and extreme weather events in the United States over a six-year period, utilizing large datasets and advanced analytical techniques. By merging extensive traffic and weather datasets, conducting principal component analysis (PCA) for dimensionality reduction, and employing regression and ARIMA time series analysis, the package aims to uncover patterns and relationships within the data. Additionally, a change detection algorithm (CUSUM) is utilized to identify tipping points in deteriorating weather conditions.

Our approach provides insights into the complex interactions between traffic congestion and extreme weather events. Through ARIMAX modeling, we were able to effectively predicts weekly travel time across the US, with visibility serving as a significant exogenous variable. Interactive visualizations developed using Tableau facilitate spatial analysis, allowing users to explore traffic and weather patterns across different regions and time periods. Despite challenges in correlating weather events with traffic delays using change detection alone, the our analysis contributes insights to transportation research.

## Installation:
To begin, you should be sure that the following packages are install on your system or virtual environment:
- [Numpy](https://numpy.org/install/)
- [Seaborn](https://seaborn.pydata.org/installing.html)
- [Sklearn](https://scikit-learn.org/stable/install.html)
- [Statsmodel](https://www.statsmodels.org/stable/install.html)
- [Pandas](https://pandas.pydata.org/docs/getting_started/install.html)
- [Matplotlib]()

The above imports can be done easily via the terminal in MacOS, Windows Shell, or through the packages website. Below are some example commands that can be used to install packages in MaacOS:

```python
# install numpy
pip install numpy

# install seaborn
pip install seaborn

# install sklearn
pip install -U scikit-learn

# install statsmodel
python -m pip install statsmodels

# install pandas
pip install pandas

# install matplotlib
pip install 
```

## Execution:

### Clone the github repo

Once your packages are installed, you will need to clone [this repo](https://github.com/pcopeland/6242project) to you local machine to begin running the packages. If you are not familiar with the process, you can find a step by step guide in the provided link:

[Clone a GitHub Repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)

### Data processing in AWS with Pytorch
#### Uploading Data to S3

Our initial processing was done in AWS because of teh size of the datasets and teh required compuataional power. 

You will need to first download the [traffic](https://www.kaggle.com/datasets/sobhanmoosavi/us-traffic-congestions-2016-2022) and [weather](https://www.kaggle.com/datasets/sobhanmoosavi/us-weather-events) datasets from Kaggle.com. Save both files to the data folder inside the cloned repository.

1. Access S3 Service:
   - Navigate to the AWS Management Console.
   - Under "All services," find and click on "S3" listed under the Storage category.

2. Create a New Bucket:
   - In the S3 console, click on "Create Bucket."
   - Provide the necessary details such as bucket name and region.
   - Select the region as "US East (N. Virginia)" to avoid data transfer charges.
   - Click "Create Bucket" at the bottom of the screen.

3. Verify Bucket Creation:
   - A new bucket will now be visible in the S3 console.

4. Upload your data:
   - click on your new bucket it and it upload at the top to import your dataset in the bucket

#### Creating an Amazon Athena Workgroup

1. Navigate to Amazon Athena:
   - Go to Amazon Athena in the AWS console.
   - Select "Workgroups" from the left menu and click on "Create workgroup."

2. Set Up Workgroup:
   - Ensure the region is set to "N. Virginia." Change it if necessary.
   - Fill out the configuration fields:
       * Name your workgroup.
       * Choose "Apache Spark" as the Analytics Engine.
       * Select "LabRole" as the IAM service role from "Additional Configurations."
       * Complete the setup by clicking on "Create workgroup."

3. Create Notebook:
   - click on workgroup and hit "create notebook"
   - or if you want to upload this notebook hit "import File"

Once you have the data and notebook loaded, you should be able to run all cells. Once the notebook has finsished running, is will write a csv filed called 'merged.csv' to the data folder. 

### Run time_processing

The next step is to open the sarimax_cusum.ipynb and run all cells. 

This file fixes arrors in the datetime format required for time series analysis and visialization.

The notebook will write a file called df_clean2.csv to the data folder in the repo. 

### Run sarimax_cusum and regression

The last two notebooks can be run in any order. They deal with time series, change detection, and regression analysis. Feel free to examine the model outputs.

This concludes the user guide for out project.


