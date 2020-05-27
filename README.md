# Bank_Note_Authentication_Docker

The below step by step actions are performed to deploy the model

1) Model building model.ipynb - This file contains the training model where cosine similarity is calculated on the input data and the model is saved as model.pkl file
-------------
2) Creating Application main.py - This File consist of Flask application where the user is asked to input the required field and the corresponding output is obtained when clicking the submit button
-------------
3) Procfile Procfile - This file contains the python server name and the flask application name
-------------
4) requirements.txt requirements.txt - This file contains the packages which are required for this project
-------------
5) Creating Docker File

 FROM continuumio/anaconda3:4.4.0      >>> This is used for extracting the base image
 COPY . /usr/app/                      >>> This is for moving all the data in current directory to docker root directory
 EXPOSE 5000                           >>> This is for networking port
 WORKDIR /usr/app/                     >>> Changing the work directory to root directory
 RUN pip install -r requirements.txt   >>> Installing the dependencies
 CMD python app.py                     >>> Running the flask application
-------------
6) Building a docker image

 docker build -t money_api .
 docker run -p 8000:8000 money_api
-------------
 7) URL is obtained 
