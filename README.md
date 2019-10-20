# Breast-Cancer-Prediction-NeuralNet
A neural network (NN) having two hidden layers is implemented, besides the input and output layers without using any libraries in python. The program predicts the probability of having breast cancer given certain features set. The code provide choice to the user to use Sigmoid, Tanh or Relu as the activation function. Prediction accuracy is computed at the end.


## Programming Part Report

From the UCI ML repository, the breast cancer dataset was chosen to train and
test the neural network. The dataset can be found here, while more information
on the dataset can be found here. The dataset contains 9 input attributes and one
output (class) attribute. It is a relatively small dataset with 286 instances.

The following parameters were tuned in order to attain better results:

- Learning Rate
- Max Iterations
- Training-Testing Data%

Training and testing error sum for different activation functions (sigmoid, tanh,
ReLu) for different values of the tuning parameters mentioned above is listed in
the tables below.

```
Learning Rate: 0.
Max Iterations: 1000
Training data %: 75%
Testing data %: 25%
Activation Function Training Error Sum Testing Error Sum
Sigmoid 88.50282234130717 34.
Tanh 178.90041754398618 71.
ReLu 107.38700614574185 35.
```
```
Learning Rate: 0.
Max Iterations: 1000
Training data %: 75%
Testing data %: 25%
Activation Function Training Error Sum Testing Error Sum
Sigmoid 86.35884827755144 34.
Tanh 267.25228846158893 87.
ReLu 107.38700614574185 35.
```

Learning Rate: 1.
Max Iterations: 1000
Training data %: 80%
Testing data %: 20%
**Activation Function Training Error Sum Testing Error Sum**
Sigmoid 113.25986633436756 29.
Tanh 303.1227633213832 70.
ReLu 113.25993561603744 29.

Learning Rate: 0.
Max Iterations: 2000
Training data %: 90%
Testing data %: 10%
**Activation Function Training Error Sum Testing Error Sum**
Sigmoid 100.6611252214229 14.
Tanh 181.04169816061201 46.
ReLu 126.18814749780508 16.

Learning Rate: 0.
Max Iterations: 2000
Training data %: 80%
Testing data %: 20%
**Activation Function Training Error Sum Testing Error Sum**
Sigmoid 93.1720275989999 29.
Tanh 239.97514451159736 70.
ReLu 113.25993561603744 29.

Learning Rate: 1.
Max Iterations: 2000
Training data %: 90%
Testing data %: 10%
**Activation Function Training Error Sum Testing Error Sum**
Sigmoid 126.1881465311347 16.
Tanh 214.3009079398663 24.
ReLu 126.18814749780508 16.


It is observed that both sigmoid as well as ReLu output the better training and
testing error sum, (sigmoid being very very slightly better), followed by tanh. It is
so because of the relatively smaller dataset (it contains only 286 instances). Plus,
the network is not that deep (it contains only 2 hidden layers with 4 nodes in the
first hidden layer and 2 nodes in the second hidden layer). Had the network been

## Sample Output
* Sample output:
	* Training on 90.0% data and testing on 10.0% data using the activation function as relu
	After 2000 iterations, and having learning rate as 0.05, the total error is 126.18814749780508

The final weight vectors are (starting from input to output layers)

[[ 0.61667749 -0.26324629  0.21841398 -0.93030455]
 [-0.29084554 -0.84296007  0.3863704  -0.97457467]
 [-0.08090943  0.92263452 -0.33162956 -0.05583316]
 [-0.7892175   0.00615181  0.77137972  0.06875468]
 [-0.43704647 -0.29083062  0.7925605  -0.51702172]
 [-0.95223181  0.93145361 -0.1400642  -0.30742297]
 [ 0.15413526 -0.74694768  0.90008662 -0.37277834]
 [ 0.90566225 -0.56321354 -0.5025996   0.72760359]
 [-0.52946334  0.63020011  0.08779447 -0.61747946]]
[[ 0.17767988 -0.90372641]
 [-0.96825404 -0.90057797]
 [-0.20116942  0.15380792]
 [ 0.73503491  0.57232448]]
[[-0.49059449]
 [-0.83549019]]
 
* Testing error sum using activation function as relu: 16.811852502194906
more deep, ReLu had been a better activation function.

* It is observed that the best (though it might not be the best and we could obtain
better results) training and testing error sum is obtained when the learning rate is
0.05, max iterations are 2000 and the train-test split is in the ratio 90%-10%.

## Programming Instructions
* Install Python3 and add scikit-learn, pandas, numpy dependencies
* Run the NeuralNet.py file on IDE such as Pycharm. It will ask for user input.
* Press the following keys for the activation functions: 
  	* Press 1 for Sigmoid 
	* Press 2 for Tanh 
	* Press 3 for ReLu 
	* Pressing any other key will result in the activation function being sigmoid
* To change the train test split percentage, input the amount in between 0.0 to 1.0 on line 230 for the variable train_test_split_size.
* To change the max iterations for training, input the amount on line 233 for the variable max_iteratons.
* To change the learning rate for training, input the amount on line 236 for the variable learning_rate.
* To change the dataset, either input the file path (relative or absolute) or give the dataset URL on line 240 for the variable dataset_file.


