# Cinema Service
It is a online platform for movie-goers to easily browse and book movie tickets, and for cinema administrators to manage and maintain their operations.

## Features:
- JWT authenticated
- Admin panel /admin/
- Documentation is located at /api/doc/swagger/
- Managing orders and tickets
- Creating movies with genres, actors
- Creating cinema halls
- Adding movie sessions
- Filtering movies and movie sessions

## Environment variables
To connect to a Postgres DB and set Secret key in project, you need to use environment variables. Before installing the project, replace the values of these variables with your own values in the .env.sample file. Then, rename this file to .env
### How to install API using GitHub
```shell
  git clone https://github.com/WDemidenko/Cinema-service.git
  cd Cinema-service
  python -m venv venv
  venv\Scripts\activate (on Windows)
  source venv/bin/activate (on macOS)
  pip install -r requirements.txt
  python manage.py migrate
  python manage.py runserver
```

### How to install API using Docker
- Make sure you have installed Docker- 
- Run `docker-compose up --build`
- Use API through localhost `127.0.0.1:8000`

### To access the pages you need to follow this steps:
- Register at `http://127.0.0.1:8000/api/user/register/`
- Get token at `http://127.0.0.1:8000/api/user/token/`
- For each page you need to send this token in the header `Authorization: Bearer <your token>`
