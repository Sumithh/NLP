Twitter Analysis

The aim of the project is to grab any trending topic from twitter and make analyse overall sentiment of the topic, (positive or neagative) and creating a machine larning model out of it.  

The whole pipeline is made in pyspark. 

Steps Involved. 
1. Tweets are grabbed from twitter api via aws kenisis to s3 bucket
2 Tweets are grabbed from amazon s3 bucket and mounted to pyspark 
3. Tweets are cleaned using pyspak regex function 
4. Feature Engineering has been done with the help of python package Textblob. 
5. For negative tweets its been labelled as 0 and for positive as 1. 
6. The pipeline has been created in the following order:
    Tokenizer --> Stopword_remover --> countVectorizer --> IDF --> VectorAssembler --> StringIndexer 
    --> LogisticRegression 