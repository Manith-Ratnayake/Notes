Principal Component Analysis (PCA)
• PCA is used to compress a dataset onto a lower-dimensional featuresubspace.
• Feature selection finds a subset of features while PCA produces asmaller new set.
• PCA helps us to identify patterns in data based on the correlation between features.
• PCA aims to find the directions of maximum variance in highdimensional data.

Applications of PCA in Machine Learning
• PCA is used to visualize multidimensional data.
• It is used to reduce the number of dimensions in healthcare data.
• PCA can help resize an image.
• It can be used in finance to analyze stock data and forecast returns.
• PCA helps to find patterns in the high-dimensional datasets.

Overfitting Vs Underfitting
 Overfitting
• Good performance on the training data, poor generalization to other data.
• A high accuracy measured on the training set.

 Underfitting
• Poor performance on the training data and poor generalization to other data.
• Reducesthe accuracy and produces unreliable predictions.

------------------------------------------------------------------------------------------------

Regression Analysis in Machine Learning
• Regression analysis is a statistical method to model the relationship between a dependent and independent variables.
• Regression helps to understand how the value of the dependent variable is changing.
• It predicts continuous/real values such as temperature, age, salary, price, etc.



• Dependent Variable:
The main factor in Regression analysis which we want to predict
or understand is called the dependent variable. It is also called target variable.

• Independent Variable: 
The factors which affect the dependent variables, or which are
used to predict the values of the dependent variables are called independent variable,
also called as a predictor.

• Outliers:
Outlier is an observation which contains either very low value or very high
value in comparison to other observed values.
• Multicollinearity:
If the independent variables are highly correlated with each other
than other variables, then such condition is called Multicollinearity. It should not be
present in the dataset, because it creates problem while ranking the most affecting variable.

• Underfitting and Overfitting:
If our algorithm works well with the training dataset but
not well with test dataset, then such problem is called Overfitting. And if our algorithm
does not perform well even with training dataset, then such problem is called underfitting    

Why Regression Analysis?
• Regression estimates the relationship between the target and theindependent variable.
• It is used to find the trends in data.
• It helps to predict real/continuous values.
• By performing the regression, we can confidently determine the most important factor, the least important factor


Types of Regression 
• Linear Regression
• Logistic Regression 
• Polynomial Regression 
• Support Vector Regression 
• Decision Tree Regression 
• Random Forest Regression 
• Ridge Regression 
• Lasso Regression


Linear Regression
• Linear regression is a statistical regression method which is used for predictive analysis.
• Linear regression shows the linear relationship between the independent variable (X-axis) and the dependent variable (Y-axis).
• If there is only one input variable (x), then such linear regression is called simple linear regression.
• If there is more than one input variable, then such linear regression is called multiple linear regression.
• 𝑌 = 𝑎𝑋 + 𝑏
• Y = dependent variables (target variables), X= Independent variables (predictor variables), a and b are the linear coefficients

Examples:
• Analyzing trends and sales estimates.
• Salary forecasting.
• Real estate prediction.
• Arriving at ETAs in traffic.


Logistic Regression

• Logistic regression is another supervised learning algorithm which isused to solve the classification problems.
• Logistic regression algorithm works with categorical variables.
• It is a predictive analysis algorithm which works on the concept of probability.
• Logistic regression uses sigmoid function or logistic function which is a complex cost function.
• The sigmoid function is used to model the data in logistic regression.
• f (x) = 1 / 1 + e ^ -x


------------------------------------------------------------------------------------------------

Support Vector Machine

• One of the most popular Supervised Learning algorithms for Classification as well as Regression problems.
• The goal is to create the best line or decision boundary that can segregate n-dimensional space into classes.
• This best decision boundary is called a hyperplane.
• SVM chooses the extreme points/vectors that help in creating the hyperplane.
• These extreme cases are called as support vectors.
• Support vector creates a decision boundary between these two data (cat and dog) and choose extreme
cases (support vectors), it will see the extreme case of cat and dog.
Based on the support vectors, it will classify it as a cat.
• SVM algorithm can be used for Facedetection, image classification, textcategorization, etc.

Types of SVM

• Linear SVM
• Linear SVM is used for linearly separable data.
• If a dataset can be classified into two classes by using a single straight line.
• Non-linear SVM
• Non-Linear SVM is used for non-linearly separated data.
• If a dataset cannot be classified by using a straight line, then such data is termed as non-linear data.


Linear SVM

• SVM algorithm helps to find the best line or decision boundarywhich is the hyperplane.
• SVM algorithm finds the closest point of the lines from both theclasses.
• These points are called support vectors.
• The distance between the vectors and the hyperplane is called as margin.
• The goal of SVM is tomaximize this margin. Thehyperplane with maximum
margin is called the optimal hyperplane.
------------------------------------------------------------------------------------------------

