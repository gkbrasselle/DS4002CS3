# DS4002Project3
# This is just copied from project 2 but will edit later 
## Section 1: Software and platform section

This project was completed using Mac and Windows platforms. The coding language used was Python and the coding environment used was Google Colab. The face-recognition package in Python was used, for which documentation can be accessed here: https://pypi.org/project/face-recognition/

## Section 2: Map of Documentation
### This repository is organized as follows:
1. DATA
    - DS4002-Project2-Data.csv --> orginial dataset before cleaning
    - DS4002-Project2-Data-CLEANED.csv --> cleaned dataset with no N/As
    - 20th_century_data.csv --> data from the cleaned dataset, but only from 1960-2001 for the ARIMA modeling 
    - Data Appendix Project 2.pdf --> Data Appendix for all variables in the dataset used for project
      
2. SCRIPTS
    - project2_script.ipynb --> a full script containing all of the code needed to reproduce results
    - p2dataappendix.R --> a script containing the code used to produce EDA plots in the data appendix
    - archived.ipynb --> contains outdated files that have been kept in case of future use

3. OUTPUT
    - EDA Output Project 2.pdf --> Exploratory Data plots
    - MI3 - ARIMA Testing Output and RMSE/Residuals --> a document with all of the plots and tables from conducting ARIMA model and residual calculations; also has some extra code using the Holt-Winters method for forecasting 
      
4. LICENSE.md
5. README.md

#### CURRENT DATASET VARIABLES:

1. Female_LFPR --> https://www.bls.gov/opub/reports/womens-databook/2021/
     * Click on "Table 2. Employment status of the civilian noninstitutional population, 16 years and older, by gender, 1948–2020 annual averages (numbers in thousands)"
     * Scroll down to the "women" section
   
2. Bachelor_percentage --> https://www.statista.com/statistics/184272/educational-attainment-of-college-diploma-or-higher-by-gender/
   
3. Wage_ratio --> https://www.pay-equity.org/info-time.html

4. First_Birth_Median_Age --> https://www.humanfertility.org/
     * In "HFD summary indicators" section, select "Mean Age at Birth"
     * This will download an excel sheet
     * Copy and paste the data from the U.S. column
  
## Section 3: Instructions for reproducing results

### Please follow these steps in order to replicate this project's experimental design:

1. Download celebrity images on google, separating them into folders by celebrity name (ex: "Margot-Robbie"). Ensure that each folder contains 100 celebrity images, labelled 01-100. Alternatively, use the image folders pre-collected in the "celebrities" folder.
2. Navigate to the "step1_testing.ipynb" in the "SCRIPTS" folder.

## References
[1] 	B. Etienne, “Time Series in Python — Exponential Smoothing and ARIMA processes,” TowardsDataScience.com, https://towardsdatascience.com/time-series-in-python-exponential-smoothing-and-arima-processes-2c67f2a52788 (accessed Oct. 23, 2024).  
[2] 	D. Abugaber, “Chapter 23: Using ARIMA for Time Series Analysis,” University of Illinois Chicago, https://ademos.people.uic.edu/Chapter23.html/ (accessed Oct. 10, 2024).  
[3] 	J. Brownlee, “How to create an Arima model for time series forecasting in Python,” MachineLearningMastery.com, https://machinelearningmastery.com/arima-for-time-series-forecasting-with-python/ (accessed Oct. 18, 2024).  
[4]	Fuqua School of Business, Introduction to ARIMA models, https://people.duke.edu/~rnau/411arim.htm (accessed Oct. 18, 2024).  
