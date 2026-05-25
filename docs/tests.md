# Tests

## Objectif

L'objectif est de couvrir environ 80 % des comportements critiques de l'application, conformément au sujet.

## Backend

Commande :

```bash
cd mmotors/backend
pytest --cov=app
```

Tests couverts :

- connexion OK ;
- inscription OK ;
- email déjà utilisé ;
- mauvais mot de passe ;
- liste véhicules ;
- filtre achat/location ;
- création véhicule admin ;
- dépôt dossier ;
- suivi dossier ;
- validation admin ;
- accès refusé ;
- health retourne 200 ;
- simulation d'alerting.

## Frontend

Commande :

```bash
cd mmotors/frontend
npm test
```

Tests couverts :

- page Login affichée ;
- page Search affichée ;
- composant VehicleCard affiché.

## Stratégie

Les tests backend vérifient les règles métier et la sécurité d'accès. Les tests frontend restent volontairement ciblés, car l'objectif de l'examen est de démontrer les parcours principaux sans surproduire une suite exhaustive.

