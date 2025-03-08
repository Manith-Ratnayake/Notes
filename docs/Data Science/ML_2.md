In 1943 

Neurophysiologist Warren McCulloh
Mathematician Walter Pitts
Propositional Logic

1960s winter
1990s popular machine Learning models were developed


Due to gaming industry high GPU power GPU's are available for training


TLU = Threshold logic unit
LTU = Linear Threshold unit


Cells that fire together, wire together - Hebb's rule


Perceptron - No probability
Logistic Regression - Probability


Researches were disappointed by XOR problem) : true on Logistic Regression but high expectation

Stacking multiple pecerptron (MLP)
MLP solves XOR problem

Feedforward Neural Network(FNN)
People say DNN even a shallow one
 

Train MLP? -> 1986 Back propagation was introduced  (Simply Gradient Descent)


Connection weight should be initialize randomly



If output between 0 and 1 = ReLU/Softplus


MSE
MASE if lot of outliers
Huber loss for both


Unsupervised Learning


We have input features X but do not have output features Y



Yann LeCun

"If intelligence was cake, unsupervised learning will be the cake, supervised learning will be
the icing on the cake reinforcement learning will be the cherry on the cake"



Clustering
- Goal is to group similar type of objects into clusters. 

Anomaly Detection ( Outlier detection )
- Goal is to learn what is normal data looks like, and use this to detect abnormal instances

Density Estimation
- Estimating PDF of the random process that generate datasets; used for anamoly detection




customer segmentation




There is no universal answer for what is cluster is, it really depends on the context and different algorithms


from sklearn.cluster import KMeans
k = 5
kmeans = KMeans(n_clusters = k)
y_pred = kmeans.fit_predict(X)



if you plot the cluster's decsion boundries you will get Voronoi Tessellation

hard clustering - Assigning each instance into a single cluster
soft clustering - score per cluster


kmeans.transform(X_new)

--------------------------------------------------------------------------------------------------------------

Dimensionality Reduction

2 main dimenionality Reduction

Proection 
Manifold

-----------------------------------------------------------------------------------------------------

ANN


from sklearn.datasets 		import load_iris
from sklearn.linear_model 	import Perception

MLP = Multi layer perceptron

When an ANN contains deep stack of Neural Networks - (DNN)


The hyperbolic tanget function 	   | tanh(z) 
The rectified Linear Unit function | ReLU


Sigmoid = S shape function 
ReLU works better



After model is created you must call `compile()` method 

Tensorboard is visulization purposes
binary file --> `event` each summary 

Transfer learning
Already trained model for transfer learning 



CNN                    - Image processing
RNN                    - Sequential Data
Autoencoders           - Represenational Learning
Generative adversarial - Model and generate data


ReLU
Leaky ReLU
RRLU (Raqndomized Leaky ReLU)
PReLU (Parametric Leaky ReLU)

Outperform ReLU 
ELU - Exponential Linear Unit
SELU  Self normalized 





Momentum optimization and RMSProp  combination is
	ADAM - Adaptive moment estimation


Batch regularization was to solve vanishing gradient problem
Dropout { Best Regularization }

Alpha Dropout = to preserve mean and std in the input

Max norm regularization 

Monte Carlo Dropout




Gradient decent works best when all the items IID Independant Identically Distributed

----------------------------------------------------------------------------------------------


The most important layer in CNN is the convolutional layer.
To have the same height and same width in the previous layer it is common to add zeros around in the inputs
ZERO PADDING


Padding must be either VALID or SAME

if set to valid ; does not need zero padding
SAME ; zero padding is required


Inference [ Making a prediction for a new instance]


Alexnet
Resnet
GoogleNet



FCN - Fully convolutional Network






