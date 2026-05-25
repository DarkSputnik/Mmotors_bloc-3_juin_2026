# Stratégie Git

## Branches

- `main` : version stable et déployable.
- `develop` : intégration des fonctionnalités validées.
- `feature/*` : développement isolé d'une user story ou d'un bloc technique.

## Workflow prévu

```bash
git init
git checkout -b develop
git checkout -b feature/auth
git add .
git commit -m "05 auth"
git checkout develop
git merge feature/auth
git checkout main
git merge develop
```

## Commits réalistes

```bash
git commit -m "01 init projet"
git commit -m "02 docs"
git commit -m "03 backend"
git commit -m "04 modèles"
git commit -m "05 auth"
git commit -m "06 véhicules"
git commit -m "07 dossiers"
git commit -m "08 admin"
git commit -m "09 frontend"
git commit -m "10 tests backend"
git commit -m "11 tests frontend"
git commit -m "12 sécurité"
git commit -m "13 monitoring"
git commit -m "14 déploiement"
git commit -m "15 documentation"
```

## Bonnes pratiques

- Commits courts et compréhensibles.
- Une branche par fonctionnalité.
- Tests exécutés avant fusion dans `develop`.
- `main` réservée aux versions prêtes à déployer.
- Variables sensibles exclues du dépôt.

