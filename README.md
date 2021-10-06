# Google Cloud Functions Course
## Starting a project
To start project go to GCP console
## Creating a virtual environment
First we have to install 'python3-venv' with the following command:
```
sudo apt install python3-env
```
Then we execute following command:
```
python3 -m venv venv
```
To activate virtual environment do:
```
venv\Scripts\activate.bat
```
In order to add new packages in our new virtual environment,
create a new file 'requirements.txt' and do:
```
pip install -r requirements.txt
```
### Deploying Cloud Functions
First, we have to set our project ID with the following command:
```
gcloud config set project [YOU_PROJECT_ID]
```
Then we deploy our function with command:
```
gcloud functions deploy [FUNCTION_NAME] --runtime python37 --trigger-http
```
## Schedule Cloud Functions
We execute the following commands:
```
gcloud components install beta
gcloud components update
gcloud pubsub topics create [TOPIC_NAME]
gcloud pubsub subscriptions create cron-sub --topic [TOPIC_NAME]
```
## Deleting Cloud Functions
To delete a Cloud Function run the following command:
```
gcloud functions delete [FUNCTION_NAME]
```