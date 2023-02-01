# ResumeScreener

India has a huge job market, millions of people seeking out jobs everyday, Although it is humanly possible to screen the Cv’s and match them with the job description but this will be a very slow process if done manly. The Hiring Team having to go through each Cv manually will be a hectic process, it’s fine if there are 1 Or 2 Cvs but when there a number of them, what should the HR team do?
Theres also an issue with the format of the CVS, not every Cv will be the same standard format, they might have a different structure, so this research is pretty much intensive and if the HR team does it manually it will be also prone to error.
Then comes the main thing which is mapping the job description to the Cv, or basically trying if to find out if the individual is capable to do what the job requires them to.


To overcome these short listing issues, I have built a resume screener, The model takes the features extracted from the candidate’s resume as input and finds their categories, further based on the required job description the categorised resume mapped and recommend the most suitable candidate’s profile to HR.


# Modules & Libraries Description

KNN
- Used for classification. "K" in the KNN repersent the number of nearest neighbours used to classify or predict in case of continuous variable. NLP
NLP enables computers to understand natural language as humans do.

NumPy
- NumPy is one of the fundamental packages for Python providing support for large multidimensional arrays and matrices


Pandas
- It is an open-source, Python library. Pandas enable the provision of easy data structure and quicker data analysis for Python. For operations like data analysis and modelling,

Matplotlib
- This open-source library in Python is widely used for publication of quality figures in a variety of hard copy formats and interactive environments across platforms. You can design charts, graphs, pie charts, scatterplots, histograms, error charts, etc. with just a few lines of code.

Seaborn
- This Python library is derived from Matplotlib and closely integrated with Pandas data structures.

Scipy
- This is yet another open-source software used for scientific computing in Python. Apart from that, Scipy is also used for Data Computation, productivity, and high- performance computing and quality assurance.

Scikit-learn
- It is a free software machine learning library for the Python programming language and can be effectively used for a variety of applications which include classification, regression, clustering

Nltk
- contains a set of libraries that provide processing solutions for numerical and symbolic language processing in English only.


# Methodology
• DATAPREPROCESSING-
With the help of the attributes present in the seaborn library we make a grid or a piechart to properly depict the categories.We will simply display the categories that the individual or the job seeker qualifies in using a grid or a plot graph where we ll clearly be able to analyse the users skills and abilities.
  
 • CLEANING THE DATASET-
Then we clean the dataset which means the removal of all the stopwords, and the unnecessary unrequired symbols with the help of the nltk library which will help us generate cleaned sentences. In cleaning, all special characters, the numbers, and the single letter words are removed. We got the clean dataset after these steps having no special characters, numbers or single letter word. The dataset is split into the tokens using the NLTK tokens, later other preprocessing steps are applied on the dataset.
• FEATURE EXTRACTION-
The next step is feature extraction. The cleaned out data is imported and feature extraction is carried out using Tf-Idf. The machine learning based classification model, need a fixed size numerical vector as input to process it. Basically used to map the most frequent words to feature indices and hence compute a word occurrence frequency matrix. (Term Frequency, Inverse Document Frequency) methodology for feature extraction.

———TF-IDF
TF- What is Term Frequency (tf)
tf is the number of times a term appears in a particular document. So it’s specific to a
document. A few of the ways to calculate tf is given below:- tf(t) = No. of times term ‘t’ occurs in a document
 
IDF-Inverse Document Frequency (idf)
idf is a measure of how common or rare a term is across the entire corpus of documents. So the point to note is that it’s common to all the documents. If the word is common and appears in many documents, the idf value will approach 0 or else approach 1 if it’s rare.
idf (t) =1 + log e [ n / df(t) ]
tf-idf value of a term in a document is the product of its tf and idf. The higher is the value, the more relevant the term is in that document
• K-NEARESTNEIGHBOURS
In this model, k-NN is used to identify the CVs that are nearest to the provided job description, in other words, the CVs that are close match to the provided job description. In knn, we get a new training point and then we match it with the available data set, we look at the similarity of the training data and the available data and then put it into the most similar category, and then train it. So to get the JD and CVs to similar word scale this library was used to generate a summary of JD and CVs and then k-NN was applied to find the CVs which are closely matching the provided JD.



# Conclusion

It’s basically a form of mapping job requirements and the qualifications of a candidate.The proposed model worked in two phases: first, classify the resume into different categories. second, recommends resume based on the similarity index with the given job description. The very purpose of this is to reduce the the time consuming factor for the administration, like manually screening and going through all the resumes.
