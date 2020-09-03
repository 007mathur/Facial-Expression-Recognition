# Facial Expression Recognition
A human facial emotional detector.<br>
<br>
## Data 
Here's the data we're going to process to train and test our models.<br>
The data is [FER-2013](https://www.kaggle.com/msambare/fer2013) from Kaggle.
<br>
The data consists of 48x48 pixel grayscale images of faces. The faces have been automatically registered so that the face is more or less centred and occupies about the same amount of space in each image.<br>
<br>
The task is to categorize each face based on the emotion shown in the facial expression into one of seven categories (*0=Angry, 1=Disgust, 2=Fear, 3=Happy, 4=Sad, 5=Surprise, 6=Neutral*). The training set consists of **28,709 examples** and the public test set consists of **3,589 examples**.<br>
<br>
The data on [Kaggle](https://www.kaggle.com/msambare/fer2013) comprises of *2* folder (*train and test*) each of which has futher *7* folders ( *Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral*) which contains the images in *jpg* file format.<br>
<br>
Before starting making the model, first upload the data into *csv files* using [Data Uploading Code](https://github.com/dochimekashiariri/Facial-Expression-Recognition/blob/master/data_uploading.ipynb)<br>
<br>
## Summary
| Model                                   |      Accuracy after 50 epoches     | Loss after 50 epoches |
| :-------------------------------------: | :--------------------------------: | :-------------------: |
| ....................................... | .................................. | ..................... |
|Convolutional Neural Network (CNN)       | 61.298%                            | 1.14859               |
|Residual Neural Network (ResNet)         | 61.033%                            | 1.03836               |
