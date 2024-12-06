# DS4002 Case Study

## Section 1: Software and platform section

This project was completed using Mac and Windows platforms. The coding language used was Python and the coding environments used were Google Colab and Gitpod. The Keras framwork was used, for which documentation can be accessed here: [https://pypi.org/project/face-recognition/](https://machinelearningmastery.com/how-to-perform-face-recognition-with-vggface2-convolutional-neural-network-in-keras)

In order to run the files, install the following packages / libraries:

pip install pandas

pip install pillow

pip install seaborn

pip install matplotlib

pip install numpy

pip install imutils

pip install opencv-python

pip install tensorflow

pip install scipy

pip install facenet-pytorch

pip install scikit-learn

## Section 2: Map of Documentation
### This repository is organized as follows:
1. DATA
      -"celebrities" subfolder --> contains 25 subfolders, each dedicated to a unique celebrity. Each celeb subfolder contains 100 google images.
      -"haarcascade_frontalface_default.xml" --> contains documentation for Haar Cascade facial encodings. This is used for facial identification in the "keras_recognition.ipynb" file**
      
2. SCRIPTS
    - initial_EDA.ipynb --> A script which uses "celeb_image_data.csv" to produce the EDA graphs in "Initial Celeb Dataset EDA".
    - image_processing.ipynb --> A script used to process the 100 images for each celeb (as contained within the "celebrities" subfolderwithin "celebrity_images"), applying transformations to the images in order to create an addition 300 augmented images per celeb. The extra augmented images are saved to the "celebrities_extra" folder.
    - keras_recognition.ipynb --> A script used to test if image augmentation was successful (i.e: by using tensorflow to see if the images in "celebrities_extra" contain faces, etc.)
    - final_testing.ipynb --> A script which uses Keras to train a model to correctly identify celebrity faces. The base dataset used is "celebrities_all" from the "celebrity_images" folder. 100 testing epochs are used.
    - epoch_analysis.ipynb --> A script which analyzes the model's facial identifiaction accuracy across epochs.

3. REFERENCES
    - Contains articles providing background information about the case study topic
    - Additional Keras documentation can be found at https://keras.io/
4. LICENSE
5. README.md
  
## Section 3: Instructions for reproducing results

### Please follow these steps in order to replicate this project's experimental design:

1. To gather the data, begin by identifying at least 25 selected celebrities of interest. Download 100 images of each celebrity from Google images, ensuring that there are no other faces/people within the image. Organize them into separate folders labeled with celebrity name in the format "First-Last". Each image within the folder should be titled with the format "##.jpg", using zeroes as placeholders for the tens place if necessary. Alternatively, use the image folders pre-collected in the "/DATA/celebrity_images/celebrities" folder for ease of replication.

2. Navigate to the "initial_EDA.ipynb" file in the scripts folder. Using the code, generate a dataframe to classify the celebrity images, in addition to producing the graphs for "Initial Celeb Dataset EDA.ipynb".

3. Using the script "image_processing.ipynb", generate 300 augmented images for each celebrity in the "celebrities" folder using image transformations. This will produce 400 images for each celebrity. The augmented folders will be saved into the "celebrities_extra" folder, whereas the entire set of photos will be saved to the "celebrities_all" folder. The latter folder will be the one used for Keras testing.

4. Using the "keras_recognition.ipynb" file, testing out tensorflow by running some tests on the augmentated images. This will ensure that the images were properly modified.

5. Using the "final_testing.ipynb" script, build a simple CNN model for use in testing. The script will utilize Keras, running 100 epochs to train the model to correctly identify celebrity images. Results will be saved to the "epoch_results.csv" file in the data folder.

6. Using the "epoch_analysis.ipynb" script, generate the "incorrect_guesses_data.csv" and "incorrect_guesses_epoch_100.csv" files, which should be saved to the data folder. These data files contain data for images which were incorrectly identified by the model during tests. "incorrect_guesses_data.csv" will contain incorrect guesses for all epochs, whereas "incorrect_guess_epoch_100.csv" will contain data only for incorrct guesses in the final epoch.

7. Use the generated .csv files to analyze the results and perform initial EDA as needed


## References
[1] 	J. Brownlee, “How to Perform Face Recognition With VGGFace2 in Keras,” Machine Learning Mastery, https://machinelearningmastery.com/how-to-perform-face-recognition-with-vggface2-convolutional-neural-network-in-keras// (accessed Nov. 15, 2024). 

[2]	A. Najibi, “Racial Discrimination in Face Recognition Technology,” Science in the News, https://sitn.hms.harvard.edu/flash/2020/racial-discrimination-in-face-recognition-technology/ (accessed Nov. 9, 2024). 

[3]	A. Rosebrock, “Keras ImageDataGenerator and Data Augmentation,” Pyimagesearch, https://pyimagesearch.com/2019/07/08/keras-imagedatagenerator-and-data-augmentation/ (accessed Nov. 14, 2024). 

[4]	opencv, “Haarcascades,” Github, https://github.com/opencv/opencv/tree/master/data/haarcascades/ (accessed Nov. 14, 2024). 

[5]	A. Jawabreh, “Exploring the Most Advanced Deep Learning Algorithm For Facial Detection,” Medium, ​​https://medium.com/the-modern-scientist/multi-task-cascaded-convolutional-neural-network-mtcnn-a31d88f501c8/ (accessed Nov. 14, 2024). 

[6] 	“Convolutional Neural Network (CNN) in Machine Learning,” Geeks For Geeks, https://www.geeksforgeeks.org/convolutional-neural-network-cnn-in-machine-learning/ (accessed Nov. 15, 2024). 

[7] 	J. Brownlee, “Gentle Introduction to the Adam Optimization Algorithm for Deep Learning,” Machine Learning Mastery, https://machinelearningmastery.com/adam-optimization-algorithm-for-deep-learning/ (accessed Nov. 15, 2024).  

[8]	“Facial Recognition Advertising for Better Targeting,” Business News Daily. Accessed: Dec. 05, 2024. [Online]. Available: https://www.businessnewsdaily.com/15213-walgreens-facial-recognition.html

[9]	“‘We try to use it as much as we can’: How facial recognition became a routine policing tool in America,” NBC News. Accessed: Dec. 05, 2024. [Online]. Available: https://www.nbcnews.com/news/us-news/how-facial-recognition-became-routine-policing-tool-america-n1004251

[10] 	SITNFlash, “Racial Discrimination in Face Recognition Technology,” Science in the News. Accessed: Dec. 05, 2024. [Online]. Available: https://sitn.hms.harvard.edu/flash/2020/racial-discrimination-in-face-recognition-technology/

[11] 	“Biased Technology: The Automated Discrimination of Facial Recognition | ACLU of Minnesota.” Accessed: Dec. 05, 2024. [Online]. Available: https://www.aclu-mn.org/en/news/biased-technology-automated-discrimination-facial-recognition

