What is sequential Learning?
Sequence learning is the study of machine learning algorithms designed for sequential data


Plain CNN are not born good at length-varying input and data

 
Ways to deal with sequence labeling

1. Autoregressive model
2. Feed-forward neural network
3. Linear dynamics systems
4. Hidden markove model
5. RNN

-------------------------------------------------------------------------------------
RNN

1. Forward Pass
2. Backward Pass
3. Bidirectional Pass
4. Training RNN

Input
Output 
Hidden State

RNN can do more than language.... 
  - drawing pictures
  - music  


Vanishing Gradient problem = if weights are small, gradient shrink exponentially. Network stop Learning
Exploding Gradient problem = if weights are large, gradient grows exponentially, Weights flucatuate and become unstable


Vanishing Gradient problem | Exploding Gradient problem => is a problem 
When sequence length increase, it becomes hard for RNN to learn long term dependencies

Different configurations in RNN

one to one = (Vanila Neural Network) . (simple)
One to many = Image captioning
many to one = Sentiment analysis
many to many = Language translation


Types of RNN
- Bi directonal RNN
- Deep RNN


The output of the network is depends on the current input and on the value of the previous internal state.
The internal state maintains a (vanishing) memory about history of all past inputs.
To train RNN with gradient descent, RNN must be unfolded

The main and important part of RNN is
        Memory state = hidden state
        Not independant unlike other neural network types

The fundamental unit of RNN is "Recurrent unit" [not called recurrent neuron]

--------------------------------------------------------------------------------------------------------


Once trained RNN can work in Natural Language generation.


The activation function in RNN is traditionally implemented by "sigmoid" 
Another common choice is "tanh"
"ReLU" not much discussed


HOW TO LIMIT Vanishing Gradient Problem?

  ----> Use ReLU activations
  ----> Use LSTM or GRU architectures
  ----> Use proper initialization of the weights "W"

-------------------------------------------------------------------------------------------------------------------------------------

Differences with CNN

CNN models : filter slides along x and y dimension
RNN models : fliter slides along time dimension


-------------------------------------------------------------------------------------------------------------------------------------

Weight Initialization


A suitable initialziation of the weights permits the graident to flow quicker through the layer
A smoother flow ensures faster convergence of the training procedures --> It helps to reduce the issue of vanishing gradient


ADDITIONAL Information: {

      When using sigmoids or hyperbolic tangent neurons, use the following weight initialization
      This has to be repeated for each layer. The value n is the number of neurons in each layer.
      This ensures that all neurons in the network initially have approximately the same output distribution.
      The biases instead should be initialized to 0.
      Random initialization is important to break symmetry (prevents coupling of neurons).
}

-------------------------------------------------------------------------------------------------------------------------------------

"BiNN"

Variation of RNN which the input information flows in both direction and then the output of both directions are combined to produce the output.

forward layer works as RNN
meanwhile backward layer works in the opposite direction by taking current input and future hidden state


-----------------------------------------------------------------------------------------------------------------------------------



Recurrent Neural Network                                Deep Neural Network

weight are same across all the layer                    Weights are different for each layer
Sequential and no of inputs are NOT predefined          Does not have any special method or data ; no of inputs are fixed
Paramters are higher than DNN                           No of parameter are lower than RNN
Exploding & Vanishing gradient is major problem         Exploding & Vanishing gradient occurs but not major



-----------------------------------------------------------------------------------------------------------
"LSTM"


Type of RNN 

Three cells 

  i. Input Gate  [Amount of new information it should memorize]
  o. Output Gate [Amount of     information it should pass to next unit]
  f. Forget Gate [Amount of     information it should forget]
  g. Candidate cell state [What to write to cell later]
  

LSTM removes or adds information to the cell state, carefully regulated by structure called "gates".
Multiplicative Gates allows LSTM memory cells to store and access information over long period of time --> Therby avoiding the vanishing gradient problem.

Like RNN , LSTM must unfolded in time to be trained and understood


Downfall of LSTM
    Eventhough it provide huge improvement to RNN, it still struggles
    Gates are really never 0 or 1, the content of cell is inevitably corrupted after long time 
    Scales up quickly!!! Lots of paramters = Lots of training data



---------------------------------------------------------------------------------------------------------------------------

"GRU"


(Gated feedback recurrent neural network)

  * Similar to LSTM
  * Mergers the Cell state and hidden state
  * Mergers the forget and input gates into "update gate"
  * Computationally efficient (less parameters, less complex structure)

[Getting popular] 


<GRU> = Simplification of LSTM unit to merge forget and input gates

----------------------------------------------------------------------------------------------------------------------------

"Encode Decode"


Problems with Encoded-Decode paradigm

* Encoding transforms the entire sentence into a single vecto
* Decoding process uses this sentence representation for predicting the output
* After few time steps decoding process may not properly use the sentence representation due to long-term dependancy


To improve the quality of predictions we can ---> [
    
  Improve the qualityof sentence embedding "OR"
  Present the sources sentence representation for prediction at each time step. "OR"
  Present the RELAVENT source sentence representation for prediction at each time step.

]


Decoder takes 2 inputs
- Sentence vector
- Attention vector


How to train RNN?
- Backpropagation algorithm
- Variant of backpropagation algorithm namely BPTT (Back-Propagation through time)

----------------------------------------------------------------------------------------------------------------------------

"Transformer"


Standard architectre for building large language model
Transformer is a nerual network with a specific structure that includes a mechanism "self Attention or multi head attention"
Transformers are not recurrent network based on multi head attention

Three major components:
  Blocks => each layer is multi layer network 
  Input encoding 
  #(wait I will add)

---------------------------------------------------------------------------------------------------------------------------------

RNN vs Feed Forward neural network 
- Both are ANN pass to the end, feed forward network can perform classification, regression ....etc  task but cant remember the previous input

RNN vs CNN
- CNN designed to perform spatial data

----------------------------------------------------------------------------------------------------------------

RNN vs Transformers 

Transformers beats RNN by
  - Self attention
  - Parallelism

-----------------------------------------------------------------------------------------------------------------------

Some other area information

Gradient clipping - It is a technique used for EXploding gradient problem


Word Representation:
    * 1 - hot representation
    * Word - embedding



Word embedding is used in Word2vec

Word2vec : framework aimed at learning word embedding by estimating the likelihood that word is close to other word
            Popular models include Skip Gram, negative sampling, CBOW

Comparing models

Cosine similarity
t - SNE 


Perplexity : Language models are commonly assesed using PP (Perplexity metric)
