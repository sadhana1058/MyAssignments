## Assignment 

### 1.What are Channels and Kernels (according to EVA)?

A channel is a container of information.Channels are semantic in nature.It can also be referred as feature map or feature bucket.Channels can be created only by a kernel.
In other words,Channels are feature containers.

A kernel is a simple 3X3 matrix  .It is weighted matrix initialized with randomly allocates values as its weights.It can also be referred as filters.A kernel convolves on top of a channels and extracts the features/information. 
In other words,Kernels are feature extractors.


### 2.Why should we (nearly) always use 3x3 kernels?



### 3.How many times do we need to perform 3x3 convolutions operations to reach close to 1x1 from 199x199 (type each layer output like 199x199 > 197x197...)

We have to perform 3x3 convolutions 100 times.
199 X 199, 197 X 197, 195 X 195, 193 X 193, 191 X 191, 189 X 189, 187 X 187, 185 X 185, 183 X 183, 181 X 181, 179 X 179, 177 X 177, 175 X 175, 173 X 173, 171 X 171, 169 X 169, 167 X 167, 165 X 165, 163 X 163, 161 X 161, 159 X 159, 157 X 157, 155 X 155, 153 X 153, 151 X 151, 149 X 149, 147 X 147, 145 X 145, 143 X 143, 141 X 141, 139 X 139, 137 X 137, 135 X 135, 133 X 133, 131 X 131, 129 X 129, 127 X 127, 125 X 125, 123 X 123, 121 X 121, 119 X 119, 117 X 117, 115 X 115, 113 X 113, 111 X 111, 109 X 109, 107 X 107, 105 X 105, 103 X 103, 101 X 101, 99 X 99, 97 X 97, 95 X 95, 93 X 93, 91 X 91, 89 X 89, 87 X 87, 85 X 85, 83 X 83, 81 X 81, 79 X 79, 77 X 77, 75 X 75, 73 X 73, 71 X 71, 69 X 69, 67 X 67, 65 X 65, 63 X 63, 61 X 61, 59 X 59, 57 X 57, 55 X 55, 53 X 53, 51 X 51, 49 X 49, 47 X 47, 45 X 45, 43 X 43, 41 X 41, 39 X 39, 37 X 37, 35 X 35, 33 X 33, 31 X 31, 29 X 29, 27 X 27, 25 X 25, 23 X 23, 21 X 21, 19 X 19, 17 X 17, 15 X 15, 13 X 13, 11 X 11, 9 X 9, 7 X 7, 5 X 5, 3 X 3, 1 X 1

### 4.How are kernels initialized? 
kernels are initialized randomly


### 5.What happens during the training of a DNN?

