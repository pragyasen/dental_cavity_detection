# Dental Cavity Detection
The project has employed visual pictures of teeth and applied a deep convolutional neural network (CNN) to categorize the teeth into caries or non-caries. Implementation done using Python.

## Objectives
1. To detect dental cavities from dental images by using an Artificial Intelligence (AI) system.
2. To find the best suitable Machine Learning algorithm for the same.
3. To validate the diagnostic results using Machine Learning.

## Dataset description & Augmentation
The dataset contains in total 884 images belonging to 2 classes, i.e., cavity and no cavity. They have been split into train and test folders in 8:2 ratio. There are 708 images belonging to class 1 and 176 images belonging to class 2. Images were in JPG format in the dataset. ImageDataGenerator from keras.preprocessing.image in python was used. 20% of images from the dataset were used for testing along with random horizontal flip. A zoom range of 0.15 and rotation of 20% was used for data augmentation purposes for this model.

## Model Used
The Tensorflow hub’s Imagenet v3 was used to create the initial layers and a dense layer was added after that to create the neural network. The 2.0 version of Tensorflow was used as the pre-trained model. <br>
Reasons for using MobileNetV2:
1. MobileNet is a general architecture and can be used for multiple use cases. Depending on the use case, it can use different input layer size and different width
factors.
2. MobileNets support any input size greater than 32 x 32, with larger image sizes offering better performance.
3. MobileNetV2 is very similar to the original MobileNet, except that it uses inverted residual blocks with bottlenecking features.
4. It is lightweight and has high execution speeds.

## Results
<img src="/model_accuracy_graph.png" alt="accuracy graph" height="300">
<img src="/model_loss_graph.png" alt="accuracy graph" height="300"> <br>

It can be seen that the model accuracy reaches 93% at the the 100th epoch which is the highest accuracy that can be obtained. The model’s loss is also low at this point for
the testing data. Hence the process is stopped at this point for the detection.
