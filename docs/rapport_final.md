# Rapport final - M-Motors

## Tableau de synthèse

| Description | Valeur |
| --- | --- |
| Lien Git frontend | A renseigner |
| Lien Git backend | A renseigner |
| Lien application | A renseigner |
| Login admin | adminLocal@Motors |
| Mot de passe admin | AdminMot1! |
| Login user | userLocal@Motors |
| Mot de passe user | UserMot1! |

## Présentation

M-Motors souhaite ajouter une offre de location longue durée avec option d'achat à son application de vente de véhicules d'occasion. La solution proposée couvre le parcours client et le back-office nécessaire au traitement des dossiers.

## Fonctionnalités livrées

Client :

- recherche de véhicules ;
- filtre achat/location ;
- inscription et connexion ;
- dépôt de dossier ;
- téléversement de documents ;
- suivi du statut.

Administration :

- création de véhicules ;
- bascule vente/location ;
- consultation des dossiers ;
- validation ou refus des dossiers.

## Architecture

React communique avec FastAPI via une API REST. FastAPI stocke les données dans SQLite en local. La cible cloud recommandée est PostgreSQL.

RPO : 15 min.

RTO : 1 heure.

## Sécurité

La solution utilise JWT, hash bcrypt des mots de passe, rôles user/admin, validation Pydantic, restriction des routes admin et contrôle des formats de documents.

## Tests

Les tests backend couvrent l'authentification, les véhicules, les dossiers, les droits admin et le healthcheck. Les tests frontend couvrent les écrans et composants demandés.

## Monitoring

L'application expose `/health`, journalise les requêtes et propose `/health/alert-test` pour démontrer un alerting simulé.

## Déploiement

Le déploiement final doit être réalisé sur Render, Railway, Heroku ou équivalent. Le lien Replit ne doit pas être utilisé comme lien final d'examen.

## Améliorations possibles

- Stockage cloud sécurisé des documents.
- Migrations Alembic.
- Scan antivirus des fichiers.
- Tableau de bord de supervision externe.
- Tests end-to-end Playwright.

