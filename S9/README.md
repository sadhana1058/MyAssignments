## S9 RESNETS AND HIGHER RECEPTIVE FIELDS(One Cycle Policy)

### Finding maximum learning rate
![image](https://user-images.githubusercontent.com/47341316/146639766-8e24e18e-4932-48fd-b695-c1c815087aa6.png)

### Data Augmentation
![image](https://user-images.githubusercontent.com/47341316/146640110-a7208179-e948-4390-a738-46cca254b312.png)

### Model Summary
```
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1           [-1, 64, 32, 32]           1,728
       BatchNorm2d-2           [-1, 64, 32, 32]             128
              ReLU-3           [-1, 64, 32, 32]               0
            Conv2d-4          [-1, 128, 32, 32]          73,728
         MaxPool2d-5          [-1, 128, 16, 16]               0
       BatchNorm2d-6          [-1, 128, 16, 16]             256
              ReLU-7          [-1, 128, 16, 16]               0
            Conv2d-8          [-1, 128, 16, 16]         147,456
       BatchNorm2d-9          [-1, 128, 16, 16]             256
             ReLU-10          [-1, 128, 16, 16]               0
           Conv2d-11          [-1, 128, 16, 16]         147,456
      BatchNorm2d-12          [-1, 128, 16, 16]             256
             ReLU-13          [-1, 128, 16, 16]               0
           Conv2d-14          [-1, 256, 16, 16]         294,912
        MaxPool2d-15            [-1, 256, 8, 8]               0
      BatchNorm2d-16            [-1, 256, 8, 8]             512
             ReLU-17            [-1, 256, 8, 8]               0
           Conv2d-18            [-1, 512, 8, 8]       1,179,648
        MaxPool2d-19            [-1, 512, 4, 4]               0
      BatchNorm2d-20            [-1, 512, 4, 4]           1,024
             ReLU-21            [-1, 512, 4, 4]               0
           Conv2d-22            [-1, 512, 4, 4]       2,359,296
      BatchNorm2d-23            [-1, 512, 4, 4]           1,024
             ReLU-24            [-1, 512, 4, 4]               0
           Conv2d-25            [-1, 512, 4, 4]       2,359,296
      BatchNorm2d-26            [-1, 512, 4, 4]           1,024
             ReLU-27            [-1, 512, 4, 4]               0
        MaxPool2d-28            [-1, 512, 1, 1]               0
           Linear-29                   [-1, 10]           5,120
================================================================
Total params: 6,573,120
Trainable params: 6,573,120
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.01
Forward/backward pass size (MB): 6.44
Params size (MB): 25.07
Estimated Total Size (MB): 31.53
----------------------------------------------------------------
```

### Parameters and Hyperparameters
* Loss Function: Cross Entropy Loss
* Optimizer: SGD
* Scheduler: One Cycle Policy
* Batch Size: 512
* Epochs: 24


### Final Training Log
```
EPOCH: 24 LR: 0.00024967178948909094
Loss=0.08902829885482788 Batch_id=97 Accuracy=96.80: 100%|██████████| 98/98 [01:10<00:00,  1.39it/s]
Test set: Average loss: 0.0004, Accuracy: 9365/10000 (93.65%)
```

### Results
Best Train Accuracy - 96.80%
Best Test Accuracy -  93.65%


### Classwise  accuracy
```
Accuracy of airplanes : 94 %
Accuracy of  cars : 97 %
Accuracy of birds : 89 %
Accuracy of  cats : 82 %
Accuracy of  deer : 93 %
Accuracy of  dogs : 87 %
Accuracy of frogs : 95 %
Accuracy of horses : 93 %
Accuracy of ships : 95 %
Accuracy of trucks : 94 %
```

### Misclassifications
![image](https://user-images.githubusercontent.com/47341316/146640009-5f9e3cdf-2c18-4096-a4b3-a3885142673e.png)

### GradCam
![image](https://user-images.githubusercontent.com/47341316/146640020-bfa8f056-4d5b-4137-b9fb-2fdf6691eeba.png)
![image](https://user-images.githubusercontent.com/47341316/146640023-8c191e0c-4a40-477b-8951-92bc90fc5720.png)
![image](https://user-images.githubusercontent.com/47341316/146640031-e547330d-d0d4-4528-91e4-1e98a1259547.png)
![image](https://user-images.githubusercontent.com/47341316/146640035-e85d175e-2cb3-4c2d-9b93-faeced0398d4.png)
![image](https://user-images.githubusercontent.com/47341316/146640040-0b84e2b5-5978-4d59-86c3-343acb1ca599.png)
![image](https://user-images.githubusercontent.com/47341316/146640047-d6f91049-77ea-4329-82ed-070d3550a803.png)
![image](https://user-images.githubusercontent.com/47341316/146640050-c6f39d44-499c-4b9c-9746-3455d11a94e4.png)
![image](https://user-images.githubusercontent.com/47341316/146640058-da551ad7-e807-4b1d-8c33-231e769c918d.png)
![image](https://user-images.githubusercontent.com/47341316/146640059-7daa5cff-546f-47f6-8dcd-098d0670a13f.png)
![image](https://user-images.githubusercontent.com/47341316/146640062-fcbdadee-eebc-430d-82dd-b8ac24fd3d0b.png)


### Graph
![image](https://user-images.githubusercontent.com/47341316/146639725-ccfb4e93-7836-4d6d-b4b1-898d53cfc5fc.png)
