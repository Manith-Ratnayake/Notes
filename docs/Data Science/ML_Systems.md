Two families of samples
    - Non probability sampling
    - Random sampling

Non probability sampling
- Convenience sampling
- Snowball sampling 
- Judgment sampling
- Quota sampling


Simple Random sampling 
Stratified Sampling 
Weighted Sampling 
Reservoir sampling 
Importance sampling 


Classical Text Processing 
- Original Text
- Stopword Removal
- Lemmatization 
- Contraction
- Punctuation 
- Lowercase
- Tokenization
- N-gram 


Missing values 
- Missing not at random(MNAR)
- Missing at random (MCAR)
- Missing completely at random(MCAR)


Discretization is the process of turning continous features into a discrete feature.
This process is also known as quantization or bining


Feature crossing is the technique to combine two or more features to generate new features. 
Helpful for model the non-linear relationships between features.


Model assumptions
1. Prediction
2. IID
3. Smoothness
4. Tractability
5. Boundaries
6. Conditional independence
7. Normally distributed 

Each model in the ensemble is called base learner
Pipeline parallelism is a clever technqiue to make different components of a model on different machines run more in parallel.

NAS (Neural Architecture Search)
1. Search Space
2. Performance estimation strategy
3. Search stratey


The process of generating responses is called inferencing


ML reality
A company requires many machine learning models
    - Uber has 1000 models 
    - Google has 1000 models training with 100's of billion paramaters
    - Booking.com has 150+ models 
    - companies with 25_000 + employees have more than 100 models in productions (Algorithmia study 2021 41% companies)

Companies 
    Alibaba, ByteDance Weibo update their models 10min 
    Etsy 50 times a day 
    Netflix 1000 times a day 
    AWS every 11.7 seconds 

ML models best right after training and degrade over time

Having two different pipelines for training and inference is a common source for bugs for ML in production
