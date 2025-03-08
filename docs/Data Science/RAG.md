Context Window
- In LLM it refers to the maximum number of tokens that model can process in a single pass.


All vector databases are vector stores, but not all vector stores are vector databases
Langchain tell vector stores!!!


Stages of RAG system
1. Indexing
2. Retrieval
3. Generation

Indexing process can be executed before user enters the query. Turning supporting data into vectors and storing them in a vector database. This can make the retrieval step is as fast as effective 

Qunatization is a lossy compression technique

Other people prompts are available on Langchain

Adaptive Retrieval - Generate multiple sets of embedding at different sizes. 
Searching lower dimension to get close to final result, searching lower dimension vectors are faster than higher dimenstion.
Once search is close to lower dimenstion searching higher dimenstion to and finalize the similarity search. 
Speed up on 30-90%
Matryoshka embeddings (named after Russina nesting doll )

Similarity metric can use different distance metrics while 
Vector search can use a different similarity metric


Vector Space / Embedding space / Latent space 
- Mathematicall construct that represent a collection of vectors in a high dimenstional space

Different ways to calculate distance between vectors
- Eucliden 
- Dot product (Inner product)
- Cosine similarity


Different Search Paradigms 
- Hybrid
- Sparse
- Dense 



Semantic Searhc Alogrithms
- KNN
- ANN

If exact nearest neigbour is required KNN, while ANN is balancing efficiency in and accuracy in larger datasets


Search Algorithms can be indexed 
- LSH
- (KD - trees)
- Ball trees
- PQ
- HNSW 

-------------------------------------------------------------------------------------

Reasons why RAG system fails

- Data used for retrieval may become outdated or irrelavent as new information emerges.
- LLM struugles to evolving user queries or changes in the target domain
- Underline hardware, software experience in performance issues and failures


Why evaluation is so important?
If you dont measure youself and after time you make changes and will be difficult to understand how or what improved


Ground Truth 
is data that represents the ideal responses you would expect if your RAG system was operating at peak performance.


CrowdSourcing 
- Amazon mechanical turk


RAGAS is a evalution platform designed specifically for RAG 

For retrieval RAGAS has 2 metrics, 
  - Context precision
  - Context recall
  
RAG provide each stage evaluation
RAGAS provides metrics for entire system called end-to-end evaluation

For generation, RAGAS has 2 metrics,
  - Answer correctness
  - Answer similarity


More evaluation techniques
  - Context relevancy
  - Context entity recall
  - Aspect critique


Additional Evaluation technique 
- Bilingual evaluation understudy (BLEU)
- Recall oriented understudy for gisting evaluation (ROUGE)
- Semantic similarity 
- Human evaluation


-------------------------------------------------------------------------------

Retrivers 
  are responsible for querying the vector store and retrieving the most relavent documents based on the input query.


Base retriever (dense embedding)
Similarity score threshold retrieval 
MMR 
BM25 retriver
Ensemble retriever
Wikipedia retriever 
KNN retriever


------------------------------------------------------------------------------------

Langchain expression language (LCEL)


-------------------------------------------------------------------------------------

Prompt Paramters
- Temperature = How likely model selects word further down the probability distribution
- (Top - p)   = focused randomness
- Seed        = like in programming reproducible seed 


No shot, single-shot, multi-shot
Shot = is an example

When filling the prompt with data from other parts of the system called "hydrating"


Fundamental of prompt design
- Be concise and specific
- Ask one task at a time.
- Turn generative tasks into classification tasks.
- Improve response quality by including examples.
- Start simple and iterate gradually
- Place instruction at the begaining of the prompt 


* Not to transfer prompts to one LLM to another LLM. Each LLM has specific technqiues for the architecture. 
Claude-3 prefer XML encoding, Llama3 uses a specific syntax when labelling different parts of the prompt


Transformations 
- Language transformation
- Tone transformation 

Expansion
Reverse of the concept of summarization 

----------------------------------------------------------------------------

Three types of RAG
1. Naive rag
2. Hybrid rag
3. Re-ranking 

If not used large amount of chunks of text, context will experience higher level of fragmentation. This fragmentation cause decrease understanding and capture of the context and semantics within chunks, reducing the effectiveness of retrieval mechanism of rag app.

Hybrid RAG expands the concepts of naive rag by using multiple vectors for the retrieval process. 


Advance Approches
  - Query Expansion
  - Query decompositon
  - (MM - RAG)

After the semantic search and keyword search completes their retrieval, re rank the results based on the rankings across both sets.

In here LLM is bringing to retrieval stage, ealier used on generation stage.(prompt engineering)

Query Decomposition
Strategy focus on improving question-answering. Falls under category of query translation which is set of approaches that focuses on improving the initial stage of the rag pipleline. In here breaking down a question into smaller questions. These questions can either be approched sequentally or independantly. After each question answered final response has broder perspective than original response


Chain of Thought (Cot)
Interleaving retrieval

Combination is called Interleave retrieval with CoT and IR-CoT


Multi Model RAG

Modality independance = multi model embedding concept of cross-modality representation of the same context is called

