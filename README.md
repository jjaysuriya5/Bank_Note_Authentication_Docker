# Bank_Note_Authentication_Docker

# 1) Creating Docker File

# FROM continuumio/anaconda3:4.4.0      >>> This is used for extracting the base image
# COPY . /usr/app/                      >>> This is for moving all the data in current directory to docker root directory
# EXPOSE 5000                           >>> This is for networking port
# WORKDIR /usr/app/                     >>> Changing the work directory to root directory
# RUN pip install -r requirements.txt   >>> Installing the dependencies
# CMD python app.py                     >>> Running the flask application


# docker run -dp 80:80 docker/getting-started

# 2) Building a docker image

# docker build -t money_api .
# docker run -p 8000:8000 money_api

# 3) URL is obtained 
