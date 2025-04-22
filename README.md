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
AWS Cloud9


flask db init 
flask db migrate -m "#comment"
flask db upgrade

flask --debug run --host=0.0.0.0
