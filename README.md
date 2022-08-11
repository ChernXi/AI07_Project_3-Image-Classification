# Project_3-Image-Classification

This project is about image classfication.
There are two classed of road image here:
Class "0" = negative, refer to the road images without crack on the surface.
Class "1" = positive, refer to the road images with crack on the surface.

In this code, I have employed the MobileNetV3 as my pretrained model to do transfer learning so that I don't have to construct a CNN model to do image's feature extraction by myself.

You may refer to the code ["Project_3(Using Transfer Learning)"].

The result we get is quite satisfying, which is about 98.5% of accuracy.

Also, another CNN model was constructed to make a comparision.
