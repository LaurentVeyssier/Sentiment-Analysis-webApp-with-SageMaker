# Creating a Sentiment Analysis Web App using Pytorch and SageMaker

This project is the final project of UDACITY's Deep Learning Nanodegree program.
In this project, I use SageMaker (AWS) to train and deploy a sentiment analysis model in Pytorch.
The deployed model uses a simple web page where users can submit a review written in plain english. The model predicts whether the review is positive or negative. The prediction is returned to the web page.
The model is trained on IMDB movie review dataset. It uses Amazon Web Service SageMaker. The model is deployed in S3, AWS cloud computing solution.


Project Information:
- Contents
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

Libraries:
The list below represents main libraries and its objects for the project.
- Amazon SageMaker (Build, train, and deploy a model)
- PyTorch (LSTM classifier)

Delete the Endpoint
Remember to always SHUT DOWN YOUR ENDPOINT if you are no longer using it. You are charged for the length of time that the endpoint is running so if you forget and leave it on, you could end up with an unexpectedly large bill !

predictor.delete_endpoint()
