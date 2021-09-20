## Assignment 

### 1.What are Channels and Kernels (according to EVA)?

A channel is a container of information.Channels are semantic in nature.It can also be referred as feature map or feature bucket.Channels can be created only by a kernel.
In other words,Channels are feature containers.

A kernel is a simple 3X3 matrix  .It is weighted matrix initialized with randomly values as its weights.It can also be referred as filters.A kernel convolves on top of a channels and extracts the features/information. 
In other words,Kernels are feature extractors.


### 2.Why should we (nearly) always use 3x3 kernels?
To understand why optimal size of kernel is 3X3, we can breakdown the question into two parts:

* Why do we prefer odd sized kernel? (why 3X3 ?why not 2x2?)\
Kernels can either be even sized or odd sized.Convolution is the process of moving kernel on top of an image.In case of even sized filters while convoluting, the center of the kernel would end up inbetween,that might result some sort of distortions . Odd sized kernels are preferred over even sized kernels as they have symmetry.

![image](https://user-images.githubusercontent.com/47341316/133960375-03738480-37a7-4bb2-bdd5-d3c5534ac214.png)

In the above image we can see that a 3X3 kernel has a centre at 93 whereas the 2X2 matrix has a centre inbetween the 4 grids.Such centers are not preferred.

* Why do we prefer small sized kernels?(why not1X1 ? Why 3X3 ?Why not 5X5 or 7X7?)\

Small sized kernels can extract large number of features.\
As they have large number of layers,they capture complex features.\
They are more computationally efficient due to the less number of weights.\
1X1  is not an optimal filter sizes as as it convolutes by 1px ,it is not efficient and adds a lot of layers.\
3X3 are the next odd sized kernels and they are small .They use less number of parameters.GPUs prefer 3X3 sized kernels as well.So they are the optimal sized kernels.\
In,5x5 and 7X7 sized kernels (matrices) we will have a large number of weights ,computation becomes expensive and the number of layers are low,so complex features cannot be extracted. Hence we dont prefer them over 3X3 matrix.\


### 3.How many times do we need to perform 3x3 convolutions operations to reach close to 1x1 from 199x199 (type each layer output like 199x199 > 197x197...)

``` Python
n=199
c=0
for i in range(199,0,-2):
  c =c+1
  if i!=1:
    print(i,"X",i,end=" > ")
  else:
    print(i,"X",i)
print(c,"convolutions")
``` 

We have to perform 3x3 convolutions 100 times.\
199 X 199 > 197 X 197 > 195 X 195 > 193 X 193 > 191 X 191 > 189 X 189 > 187 X 187 > 185 X 185 > 183 X 183 > 181 X 181 > 179 X 179 > 177 X 177 > 175 X 175 > 173 X 173 > 171 X 171 > 169 X 169 > 167 X 167 > 165 X 165 > 163 X 163 > 161 X 161 > 159 X 159 > 157 X 157 > 155 X 155 > 153 X 153 > 151 X 151 > 149 X 149 > 147 X 147 > 145 X 145 > 143 X 143 > 141 X 141 > 139 X 139 > 137 X 137 > 135 X 135 > 133 X 133 > 131 X 131 > 129 X 129 > 127 X 127 > 125 X 125 > 123 X 123 > 121 X 121 > 119 X 119 > 117 X 117 > 115 X 115 > 113 X 113 > 111 X 111 > 109 X 109 > 107 X 107 > 105 X 105 > 103 X 103 > 101 X 101 > 99 X 99 > 97 X 97 > 95 X 95 > 93 X 93 > 91 X 91 > 89 X 89 > 87 X 87 > 85 X 85 > 83 X 83 > 81 X 81 > 79 X 79 > 77 X 77 > 75 X 75 > 73 X 73 > 71 X 71 > 69 X 69 > 67 X 67 > 65 X 65 > 63 X 63 > 61 X 61 > 59 X 59 > 57 X 57 > 55 X 55 > 53 X 53 > 51 X 51 > 49 X 49 > 47 X 47 > 45 X 45 > 43 X 43 > 41 X 41 > 39 X 39 > 37 X 37 > 35 X 35 > 33 X 33 > 31 X 31 > 29 X 29 > 27 X 27 > 25 X 25 > 23 X 23 > 21 X 21 > 19 X 19 > 17 X 17 > 15 X 15 > 13 X 13 > 11 X 11 > 9 X 9 > 7 X 7 > 5 X 5 > 3 X 3 > 1 X 1\
100 convolutions

### 4.How are kernels initialized? 
In Neural Networks,Kernels are initialized to small random numbers.\
Neural networks uses randomness in order to find a good enough set of weights for kernels for that particular extraction of a feature for that image.\
They are initialized to random values as it removes any kind of bias while extracting the features.This improves the efficiency of training a Neural Network.\


### 5.What happens during the training of a DNN?
A DNN  has 3 types of layer:\
* Input Layer
* Hidden Layer
* Output Layer

![image](https://user-images.githubusercontent.com/47341316/133975592-af6780d6-0a49-4885-a0a1-900c71b74613.png)

A deep neural network has one input layer, one or more hidden layers and one output layer.\
They have neurons similar to human brain.Each layer consists of many neurons.

During training of a DNN,the first layer,i.e. input layer contains all the information/image
the kernel extracts the required features from input layer and creates a hidden layer . If the data is complex it creates multiple hidden layers before predicting the output,else it stops at 1 or 2 hidden layers.Then the data is transferred from hidden layer to output layer.The output layer takes in the inputs from the previous layers, performs the necessary calculations with the help of its neurons and then computes the output.

Let us take an example to understand how they work
![image4](https://user-images.githubusercontent.com/47341316/133978249-1c415ccb-89e1-4d73-ae97-3880f786ad8c.png)

In the above image,we  can  see how features are extracted using kernels from a feature bucket,channel.
Initially the model  identifies the edges ,which is then combined to identify textures in the second layer ,then we combine the previous two layers to identify patterns ,then the next layer identifies parts,which upon combining  identifies objects.

