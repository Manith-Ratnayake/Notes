start of sequence (SOS) =

Language model predicts the proability of the sequence of words / characters
Chacracter level language model : meaning the model will predict the next character in a sequence given the previous characters

"hello"  -> " "

model will train on large text corpsus

RNN Based language model component :


Embedding layer :

converts characters into dense vectors : they capture relationship
simmilar charaters have simmilar embedding



RNN layer :

use embeddins to predict previous characters 
final layer = hidden state of RNN 

Output layer 
output layer is a usually softmax layer -> generates a probability distirbution 


Perplexity:
  Language model evaluation technique
  Exponention of the average negative log-likelihood 
  the lower the better


log-likelihood:
  Should give high proability to next tokens

SOS :
  start of the begaining of a sequence 
  it is a special token in the model tells where the sequence starts
  the model is use to how to initiate and generate next meagniful characters


chucking
sequence of characters rather than one large sequence -> this allows the model to predict multiple charater in parallel


Zero state initialization : You initialize the RNN hidden state to zeroes at the start of each chunk
Burn in                   : You let the model run few characters before making a prediction (helpful for model to warm up)
Carryig over state        : The final hidden state of 1 chuck can be used as the initial state for next chunk, : helping the model maintain                             conetxt across chunks


Initialzing the RNN to zero is not the most ideal way to 

SOS = is a input marker

Branching factor : model has to has wide options


Context = no of words/ can look at for given word