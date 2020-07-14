# Creating a Sentiment Analysis Web App using Pytorch and SageMaker #

This project is the final project of UDACITY's Deep Learning Nanodegree program.
In this project, I use SageMaker (AWS) to train and deploy a sentiment analysis model in Pytorch.
The deployed model uses a simple web page where users can submit a review written in plain english. The model predicts whether the review is positive or negative. The prediction is returned to the web page.

![](/website/webpage.PNG)

## Instructions

- Open the SageMaker Project.ipynb file.
- Read and follow the instructions fron the notebook.


## Dependencies ##
This project assumes some familiarity with SageMaker.

The model is trained on IMDb movie review dataset. The dataset can be downloaded from the notebook.

It uses Amazon Web Service SageMaker. From step 3 of the notebook, the model is deployed in S3, AWS cloud computing solution, and runs using SageMaker resources.

To run the code, an AWS account will be required.

The notebook uses helper functions which are located in train and serve folders. These include model definitions (model.py), train code (train.py) and inference code (predict.py).
The web app runs using index.html file. 

## Installation ##
To deploy the model, it will be required to set up a Lamba function in SageMaker with the appropriate permission and endpoint connection. The endpoint connection is provided by the following code line in the notebook :
`predictor.endpoint`

You will have to create an API gateway in SageMaker to trigger the Lambda function.

Finally you will be required to update the API url in the index.html file located in website folder. This will link the web page to the API you have created.

For step-by-step instructions, refer to step 7 (Lambda and API gateway set-up) and step 8 (API url update) in the notebook.


## Project Information: ##
Contents of the main notebook
- General Outline
- Step 1: Downloading the data
- Step 2: Preparing and Processing the data
- Step 3: Upload the data to S3
- Step 4: Build and Train the PyTorch Model
- Step 5: Testing the Model
- Step 6: Deploying the model for testing
- Step 7: Use the model for testing
- Step 6: Deploy the model for the web app
- Step 7: Use the model for the web app
- Step 8: Deploying our web app

## Libraries: ##
The list below represents main libraries and its objects for the project.
- Amazon SageMaker (Build, train, and deploy a model)
- PyTorch (LSTM classifier)

## Important note: Delete the Endpoint ##
Remember to always SHUT DOWN YOUR ENDPOINT if you are no longer using it. You are charged for the length of time that the endpoint is running so if you forget and leave it on, you could end up with an unexpectedly large bill !

`predictor.delete_endpoint() `
