# CardsCVML

Computer Vision generative Dataset and Machine learning on playing cards

This project is using
  - python 3.6.7 and several libraries
  - opencv
  - CV libraries
  - imgaug
  
For full project go to **DatasetCreator.ipynb**

## Quick resume
#### 1: extract cards from videos 
![png](data_ex/output_17_2.png)

#### 2 : Get top and bottom corner
![png](data_ex/output_20_1.png)

#### 3 : affine selection by convexing select

![png](data_ex/output_23_1.png)

#### 4 : generate scenes with bbox's

![png](data_ex/output_32_1.png)


## Generated data example
![alt text](https://raw.githubusercontent.com/hugofloter/CardsCVML/master/data_ex/hand_ex.jpg)
  
 
## Train cards with YOLOv3 OR/AND Tensorflow and the generated datasets
### A. use Tensorflow on google colab
## B. Run the train and export  frozen model.pb with tf
## C. result with tf
here are the result at step 170k

![alt text](https://raw.githubusercontent.com/hugofloter/CardsCVML/master/data_ex/ML/result3.jpg)
![alt text](https://raw.githubusercontent.com/hugofloter/CardsCVML/master/data_ex/ML/result1.jpg)
![alt text](https://raw.githubusercontent.com/hugofloter/CardsCVML/master/data_ex/ML/result2.jpg)
![alt text](https://raw.githubusercontent.com/hugofloter/CardsCVML/master/data_ex/ML/result4.jpg)
