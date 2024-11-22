# DS4002Project3

## Section 1: Software and platform section

This project was completed using Mac and Windows platforms. The coding language used was Python and the coding environments used were Google Colab and Gitpod. The Keras framwork was used, for which documentation can be accessed here: [https://pypi.org/project/face-recognition/](https://machinelearningmastery.com/how-to-perform-face-recognition-with-vggface2-convolutional-neural-network-in-keras)

## Section 2: Map of Documentation
### This repository is organized as follows:
1. DATA
    - celeb_image_data.csv --> initial dataset used for analysis. This dataset reflects all of the images in the "celebrities" folder, which are separated into celebrity folders with 100 images per celeb.
    
    - Data Appendix Project 3.pdf --> Data Appendix for all variables in the dataset used for project
      
2. SCRIPTS
    - p3dataappendix.R --> a script containing the code used to produce summary statistics and histograms for the data appendix
    - step1_testing.ipynb --> 
    - step2_EDA.ipynb --> script containing the intial exploratory data analysis plots
    - final_testing_v4.ipynb --> the final file used to train and test the model
    - epoch_analysis.ipynb --> a script containing commands to isolate the incorrect guesses of the model 

3. OUTPUT
    - epoch_results.csv --> a csv file containing the epoch number, the image filepath, the true class of the image, the predicted class of the image, and the confidence level of the guess
    - incorrect_guesses.csv --> a csv file containing information about the incorrect guesses of the model
    - incorrect_guesses_epoch_100.csv --> a csv file containing all the incorrect guesses from the last epoch (created from incorrect_guesses.csv)

      
5. LICENSE
6. README.md
  
## Section 3: Instructions for reproducing results

### Please follow these steps in order to replicate this project's experimental design:

1. Download celebrity images on Google, separating them into folders by celebrity name, such as "Margot-Robbie" or "Will-Smith." Ensure that each folder contains 100 celebrity images, labelled 01-100. Alternatively, use the image folders pre-collected in the "celebrities" folder for ease of replication.
2. Navigate to the "step1_testing.ipynb" in the "SCRIPTS" folder. Install the necessary libraries / dependencies to run the code (listed at the top of the file).
3. Next, open the "step2_EDA.ipynb" in the "SCRIPTS" folder to create some visuals. This will help better understand the variables used in the dataset.

## References
[1] 	J. Brownlee, “How to Perform Face Recognition With VGGFace2 in Keras,” Machine Learning Mastery, https://machinelearningmastery.com/how-to-perform-face-recognition-with-vggface2-convolutional-neural-network-in-keras// (accessed Nov. 15, 2024).   
[2]	A. Najibi, “Racial Discrimination in Face Recognition Technology,” Science in the News, https://sitn.hms.harvard.edu/flash/2020/racial-discrimination-in-face-recognition-technology/ (accessed Nov. 9, 2024).   
[3]	A. Rosebrock, “Keras ImageDataGenerator and Data Augmentation,” Pyimagesearch, https://pyimagesearch.com/2019/07/08/keras-imagedatagenerator-and-data-augmentation/ (accessed Nov. 14, 2024).   
[4]	opencv, “Haarcascades,” Github, https://github.com/opencv/opencv/tree/master/data/haarcascades/ (accessed Nov. 14, 2024).   
[5]	A. Jawabreh, “Exploring the Most Advanced Deep Learning Algorithm For Facial Detection,” Medium, ​​https://medium.com/the-modern-scientist/multi-task-cascaded-convolutional-neural-network-mtcnn-a31d88f501c8/ (accessed Nov. 14, 2024).   

