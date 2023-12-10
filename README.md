# MLflow-Basic-Operation



## For Dagshub:

MLFLOW_TRACKING_URI=https://dagshub.com/Sagar230595/MLflow-Basic-Operation.mlflow \
MLFLOW_TRACKING_USERNAME=Sagar230595 \
MLFLOW_TRACKING_PASSWORD=b946b0e3def1533ba2d91acb82c680ba39f12bb1 \
python script.py

```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/Sagar230595/MLflow-Basic-Operation.mlflow

export MLFLOW_TRACKING_USERNAME=Sagar230595

export MLFLOW_TRACKING_PASSWORD=b946b0e3def1533ba2d91acb82c680ba39f12bb1

```

# MLflow on AWS


## MLflow on AWS Setup:

1. Login to AWS console.
2. Create IAM user with AdministratorAccess
3. Export the credentials in your AWS CLI by running "aws configure"
4. Create a s3 bucket
5. Create EC2 machine (Ubuntu) & add Security groups 5000 port

Run the following command on EC2 machine
```bash
sudo apt update

sudo apt install python3-pip

sudo pip3 install pipenv

sudo pip3 install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell


## Then set aws credentials
aws configure


#Finally 
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-test-23

#open Public IPv4 DNS to the port 5000


#set uri in your local terminal and in your code 
export MLFLOW_TRACKING_URI=http://ec2-54-147-36-34.compute-1.amazonaws.com:5000/
```



