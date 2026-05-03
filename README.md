# SiteGuard

A lightweight website status monitor built with Django. Add sites to watch,
and the dashboard shows their real-time online/offline status at a glance.

## Features

- Add and remove monitored websites from the web UI
- Real-time status checks via HTTP HEAD requests
- Bootstrap-styled responsive dashboard
- SQLite storage, no external database required

## Quickstart

```bash
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

Then open `http://localhost:8000/`.

## Docker

```bash
docker build -t siteguard .
docker run -p 8000:8000 siteguard
```

## Configuration

| Env Variable | Default | Description |
|---|---|---|
| `DJANGO_SECRET_KEY` | `dev-only-secret-change-in-prod` | Django secret key |
| `ALLOWED_HOSTS` | `*` | Comma-separated allowed hosts |
| `DB_PATH` | `/tmp/siteguard.sqlite3` | SQLite database path |

## License

MIT
