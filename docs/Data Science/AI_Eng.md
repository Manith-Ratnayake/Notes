2 types of language model 
    - Masked language model
    - Auto regressive model


Masked Language model 

is trained to predict missing tokens anywhere in a sequence, using the context from both before and after the missing token.
ex : BERT 

LLM can be trained using self-supervision
A model that can work with more than one data modality is also called multi modal model
A generative multimodel is also called a large multi model (LMM)

AI Engineering
refers to process of building applications on top of foundation models


Dataset Engineering
refers to curating, generating and annotating the data needed for training and adapting AI model

2014 seq2seq
Have encoder process input and a decoder that generates output
Encoder output to final hidden state, then decoder outputting using final hidden state and previous generated output

2 problems addresssed in Vasawani et al. (2017)
vanila seq2seq decoder output tokens using only final hidden state of the input
RNN encoder and decoder means both input and output is done sequentially making it slow for long sequence

Attention mechanism is introduced three years before transformer architecture
Attention mechanism can be used with other other architectures
2016 Google seq2seq with attention mechanism GNMT 


With transfomers the input tokens are processed in parallel. speeding up input processing
Still output processing is slow

Inference for transformer based language models cosnsist 2 steps
    - Prefil
    - Decode 


Attention mechanism 
    - Query vector = current stage of decoder at each decoding step
    - Key vector = previous token 
    - Value vector = actual value of a previous token

Each previous token has key and value vector. The longer the sequence, more key and value need to computed and stored.
This makes hard to increase context length of the transformer model 


Attention mechanism always almost multi headed
Multiple heads allow the model to attend to different groups of previous tokens simulataneously
All output of attention heads are concatenated, output projection matrix used applying another transformation before fedding into next computation


Tranformer archiecture
    consist of multiple transformer model
    the exact content of block varies between different models
    In general it has,
             Attention module = [query, key, value, output projection ] 
              MLP = each linear layer is separated by non linear activation function
                        (Where an activation function allows the linear layers to learn non linear pattern)


Linear layer = feedforward layer
No of transfomer blocks in a transfomer model is reffered to as that model's number of layers. 

AlexNet - 2012
GAN      - (2014 -  2019)

1 popular model is RKWV 
It does not have the same context length limitation like transformer model. however no context length limitation doesnt guarantee good performance with long context

if a model has 7 billion parameters and each parameter using 2 bytes = 14 billion bytes GPU 
No of parameters may be misleading if the model is sparse. A sparse model large percentage of zero value parameters
7B model 90% sparse means only only 700million non zero paramters
Sparcity allows for more efficient data storage and computation. Large sparse model can require less compute than a small dense model

A type of sparse model that MoE (Mixture of experts)
An MoE is divided into groups of paramters each group is an expert. Only subset of the experts is active for process token
Ex : Mistral 8x7B is a mixture of 8 experts. each expert with 7B paramters, 8 x 7 = 56 due to parameter sharing only 46.7B


FLOPS - Floating point of operation
Hyperparameter transfering


Eventually LLM will use all internet data
This is like if post something will be indexed by google

Every model post training is different
    - Supervised finetunning (SFT)
    - Preference finetunning = typically done using reinforcement learning

Pre training - to acquire knowledge 
Post training - learning how to use that knowledge 

Pre trained model is optimized for completition rather than conversing 
Companies use highly educated labelers to generate demonstration data 


RLHF consist of 2 parts 
- Train a reward model that scores the foundation model output
- Optimize the foundation model to generate responses for which the reward model will give maximal scores

RLHF used today, DPO are getting popular
Evaluating each sample independently is `pointwise evaliation`

A model construct its output through a process known as sampling

Always picking the most likely outcome is called greedy sampling
However for large language model, greedy sampling creates boring output
Higher temperature reduces common token, increases rarer token making creative response


Neural network's probabilities because it helps reduce the underflow problem
Small numbers rounded to 0, log scale helps reduce the problem

Top -k is a sampling strategy to reduce the computation workload without sacrificing too much the model's response diversity.
Softmax need 2 passes over all possible values. 
    One to perform the exponential sum
    One to perform for each value
    - for LLM with large vocab this is expensive

Top P also nucleus sampling
model sums the probabilities of the most likely next value in descending order and stop when the sum reach p
Only values within cumulative probability are considered.

Related sampling strategy is min-p, set minimum probability token must reach to be considered during sampling



Generating 2 output is expensive
OpenAI (2021) found that sampling more outputs led to better performance, but only up to 400 outputs.

A model is considered robust when the input is slightly change but does not affect the output
A model tends to repeat same mistakes across queries

Constraint sampling
    is a technique for guiding the generation of text toward certain constraints

Snowballing hallucination - after making an incorrect assumption a model can continue hallucinating to justify the initial wrong assumption (Zhang et al 2023)

Incorrect assumption make mistakes by model otherwise model knows the true answer



Evaluating LLM model is harder compared to traditional ML system
ex : First grade student math and Ph.D level student



Language modelling metrics 
    - Cross entropy
    - Perplexity
    - BPC
    - BCP


Entropy measures how much information, on average a token carries. The higher the entropy the more information each token carries out 


A language model's cross entropy means how difficult it is for the language model to predict what comes next in the dataset


Fundamental correctness evaluation means evaluating a system based on whether it performs the intended functionality
But not straightforward to measure and cannot be automated

Lexical similarity measures how much two texts overlap
1. counting how many token two text have in common
2. n-gram similarity
... BLEU, ROUGE, METEOR++, TER, CIDEr

Teaching models what to do via prompts is in context learning


Vector Search algorithms
- LSH (locality sensitive hashing)
- HNSW (Hierarchical Navigable small world)
- Product qunatization 
- IVF (Inverted file index)
- Annoy (Approximate Nearest Neighbors Oh yeah)

Other algorithms 
    - Microsoft SPTAG (Space Parition Tree And Graph)
    - FLANN  (Fast Library for Approximate Nearest Neigbors)

Any database that can store vectors can be called vector database
Term base retriveal is generally much faster than embedding-based retriveal during both indexing and query


Context precision - out of all the documents retrieved, what percentage is relavent to the query
Context recall - out of all documents that are relavent to the query, what percentage is retrived

Context precision is also called context relevance


Query rewriting is also query reformulation, query normalization, query expansion
Long-term memory can be used to store the overflow from short-term memory.
Finetuning is the process of adapting a model to a specific task by further training the whole model or part of the model

Finetuning bias mitigation
If a model constantly assign male CEO can be added with female CEO
Distills larger model knowledge into smaller model is called distillation
ex : Flan-T5 model outperform GPT 3 in various text editing task despite it being 60 times smaller


Possible to fine tune larger model but fine tunning smaller model is more common


Fine tunning is a one way to transfer learning - concept in 1976 by Bozinovski and Fulgosi
Google multi lingual translation system : Portugeese-English , English-Spanish to directly to Spanish-Portugees


Like for transfer learning can use finetunning, also feature base learning 
Common in computer vision
ex: 2010 Imagenet dataset to extract features used for such as object detection, image segmentation

Self supervised finetuning is also called continued pre-training
Possible to extend model context length. Long context finetunning typically requires modifying the model architecture


Parameters that are kept unchange is called frozen parameters
During inferencing only forward pass
How much each parameter should be readjusted given its gradient value decide by optimizer

Training memory = model weights + activation + gradient + optimizer states
Gradient checkpoining, activation recomputation - instead of storing activation for reuse, recompute activations when necessary

