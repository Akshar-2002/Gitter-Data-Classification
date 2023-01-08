# Gitter Data Classification

Gitter is a modern instant messaging and collaboration platform that has revolutionized team communications and project coordination by providing a user-friendly way of organizing conversations.

GitterCom Dataset was leveraged for the project. It is a dataset of developers in open-source communities in Gitter consisting of 10,000 messages.

The objective of the project is to build various models to classify the purpose of the messages in the discussions on the Gitter Platform and compare the performances of the models developed.


## Word Embeddings
Nine Word Embedding techniques were applied:
1. CBOW
2. Skip-Gram
3. GloVe 50d
4. GloVe 100d
5. GloVe 300d
6. Word2Vec
7. fastText
8. GPT
9. GPT-2

The codes for each of these techniques can be found in the Codes folder.

The files 1.csv - 9.csv have been generated by applying the word embedding techniques on the 'GitterCom.csv' dataset in the following order:
CBOW, Skip-Gram, GloVe 50d, GloVe 100d, GloVe 300d, Word2Vec, fastText, GPT, GPT-2.

## Dimensionality Reduction

Two dimensionality reduction techniques were used:

1. One-Way ANOVA Test
- This test is applied to discard the non-influential features from the data.
- One-Way ANOVA Test is applied on files 1.csv - 9.csv to generate the files 10.csv - 18.csv respectively.

2. Principal Component Analysis (PCA)
- This technique is used to generate a smaller number of uncorrelated features from the given data.
- One-Way ANOVA Test is applied on files 1.csv - 9.csv to generate the files 19.csv - 27.csv respectively.

The codes for applying these techniques can be found in the Codes folder.

## Data Sampling

Synthetic Minority Oversampling Technique (SMOTE) technique was used to sample data to solve the class imbalance problem.

Files 28.csv - 54.csv were generated corresponding to the first 27 files using this technique.

The code for applying SMOTE can be found in the Codes folder.

## Classification Algorithms

The following algorithms were applied for classifying the purpose of the messages

- Naive Bayes (Multinomial, Bernoulli and Gaussian)
- Decision Tree 
- Logistic Regression
- K Nearest Neighbors (KNN)
- KNN, Mulitnomial NB, Logistic Regression and Decision Tree with Bagging
- Random Forest
- Extra Trees
- Ada Boost
- Gradient Boosting
- Multi Layer Perceptron with Limited-memory BFGS, Stochastic Gradient Descent and Adam Optimizers 

Both One-vs-Rest and One-vs-One for Multi-Class Classification strategies were applied for all the algorithms mentioned above.

## Output Files

The Embeddings folder consists of the files 1.csv - 54.csv which are the files generated after applying the word embedding, dimensionality reduction and data sampling techniques on the dataset.

The Outputs folder consists of files 1pred.csv - 54pred.csv and 1predp.csv - 54predp.csv which correspond to the prediction of the purpose made by the classification algorithms on the 54 input files.

Each xpred.csv file consists of 35 columns:
- The forst 34 columns corresponding to the predictions of 34 classification algorithms (17 one vs rest and 17 one vs one algorithms) on the x.csv file data.
- The last column corresponds to the ground truth labels.

Each xpredp.csv file consists of 52 columns:
- Each set of 3 columns consist of the class probabilities for each data point for the 17 one vs one classification algorithms applied.
- The last column corresponds to the ground truth labels.
