# Render FastAPI demo (Jedha Launch)

Slim FastAPI teaching demo for Render Free (512 MB).

## Files

- `app.py` — health, greetings, local CSV blog routes, tiny salary formula `/predict`
- `Dockerfile` — `python:3.12-slim`, binds `$PORT`
- `requirements.txt` — fastapi, uvicorn, pydantic, python-multipart
- `data/articles.csv` — local sample articles

## Push + deploy

See the day runbook:

`AIFS/.changelogs/M08-ML_Engineering/D06-Launch/MANUAL_DEPLOY_RUNBOOK.md`

## Local (no Docker)

```bash
pip install -r requirements.txt
PORT=10000 uvicorn app:app --host 0.0.0.0 --port 10000
```

Open `http://127.0.0.1:10000/health` and `/docs`.
