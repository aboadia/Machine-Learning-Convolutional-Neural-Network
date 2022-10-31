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
The learning rate controls how qucikly the model adapts to the problem. I tried three different learning rates:
0.01 which produced an accuracy of 10%
0.02 which also produced an accuracy of 10%
0.1 which interestingly produced an accuracy of 10%


3. What is the effect of batch size on the training process? Which performed best?
4. Try different hyperparameters to obtain the best accuracy on the test set. What is your
best performance and what were the hyperparameters?
4. Implement an equivalent feed forward network for the same task with each hidden layer
containing the same number of neurons as the number of filters in each convolution layer. Use the ‘Adam’ optimizer to train your network on the CIFAR-10 dataset for a fixed set of 25 epochs. Compare its performance with your LeNet implementation based on the following questions:
a. What is its performance?
b. How many parameters are there in this network compared to the LeNet
[Question 3]
[10 points]
implementation? Are they worth it?

