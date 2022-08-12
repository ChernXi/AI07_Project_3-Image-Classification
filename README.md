# Project_3-Image-Classification

This project is about image classfication. There are two classes of road image here:<br>

Class "0" = negative, refer to the road images without crack on the surface.<br>
Class "1" = positive, refer to the road images with crack on the surface.<br>

Our code aims to classify the targeted images to one of two classes as stated above.<br>

In this code, I have employed the MobileNetV3 as my pretrained model to do transfer learning so that I don't have to construct the model's architecture to do image's feature extraction by myself.<br>

You may refer to the code ["Project_3(Using Transfer Learning)"](https://github.com/ChernXi/Project_3-Image-Classification/blob/main/Project_3(Using_Tranfer_Learning)%20.ipynb).<br>

Also, another CNN model was constructed to make a comparision.<br>

## Result
|        Model        |    Accuracy    |   Time-Taken   |
|        :---:        |     :---:      |     :---:      | 
| MobileNetV3-based   |  99.6%~99.8%   | 8 mins 20 secs |
| Simple CNN          |  99.6%~99.7%   | 1 hours 48 mins|

## Remarks
From the result shown above, we see that both tranfer-learning approach and self-construct CNN approach can achieve very high accuracy in image classification.<br>
The simple CNN model above in fact is highly simplified to save the cost of running time.<br>
By modifying the architecture of the CNN model, it is possible to further improve the accuracy of prediction.(I actually did this, and the code attached above is itself an improved version.)<br>
However, all this are on the price of running time.(=Your priceless living time + our world priceless natural resources!)
Hence, I highly recommend to use the transfer-learning approach in constructing model to do image classification.
