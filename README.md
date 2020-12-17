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
The distribution of images per category was:<br>
<table>
  <tr>
    <th>Data Type</th>
    <th>Surprise</th>
    <th>Fear</th>
    <th>Angry </th>
    <th>Neutral</th>
    <th>Sad</th>
    <th>Disgust</th>
    <th>Happy</th>
    <th>Total</th>
  </tr>
  <tr>
    <td>Train</td>
    <td>3171</td>
    <td>4097</td>
    <td>3995</td>
    <td>4965</td>
    <td>4830</td>
    <td>436</td>
    <td>7215</td>
    <td>28709</td>
  </tr>
  <tr>
    <td>Test</td>
    <td>831</td>
    <td>1024</td>
    <td>958</td>
    <td>1233</td>
    <td>1247</td>
    <td>111</td>
    <td>1774</td>
    <td>7178</td>
  </tr>
</table>
As you can see the data of **Disgust** was very less as compared to the categories and that of Happy was very large. So, I perform image rotation **data augmentation** operations to increase the data of digust. After the operation the Data Stats were:<br>
<br>
<table>
  <tr>
    <th>Data Type</th>
    <th>Surprise</th>
    <th>Fear</th>
    <th>Angry </th>
    <th>Neutral</th>
    <th>Sad</th>
    <th><b>Disgust</b></th>
    <th>Happy</th>
    <th>Total</th>
  </tr>
  <tr>
    <td>Train</td>
    <td>3171</td>
    <td>4097</td>
    <td>3995</td>
    <td>4965</td>
    <td>4830</td>
    <td><b>3171</b></td>
    <td>7215</td>
    <td><b>31444</b></td>
  </tr>
  <tr>
    <td>Test</td>
    <td>831</td>
    <td>1024</td>
    <td>958</td>
    <td>1233</td>
    <td>1247</td>
    <td><b>111</b></td>
    <td>1774</td>
    <td><b>7178</b></td>
  </tr>
</table>
Before starting making the model, first upload the data into *csv files* using [Data Uploading Code](https://github.com/dochimekashiariri/Facial-Expression-Recognition/blob/master/data_uploading.ipynb)<br>
<h2>Results</h2>
<table>
  <tr>
    <th>Model</th>
    <th>Accuracy after 60 epoches</th>
    <th>Loss after 60 epoches</th>
  </tr>
  <tr>
    <td>Convolutional Neural Networks</td>
    <td>63.806%</td>
    <td>0.99006</td>
  </tr>
  <tr>
    <td>Residual Neural Networks</td>
    <td>63.597%</td>
    <td>1.28889</td>
  </tr>
</table>
