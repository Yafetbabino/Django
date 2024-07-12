# DJANGO lab3 MVT

```
wget "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-CD0251EN-SkillsNetwork/labs/m4_django_app/lab3_template.zip"
unzip lab3_template.zip
rm lab3_template.zip
```
```
cd lab3_template
```
```
pip install --upgrade distro-info
pip3 install --upgrade pip==23.2.1
pip install virtualenv
virtualenv djangoenv
source djangoenv/bin/activate
pip install -U -r requirements.txt
```
```
python3 manage.py makemigrations
```

```
python3 manage.py migrate
```
