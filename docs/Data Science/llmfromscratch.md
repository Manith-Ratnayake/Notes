
Chapter 1


LLM can understand means --> can process and generate text way that coherent contextually relavent, 
not like they have human level consciousness or comphrehension


NLP designed for specific task , narrow applications, LLM have broader usage
    - Text categorization 
    - language translation


The first stage of training an LLM is known as pretraining, often called as foundation model. 
Like text completion


2 ways to fine tune an LLM 
    - Instructional := question and answers
    - Classification := spam or not


2017 Research paper Attention is all you need 
A key component of transformer architecture is self attention ( weights the importance of the word)


BERT - Bidirectional encoder representations from transformers
GPT - Generative pretrained transformers


few shot setting - 
zero shot setting - without specific example 
All LLMS are not transformers : RNN is used
ALL transformers are not LLM : Computer vision is used


Self supervised learning = self labelling
GPT is decoder part without and encoder 
Autoregressive model - predicting text at a 1 one time 


2020 GPT 3 release
GPT models also capable in perfroming translation tasks. This shocked scientists 
Emergent behaviour where the model is not told explictly to what
Original transformer (has encoder and decoder ) designed for language translation


1. Data prepraration process
2. Pretraining an LLM to create a foundation model
3. Fine tuning 


-------------------------------------------------------------------------------
Chapter 2


The process of converting words to vectors are known as embedding 
Word2Vec 
GPT2 models -    768 dimensions
GPT3 models - 12,288 dimensions


The token used for GPT models used only <|endoftext> for simplicity.
In batch using mask instead of padding 


Byte Pair Encoding (BPE)

* Used in GPT2 GPT3 models  
* BPE tokernizer break down unknown words into subwords and individual characters. So no need to replace with <|unk|> special tokens.
* It build vocabulary by iteratievly merging frequent characters into subwords and frequent subwords into words. 

Embedding layer is just a more efficient way than one hot encoding matrix multiplication in a FC
Just like regular batch_size in deep learning, LLM size also has to experiment. Less batch size less memory but more noisy model updates


Position is not aware and produce 2 similar vectors
Position aware embeddings
    - Relative positional embedding = how far apart
    - Absolute positional embedding = at which exact position | unique embedding 


OpenAI ChatGPT model use absolute positional embedding 


Input Processing pipeline 
Input Text ---> Individual Tokens ---> Token ID ----> Embedding vectors 


-------------------------------------------------------------------------------
Chapter 3.

1. Simple
2. Self attention with trainable weights 
3. Casual attention - Add a mask to previous output and current input 
4. Multi Head attention - organize the attention into multiple heads : allowing to capture ideas parallely


Cant translate word by word, must understand the context 
Limitation is encoder-decoder rnn is that rnn cant access directly earlier hidden states from the encoder during decoding phase. Also solely focus on current hidden state
RNN is good for short sentences. 
Before transformers RNN is the most popular encoder and decoder


Bahdanau attention 

Self attention used by transformers to compute efficient input repre by allowing each position in a sequence to interact with the weigh the importance of all other positions within the same sequence.


Goal of self attention is to compute context vector for each input vector that combines information from all other input elements. 

The higher dot product means higher similarity while lower means low similarity 

--------------------------------------------------------------------------------------
Chapter 4


GPT 2 weight are public , GPT 3 weights are not public
Layer Normalization - Adjust the activation(output) of a nerural network layer to have a mean 0 and variance of 1. 
RELU - Negative inputs to 0

GELU (Gaussian error linear unit)
SwisGLU (Swish-gated linear unit)

GELU used in LLM 

Batch normalization, across the batch dimensions
Layer normalization, normalize across the feature dimension 


Shortcut connections (skip and residual connections)

Vanishing gradient problem - where gradients become smaller as they propagate backward through the layers, making it difficult to effectively train earlier layers

Pre Layer Norm 
Post Layer Norm 

Weight Tying 


Chapter 5
-----------------------------------------------------------------------------

Backpropagation needs a loss function 
Perplexity measures how well the probability distribution predicted by the model matches the actual distribution of the words in the dataset


AdamW 
Variant of Adam improves the weight decay approach


Decoding strategies (text generating strategies)
Temperature scaling - probabilistic selection process to the next token generation task.
Greedy decoding - sampled the token with the highest probability as the next token 
Top K sampling

Chapter 6
-------------------------------------------------------------------------

Instruction fine tunning is more versatile. It demands larger dataset and greater computational resources to develop
Classification fine tunning require less data and less compute power

