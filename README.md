# argonautts.blog

This repository contains the source code of my blog — https://...


## ⚙️ Tech details

**Backend:**
- Python 3.11+
- Django 4+
- PostgreSQL
- [Poetry](https://python-poetry.org/) as a package manager

**Frontend:**
- [htmx](https://htmx.org/)
- Mostly pure JS
- No CSS framework

**Blogging part:**
- Markdown with a bunch of [custom plugins](common/markdown/plugins)

**CI/CD:**
- Github Actions + SSH deployment using [docker-compose.production.yml](docker-compose.production.yml) as a service configuration


## 🏗️ How to build

If you like to build it from scratch:

```
$ pip3 install poetry
$ poetry install
$ poetry run manage.py migrate
$ poetry run manage.py runserver 8000
```

Don't forget to create an empty Postgres database called `argonautts_blog` or your migrations will fail.

Another option for those who prefer Docker:

```
$ docker-compose up
```

Then open http://localhost:8000 and see an empty page.
