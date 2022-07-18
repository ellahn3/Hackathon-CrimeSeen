# Hackathon-CrimeSeen
Hackathon CrimeSeen startup
![image](https://user-images.githubusercontent.com/73067197/179469520-abe80f2d-a3d8-42ab-af88-81cee91f2587.png)

### Selected issue:
Security bodies around the world, in particular the Israel Police, are constantly engaged in maintaining public safety. 
One of the main challenges in this task is the early detection of ammunition. There are many means of detection such as magnetometers and more but security officials do not always want the means to be visible, or prominent as the detection means that are used until now .

### Solution:
Weapon identification by thermal camera along with facial identification by another camera, which checks whether the person is in an existing face in the police database of criminals who have a criminal record. In the event that a match is found, a warning will be sent to police officials.

![image](https://user-images.githubusercontent.com/73067197/179469369-5ecf0adb-ab13-4d23-9bba-e79e591634b2.png)


To implement our statup we built a neural network that builds a model based on machine learning.
The model will learn how to identify from a thermal image whether there is a weapon hidden under a person's clothing.
If so the system will scan the person's face with the police face recognition system.
If the weapon holder is in fact a criminal, who is legally prohibited from walking around with a weapon, the system will send an alert.

## DATA:
The data contain 2 thypes of infrared images

1- infrared images whit gun

2- infrared images whitout gun

3-criminal faces

## ResNet-50 Model:
ResNet-50 is a convolutional neural network that is 50 layers deep. ResNet, short for Residual Networks. The resnet 50 architecture contains the following element:

A convoultion with a kernel size of 7 * 7 and 64 different kernels all with a stride of size 2 giving us 1 layer.
Next we see max pooling with also a stride size of 2.
In the next convolution there is a 1 * 1,64 kernel following this a 3 * 3,64 kernel and at last a 1 * 1,256 kernel, These three layers are repeated in total 3 time so giving us 9 layers in this step.
Next we see kernel of 1 * 1,128 after that a kernel of 3 * 3,128 and at last a kernel of 1 * 1,512 this step was repeated 4 time so giving us 12 layers in this step.
After that there is a kernal of 1 * 1,256 and two more kernels with 3 * 3,256 and 1 * 1,1024 and this is repeated 6 time giving us a total of 18 layers.
And then again a 1 * 1,512 kernel with two more of 3 * 3,512 and 1 * 1,2048 and this was repeated 3 times giving us a total of 9 layers.
After that we do a average pool and end it with a fully connected layer containing 1000 nodes and at the end a softmax function so this gives us 1 layer.
We don't actually count the activation functions and the max/ average pooling layers.

so totaling this it gives us a 1 + 9 + 12 + 18 + 9 + 1 = 50 layers Deep Convolutional network.

## face recognition:
unknown image=> model for infrared images=>face recognition
