---
layout: post
title:  Django Girls Tutorial Deploy to Heroku
date:   2017-03-29 21:11:00 -0800
categories: Python Django Heroku
tags: Python Django Heroku
---

Today I finished the [Django Girls Tutorial: Extensions](https://djangogirls.gitbooks.io/django-girls-tutorial-extensions/content/){:target="_blank"} exercises. I ran into database issues due to outdated config instructions from the tutorial. After asking for help from my alumni Slack channel and close inspection of Heroku docs, I successfully migrated my database and created a super user.

Changes for **mysite/settings.py**
```
import dj_database_url

...

DEBUG = False

ALLOWED_HOSTS = ['127.0.0.1', '.herokuapp.com']

...

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': 'djangogirls',
        'USER': 'yenly',
        'PASSWORD': '',
        'HOST': 'localhost',
        'PORT': '',
    }
}

...

db_from_env = dj_database_url.config(conn_max_age=500)
DATABASES['default'].update(db_from_env)
```

Link to work:
* [Django Girls Tutorial Blog](https://github.com/yenly/django_girls_blog)
* [Yenly's Django Blog - Deployed Demo on PythonAnwhere](http://yencodes.pythonanywhere.com/)
* [Yenly's Django Blog - Deployed Demo on Heroku](https://hipgibberish.herokuapp.com/)

Helpful resources:
* [Optional: PostgreSQL Installation](https://djangogirls.gitbooks.io/django-girls-tutorial-extensions/content/optional_postgresql_installation/){:target="_blank"}
* [Django Girls Tutorial: Deploy your website on Heroku](https://djangogirls.gitbooks.io/django-girls-tutorial-extensions/content/heroku/){:target="_blank"}
* [Getting Started on Heroku with Python - Provision a database](https://devcenter.heroku.com/articles/getting-started-with-python#provision-a-database){:target="_blank"}
* [Deploying Python and Django Apps on Heroku](https://devcenter.heroku.com/articles/deploying-python){:target="_blank"}
