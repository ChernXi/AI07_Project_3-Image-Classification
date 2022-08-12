# AI07_Project_3-Image-Classification

This project is about image classfication. 

You may obtain the dataset from https://data.mendeley.com/datasets/5y9wdsg2zt/2.

In the dataset, there are two classes of concrete image:<br>

"Negative" , which is equivalent to class "0" in my code, refer to the concrete images without crack on the surface.<br>
"Positive" , which is equivalent to class "1" in my code, refer to the concrete images with crack on the surface.<br>

Below are some of the sample images:
![concrete_crack](https://user-images.githubusercontent.com/108325848/184343265-01b7cb56-8133-4f13-9635-6cba6062d24b.png)

The aims of this project is to construct a model that can classify the targeted images to one of two classes as stated above.<br>

In my first attempt, I employed the MobileNetV3 as my pretrained model to do transfer learning so that I don't have to construct the model's architecture to do image feature extraction by myself.<br>

You may refer to the code in [Project_3(MobileNetV3-based)](Project_3(MobileNetV3-based).ipynb) to study the whole process.<br>

Also, a CNN model was constructed in [Project_3(Simple CNN)](Project_3(Simple-CNN).ipynb) to make a comparision.<br>

## Result
|        Model        |    Accuracy    |   Time-Taken for training  |
|        :---:        |     :---:      |            :---:           | 
| MobileNetV3-based   |  99.6%~99.8%   |        8 mins 20 secs      |
| Simple CNN          |  99.6%~99.7%   |        1 hours 48 mins     |

## Remarks
From the results shown above, we see that both the transfer-learning approach and the self-construct CNN approach can achieve very high accuracy in image classification.<br>
The simple CNN model above, in fact, is highly simplified to save the cost of running time.<br>
By modifying the architecture of the CNN model, it is possible to further improve the accuracy of prediction.(I actually did this, and the code attached above is itself an improved version.)<br>
However, all this comes at the price of running time. (=Your priceless living time + our world's priceless natural resources!) <br>
Hence, I highly recommend using the transfer-learning approach in constructing models to do image classification.<br>
