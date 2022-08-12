# AI07_Project_3-Image-Classification

## Introduction
This project is about image classfication. 

You may obtain the dataset from https://data.mendeley.com/datasets/5y9wdsg2zt/2.

In the dataset, there are two classes of concrete image:<br>

"Negative" , which is equivalent to class "0" in my code, refer to the concrete images without crack on the surface.<br>
"Positive" , which is equivalent to class "1" in my code, refer to the concrete images with crack on the surface.<br>

Below are some of the sample images:<br>
![concrete_crack](https://user-images.githubusercontent.com/108325848/184343927-a8ad0902-af29-4222-a74f-7300927dbb08.png) <br>

The objective of this project is to construct a model that can classify the targeted images to one of two classes as stated above.<br>

In my first attempt, I employed the MobileNetV3 as my pretrained model to do transfer learning so that I don't have to construct the model's architecture to do image feature extraction by myself.<br>

You may refer to the code in [Project_3(MobileNetV3-based)](Project_3(MobileNetV3-based).ipynb) to study the whole process.<br>

Also, a CNN model was constructed in [Project_3(Simple CNN)](Project_3(Simple-CNN).ipynb) to make a comparision.<br>

## Result
|        Model        |    Accuracy    |   Time-Taken for training  |
|        :---:        |     :---:      |            :---:           | 
| MobileNetV3-based   |    ~99.7%      |        6 mins 02 secs      |
| Simple CNN          |    ~99.7%      |        1 hours 48 mins     |

Some prediction samples:<br>
![Sample_Prediction](https://user-images.githubusercontent.com/108325848/184414623-74ef5d68-78a9-4d06-9a05-e20c9003956a.png)<br>

## Remarks
From the results shown above, we see that both the transfer-learning approach and the self-construct CNN approach can achieve very high accuracy in image classification.<br>
The simple CNN model above, in fact, is highly simplified to save the cost of running time.<br>
By modifying the architecture of the CNN model, it is possible to further improve the accuracy of prediction.(I actually did this, and the code attached above is itself an improved version.)<br>
However, all this comes at the price of running time. (=Your priceless living time + our world's priceless natural resources!) <br>
Hence, I highly recommend using the transfer-learning approach in constructing models to do image classification.<br>
