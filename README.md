[![ahmedo42](https://circleci.com/gh/ahmedo42/ml-microservice.svg?style=svg)](https://app.circleci.com/pipelines/github/ahmedo42/ml-microservice)

## Project Overview

This project is an example of a Machine Learning Microservice API using Docker & Kubernetes.

A pre-trained, `sklearn` model that  been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing)

 A Python flask app in `app.py` serves out predictions about housing prices through API calls. This project could be extended to any pre-trained machine learning model.

---

## Project Layout

<ui>

`model_data` : pre-trained model binaries and training data

`output_txt_files` : output result from running inference on docker and kubernetes

`app.py` : entry point for flask server

`make_predictions.sh` : a  script for sending prediction request to the flask server

`run_docker.sh` : a script for building and running the docker container

`run_kubernetes.sh` : a script for running the app in a local kubernetes cluster

`upload_docker.sh` : a  script for uploading the image to docker hub

</ui>


## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
