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
## Embeddings Outputs
The files 1.csv - 9.csv have been generated by applying the word embedding techniques on the 'GitterCom.csv' dataset in the following order:
CBOW, Skip-Gram, GloVe 50d, GloVe 100d, GloVe 300d, Word2Vec, fastText, GPT, GPT-2.

One-Way ANOVA Test is applied on these 9 files to generate the files 10.csv - 18.csv respectively.
This test is applied to discard the non-influential features from the data.

The files 1.csv - 18.csv can be found in the Embeddings folder.

The code for applying the One-Way ANOVA Test can be found in the Codes Folder.
