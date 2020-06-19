# Django-Docker

This is a Docker container for django, gunicon.
The code base for this can be found at https://github.com/BenDowswell/Recipe-Site

#This was created on Ubuntu 20.4
Prerequisites:
Docker installed
Python 3.7 or higher installed

Steps:
1: In a new folder clone down the following repo's
    https://github.com/BenDowswell/Recipe-Site.git
    https://github.com/BenDowswell/Django-Docker.git
2:  Run command: python3 -m venv venv
3:  Copy the contents of Django-Docker folder into the folder you made in step 1, and delete Django-Docket folder.
4:  Activate venv by running: source venv/bin/activate
4:  Run command: pip install -r requirements.txt   (might see an error but pip fixes it)
5:  cd into Recipe-Site
6:  Run command: Python manage.py runserver
7:  surf to http://127.0.0.1:8000/  the deb website should load.  ctrl C in the terminal to close
8:  Run command: python manage.py collectstatic
9:  Run command: cd ..
10: Run command: chmod 755 start-server.sh
11: Run command: mkdir -p .pip_cache
12: Run command: sudo docker build -t recipesite .
13: Run command: sudo docker run -it -p 8020:8020 recipesite
14: surf to http://localhost:8020/   webapp should load


