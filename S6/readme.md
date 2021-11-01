## Assignment 6 EVA7

In the notebook,we have imported libraries.Loaded our data created dataloaders,imported model from model.py file trained three 
---
Normalization in Nueral Networks

* In nueral networks we add normalization layer to make the models learn more efficiently 
* It is a way of regularization to avoid overfitting of the model

In our assignment we are using 3 different normalization techniques

* i.Group Normalization
* ii.Layer Normalization
* iii.Batch Normalization

---
### 6.1 Network with Group Normalization 
n testing the model with L1 loss and  batch normalization.

optimizer: SGD with lr=0.01, momentum=0.9
scheduler: StepLR with step size=6 and gamma=0.1
l1 lambda=0.001


---
### 6.2 Network with Layer Normalization
n testing the model with L1 loss and  batch normalization.

optimizer: SGD with lr=0.01, momentum=0.9
scheduler: StepLR with step size=6 and gamma=0.1
l1 lambda=0.001


---
### 6.3 Network with L1 loss + Batch Normalization

On testing the model with L1 loss and  batch normalization.

optimizer: SGD with lr=0.01, momentum=0.9
scheduler: StepLR with step size=6 and gamma=0.1
l1 lambda=0.001

The test and train loss quickly reduces when L1 regularization is applied. moreover, the train and test accuracy of the model reduces quickly too
---
