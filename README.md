[![CircleCI](https://dl.circleci.com/status-badge/img/gh/Rukeeo1/project-ml-microservice-kubernetes/tree/master.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/Rukeeo1/project-ml-microservice-kubernetes/tree/master)

## Project Overview
This project operationalizes a machine learning microservice ***sklearn*** using [kubernetes](https://kubernetes.io/), The model predicts housing prices in Boston according to several features, such as average rooms in a home and data about highway access. For more information please refer to [the data source site](https://www.kaggle.com/c/boston-housing)


## Running the project

### Requirements
 - Python 3.7
 - Clone the repo to your local machine

---

##  1. Setup the Environment

* Create a virtualenv with Python 3.7
```
make setup
```
* Install dependencies
```
make install
```
## 2. Running the Application
* To run Standalone:
```
python app.py
```
* To run in Docker:
```
./run_docker.sh
```
* To run in Kubernetes:
```
./run_kubernetes.sh
```

## 3. Deployment
* To upload to docker (replace ```rukeeo1``` in docker path with your docker username)
```
./upload_docker.sh
```

## 4. The files:
1. ```app.py``` contains the flasks application
2. The ```MakeFile``` defines the relevant set of task to be executed for the application to run
3. The ```Docker``` file contains the requirements to build the Image
4. The files ending with ```.sh``` contains the relevant bash scripts, to run docker or kubernetes, upload and image and make a prediction