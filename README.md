# wttd-eventex
An Event System using Django

[![Build Status](https://travis-ci.org/matheusabr/wttd-eventex.svg?branch=master)](https://travis-ci.org/matheusabr/wttd-eventex)

[![Code Health](https://landscape.io/github/matheusabr/wttd-eventex/master/landscape.svg?style=flat)](https://landscape.io/github/matheusabr/wttd-eventex/master)

## How to run and contrib?

1. Clone repo
2. Create a virtualenv (Python v3.6)
3. Activate virtualenv
4. Install dependencies
5. Config instance with .env
6. Run tests

```console
git clone git@github.com:matheusabr/wttd-eventex.git wttd
cd wttd
python -m venv .wttd
source .wttd/bin/activate
pip install -r requirements-dev.txt
cp contrib/env-sample .env
python manage.py test
```

## How to deploy (Heroku)?
1. Create a Heroku instance
2. Set Heroku config
3. Define a safe SECRET_KEY
4. Set DEBUG=False
5. Config email service
6. Send code to Heroku

```console
heroku create myinstance
heroku config:push
heroku config:set SECRET_KEY=`python contrib/secret_gen.py`
heroku config:set DEBUG=False
# Config an email service
git push heroku master --force
```