<img src="https://circleci.com/gh/thepractitioner1/Operationializing-a-Machine-Learning-Microservice-API.svg?style=svg" alt=CircleCI />



## Project Overview

This project uses kubernetes to operationalize a machine learning microservice Kubernetes is an open-source framework for automating containerized application management.
This project may be applied to any previously trained model of machine learning, such as those for image recognition and data labeling.


### Instructions
**1)** Use this command to clone the repository:

__`- git clone https://github.com/thepractitioner1/Operationializing-a-Machine-Learning-Microservice-API.git`__

**2)** Enter this directory:

__`❍ cd Operationializing-a-Machine-Learning-Microservice-API`__

**3)** Install [python](https://www.python.org/) if not already installed and run this command to create a virtual environment and activate it:

__`❍ make setup`__

**4)** Use this command to install the project dependencies:

__`❍ make install`__

**5)** Use this command to lint the project files:

__`❍ make lint`__

**6)** Use this command to run the script to build a docker image for the app and start the app in a docker container:

__`❍ ./run_docker.sh `__

**7)** Use this command to run script to get a prediction from the app running in the Docker container:

__`❍ ./make_prediction.sh `__

**8)** Use this command to run the script to upload the docker image to your Docker hub account. Note you'll have to edit the script and change the Docker ID to yours:

__`❍ ./upload_docker.sh `__

**9)** Use this command to run the script to run the service in a kubernetes cluster.Here are some things to note: You'll be making use of my image repo. You can edit the script and change to your image repo on Docker hub if you've built and pushed your image. This script will be run twice to activate the port forwarding. Give some minutes after first run so that the pod can be up and running before attempting port forwarding:

__`❍ ./run_kubernetes.sh `__

**10)** use this command to run this script to get a prediction from the app running in the Kubernetes Cluster after port forwarding is successful:

__`❍ ./make_prediction.sh `__

&nbsp;

## :information_source: Files:

* app.py: This is the flask app that runs the service
* Makefile: This file has make commands that allows for easy setup of a project
* Dockerfile: This file has the setup for creating a Docker image for the microservice
* run_docker.sh: This script creates a docker image from the Dockerfile, list the images and starts a container
* make_prediction.sh: This script sends data for prediction using curl and prints the predicted value on the command line
* upload_docker.sh: This script uploads a docker image to docker hub
* run_kubernetes.sh: This script runs the docker image in a kubernetes cluster

