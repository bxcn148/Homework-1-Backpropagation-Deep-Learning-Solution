Download link :https://programming.engineering/product/homework-1-backpropagation-deep-learning-solution/


# Homework-1-Backpropagation-Deep-Learning-Solution
Homework 1: Backpropagation Deep Learning Solution
Download link :
1 Theory (50pt)

To answer questions in this part, you need some basic knowledge of linear algebra and matrix calculus. Also, you need to follow the instructions:

Every vector is treated as column vector.

You need to use the numerator-layout notation for matrix calculus. Please refer to Wikipedia about the notation.

You are only allowed to use vector and matrix. You cannot use tensor in any of your answer.

Missing transpose are considered as wrong answer.

1.1 Two-Layer Neural Nets

You are given the following neural net architecture:

Linear1 ! f ! Linear2 ! g

where Lineari(x) ˘ W( i ) x ¯ b(i) is the i-th affine transformation, and f , g are element-wise nonlinear activation functions. When an input x 2 Rn is fed to the network, yˆ 2 RK is obtained as the output.

1.2 Regression Task

We would like to perform regression task. We choose f (¢) ˘ (¢)¯ ˘ ReLU(¢) and g to be the identity function. To train this network, we choose MSE loss function ‘MSE(yˆ, y) ˘ kyˆ ¡ yk2, where y is the target output.

(1pt) Name and mathematically describe the 5 programming steps you would take to train this model with PyTorch using SGD on a single batch of data.

(5pt) For a single data point (x, y), write down all inputs and outputs for for-ward pass of each layer. You can only use variable x, y,W(1), b(1),W(2), b(2) in your answer. (note that Lineari(x) ˘ W(i) x ¯ b(i)).

(8pt) Write down the gradient calculated from the backward pass. You can only use the following variables: x, y,W(1), b(1),W(2), b(2), @‘ , @z2 , @yˆ in your

yˆ @z1 @z3

answer, where z1, z2, z3, yˆ are the outputs of Linear1, f ,Linear2, g.

(d) (3pt) Show us the elements of

@z2

,

@yˆ

and

@‘

(be careful about the dimen-

@z3

@yˆ

sionality)?

@z1


1.3 Classification Task

We would like to perform multi-class classification task, so we set both f , g ˘ ¾, the logistic sigmoid function ¾(z) ˘. (1 ¯exp(¡z))¡1.

(5pt + 8pt + 3pt) If you want to train this network, what do you need to change in the equations of (b), (c) and (d), assuming we are using the same MSE loss function.

(1pt) Things are getting better. You realize that not all intermediate hidden activations need to be binary (or soft version of binary). You decide to use f (¢) ˘ (¢)¯ but keep g as ¾. Explain why this choice of f can be beneficial for training a (deeper) network.

1.4 Conceptual Questions

(2pt) Why is softmax actually soft(arg)max?

(2pt) In what situations, soft(arg)max can become unstable?

(2pt) Should we have two consecutive linear layers in a neural network? Why or why not?

(4pt) We covered various activation functions in class including ReLU, Tanh, Sigmoid, and LeakyReLU. Can you give one advantage and disadvantage of each function?

(4pt) What are 4 different types of linear transformations? What is the role of linear transformation and non linear transformation in a neural network?

(2pt) How should we adjust the learning rate as we increase or decrease the batch size?


2 Implementation (50pt)

You need to implement the forward pass and backward pass for Linear, ReLU, Sigmoid, MSE loss, and BCE loss in the attached mlp.py file. We provide three example test cases test1.py, test2.py, test3.py. We will test your implemen-tation with other hidden test cases, so please create your own test cases to make sure your implementation is correct.

Recommendation: Go through this Pytorch tutorial to have a thorough under-standing of Tensors.

Extra instructions:

Please use Python version ‚ 3.7 and PyTorch version 1.7.1. We recommend you to use Miniconda the manage your virtual environment.

We will put your mlp.py file under the same directory of the hidden test scripts and use the command python hiddenTestScriptName.py to check your implementation. So please make sure the file name is mlp.py and it can be executed with the example test scripts we provided.

You are not allowed to use PyTorch autograd functionality in your imple-mentation.

Be careful about the dimensionality of the vector and matrix in PyTorch. It is not necessarily follow the the Math you got from part 1.
