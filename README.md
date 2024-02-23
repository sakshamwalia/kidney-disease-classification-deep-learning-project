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