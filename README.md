### Deep Learning and ML for Medical Image Classification

<img src="https://github.com/selimslab/portfolio/blob/master/assets/pn.jpg" alt="architecture">

## intro
+ 30 000 images from 26 000 patients
+ 8000 pneumonia, 10 000 healthy, others sick but not pneumonia
+ convolutional layers of deep networks are used to map input space to feature space

## feature extraction
+ minimal preprocessing, just resizing, pixel color normalization, and augmentation 
+ base layers of densenet121, densenet201, resnet50, InceptionResNetV2, vgg16, vgg19, xception, mobilenet-v2, nasnet-mobile are used with global average pooling
+ Resulting feature spaces are up to 2000 element tensors

## training and test
+ Feature space are split into training, test and validation sets
+ Custom fully connected layers on top of the base layers are trained, with base layer weights frozen 
+ SVMs, desicison trees, random forests, gaussian naive bayes, linear and quadratic discriminant classifiers are trained

## results
+ The best classification results are around 0.83 AUROC score with InceptionResNetV2, resnet50,xception,and densenet generated feature spaces and random forests as top classifier. 
