LLM twin concept 
* is an AI character that incorporates writing style, voice and personality into an LLM.
Digital version of a person 


In MVP : V means viable it does not mean incomplete features, good product working that users like to see what will happen in future 


FTI Architecture (Feature/Training/Inference)
- Any ML activity can be break down into this : similar to classic software(DB, Model,  UI)


The feature Pipeline 
Instead of directly passing to the model, we store, version control and share them.


The training pipeline 

The models are stored on a model registry : it will store models, versions, share models with the inference pipeline. 
Most modern regiters store metadata
Model registry is a centralized repositary that manages ML models throughout their lifecycle.


The inference pipeline
Takes features from feature pipeline and training pipeline takes models and then train 
  if batch system - store on a database
  if real time - sending it to the client 


Can easily upgrade or roll back models, because we know model v1 takes f1,f2,f3 and v2 takes f4,f5,f6
FTI pattern does not have to contain only three pipeline, often it have more 

Pipeline can compose of 
Feature pipeline - Computes features, Validate features
Training pipeline - training and evaluation 

Each pipeline can evolve differently without knowing the prescence of others 
When added new features it wont break the system therefore can expand

Knowing how the ML system works is valuable understanding other peoples work 


Data Collection 
ETL (Extract Load Transform)
Output of this is a NoSQL database

Collected data
  Articles
  Posts 
  Code 

Training Pipeline 
  - Data scientists will run best hyperparameters

  
Inference pipeline 
 - It is connected to the model registry and logical fetaure store 


Feature - cpu bases
Training - gpu based 
Inference - intermediate, but has to give the result to user in minimum latency 

Data 
* Collect data from sources 
* Clean the raw data 
* Create instruct datasets for fine tunning LLM 
* Chunk and embed data 


Train 
* Fine tune LLM (7B, 14B, etc ...)
* Switch between LLM types 
* Track and compare experiments 
* Automatically start when new dataset available 

Inference 
* Autoscaling based on user requests
* Automatically deploy models that pass evaluation steps 
* Inference with LLMs for various size 


------------------------------------------------------------------------------------------------
LLMOps - Instruction dataset, model versioning, experiment tracking, CT/CI/CD, Prompt and system monitoring 
ZenML - Orchestrator fill gap between ML and MLOps 


NoSQL can use as a datawarehouse also development easier 
For large scale can use snowflake or bigquery

-----------------------------------------------------------------------------------------------------

Any LLM will understand data it was trained on, sometimes called parameterized knwoledge

There are 2 problems RAG solves, 
  - Hallucinations
  - Old or private information 

Any LLM is trained or fine tune has issues:
  - Private data 
  - New data 
  - Cost 

A RAG system is composed of 3 main modules:
  - Ingestion pipeline [batch or streaming pipeline used to populate vector DB]
  - Retrieval pipeline - A module that queries the vector db and retrieves relavent entries to user input
  - Generation pipeline - Retrive data to augment the prompt and LLM to generate answers 

RAG 
* Data extraction module - gather data from data sources  
* Cleaning layer - Removing unwanted data 
* chunking module - Split the cleaned documents into smaller one
* embedding component - uses an embedding model to take chunk's content
* loading module - embedded chunks along with metadata 


Must use a distance metric to compute 2 vectors,
  - Eucliden
  - Manhatton 
  - Cosine (popular) [ 1 - cosine of the angle between 2 vectors]

-1 to 1 : opposite 
0 : orthonogol
1 : same direction 

** Choosing proper distance between 2 models depends on the data and the embedding model 
User input and embeddings must be in same vector space. Otherwise cant compute distance
For that it is essential preprocess same way as raw documents and user input :same function, models, hyperparameters
inference will produce wrong results ---> training-serving skew


Dimensionality Reduction algorithm 
- PCA, UMAP, t-SNE 

Feature hashing (hashing encoding, hash trick)
technique used to convert categorical variables into numerical features by applying a hash function to category value
reduces dimensionality of the feature space by mapping categories into a fixed number of bins or buckets
This makes it efficient in computing and memory. Different categories might map to the same bin leading to loss of information
Difficult to understand the relationship between the original catgories and hash feature


Word to embedding 
   - Word2vec
   - GloVe

encoder only transformer : such as BERT (family RoBERTA)
Python SentenceTransformer 

MTEB (Massive Text Embedding Benchmarking)

Vector DB use ANN(Approximate Nearest Neigbor) to find the close neigbors  
ANN does not return top result ; trade off between accuracy and latency favors ANN 

Vectors are index using data structures 
  - Hierarchical navigable small word(HNSW)
  - Random projection
  - Product quantization (PQ)
  - Locally-sensitive hashing (LSH)

Algorithms for creating the vector index 
 - Random projection [Reduce dimenstion of vectors by using a random matrix]
 - PQ [compress vectors by dividing them into smaller sub vectors then quantize to representative code]
 - LSH [similar vectors into buckets ; faster apporixate nearest neigbor ]
 - HSNW [multi layer graph where each node represent a set of vectors, simmilar nodes connected]


Advance RAG
1. Evaluation module
2. Algorithm 

Vanila RAG can optimize in 3 ways 
 - Pre Retrieval
 - Retrieval
 - Post Retrieval

Pre retrieval 
  - Data indexing 
  - Query optimizing 

FAISS are effective in similarity search. But lack comphrehensive data management capabilities.
  
Query Routing 
* Query rooting is which action should take base on the user input 


Retrieval optimization 
- Improving the embedding models 
- Leveraging the DB's filter and seacrh filters 

Instead of fine tunning, can guide the embedding generation 

Hybrid Search 
Filtered vector search 

2 popular methods in post retrieval steps 
  1. Prompt compression 
  2. Re-ranking 

RAG system is built on 2 independant systems
 - ingestion pipeline :
 - inference pipeline :  


Feature store
will be the central access point for all the features used within training and inference 

Batch Processing advantages 
   - Does not require immediate data processing 
   - Simplicity 

CDC (Change data capture)
keep 2 or more data storage in sync without computing and I/O overhead
DDD (Domain driven design )

---------------------------------------------------------------------------------------
Data duplication 

Overfitting
Biased performance 
Inefficient training 
Inflated evaluation metrics 

Exact deduplication removes identical samples through data normalization, hash generation, duplicate removal

Fuzzy deduplication
popular is Minhash deduplication

Semantic similarity 
focusing meaning of the text. Use word2...FasText for transforming to vectors to capture meaning

Data decontamination 
Process of ensuring that the training dataset does not contains samples that are identical to testsing set


LLM as a judge is known to have serveral biases 


Small epoch - underfitting
Large epoch - overfitting 

Optimizer 
AdamW

--------------------------------------------------------------------------------------
Reinforcment Learning from Human Feedback (RLHF)

Direct Preference Optimization (DPO)


KV Cahche 

