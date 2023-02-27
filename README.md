[![CircleCI](https://dl.circleci.com/status-badge/img/gh/SokEarth/An-ML-Microservice-API/tree/master.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/SokEarth/An-ML-Microservice-API/tree/master)

## Project Overview

This project operationalizes a Machine Learning Microservice API.

Given a pre-trained, sklearn model that has been trained to predict housing prices in Boston according to several features, 
such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. 
You can read more about the data, which was initially taken from Kaggle, on the data source site. 
This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

---

## Project Tasks

### The following tasks were performed:

* Test project code using linting
* Complete Dockerfile to containerize the application
* Deploy the containerized application using Docker and make a prediction
* Improve the log statements in the source code
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

---

## Description of folders and files in this repository:

* .circleci: For the circlecI build server.
* model_data : This folder has the pretrained sklearn model and housing csv files.
* output_txt_files: This folder has the sample output logs from running ./run_docker.sh and ./run_kubernetes.sh.
* app.py : This houses the flask app.
* Dockerfile: This file contains instructions to containerise the application.
* Makefile : This makefile has the instructions for environment setup and lint tests.
* requirements.txt: This is the list of required dependencies.
* run_docker.sh: This bash script is for building a docker image and running the application in a docker container.
* upload_docker.sh: This bash script is used to upload the built docker image to dockerhub.
* run_kubernetes.sh: This bash script is used to run the application in a kubernetes cluster.
* make_prediction.sh: This bash script is used to make predictions against the docker container and k8s clusters.
* README.md: This README file.

---

## Instructions

### Setup the Environment

* Create a virtualenv and activate it.
* Run make install to install the necessary dependencies.

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally.
* Setup and Configure Kubernetes locally.
* Create Flask app in Container.
* Run via kubectl.