Decision Trees

• Decision Tree is a Supervised learning technique that can be used for both classification and Regression problems.
• It is a tree-structured classifier.
• Internal nodes represent the features of a dataset, branches represent the decision rules, and each leaf node represents the outcome.
• In a Decision tree, there are two nodes, which are the Decision Node and Leaf Node.
• Decision nodes are used to make any decision whereas Leaf nodes are the output of those decisions.
• It is called a decision tree because, similar to a tree, it starts with the root node.
• In order to build a tree, the Classification and Regression Tree (CART) algorithm is used.
• A decision tree simply asks aquestion and based on the answer (Yes/No), it furthersplit the tree into subtrees.
• Decision Trees usually mimic human thinking ability while making a decision, so it is easy to understand.
• The logic behind the decision tree can be easily understood becaus it shows a tree-like structure

Hunt’s algorithm
❖ Most decision tree induction algorithms are based on Hunt’s algorithm

Pros & Cons
 Pros
• It is simple to understand as it follows the same process which a human follow while making any decision in real-life.
• It can be very useful for solving decision-related problems.
• It helps to think about all the possible outcomes for a problem.
• There is less requirement of data cleaning compared to other algorithms.
 Cons
• The decision tree contains lots of layers, which makes it complex.
• It may have an overfitting issue, which can be resolved using the Random Forest algorithm.
• For more class labels, the computational complexity of the decision tree may increase.

------------------------------------------------------------------------------------------------
K-Nearest Neighbor (K-NN)

• K-NN is one of the simplest ML algorithms.
• K-NN algorithm assumes the similarity between the new case/data and available cases and put the new case into the category that is
most similar to the available categories.
• K-NN algorithm stores all the available data and classifies a new data point based on the similarity.
• K-NN algorithm can be used for Regression as well as for Classification.

Pros & Cons of K-NN

Pros
• It is simple to implement.
• It is robust to the noisy training data.
• It can be more effective if the training data is large.

Cons
• Always needs to determine the value of K which may be complex some time.
• The computation cost is high because of calculating the distance between the data points for all the training samples.
Random Forest
• Random Forest is a popular machine learning algorithm that belongs to the supervised learning technique.
• It can be used for both Classification and Regression problems in ML.
• It is based on the concept of ensemble learning, which is a process of combining multiple classifiers to solve a complex problem.
• Random Forest is a classifier that contains a number of decision trees on various subsets of the given dataset.

Working Model of Random Forest
• It is possible that some decision trees may predict the correct output, while others may not.
• But together, all the trees predict the correct output.
• There should be some actual values in the feature variable of the dataset so that the classifier can predict accurate results.
• The predictions from each tree must have very low correlations

Why Random Forest?
• It takes less training time as compared to other algorithms.
• It predicts output with high accuracy, even for the large dataset it runs efficiently.
• It can also maintain accuracy when a large proportion of data is missing.

Applications of Random Forest
• Banking: Banking sector mostly uses this algorithm for the identification of loan risk.
• Medicine: With the help of this algorithm, disease trends and risks of the disease can be identified.
• Land Use: We can identify the areas of similar land use by this algorithm.
• Marketing: Marketing trends can be identified using this algorithm

Pros & Cons of Random Forest
Pros
• It can perform both Classification and Regression tasks.
• It is capable of handling large datasets with high dimensionality.
• It enhances the accuracy of the model and prevents the overfitting issue.
 Cons
• Although random forest can be used for both classification and regression tasks, it is not more suitable for Regression tasks.
------------------------------------------------------------------------------------------------

Unsupervised Learning 

• Clustering
• Dimenstionality Reduction
• Association Rule Mining


Dimenstionality Reduction Methods
 - PCA (Principal Component Analysis)
 - LDA (Linear Discriminant Analysis)
 - NMF (Non-negative Matrix factorization)
 - LLE (Locally Linear Embedding)
 - Isomap


Clustering in Machine Learning

• A way of grouping the data points into different clusters, consisting of similar data points.
• Clustering is an unsupervised learning method; hence no supervision is provided to the algorithm.
• The objects with the possible similarities remain in a group that has less or no similarities with another group.
• After applying the clustering technique, each cluster or group is provided with a cluster-ID

Clustering in Machine Learning

• Market Segmentation
• Statistical data analysis
• Social network analysis
• Image segmentation
• Anomaly detection


Use cases

