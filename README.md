# Machine-Learning-Convolutional-Neural-Network

## Question 3 number 1

The input dimension= 6x6x1 
The filter dimension = 3x3x1
Number of parameters= filter layer * depth + 1
= (3x3x1)+1= 10 parameters

## Question 3 number 2
The output activation map when you apply the convolutional operation using the filter f on the input without padding is:

![Screen Shot 2022-10-31 at 10 30 33 AM](https://user-images.githubusercontent.com/89150972/199070702-61147d5a-ae74-45dc-a619-f4ebd3a4225c.png)

## Question 3 number 3
The output when you apply a max-pooling operation on the output from number 2 is:

![Screen Shot 2022-10-31 at 10 30 53 AM](https://user-images.githubusercontent.com/89150972/199070901-af49361a-36c8-4535-996d-bd0b24f40f5e.png)

### Documentation or code used in finding numbers 2 and 3:

![Screen Shot 2022-10-31 at 12 29 28 PM](https://user-images.githubusercontent.com/89150972/199071387-50512444-f1d9-4dcd-ab56-58d69466d101.png)



![Screen Shot 2022-10-31 at 12 29 35 PM](https://user-images.githubusercontent.com/89150972/199071460-0b6e9503-bb6d-47a1-a3ce-4c6694eb7756.png)


## Question 2

### Implementing LENET CNN

1. What is the effect of learning rate on the training process? Which performed best?

ANSWER: The learning rate controls how qucikly the model adapts to the problem. I tried three different learning rates:
0.01 which produced an accuracy of 10%
0.02 which also produced an accuracy of 10%
0.1 which interestingly produced an accuracy of 10%
I cannot conclude on which learning rate performed the best because they all gave the same accuracy levels. 


2. What is the effect of batch size on the training process? Which performed best?

Answer: Batch size specifies how many samples must be processed before the internal model parameters are updated. 
I again tried three different batch sizes:
32 which produced an accuracy of 10%
50 which also produced an accuracy of 10%
100 which interestingly produced an accuracy of 10%
I found it surprising my models produced the same accuracy regardless of the batch size I chose and hence made it difficult to conlucde on the best batch size as in the case of the learning rate.

3. Try different hyperparameters to obtain the best accuracy on the test set. What is your
best performance and what were the hyperparameters?

ANSWER: I changed the epochs as well since it is also a hyperparameter using epoch of 10, 12 and 25 and still had an accuracy of 10%.


4. Implement an equivalent feed forward network for the same task with each hidden layer
containing the same number of neurons as the number of filters in each convolution layer. Use the ‘Adam’ optimizer to train your network on the CIFAR-10 dataset for a fixed set of 25 epochs. Compare its performance with your LeNet implementation based on the following questions:
a. What is its performance?

ANSWER: The feed forward network produced the same accuracy as with the LeNet CNN model I built in previous question. 

b. How many parameters are there in this network compared to the LeNet
implementation? Are they worth it?

ANSWER: There are 62,006 parameters compared to 10 parameters in the LeNet model. It was not worth building the feedforward network because they all produced the same results. 

## Question 1

### Regular CNN 
1. A regular CNN where the number of filters in each layer increases as the depth of the network grows i.e., the Lth layer will have more filters than the (L-1)th layer.

ANSWER: 

![Screen Shot 2022-10-31 at 12 46 16 PM](https://user-images.githubusercontent.com/89150972/199074590-a1c039a4-40ed-4eaa-b6d9-23e111f353dd.png)

The image above shows the regular CNN I built, I built this cnn firstly using:
Optimizer: Adam
lrate= 0.01
batch_size = 32
epoch = 25
this produced an accuracy of 11.35%

Secondly, 
Optimizer: SDG
lrate= 0.02
batch_size = 50
epoch = 10
this produced an accuracy of 98.33%

Finally, 
Optimizer: RMSprop
lrate= 0.03
batch_size = 100
epoch = 10
this produced an accuracy of 11.35%



2. An inverted CNN where the number of filters in each layer decreases as the depth of the network grows i.e., the Lth layer will have less filters than the (L-1)th layer.
ANSWER:

![Screen Shot 2022-10-31 at 12 51 35 PM](https://user-images.githubusercontent.com/89150972/199075588-41ba06a7-15c7-4556-89a8-a8de71ca7f84.png)

The image above shows the inverted CNN I built, I built this cnn firstly using:
Optimizer: Adam
lrate= 0.01
batch_size = 32
epoch = 25
this produced an accuracy of 11.35%

Secondly, 
Optimizer: SDG
lrate= 0.1
batch_size = 90
epoch = 10
this produced an accuracy of 11.35%

Finally, 
Optimizer: RMSprop
lrate= 0.05
batch_size = 110
epoch = 9
this produced an accuracy of 11.35%

3. An hour-glass shaped CNN where the number of filters will increase till the Lth layer and reduce afterwards.

ANSWER:

![Screen Shot 2022-10-31 at 12 56 26 PM](https://user-images.githubusercontent.com/89150972/199076525-58a254fb-6342-443e-9878-257a9970e576.png)

The image above shows the hour-glass shaped CNN I built, I built this cnn firstly using:
Optimizer: Adam
lrate= 0.01
batch_size = 32
epoch = 25
this produced an accuracy of 11.35%

Secondly, 
Optimizer: SDG
lrate= 0.09
batch_size = 120
epoch = 10
this produced an accuracy of 11.35%

Finally, 
Optimizer: RMSprop
lrate= 0.011
batch_size = 85
epoch = 12
this produced an accuracy of 11.35%


I found it interesting my accuracy was the same regardless of changes in hyperparameters.
