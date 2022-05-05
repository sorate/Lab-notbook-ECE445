# Justin Hsieh

# Table of Contents
1. [02/28/2022](#02/28/2022)
2. [03/07/2022](#03/07/2022)
3. [04/04/2022](#04/04/2022)
4. [04/21/2022](#04/21/2022)
5. [04/25/2022](#04/25/2022)
## 02/28/2022 - Researching CNN for image classification <a name = "02/28/2022"></a>

Begun research into convolutional nerual networks and its use in multi-class image classification. 

## 03/07/2022 - LeNet Experimentation and Begin Dataset collection  <a name = "03/07/2022"></a>

Research into LeNet architecture and its applications in image classification.

Set up training rig using SLR camera and tripod. To simulate training conditions with the actual camera and rig setup, I set the camera at 35mm focal length around 24 inches above a letter size sheet of paper with the paper filling the frame entirely. 

Begin training with the first 2 classes - the one dollar and five dollar bills. 

## 04/04/2022 - Model Architecture Modifications <a name = "04/04/2022"></a>

Ran into issues with adding more classes into the classifier. Model was unable to train past a little over random and severe overfitting still persisted. 

Research into different architectures for image classification that used more layers. 

Research into resnet and its derivations due to its success in other forms of image classification. 

experimenting with using resnet50 architecture with a pre-trained model, then using transfer learning to train using my dataset

## 04/21/2022 - Additional Dataset Collection and Training <a name = "04/21/2022"></a>

Acquired 50 dollar and 100 dollar bill, begin more dataset collection for the 2 additional classes. 

## 04/25/2022 - Model Compression and Architecture Change <a name = "04/25/2022"></a>

Model size with ResNet50 roughly 100Mb after quantization, since the microprocessor only has 512Kb flash, need to compress model to fit.

Experimenting with TFlite to aid with model compression. 

Unable to compress the ResNet50 model further to any reasonable degree, deciding on using a different architecture to try to get anything to fit.

Research into SqueezeNet and MobileNet architectures as viable alternatives. 

Final implementation of MobileNetV2 using transfer learning to achieve 2.53Mb model size after quantization and using TFlite. 


