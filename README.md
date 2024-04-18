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

##

# install multiple extras together
pip install pycaret[analysis,models]



## Execution:
