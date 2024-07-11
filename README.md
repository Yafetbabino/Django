### Coursera Django course

set upa a virtual environment which has all the packages we need.
```
pip install virtualenv
virtualenv djangoenv
source djangoenv/bin/activate
pip install Django psycopg2-binary

```

Then generate migration scripts for app related_objects
```
python3 manage.py makemigrations related_objects
```

run migration
```
python3 manage.py makemigrations related_objects
```