• In Identification of Cancer Cells: It divides the cancerous and noncancerous data sets into different groups.
• In Search Engines: It does it by grouping similar data objects in one group that is far from the other dissimilar objects. 
The accurate result of a query depends on the quality of the clustering algorithm used.
• Customer Segmentation: It is used in market research to segment the customers based on their choice and preferences.
• In Biology: It is used in the biology stream to classify different species of plants and animals 
using the image recognition technique.
• In Land Use: The clustering technique is used in identifying the area of
similar lands use in the GIS database.


Types of Clustering Methods

• Partitioning Clustering
• Density-Based Clustering
• Distributional Clustering
• Hierarchical Clustering
• Fuzzy Clustering


Partitioning Clustering

• A type of clustering that divides the data into non-hierarchical groups.
• It is also known as the centroid-based method.
• The most common example of partitioning clustering is the KMeans Clustering algorithm.
• The dataset is divided into a set of groups, where K is used to define the number of pre-defined groups.
• The cluster center is created in such a way that the distance
between the data points of one cluster is minimum.


K-Means Pros & Cons

Pros
• Simple, understandable
• Quick
• Instances automatically set to clusters
 Cons
• All instances lead to a single cluster
• Sensitive to more outliers
• Cluster must be picked beforehand


Distributional Clustering

• The data is divided based on the probability of how a dataset belongs to a particular distribution.
• The grouping is done by assuming some distributions commonly Gaussian Distribution.
• The example of this type is the Expectation-Maximization Clustering algorithm.
• This is based on Gaussian Mixture Models (GMM).


Hierarchical Clustering

• In this algorithm, we develop the hierarchy of clusters in the form of a tree.
• This tree-shaped structure is known as the dendrogram.
• Sometimes the results of K-means clustering and hierarchical clustering may look similar.
• The hierarchical clustering technique has two approaches: Agglomerative & Divisive.
• Hierarchical agglomerative clustering (HAC) merges the
most similar clusters, starting with each data point as a separate cluster.
• Divisive clustering starts by considering all the data points into a big single cluster and splitting them into smaller
heterogeneous clusters continuously until all data points are in their cluster.


Agglomerative Hierarchical Clustering

• Hierarchical agglomerative clustering (HAC) merges the most similar
clusters, starting with each data point as a separate cluster.
• Use Euclidean distance to calculate the similarity.
• Use Single linkage, Complete linkage, and Centroid linkage methods
to calculate the distance between clusters.


Association Rule Learning

• Association rule learning is a type of unsupervised learning technique.
• It checks for the dependency of one data item on another data item and maps accordingly.
• It is based on different rules to discover the interesting relations between variables in the database.
• It is employed in Market Basket analysis, Web usage mining, continuous production, etc


How does Association Rule Learning Work?

• Association rule learning works on the concept of If and Else Statement, such as if A then B.
• Here the If element is called antecedent, and then statement is called as Consequent.
• These types of relationships where we can find out some association or relation between two items is known as single cardinality.
• It is all about creating rules, and if the number of items increases, then cardinality also increases.


Mining Association Rules

• Two step approach
• Step 1 -> Frequent Itemset Generation
• Generate all itemsets whose support >= minsup
• Step 2 -> Rule Generation
• Generate high confidence rules from each frequent itemset where each rule is a binary partitioning of a frequent itemset

Matrix factorization and singular value decomposition is a way to simplify data by reducing  rows and columns 



Apriori Algorithm

• This algorithm uses frequent datasets to generate association rules.
• This algorithm uses a breadth-first search and Hash Tree to calculate the itemset efficiently.
• It is mainly used for market basket analysis and helps to understand the products that can be bought together.
• It can also be used in the healthcare field to find drug reactions for patients
----------------------------------------------------------------------------------------------------------------------------

Ensemble Methods in Machine Learning

• Machine learning models are often trained with a variety of different methods in order to create a more accurate prediction.
• Ensemble methods are one way to do this and involve combining the predictions  of several
 different models in order to get a more accurate result.
• It combines low performing classifiers and combine individual model prediction for the final prediction.
• Based on type of base learners, ensemble methods can be
categorized as homogeneous and heterogeneous ensemble methods.


Ensemble Learning Methods

• Bagging
• Boosting
• Stacking

Bagging

• Bagging is an acronym for Bootstrapped Aggregation.
• Bootstrapping means random selection of records with replacement from the training dataset.
• The idea behind bagging is combining the results of multiple models to get a generalized result.
• Bagging technique works by creating several models, called “bags”, each of which is based on a 
different randomly-selected sample of the data.

Boosting

