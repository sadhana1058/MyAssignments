## Assignment 6 EVA7

In the notebook,I have 
* import libraries(imported Net from model.py file)
* transformed our data
* created train and test data
* created dataloader arguments,checked data statistics
* used Net that was imported from model.py
* checked parameters for all models
* created train and test functions
* created a function to misclassify the images
* trained and tested same model with different normlaization techniques
rained three with three different kinds of normalization
* plotted graphs for train and test accuracy
In the model.py file,I have
* created a function to choose normalization type and merge it with convolution layer
* created a  nueral network which takes input parameter for normalization type  and adds it each block of nueral network
---
### Normalization in Nueral Networks
* Normalization is just a way of representing data.We don't destroy data when we normalize them
* In nueral networks we add normalization layer to make the models learn more efficiently 
* It is a way of regularization to avoid overfitting of the model
* Image normalization helps the model to handle different variation of images.

In our assignment we are using 3 different normalization techniques

* i.Group Normalization
* ii.Layer Normalization
* iii.Batch Normalization

---
 ### i.Group Normalization
 Group normalization (GN) divides the channels into groups and computes the first-order statistics within each group.\
 GN’s computation is independent of batch sizes, and its accuracy is more stable than BN in a wide range of batch sizes.\

 ![Group Normalization](https://theaisummer.com/static/cc4cab7d3928c37b81f620fb95f2fb23/63a68/group-normalization.png)

In GN,we calculate mean and standard deviation across every channel of every image for every group in that batch.

 ### ii.Layer Normalization
 In  Layer Normalization (LN), the statistics (mean and variance) are computed across all channels and spatial dims.
 ![Layer Normalization](https://theaisummer.com/static/3ed7199184645f3e632d17ab6441244f/63a68/layer-norm.png)

In LN,
we calculate mean and standard deviation across every pixel in every channel of all images 
 ### iii.Batch Normalization
Batch Normalization (BN) normalizes the mean and standard deviation for each individual feature channel/map.\

We can think of it as bringing the features of the image in the same range.\
![Batch Normalization](https://theaisummer.com/static/4dcafb4538eae7ec712691afaee981cb/63a68/batch-norm.png)


BN accelerates the training of deep neural networks.\

For every input mini-batch we calculate different statistics. This introduces some sort of regularization.

In BN,
we calculate mean and standard deviation across every channel of every image in that batch 
---
### 6.1 Network with Group Normalization 
n testing the model with L1 loss and  batch normalization.

optimizer: SGD with lr=0.01, momentum=0.9
scheduler: StepLR with step size=6 and gamma=0.1
l1 lambda=0.001


---
### 6.2 Network with Layer Normalization
On testing the model with layer normalization.

optimizer: SGD with lr=0.01, momentum=0.9

The e

---
### 6.3 Network with L1 loss + Batch Normalization

On testing the model with L1 loss and  batch normalization.

optimizer: SGD with lr=0.01, momentum=0.9
scheduler: StepLR with step size=6 and gamma=0.1
l1 lambda=0.001

The test and train loss quickly reduces when L1 regularization is applied. moreover, the train and test accuracy of the model reduces quickly too
---
### Graphs for Models with different normalization techniques


#### Train accuracy and train losses
![image](https://user-images.githubusercontent.com/47341316/139875095-ef821307-9e88-4113-a626-bc5f5d361476.png)

#### Test accuracy and  test losses
![image](https://user-images.githubusercontent.com/47341316/139875051-ba941983-f3a4-4eff-a69e-3a0e2de69163.png)

---
### Misclassified images

#### Group Normalization
![image](https://user-images.githubusercontent.com/47341316/139874984-53a62cfd-c352-4d9b-8190-51905d874263.png)

#### Layer Normalization
![image](https://user-images.githubusercontent.com/47341316/139874857-c8d5e660-42ac-4cad-b388-1f7b9ca79ac6.png)

#### Batch Normalization
![image](https://user-images.githubusercontent.com/47341316/139874758-4ecf6f23-8d10-4442-9b3f-94b7fe3bfa7c.png)

