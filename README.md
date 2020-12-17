# Facial Expression Recognition
A human facial emotional detector.<br>
<br>
## Data 
Here's the data we're going to process to train and test our models.<br>
The data is [FER-2013](https://www.kaggle.com/msambare/fer2013) from Kaggle.
<br>
The data consists of 48x48 pixel grayscale images of faces. The faces have been automatically registered so that the face is more or less centred and occupies about the same amount of space in each image.<br>
<br>
The task is to categorize each face based on the emotion shown in the facial expression into one of seven categories (*0=Angry, 1=Disgust, 2=Fear, 3=Happy, 4=Sad, 5=Surprise, 6=Neutral*). The training set consists of **28,709 examples** and the public test set consists of **3,589 examples**.
<br>
The data on [Kaggle](https://www.kaggle.com/msambare/fer2013) comprises of *2* folder (*train and test*) each of which has futher *7* folders ( *Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral*) which contains the images in *jpg* file format.<br>
<br>
The distribution of images per category was:
| Data Type | Surprise | Fear | Angry | Neutral | Sad  | Disgust | Happy | Total |
| :-------: | :------: | :--: | :---: | :-----: | :--: | :-----: | :---: | :---: |
| Train     | 3171     | 4097 | 3995  | 4965    | 4830 | 436     | 7215  | 28709 |
| Test      | 831      | 1024 | 958   | 1233    | 1247 | 111     | 1774  | 7178  |
<br>
As you can see the data of **Disgust** was very less as compared to the categories and that of Happy was very large. So, I perform image rotation **data augmentation** operations to increase the data of digust. After the operation the Data Stats were:
<br>
| Data Type | Surprise | Fear | Angry | Neutral | Sad  | **Disgust** | Happy | **Total** |
| :-------: | :------: | :--: | :---: | :-----: | :--: | :---------: | :---: | :-------: |
| Train     | 3171     | 4097 | 3995  | 4965    | 4830 | **3171**    | 7215  | **31444** |
| Test      | 831      | 1024 | 958   | 1233    | 1247 | **111**     | 1774  | **7178**  |
<br>
<br>
Before starting making the model, first upload the data into *csv files* using [Data Uploading Code](https://github.com/dochimekashiariri/Facial-Expression-Recognition/blob/master/data_uploading.ipynb)<br>
<br>
## Summary
| Model                                   |      Accuracy after 60 epoches     | Loss after 60 epoches |
| :-------------------------------------: | :--------------------------------: | :-------------------: |
|Convolutional Neural Network (CNN)       | 63.806%                            | 0.99006               |
|Residual Neural Network (ResNet)         | 63.597%                            | 1.28889               |
