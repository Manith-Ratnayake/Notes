Word Representing methods 

Bag of words

First mentioned in 1950s but became popular in 2000s.
1. Tokenization. Splitting up the sentence into individual words or subwords. 
Most common way is to split it by whitespace. Disadvantage is languages like Mandarin do not have whitespaces around individual words.
2. Vector Represention

Bag of words ignores the semantic meaning of the words


Word2Vec 

Released in 2013, first attempt to capture the meaning of the text in embedding. 
Embeddings are vector representation of data that attempts to capture its meaning. 


There are many types of embedding 
1. Word embedding
2. Sentence embedding 

Bag of words = Document level embedding 
Word2Vec = word embedding 

Autoregressive - when generating the next word, this architecture needs to consume all previous generated words. 


Compared to RNN, transformers can be trained in parallel. 


The encoder block of transformer has 
- Self attention 
- Feedforward Neural network

Self attention can look into multiple tokens at a time


[CLS] classification token 
BERT like models are commonly used for transfer learning

Encoder only model = Representation models (only focus on creating embedding)
Decoder only model = Generative models (only focous on text generation)

BERT - Encoder only architecture
GPT - Decoder only architecture 

GPT-1 was trained on 7_000 books and common crawl (web data) : 117 millions paramters
GPT-2   1.5 billion parameters
GPT-3   175 billion parameters

Context_length = Maximum number of tokens model process
Context_window = Entire document 

New promising architectures 
    - Mamba 
    - RWKV 

VRAM - (Video Random Access Memory ) - Amount of memory have in GPU


Tokenization Scheme
    - Word Token &  - Subword Token
    - Character Token & - Byte Token 

Some subword tokenizer also include bytes as token for some vocabulary. Otherwise cant represent this does make it byte because it does not use all 

Instead of using each token with a static word. LLM create contextualized word embedding 

Word2Vec proposed paper - Efficient Estimation of Word Representations in Vector Space
Word2 vec 
    - Skip-gram (Method of selecting neigbouring word)
    - Negative Sampling (Adding negative examples by random sampling from the dataset)


The method of choosing a single token from the probability distribution is called the "decoding strategy"


