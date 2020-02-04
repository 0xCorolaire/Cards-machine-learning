# CardsCVML

Computer Vision generative Dataset and Machine learning on playing cards

This project is using
  - python 3.6.7 and several libraries
  - opencv
  - CV libraries
  - imgaug
  
For full project go to **DatasetCreator.ipynb**

## Quick resume
#### 1 : extract cards from videos 
- Load video from phone or camera
- use cv2 lib to capture video and find countours of card

![png](data_ex/output_17_2.png)  <!-- .element height="50%" width="50%" -->

#### 2 : Get top and bottom corner
- cv2 to check both corners to match the entire sign
- idea is to label all sign of the card

![png](data_ex/fiirst.png)  <!-- .element height="50%" width="50%" -->

#### 3 : affine selection by convexing select
- using opencv findCountours functions and aprox

![png](data_ex/secondd.png)  <!-- .element height="50%" width="50%" -->

#### 4 : generate scenes with bbox's
- Load background random dataset
- Load all card from pickle file and store them in a var
- use imgaug and shapely to transform image using img transformation for card and BoundingBoxes

![png](data_ex/thirddd.png)  <!-- .element height="50%" width="50%" -->


## Generated data example
![alt text](https://raw.githubusercontent.com/hugofloter/CardsCVML/master/data_ex/hand_ex.jpg)  <!-- .element height="50%" width="50%" -->
  
 
## Train cards with Tensorflow and the generated datasets
CNNs are regularized versions of multilayer perceptrons. Multilayer perceptrons usually mean fully connected networks, that is, each neuron in one layer is connected to all neurons in the next layer. The "fully-connectedness" of these networks makes them prone to overfitting data. 

CNNs take advantage of the hierarchical pattern in data and assemble more complex patterns using smaller and simpler patterns. Therefore, on the scale of connectedness and complexity, CNNs are on the lower extreme.

The hidden layers are mostly convolutional layers : 
+ Input is a tensor with shape (number of images) x (image width) x (image height) x (image depth).
+ Convolutional kernels whose width and height are hyper-parameters, and whose depth must be equal to that of the image => using image convulution to reduce dimension
+ Convolutional networks may include local or global pooling layers to streamline the underlying computation. Pooling layers reduce the dimensions of the data by combining the outputs of neuron clusters at one layer into a single neuron in the next layer
+ Activation layers :  **ReLu layers**  that removes negative values from an activation map by setting them to zero and maight be some **Pooling layers**


### A. Used algorithm : Faster R-CNN Inception V2

In the R-CNN algorithm, we feed the input image to the CNN to generate a convolutional feature map

### B. use Tensorflow on google colab

Setup environnement, CuDa and so on on a jupyter collab file and run model
Then, we run the train and export frozen model.pb with tf

## C. result with tf
Analysis can be found : https://github.com/hugofloter/Cards-machine-learning/blob/master/analyse_tensorflow.ipynb

**F1 score obtained : 0.8125**

here are the result at step 50k

![alt text](https://raw.githubusercontent.com/hugofloter/CardsCVML/master/data_ex/ML/result3.jpg)  <!-- .element height="50%" width="50%" -->
![alt text](https://raw.githubusercontent.com/hugofloter/CardsCVML/master/data_ex/ML/result1.jpg)  <!-- .element height="50%" width="50%" --> 
![alt text](https://raw.githubusercontent.com/hugofloter/CardsCVML/master/data_ex/ML/result2.jpg)  <!-- .element height="50%" width="50%" -->
![alt text](https://raw.githubusercontent.com/hugofloter/CardsCVML/master/data_ex/ML/result4.jpg)  <!-- .element height="50%" width="50%" -->