• If a data point is incorrectly predicted by the first model, and then the next will combining the predictions provide better results? Such situations are taken care of by boosting.
• Boosting is a sequential process, where each subsequent model attempts
to correct the errors of the previous model.
• After classification, sample weights are changed. Weight of correctly
classified sample is reduced, and weight of incorrectly classified sample is increased.
• Boosting can help data scientists adjust the weights of the models so that
the better models have more influence on the final prediction.


Stacking

• Stacking uses predictions from multiple models (for example decision tree, KNN or SVM) to build a new model.
• The models are “stacked” on top of each other, and the predictionsfrom each model are combined to produce a final prediction.
• This can be used for regression or classification tasks, and it has been shown to outperform traditional machine learning methods.
• The ultimate model is powerful because it can combine the strengths of different models to produce a more accurate prediction.
• Overall, it is difficult to implement, and it requires a great deal of tuning to get the best results.
• The stacking ensemble method can be used for solving a variety of machine learning problems, such as regression and classification.
• For example, imagine that you are trying to predict the price of a house.
• You could use a model to predict the price of a house based on its
size and location, and then use a second model to predict the price of a house based on its age and condition.
• The predictions from each model would be combined to produce a final prediction for the price of the house.

-------------------------------------------------------------------------------------------------------------------------------

Model Evaluation

• Model evaluation is a process of assessing the model’s performance
on a chosen evaluation setup
• Model selection is the process of choosing the best classifier for a
given task
• It is done by comparing various model candidates on chosen
evaluation metrics
• Choosing the correct evaluation schema, whether a simple train test
split or a complex cross-validation strategy


Model selection in machine learning

• Resampling methods
• Simple techniques of rearranging data samples to inspect if the model performs well on data samples
• Resampling helps us understand if the model will generalize well
• Random split
• Used to randomly sample a percentage of data into training, testing, and preferably validation sets
• Random splitting will prevent a biased sampling of data: test set is used for model evaluation


Model selection in machine learning

• Time-Based Split
• There are some types of data where random splits are not possible
• If we have to train a model for weather forecasting, we cannot randomly divide the data into training and testing sets.
• K-Fold Cross-Validation
• Randomly shuffling the dataset and then splitting it into k groups
• Model is tested on the test group and the process continues for k groups
• Stratified K-Fold
• unlike in k-fold cross-validation, the values of the target variable is taken into consideration in stratified k-fold.


How to choose performance metrics

• Right choice of an evaluation metric is crucial and often depends upon the problem
• A clear understanding of a wide range of metrics can help the evaluator to chance upon an appropriate match
• Types
        • Classification metrics
        • Regression metrics
        • Clustering metrics
    

Classification evaluation metrics

Log loss
• Log loss is a very effective classification metric and is equivalent to -1* log (likelihood function) where the likelihood function suggests how likely the model thinks the observed set of outcomes was
Gain & Lift
• Lift charts measure the improvement that a model brings in compared to random predictions.
• Gain and lift charts evaluate the model on portions of the whole population
K-S chart
• The K-S chart determines the degree of separation between positive class distribution and the negative class distribution
• he higher the difference, the better is the model at separating the positive and negative cases


Regression evaluation metrics

• Regression models provide a continuous output variable, unlike classification models that have discrete output variables
• Mean Squared Error
• Calculatesthe difference between the actual value and the predicted value (error)
• Root Mean Squared Error
• Helps to bring down the scale of the errors closer to the actual values, making it more interpretable
• Mean Absolute Error
• Mean of the absolute error values (actuals – predictions)


Clustering evaluation metrics

• Clustering algorithms predict groups of datapoints and hence, distance-based metrics are most effective
• Dunn Index
• Focuses on identifying clusters that have low variance
• Silhouette Coefficient
• Tracks how every point in one cluster is close to every point in the other clusters in the range of -1 to +1
• Elbow method
• Determine the number of clusters by plotting the number of clusters on the x-axis against
 the percentage of variance explained on the y-axis


Trade-offs in model selection
Bias vs Variance
• A model with high bias will oversimplify by not paying much attention to the training points
• Bias occurs when a model is strictly ruled by assumptions
• This leads to underfitting when the actual values are non-linearly related to the independent variables
• A model with high variance will restrict itself to the training data by not generalizing for test points
• Variance is high when a model focuses on the training set too much


Ethics in machine learning
Data
• A good ML system needs lots of data. But where are we going to get this data?
• Is it alright if you steal the someone’s private data?
 Algorithms
• What if a patented algorithm, in the right hands can help millions?
• Can one’s own sense of right and wrong be used to reverse engineer the algorithm to benefit others?

Results
• If you get the same practice questions in the exam, is your score on the exam a good measure of how much you learnt?
• Or is it a measure of how much you were able to memorize?
