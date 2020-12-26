# flask_basic_heroku

install vituallenv: 
pip install virtualenv

create:
virtualenv mypython

activate:
cd mypython
Scripts\activate

intall flask e gunicorn
pip install flask gunicorn

Create an app folder:
mkdir app
cd app
####code 
from flask import Flask
app= Flask(__name__)
@app.route('/')
def index():
  return "<h1>Welcome to CodingX</h1>"
####

freeze:
pip freeze
pip3 freeze > requirements.txt

gunicorn:
web: gunicorn app:app

Create an app in Heroku:
acesse e crie uma conta e um app...

Deploy heroku:
heroku login
git init
heroku git:remote -a name_server
git add.
git commit -am "First python app"
git push heroku master
