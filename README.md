# Computer-Vision-openCV-and-DL-smiling-not-smiling
Use OpenCV and deep neural network to detect if a person is smiling Or not -- A  case of Binary Classification...
# The Basic Pipeline for this Classification includes

1. Getting the training Dataset : We use Smiles Dataset having arond 13500 smiling and not smiling grayscale pictures.With non-smiling to smiling ratio of 2.96. 
2. Since this is a Grayscale image  we use LeNet Network which has only one channel and the input image is 28 * 28 * 1 shape.
3. We preprocess the image : 
a) by reshaping the image to 28 * 28.
b) normalizing the image to [0 - 255] range.
convert the labels smiling and non smiling into one hot encoding [0 ,1] and [1,0]
c) we then tackle the dataset imbalance by changing the weights appropriately.
Finally we train the network using LeNet architecture ([Conv2D] >> [relu]>> [maxpooling])* 2 => Fully connected layer => sigmoid => binary classification

# Prediction :
We use openCV along with the pretrained Haar Cascades(Viola Jones Algorithm) that come with it , to localise the face in the new image provided , once the face is detected then we go on to feed the face into the network , the inage is forward propagated through the network to get the predictions and using the labels we classify whether the image is that of a smiling person or not smiling person.

# Extension :

we can feed a video to openCV to detect smiling or not smiling person in real time.

Codes on the way...
