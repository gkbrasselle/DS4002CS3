# DS4002Project3

## Section 1: Software and platform section

This project was completed using Mac and Windows platforms. The coding language used was Python and the coding environments used were Google Colab and Gitpod. The Keras framwork was used, for which documentation can be accessed here: [https://pypi.org/project/face-recognition/](https://machinelearningmastery.com/how-to-perform-face-recognition-with-vggface2-convolutional-neural-network-in-keras)

## Section 2: Map of Documentation
### This repository is organized as follows:
1. DATA

    **FOLDER 1: "celebrity_images" contains the following:**

        -"celebrities" subfolder --> contains 25 subfolders, each dedicated to a unique celebrity. Each celeb subfolder contains 100 google images.

        -"celebrities_all" subfolder --> contains 25 subfolders, each dedicated to a unique celebrity. Each celeb subfolder contains the 100 original images for a unique celeb (sourced from the "celebrities" folder), as well as 300 augmented images for that celeb (sourced from the "celebrities_extra" folder).

        -"celebrities_extra" subfolder --> contains 25 subfolders, each dedicated to a unique celebrity. Each celeb subfolder contains 300 augmented images for that celebrity, as generated form the inital 100 photos.


    **FOLDER 2: "image_data" contains the following:**

        -**"celeb_image_data" subfolder with the following files:**

                -"all_celebs_image_data.csv" --> contains image data (brightness, celeb gender, etc.) for each of the 400 images in the complete "celebrities_all" folder (including augmented images). Each image is denoted with a filepath.

                -"celeb_image_data.csv" --> contains image data (brightness, celeb gender, etc.) for each of the 100 images in the "celebrities" folder (which does not include augmented images). Each image is denoted with a filepath.

        -**"incorrect_guesses_data" subfolder with the following files:**

                -"incorrect_guesses_data.csv" --> contains complete image data (brightness, celeb gender, etc.) for images which were incorrectly identified during the last testing epoch (epoch 100). Images are denoted with filepaths.

                -"incorrect_guesses_epoch_100.csv" --> contains a list of images which were incorrectly identified during the last tesing epoch (epoch 100). Created from incorrect_guesses.csv. This was later merged with "all_celebs_image_data.csv" to produce "incorrect_guesses_data.csv". 

                -"incorrect_guesses.csv" --> contains a full list of images which were misidentified in each epoch.

        -**"testing_epoch_data" subfolder with the following files:**

                -"epoch_results_v4.csv" --> a csv file containing the epoch number, the image filepath, the true class of the image, the predicted class of the image, and the confidence level of the guess
    
    
    **Data Appendix Project 3.pdf --> Data Appendix for all variables in the dataset used for project**

    **"haarcascade_frontalface_default.xml" --> contains a script containing facial encodings. This is used for facial identification.**
      
2. SCRIPTS
    - STEP1-initial_EDA.ipynb --> 

3. OUTPUT

    - Initial Celeb Dataset EDA.pdf --> contains graphs analyzing "celeb_image_data.csv". The initial 100 images are analyzed for each of the 25 celebs.

    - Misidentified Images EDA.pdf --> contains graphs analyzing "incorrect_guesses_data.csv". The graphs explore distributions in characteristics for images which were misidentified in the last epoch.

      
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

