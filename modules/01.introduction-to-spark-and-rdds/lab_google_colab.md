# Data Engineering with Spark

## Lab 1: Unstructured data analysis with RDDs

Analyze unstructured data (text) with RDDs and Spark Core Functions.

### Prerequisites

- Connect to [Google Colab](https://colab.research.google.com/)
- Upload the provided [notebook](./lab_google_colab/word_count_colab.ipynb)

### Goals

- Get familiar with the Databricks environment
- Get familiar with the most frequently used functions for RDD processing: `map`, `flatMap`, `reduceByKey`
- Learn how to define lambda functions
- Learn when you can use pure Python functionalities and constructs in Spark environment

### Lab resources

- [Notebook](./lab_google_colab/word_count.ipynb)
- The text file is obtained from [Project Gutenberg](https://www.gutenberg.org/ebooks/103.txt.utf-8) using the cell magic `!wget` in the ipynotebook.

### Useful links

- [RDD programming guide](https://spark.apache.org/docs/latest/rdd-programming-guide.html)
    - especially chapters `Transformations` and `Actions`

### TO DO

Go through the notebook and follow the instructions in the cells:

1. Open the book obtained from project guttenberg and:

- count the occurrence of each word
- change all capital letters to lower case
- remove stopwords
- sort the words and their counts in alphabetical order
- sort from most to least frequent word
- remove punctuations
- answer questions about code where applicable

2. Look at the given code and try to understand what it does.

- provide line by line code comments
