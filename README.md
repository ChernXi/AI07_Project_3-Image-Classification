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
