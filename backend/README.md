# Backend M-Motors

API FastAPI pour gérer l'authentification, les véhicules, les dossiers clients, le back-office, les logs et le healthcheck.

## Lancement

```bash
cd mmotors/backend
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
uvicorn app.main:app --reload
```

## Comptes créés au démarrage

| Rôle | Email | Mot de passe |
| --- | --- | --- |
| Admin | adminLocal@Motors | AdminMot1! |
| User | userLocal@Motors | UserMot1! |

Les emails sont normalisés en minuscules en base, mais la connexion accepte les identifiants fournis dans le sujet.

## Endpoints principaux

- `POST /auth/register`
- `POST /auth/login`
- `GET /auth/me`
- `GET /vehicles`
- `POST /applications`
- `GET /applications/me`
- `POST /admin/vehicles`
- `PATCH /admin/vehicles/{id}/switch`
- `GET /admin/applications`
- `PATCH /admin/applications/{id}/status`
- `GET /health`
- `POST /health/alert-test`

## Tests

```bash
cd mmotors/backend
pytest --cov=app
```

## Base de données

SQLite est utilisée pour simplifier le développement et la correction. Le passage PostgreSQL est documenté dans `docs/migration.md`.

