# AI07_Project_3-Image-Classification

## 1. Introduction
This project is about image classfication. 

You may obtain the dataset from https://data.mendeley.com/datasets/5y9wdsg2zt/2.

In the dataset, there are two classes of concrete image:<br>

"Negative" , which is equivalent to class "0" in my code, refer to the concrete images without crack on the surface.<br>
"Positive" , which is equivalent to class "1" in my code, refer to the concrete images with crack on the surface.<br>

Below are some of the sample images:<br>
![concrete_crack](https://user-images.githubusercontent.com/108325848/184343927-a8ad0902-af29-4222-a74f-7300927dbb08.png) <br>

## 2. Objective 
The objective of this project is to construct a model that can classify the targeted images to one of two classes as stated above.<br>

## 3. IDE and Framework
The main IDE of this project is [Google Colab](https://colab.research.google.com/?utm_source=scs-index). <br>
The main frameworks used in this project are: [Tensorflow Keras](https://keras.io/about/), [Numpy](https://www.w3schools.com/python/numpy/numpy_intro.asp#:~:text=NumPy%20is%20a%20Python%20library,you%20can%20use%20it%20freely.), and [Matplotlib](https://matplotlib.org/stable/gallery/index.html).<br>

## 4. Methodology
In my first attempt, I employed the MobileNetV3Small as my pretrained model to do transfer learning.<br>
The MobileNetV3Small model will take care of the features extraction part, so I only add some dense layers as the classification layers to the model's architecture.<br>

You may refer to the code in [Project_3(MobileNetV3-based)](Project_3(MobileNetV3-based).ipynb) to study the whole process.<br>
The framework of the MobileNetV3-based model is as below:<br>
![image](https://user-images.githubusercontent.com/108325848/184523287-0a0947cf-6d30-4249-961a-0535b75aa8fb.png)

Also, a CNN model was constructed in [Project_3(Simple CNN)](Project_3(Simple_CNN).ipynb) to make a comparision.<br>
Here, 3 convolutional layers were used as the features extraction layers.<br>
The framework of the simple CNN model is as below:<br>
![image](https://user-images.githubusercontent.com/108325848/184534510-cd76e512-e4c2-46d4-bbdc-fc3e19669bae.png)

## 5. Result
|        Model        |    Accuracy    |   Time-Taken for training  |
|        :---:        |     :---:      |            :---:           | 
| MobileNetV3-based   |    ~99.9%      |        6 mins 02 secs      |
| Simple CNN          |    ~99.7%      |        1 hours 48 mins     |

Test loss and Test Accuracy of MobileNetV3-based model: <br>
![image](https://user-images.githubusercontent.com/108325848/184522697-984922be-7895-4573-8b37-82cc6479b518.png)

Some prediction samples:<br>
![image](https://user-images.githubusercontent.com/108325848/184523361-d19efcf3-382f-42a6-b9d1-9aa35a580dfd.png) <br>

## 6. Remarks
From the results shown above, we see that both the transfer-learning approach and the self-construct CNN approach can achieve very high accuracy in image classification.<br>
The simple CNN model above, in fact, is highly simplified to save the cost of running time.<br>
By modifying the architecture of the CNN model, it is possible to further improve the accuracy of prediction.(I actually did this, and the code attached above is itself an improved version.)<br>
However, all this comes at the price of running time. (=Your priceless living time + our world's priceless natural resources!) <br>
Hence, I highly recommend using the transfer-learning approach in constructing models to do image classification.<br>
