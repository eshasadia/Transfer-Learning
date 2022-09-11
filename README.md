# Transfer-Learning-Cats_n_Dogs
In this project I have done basic transfer learning on cats and dogs private dataset.
CIFAR-10 Dataset
It is a dataset with 10 classes ranging from automobiles, airplanes, to horses having 6,000 images of each class total of 60,000 total images in dataset. each image dimension is 32 x 32 pixels.
ResNet-50 is a 50 layer deep residual network designed for image classification.
First the resnet architecture is designed with 224x224 pixels images, howver in CIFAR dataset images are 32x32 pixels, so we wil upsample images to reuired size 224x224 using tensorflows built-in *UpSample2d* library.
Here we will re-train the 50 layers of resNet 50 model via using pretrained weights from image-net dataset. here we will refer ResNet-50 as feature extraction part of our model.
Then we'll use pooling for reduce width and height of the image and flatten for feeding image as a 1D vector to the dense layers and in the end 10-way softmax classifier layer since CIFAR has 10 classes.
Using pre-trained weights and further training them on our own dataset is called fine tuning
