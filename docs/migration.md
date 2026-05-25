# Migration SQLite vers PostgreSQL

## Situation actuelle

SQLite est utilisé pour simplifier le développement local, les tests et la correction.

## Cible recommandée

PostgreSQL managé sur Render, Railway, Heroku ou équivalent.

## Étapes de migration

1. Créer une base PostgreSQL dans le cloud.
2. Récupérer l'URL de connexion.
3. Définir la variable d'environnement :

```bash
DATABASE_URL=postgresql://user:password@host:5432/database
```

4. Installer le driver PostgreSQL si nécessaire :

```bash
pip install psycopg2-binary
```

5. Ajouter `psycopg2-binary` dans `backend/requirements.txt`.
6. Démarrer l'API : les tables sont créées automatiquement au démarrage.
7. Exécuter le seed pour créer les comptes de démonstration.
8. Importer les données existantes si nécessaire.

## Migration des données

Pour un petit volume, exporter SQLite en CSV puis importer dans PostgreSQL est suffisant. Pour un projet plus avancé, Alembic serait ajouté pour versionner les migrations.

## Sauvegardes

Le choix PostgreSQL cloud facilite :

- les sauvegardes automatiques ;
- la restauration à un instant donné ;
- le respect du RPO de 15 minutes ;
- le respect du RTO de 1 heure.

