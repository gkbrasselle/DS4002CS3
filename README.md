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

1. Extract the data from the links above in Section II. Copy and paste into an excel sheet and convert the file to a CSV file. The file named "DS4002-Project2-Data-CLEANED.csv" can also be accessed in the DATA folder. This is the cleaned dataset and can be used for ease of replicating.  
3. Navigate to "project2_script.ipynb" file, which is located in the SCRIPTS folder.
4. Load the datset using the code in the file, and then follow the code to perform inital EDA. Using the code from "p2dataappendix.R" in the SCRIPTS folder, this will display additional summary statistics of variables included in the dataset.
5. Navigate back to "project2_script.ipynb" in the SCRIPTS folder, begin the ARIMA modeling process after downloading the necessary Python libraries. Select appropriate values for p, d, and q values using the data visualizations created in the code. The code under the "Choosing best ARIMA parameters" section consists of some tests and plots used to determine appropriate parameters. Feel free to change the parameters if you feel there are more fitting values.
6. The second part of the ARIMA modeling process is the code located under the "Now actually using the ARIMA model" section. This is where ARIMA will use the historical wage ratio data from 1960-2000 to predict the wage ratios for 2001-2019. A model fit summary and dataframe of the predicted and actual wage ratios will be generated to easily compare the values. 
7. Then, the MSE, RMSE, and residuals are calculated. The code will plot the residuals on a plot, display summary statistics of the residuals, and display a graphic of the actual and predicted wage ratios.
8. Lastly, the section "Attempting To Model Using Holt's Dampened Trend" is a little extra code we deployed that tried to forcast the wage ratio using exponential smoothing techniques. This step is optional.

## References
[1] 	B. Etienne, “Time Series in Python — Exponential Smoothing and ARIMA processes,” TowardsDataScience.com, https://towardsdatascience.com/time-series-in-python-exponential-smoothing-and-arima-processes-2c67f2a52788 (accessed Oct. 23, 2024).  
[2] 	D. Abugaber, “Chapter 23: Using ARIMA for Time Series Analysis,” University of Illinois Chicago, https://ademos.people.uic.edu/Chapter23.html/ (accessed Oct. 10, 2024).  
[3] 	J. Brownlee, “How to create an Arima model for time series forecasting in Python,” MachineLearningMastery.com, https://machinelearningmastery.com/arima-for-time-series-forecasting-with-python/ (accessed Oct. 18, 2024).  
[4]	Fuqua School of Business, Introduction to ARIMA models, https://people.duke.edu/~rnau/411arim.htm (accessed Oct. 18, 2024).  
