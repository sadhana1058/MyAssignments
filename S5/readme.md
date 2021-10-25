## Part 1
### Setup
* set up transforms
* set up dataloaders
* look at the data,statistics,shapes, min, max, mean, std, var of train data
* set up train and test loops

### Results:
* Parameters: 6.3M
* Best Training Accuracy: 100.00
* Best Test Accuracy: 99.36



### Analysis:
* Extremely Bulky Model 
* Model is over-fitting, our test accuracy is low

## Part 2
### Target:

* Setting the basic foundations,Skeleton structure
* Make the model lighter 

### Results:

* Parameters: 15.3k
* Best Train Accuracy: 99.28
* Best Test Accuracy: 98.8

### Analysis:

* The model has more than 10k parameters
* model is slightly overfitted

## Part 3
### Target:

* To fix overfitting.
* Make the model lighter 
* To add GAP to convert 2D data to 1D data

### Results:

* Parameters: 8.3k
* Best Train Accuracy: 99.05
* Best Test Accuracy: 98.92

### Analysis:

* The model is lighter
* GAP layer reduces the number of parameters
* The model is still slightly overfitted

## Part 4
### Target:

* Make the model efficient
* To add Batch-normalization 

### Results:

* Parameters: 8.3k
* Best Train Accuracy: 99.53
* Best Test Accuracy: 99.26

### Analysis:
* there is over-fitting


## Part 5
### Target:

* Make the model efficient
* To add dropout

### Results:

* Parameters: 8.3k
* Best Train Accuracy: 99.28
* Best Test Accuracy: 99.35

### Analysis:
* Small number of channels are there
* There is almost no over-fitting
* Regularization is working



## Part 6
### Target:

* To increase the capacity of model
* To acheive 99.4% accuracy

### Results:

* Parameters: 9.1k
* Best Train Accuracy: 99.02
* Best Test Accuracy: 99.36

### Analysis:
* The model has less than 10k parameters
* Increasing the capacity has helped the model to learn model

## Part 7
### Target:

* To Add LR Scheduler
* To acheive 99.4% accuracy

### Results:

* Parameters: 9.1k
* Best Train Accuracy: 99.02
* Best Test Accuracy: 99.36

### Analysis:
* The model has less than 10k parameters
* Increasing the capacity has helped the model to learn model


