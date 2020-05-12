# Host_Url-Anomaly-Detection-with-Word-Embedding
This project explores the dataset in the internal system, aiming to accurately spot the potential host_url anomaly with the help 
of word embeddings. 

# Data 
Fetched from elasticsearch with the assigned score to indicate its severity level. Complied in a csv file with roughly 80000 samples 
and a bunch of features. The purpose of this project is to conduct a NLP study on detecting anomaly on the host url combination.

# Method
Pre-process the dataset to get the root from text information and standardized the expression. Also created a word dictionary to
assign index to each word in the dataset. Generate a 28000*28000 matrix co-occurrence matrix with row being the word and the blank being
the number of two occurring in the given windows size, which, in this case, equals 4. Transform the giant co-occurrence matrx in 2-D
matrix using truncatedSVD method for faster computation and ease the memory burden. 


# Output
Produced a 2-D plot with a test case in which most of them are threat and two others are benign. Since most threats are clusterd together, 
it is guaranteed that the word embeddings is capable of detecting the anomaly in the text by using "significant" term to pre-screen
the dataset
