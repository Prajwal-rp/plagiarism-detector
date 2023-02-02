# Plagiarism-Detector

Detecting plagiarism is an active area of research.

Building a plagiarism detector that examines a text file and performs binary classification labeling that file as either plagiarized or not, depending on how similar that text file is to a provided source text.

# About the data

- The no of files in the dataset are 100
- The number of unique tasks in the are 5
- Unique tasks:['a' 'b' 'c' 'd' 'e']
- Number of plagiarism categories are 5

## Unique categories:['non' 'cut' 'light' 'heavy' 'orig']

- The orig in the category refers to the source text for each type of task i,e(a,b,c,d,e) and will be used to compare each answers with this source file(wikipedia source file).
- The non category refers that the file or data is not plagiarised.
- The other three categories that are cut>light>heavy indicates that the document/answers are plagiarised.
- Cut indicates copy pasted plagiarism
- light indicates that the answer/document includes some sort of copying and paraphrasing from the source
- Heavy indicates that the document/answer is taken from the source but changing some of the words and also the structure(challenging type of plagiarism and hard to detect)
  ![plagiarism_class_distribution](https://user-images.githubusercontent.com/93460334/182436727-98674b80-1c36-462f-9275-266f101af991.png)

# Feature Engineering

To know whether a document/answer has been plagiarized or not we have to check the similarity between the document and the source.
To check this similarity we have to extract the similarity features
Some of the similarity features that are considered for the feature extraction are:

- Containment Features(extracted using different ngrams)
- Longest Common Subsequence(extracted using dynamic programming)

# Model Building

- Using Random Forest Classifier to build the model using the extracted features
- Using Cross Validation to reduce the overfitting of the model on the training data
- Performing hyperparameter tuning to tune the model for further improvements
- obtained an accuracy of 94% on the Testing data

The notebook for this project has been attached to this repository
