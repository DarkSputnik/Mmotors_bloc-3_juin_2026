# Tests backend

Date :
25/05/2026

Objectif :
Valider le fonctionnement du backend avant intégration frontend.

---

## Test 1 — Health Check

Route :
GET /health

Résultat :
200 OK

Vérifications :

- API démarrée
- Base de données accessible
- Monitoring simulé actif
- RPO = 15 min
- RTO = 1 heure

Statut :
VALIDÉ

---

## Test 2 — Authentification administrateur

Route :
POST /auth/login

Compte :

adminLocal@Motors

Résultat :

200 OK

Vérifications :

- JWT généré
- rôle admin reconnu

Statut :
VALIDÉ

---

## Test 3 — Authentification utilisateur

Route :
POST /auth/login

Compte :

userLocal@Motors

Résultat :

200 OK

Vérifications :

- JWT généré
- rôle user reconnu

Statut :
VALIDÉ

---

## Test 4 — Mauvais mot de passe

Route :
POST /auth/login

Résultat :

401 Unauthorized

Vérifications :

- accès refusé
- message d’erreur cohérent

Statut :
VALIDÉ

---

## Test 5 — Route protégée sans authentification

Route :
GET /auth/me

Résultat :

401 Unauthorized

Vérifications :

- accès anonyme refusé

Statut :
VALIDÉ

---

## Test 6 — Liste véhicules

Route :
GET /vehicles

Résultat :

200 OK

Vérifications :

- véhicules affichés
- achat/location distingués

Statut :
VALIDÉ

---

## Test 7 — Détail véhicule

Route :
GET /vehicles/4

Résultat :

200 OK

Vérifications :

- données cohérentes
- véhicule trouvé

Statut :
VALIDÉ

---

## Test 8 — Véhicule inexistant

Route :
GET /vehicles/9999

Résultat :

Erreur gérée

Vérifications :

- réponse cohérente
- cas limite pris en compte

Statut :
VALIDÉ

