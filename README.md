# django-docker

## build and django startproject

```bash
$ docker-compose build
```

start django project

```
$ docker-compose run --rm django-admin startproject config .
```

## django database setting

edit app/config/settings.py DATABASE

```PYTHON
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'django',
        'USER': 'root',
        'PASSWORD': '',
        'HOST': 'db',
        'PORT': 3306,
    }
}
```

### docker-compose up

```bash
$ docker-compose up
```

### django database migrate and create superuser

```bash
$ docker exec -it django bash
```

django database migration

```bash
$ python manage.py migrate
```

django create superuser

```
$ python manage.py createsuperuser
```

### Login

[`localhost:8000/admin`](http://localhost:8000/admin/)