# README file
This repository contains the Jupiter notebook for Google
Colab to train and use the YoloV3 and YoloV4 object detection
models.

Each folder in this repository contains the corresponding
Jupiter notebook, and the results of passing the different test
images throught the networks.

Additionally, the test videos has been uploaded to YouTube, and
the corresponding links are the following:

## YoloV3 results:
* Test video 1 results: https://youtu.be/En4d0sX2Yww
* Test video 2 results: https://youtu.be/GTgE8P8NZ58

## YoloV4 results:
* Test video 1 results: https://youtu.be/mZBn-tUUofw
* Test video 2 results: https://youtu.be/KOCAnCNwI84

The results obtained in this project are the results of modifying the network
such that it can detect two classes only: Mask and No Mask. For doing so,
the network parameters has been modified such that:
* The number of filters in each Yolo class are filter=(classes + 5) * 3
* The amount of Epochs = 6000, since the amount of epochs should be 2 * classes = 4000,
   but this number is less than the minimum, which is 6000.
* The learning rate has been reduced to 0.0001

With these modifications, we obtained a mAP of 72.30% for the YoloV3 model,
and a mAP of 79.17% for the YoloV4 model.
