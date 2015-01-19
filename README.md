Using Celery with Flask-SocketIO
=======================

This repository contains example code based off of Miguel Grinberg's excellent blog article [Using Celery with Flask](http://blog.miguelgrinberg.com/post/using-celery-with-flask) and his [example code](https://github.com/miguelgrinberg/flask-celery-example).  

The difference is that this code uses Flask-SocketIO (another excellent package by Miguel) to communicate status to the client without the client having to poll the server for status.

Quick Setup
-----------

1. Clone this repository.
2. Create a virtualenv and install the requirements.
3. Open a second terminal window and start a local Redis server (if you are on Linux or Mac, execute `run-redis.sh` to install and launch a private copy).
4. Open a third terminal window. Start a Celery worker: `venv/bin/celery worker -A app.celery --loglevel=info`.
5. Start the Flask application on your original terminal window: `venv/bin/python app.py`.
6. Go to `http://localhost:5000/` and enjoy this application!

