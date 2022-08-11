# Project_3-Image-Classification

This project is about image classfication.<br>
There are two classed of road image here:<br>
Class "0" = negative, refer to the road images without crack on the surface.<br>
Class "1" = positive, refer to the road images with crack on the surface.<br>

Our code aims to classify the targeted images to one of two classes as stated above.<br>

In this code, I have employed the MobileNetV3 as my pretrained model to do transfer learning so that I don't have to construct the model's architecture to do image's feature extraction by myself.<br>

You may refer to the code ["Project_3(Using Transfer Learning)"].<br>

The result we get is quite satisfying, which is about 98.5% of accuracy.<br>

Also, another CNN model was constructed to make a comparision.<br>
