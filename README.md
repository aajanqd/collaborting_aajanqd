# 1.1 Convolution
### 1

The equation to be used is:

(n-f+2p)/s + 1

64x111x111 -> 4x234x234

---------

x-dimension: 64 -> 4
n = 64, f = 61, p = 0, s = 1

(64-61+2(0))/1 + 1 = 3 + 1 = 4

---------

y-dimension: 111 -> 234

n = 111, f = 2, p = 62, s = 1

(111-2+2(62))/1 + 1 = 109+ 124 + 1 = 234

---------

z-dimension: same as y-dimension

### 2

256x56x56 -> 14x126x126

x-dimension: 256 -> 14

n = 256, f = 243, p = 0, s = 1

(256-243+2(0))/1 + 1 = 13 + 1 = 14

---------

y-dimension: 56 -> 126

n = 56, f = 3, p = 36, s = 1

(56-3+2(36))/1 + 1 = 53 + 72 + 1 = 126

---------

z-dimension: same as y-dimension

### 3

256x56x56 -> 42x72x72

x-dimension: 256 -> 42
n = 256, f = 215, p = 0, s = 1

(256-215+2(0))/1 + 1 = 41 + 1 = 42

---------

y-dimension: 56 -> 72
n = 56, f = 3, p = 9, s = 1

(56-3+2(9))/1 + 1 = 53 + 18 + 1 = 72

---------

z-dimension: same as y-dimension

# 1.2 Dropout
### 1
torch.nn.Dropout() (default probability = 0.5)

### 2
The dropout technique used in neural networks is more or less the equivalent of the bagging technique used in standard machine learning models. Both bagging and dropout are based on the idea of testing an ensemble of models on subsets of the training data in order to maximize predictive capacity. Simply put, training multiple models and picking the one with the best performance is always better than only using one model. However, bagging and dropout differ in the following ways:
1) In bagging, all models are independent of one another (and in many cases, entirely different models are used - e.g. bagging SVM and logistic regression). In dropout, the models are simply subnetworks of the parent neural network. They are not independent, as they share parameters.
2) In bagging, all models are trained to conversion. In dropout, training every single possible subnetwork would not be doable. Therefore, only a small subset of all subnetworks is trained.

The dropout technique is a useful form of regularization with two distinct advantages: a) it's computationally inexpensive, and b) it is not limited to any specific type of model.


# 1.2 Batch Norm
### 1
A mini-batch is a subset of your training data. For example, if you like to train your model to identify different types of dogs, you may begin with 1000 pictures of dogs. A mini-batch might be 10 (or 20, or 50, or 100) of those images.

### 2
