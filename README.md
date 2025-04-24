# ea_assignment_hint_B
[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=19179273)

# Report
https://vtcmca-my.sharepoint.com/:w:/g/personal/240115725_stu_vtc_edu_hk/EWfqy1EUSBpBsZda7Q1pq5MB6cRU1hSlFqNQZo0JrFCBEA?e=DInHKa

# How to create translation
Run following commands
```
cd app/
mkdir translations
pybabel extract -F babel.cfg -k lazy_gettext -o translations/messages.pot .
pybabel init -i translations/messages.pot -d translations -l en
pybabel init -i translations/messages.pot -d translations -l es
pybabel init -i translations/messages.pot -d translations -l zh
pybabel compile -d translations
cd app/
pybabel update -i translations/messages.pot -d translations
```

# How to Use it
flask db init 
flask db migrate -m "#comment"
flask db upgrade

flask --debug run --host=0.0.0.0


# Technical Specification:

- **Project Type**: A Flask web application using docker and postgre database
- **Programming Language**: Python (using Flask framework).
- **Database Migration**: Uses Flask-Migrate commands to initialize, migrate, and upgrade the database schema:
    - **`flask db init`**
    - **`flask db migrate -m "#comment"`**
    - **`flask db upgrade`**
- **Running the Application**: The app can be run in debug mode, listening on all interfaces (**`0.0.0.0`**), suitable for cloud environments like AWS Cloud9:
    - **`flask --debug run --host=0.0.0.0`**
- **Directory Structure**: Most of the file are inside **`app/`** directory.Database from [models.py](https://github.com/RW0NG722/ea_assignment_hint_B/blob/main/app/models.py), routes of different page from [routes.py](https://github.com/RW0NG722/ea_assignment_hint_B/blob/main/app/routes.py), input forms from [forms.py](https://github.com/RW0NG722/ea_assignment_hint_B/blob/main/app/forms.py) and page info inside [templates](https://github.com/RW0NG722/ea_assignment_hint_B/tree/main/app/templates) file.
- **Translation Directory**: Translations are stored in **`app/translations`**.

# Requirements

1. Bootstrap v3 or higher
2. Python 3.6 or higher
3. MySQL 5.5 or higher

# Deploy to AWS

1.Create cloud9 environment and open EC2 at least have 8GB RAM

2.expand the hard disk size ,at least 30 GB

3.pull docker image,install requirements.txt

4. open ports

5. run docker

# Deploy to GCP(GKE)

1.Use kompose to convert Docker Compose to Kubernetes file

2. open a cluster,use cloud shell to deploy 

?Source code to GitHub for Version Control?

