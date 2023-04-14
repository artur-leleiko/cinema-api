# Cinema API
API service for cinema management written on DRF

## Installing using GitHub
Install PostgreSQL and create db

```
git clone https://github.com/artur-leleiko/cinema-api.git
cd cinema_API
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
set DB_HOST=<your db hostname>
set DB_NAME=<your db name>
set DB_USER=<your db username>
set DB PASSWORD=<your db user password>
set DJANGO_SECRET_KEY=<your secret key>
python manage. py migrate
python manage. py runserver
```

## Run with docker
Docker should be installed
```
docker-compose build
docker-compose up
```

## Getting access
```
Create user via /api/user/register/
Get access token via /api/user/token/
Install ModHeader extension and create Request header with value: Bearer <Your access token>
```

## Features
- JWT authenticated
- Admin panel /admin/
- Documentation is located at /api/doc/swagger/
- Managing orders and tickets
- Creating movies with genres, actors
- Creating cinema halls
- Adding movie sessions
- Filtering movies and movie sessions

## Creating Admin user
- Display containers list: 
```
docker ps
```
- Copy container ID
- Run
```
docker exec -it <container ID> bash
```
- Create superuser
```
python manage.py createsuperuser
```
