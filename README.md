# Deploy flask app to GCP

## Guide

Visit https://console.cloud.google.com/getting-started

### 1. Create project

Be sure to setup billing too.

### 2. Access Settings

```
Navigation Menu -> IAM & Admin -> Settings
```

### 3. Activate Cloud Shell

Press that button at top right.

### 4. Clone this repo

```
git clone https://github.com/fsmosca/uflask.git
```

### 5. Change directory to uflask

```
cd uflask
```

### 6. Create virtual environment.

```
python -m venv venv
```

### 7. Activate the venv

```
source venv/bin/activate
```

### 8. Install the modules in the requirements.txt

```
pip install -r requirements.txt
```

### 9. Test it

We are not deploying yet.

```
gunicorn main:app
```

You should see:

"Hello from Flask."

Send control+c in shell to exit.

### 10. Create app

```
gcloud app create
```

### 11. Deploy the app

```
gcloud app deploy --appyaml=app.yaml
```

### 12. Browse the app

```
gcloud app browse
```

You will be given a url for your app.


## Others

You may type `gunicorn --help` to know more about its other options.
