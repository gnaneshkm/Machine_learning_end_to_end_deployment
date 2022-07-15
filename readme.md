# Task Description
The final goal of the task is, with the provided dataset, to build an ML prediction service.
## Data analysis and feature engineering
Data exploratory analysis. Get a general picture of the data. Identify problems within the data, and propose 
and apply feature engineering solutions. These analyses should help you to decide on how to proceed with the 
next task.
## Modelling
Once the data is ready, train a classifier. You are free to choose the type of model but, please, justify your 
decision. How you train your model and which metrics you are evaluating are important.
## Dockerising, ML as a service.
Save the model in a binary file and, using a Flask in a Docker container, create a REST API. For a well-formed 
prediction request, the Flask app shall load the model, compute the prediction and will respond to the 
prediction request with a JSON.
## Databases and UI
When there’s a prediction made, the app shall store: the current timestamp, the input values and the 
prediction in a database (not in a file). Additionally, the Flask app should have a URL destination in which we 
can see a simple table with all the saved predictions. You are free to choose the type of database but, please, 
justify your decision



## Steps to run the Application
Install packages: `pip install -r requirements.txt`

Create/Activate an virtual environment: $ `. venv/bin/activate`

Deactivate the virtual environment: $ `. venv/bin/deactivate`

Run the flask app: $ `flask run`

Docker build command: `docker build -t docker.prediction.com:latest .`

Docker run command: `docker run -d -p 8081:5000 --name=prediction-app docker.prediction.com:latest`

Docker stop: `docker stop prediction-app`

Docker prune: `docker prune prediction-app`
