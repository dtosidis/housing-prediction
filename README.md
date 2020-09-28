[![CircleCI](https://circleci.com/gh/dtosidis/housing_prediction.svg?style=svg)](https://circleci.com/gh/dtosidis/housing_prediction)


## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting `make lint`
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**


### Included Files
* .circleci/config.yml: Circleci configuration file
* model_data : Model training data
* output_txt_files: TXT files with the requested output logs
* app.py: The Flask app starter file with the API routes
* Dockerfile: Docker is using the commands of this file to construct the image
* make_prediction.sh: script which sends a prediction request to the running server
* Makefile: Defines a set of tasks to be executed using the make utility
* requirements.txt: All application dependencies on external libs are described here
all dependencies needed for application
* run_docker.sh : Script for running docker container
* run_kubernetes.sh : Script for running the docker container inside kubernetes
* upload_docker.sh: Script for uploading the docker image to the registry

---

## Setup the Environment

* Create a virtualenv and activate it


  ```shell
  python3 -m venv ~/.devops
  source ~/.devops/bin/activate
  ```

> **_NOTE:_**  The project is requiring python3.7. In case your default python version is different 
you may face issues with the dependencies. A way to resolve this problem is to use pyenv and 
pyenv-virtualenv for managing the virtual environment using another python version from the system 
default. Pyenv and pyenv-virtualenv must be installed for running the following commands.

  ```shell
  pyenv install 3.7.3
  pyenv virtualenv 3.7.3 .devops
  pyenv activate .devops
  ```



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
