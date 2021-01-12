# SageMaker Deployment Project

In this project, a simple web app is deployed using Amazon SageMaker and PyTorch using the [IBDM Dataset](https://www.imdb.com/interfaces/). The web app interacts with a deployed recurrent neural network performing sentiment analysis on movie reviews. 

### Table of Contents

1. [Installation](#installation)
2. [Introduction](#Introduction)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

1. Python versions 3.6
2. Library and packages: pytorch 0.4, sagemaker 1.72.0, os, glob, numpy, pandas, matplotlib, sklearn, pickle

## Introduction <a name="Introduction"></a>

In this project, I deployed a sentiment analysis Web App through Amazon SageMaker and Pytorch using the IMDB Dataset. I first trained the model using LSTM model with hidden dimension set to 200 and epochs 10. The I deployed the model using Pytorch, with four functions model_fn, input_fn, output_fn, and predict_fn.
To sensure the model working well, I tested the deployed model and the accuracy score is 0.87. After ensure the model is accurate, I then deployed the model to a web app following: (1) create IAM role for Lambda function; (2) create a Lambda function; (3) set up API Gateway using POST method. Finnaly, I tried out the Web App using random reviews from rotten tomato, and the Web App seems to work pretty well.

## File Descriptions <a name="files"></a>

#### Folders: 
* images: contains the images used in the SageMaker Project notebook
* serve: contains the model and train function when using pytorch to deploy a model
* train: contains the model and train functions when using sagemaker to deploy a model
* website: contains the index.html for the web app

#### Files:
* SageMaker Project.ipynb: the main notebook 
* report.html: the SageMaker Project.ipynb exported in html format

## Results<a name="results"></a>

The main outcome of this project is a web app thant can be deployed anywhere for sentiment analysis. The web app demo is given below:

![Web app example](.images/web_app_demo.gif)

## Licensing, Authors, and Acknowledgements<a name="licensing"></a>

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Acknowledge to [Udacity](https://www.udacity.com/) and [IBDM](https://www.imdb.com/interfaces/) for the data.  


