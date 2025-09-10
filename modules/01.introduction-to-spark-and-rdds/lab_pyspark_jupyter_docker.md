# Data Engineering with Spark

The following lab utilizes Spark RDDs to perform basic text cleaning of unstructured text data.

## Lab Prerequisites

This lab utilizes a [Jupyter Docker Stacks](https://jupyter-docker-stacks.readthedocs.io/en/latest/index.html) image for experimenting with pyspark locally. These instructions assume docker is already [installed](https://docs.docker.com/get-started/get-docker/) and that some form of unix-like terminal (linux/mac or git bash/wsl on windows) is being used.

### Start the docker container and initialize a volume for persistance

```bash
docker run --name pyspark_notebook --rm -v pyspark_notebook_volume:/home/jovyan/work --detach -p 8888:8888 -p 4040:4040 -p 4041:4041 quay.io/jupyter/pyspark-notebook
```

**NOTE:** All future runs of the container will use the same command but the notebook will only need to be copied on the first run.

### Copy the lab to the volume

```bash
docker cp lab_pyspark_jupyter_stand_alone/word_count_pyspark_jupyter_docker.ipynb  pyspark_notebook:/home/jovyan/work/
```

## Lab 1: Unstructured data analysis with RDDs

Analyze unstructured data (text) with RDDs and Spark Core Functions.

### Goals

- Get familiar with the Databricks environment
- Get familiar with the most frequently used functions for RDD processing: `map`, `flatMap`, `reduceByKey`
- Learn how to define lambda functions
- Learn when you can use pure Python functionalities and constructs in Spark environment

### Lab resources

- [Notebook](./lab_pyspark_jupyter_docker/word_count.ipynb)
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
