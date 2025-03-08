
Properties of Data
• Volume: Scale of Data.
• Variety: Different forms of data.
• Velocity: Rate of data streaming and generation.
• Value: Meaningfulness of data in terms of information.
• Veracity: Certainty and correctness in data.

Data Preprocessing
It is a process that involves transforming raw data into an understandable
format.
• Data cleaning
• Data integration
• Data transformation
• Data reduction
Why pre-process the data?
• Data in the real world is:
• incomplete: lacking values, certain attributes of interest, etc.
• noisy: containing errors or outliers
• inconsistent: lack of compatibility or similarity between two or more facts

Data Cleaning
• Process of fixing or removing:
• Incorrect
• Corrupted
• Incorrectly formatted
• Duplicate
• Incomplete data within a dataset
• If data is incorrect, outcomes and algorithms are unreliable.
• There is no one absolute way to prescribe the exact steps in the data cleaning process.

Step 1: Removing Duplicate or Irrelevant Observations
• Duplicate observations will happen most often during data collection.
• De-duplication is one of the largest areas to be considered in this process.
• Irrelevant observations are when you notice observations that do not fit into the specific problem.
• Creating a more manageable and more performant dataset

Step 2: Fixing Structural Errors
• Strange naming conventions.
• Typos.
• Incorrect capitalization.
• Inconsistencies can cause mislabeled categories or classes.
• “N/A” and “Not Applicable” both appear, but they should be analyzed as the same category.

Step 3: Filtering Unwanted Outliers
• There will be one-off observations where do not appear to fit within the data.
• Just because an outlier exists, doesn’t mean it is incorrect.
• This task is needed to determine the validity.
• If an outlier proves to be irrelevant for analysis or is a mistake, consider removing it.

Step 4: Handling Missing Data
• You can’t ignore missing data because of many algorithms.
• There are a couple of ways to deal with missing data.
• Observations that have missing values can be dropped, but doing this will drop or lose information, so be mindful of this before removing it.
• Secondly you can input missing values based on other observations.
• You might alter the way the data is used to effectively navigate null values

Step 5: Validation
• Does the data make sense?
• Does the data follow the appropriate rules for its field?
• Does it prove or disprove your working theory, or bring any insight to light?
• Can you find trends in the data to help you form your next theory?
• If not, is that because of a data quality issue?

DT is the process of converting data from one format or structure into another.

Feature Extraction (Reduction) Techniques
• Unsupervised
• Latent Semantic Indexing (LSI): truncated SVD
• Independent Component Analysis (ICA)
• Principal Component Analysis (PCA)
• Supervised
• Linear Discriminant Analysis (LDA)
• Canonical Correlation Analysis (CCA)
• Partial Least Squares (PLS)

