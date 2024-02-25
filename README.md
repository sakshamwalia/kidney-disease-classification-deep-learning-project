# kidney-disease-classification-deep-learning-project

## Workflows

1. Update config.yaml
2. Update secrets.yaml
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src/config
6. Update the components
7. Update the pipeline
8. Update the main.py
9. Update the dvc.yaml
10. Update the app.py

# How to run ?

### steps :

clone the repository:

```bash
https://github.com/sakshamwalia/kidney-disease-classification-deep-learning-project.git
```

### STEP 1 : create the conda enviroment after opening the repository:

```bash
conda create -n cnncls python==3.8 -y
```

### activate the enviroment:
```bash
conda activate cnncls
```

### STEP 2 : install the requirements:
```bash
pip install -r requirements.txt
```

[Documentation](https://mlflow.org/docs/latest/index.html)

### cmd
- mlflow ui

### dagshub
[dagshub](https://dagshub.com)

MLFLOW_TRACKING_URI=https://dagshub.com/sakshamwalia/kidney-disease-classification-deep-learning-project.mlflow \
MLFLOW_TRACKING_USERNAME=sakshamwalia \
MLFLOW_TRACKING_PASSWORD=549c5cc4ae00fd52e55b92e68cec5dc45a19bc65 \
python script.py

Run this above code to export as env variable:

```bash
export MLFLOW_TRACKING_URI=https://dagshub.com/sakshamwalia/kidney-disease-classification-deep-learning-project.mlflow

export MLFLOW_TRACKING_USERNAME=sakshamwalia

export MLFLOW_TRACKING_PASSWORD=549c5cc4ae00fd52e55b92e68cec5dc45a19bc65
```

### DVC==3.32.0
1. Command 1:
```bash
dvc init
```
2. Command 2:
```bash
dvc repro
```
3. Command 3:
```bash
dvc dag
```

## AWS CICD Deployment With Github Actions

### 1. Login to AWS Console

### 2. Create IAM User for deployment :

    with specific access:

1. EC2 access : It is virtual machine

2. ECR: Elastic Container registry to save your docker image in aws


#Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2

#Policy:

1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess

### 3. Create ECR repo to store/save docker image
```bash
- Save the URI: 730335464343.dkr.ecr.ap-southeast-2.amazonaws.com/kidney
```

### 4. Create EC2 machine (Ubuntu)

### 5. Open EC2 and Install docker in EC2 Machine:
```bash
#optional

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
```

### 6. Configure EC2 as self-hosted runner:
```bash
setting>actions>runner>new self hosted runner> choose os> then run command one by one
```

### 7. Setup github secrets:
```bash
AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = ap-southeast-2

AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

ECR_REPOSITORY_NAME = kidney
```

