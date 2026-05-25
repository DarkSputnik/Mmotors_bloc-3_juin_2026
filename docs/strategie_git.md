# Stratégie Git

## Branches

- `main` : version stable et déployable.
- `develop` : intégration des fonctionnalités validées.
- `feature/*` : développement isolé d'une user story ou d'un bloc technique.

Le projet a été généré puis validé selon une démarche d’intégration progressive : documentation initiale, validation backend/API, validation applications et administration, intégration frontend/backend, puis validation du parcours complet. Même si un nombre plus important de commit aurait potentiellement été nécessaire. Il en compte 5.

## Bonnes pratiques

- Commits courts et compréhensibles.
- Une branche par fonctionnalité.
- Tests exécutés avant fusion dans `develop`.
- `main` réservée aux versions prêtes à déployer.
- Variables sensibles exclues du dépôt.

