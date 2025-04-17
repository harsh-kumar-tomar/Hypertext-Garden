[[Django]] setup

```python
# for setting up virtual env
python -m venv name_of_virtual_env

# run activate venv
.\Scripts\activate

# this command to deactivate venv
deactivate
```

possible error

```
cannot be loaded because running scripts is disabled on this system
```

solution

```
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```


```python
# to install Django
python -m pip install Django

# to check django version
# note : no spaces in django-admin

django-admin --version

# to set up django project
django-admin startproject project_name

# to run server
# it will listen on port http://127.0.0.1:8000/
# ctr + c to exit server
python manage.py runserver

```



```python
# it is necessary to be at project level to run this command
# as manage.py is only available inside the project_name folder
python manage.py startapp app_name 

# create urls.py inside app_name


```