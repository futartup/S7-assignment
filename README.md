# S7-assignment
S7 assignment submission, CIFAR10 

## Result-
1. S7-assignment-overfitting.ipynb = Overfitting 
2. 80.13% accuracy in 15 epochs.




## Model Diagram
![Test Image](https://github.com/futartup/S7-assignment/blob/master/S7-assignment-model-diagram.png)





## Model Description
| s,p| Dilation | Input | kernel | Output | GRF | Total Parameters | Jout |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 1,1| 1| 32 * 32 * 3 | 3 * 3 * 3 * 16 | 32 * 32 * 16 | 3 | 432 | 1 |
| 1,1 | 2 | 32 * 32 * 16 | 3 * 3 * 32 | 30 * 30 * 32 | 7 | 4608 | 1 |
| 2, 0 | 0 | 30 * 30 * 32 | 2 * 2 | 15 * 15 * 32 | 8 | 8 | 2 |
| 1,1 | 1 | 15 * 15 * 32 | 3 * 3 * 64 | 15 * 15 * 64 | 12 | 18432 | 2 | 
| 1,1 | 2 | 15 * 15 * 64 | 3 * 3 * 128 | 13 * 13 * 128 | 20 | 73728 | 2 |
| 2,0 | 0 | 13 * 13 * 128 | 2 * 2 | 6 * ^ * 128 | 22 | 0 | 4 |
| 1,1 | 1 | 6 * 6 * 128 | 3 * 3 * 128 | 6 * 6 * 128 | 30 | 1152 | 4 |
| 1,1 | 0 | 6 * 6 * 128 | 1 * 1 * 256 | 8 * 8 * 256 | 30 | 32768 | 4 |
| 2,0 | 0 | 8 * 8 * 256 | 2 * 2 | 4 * 4 * 256 | 34 | 0 | 8 |
| 1,1 | 0 | 4 * 4 * 256 | 3 * 3 * 10 | 2 * 2 * 10 | 50 | 23040 | 8 |
| | | | | | | Total Parameters = 155,408 | |
