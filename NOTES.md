## Ajouts propres à ce build Mac

Le patch `0002-incomes-ledger-categories.patch` ajoute des fonctions qui ne sont pas dans le Nebula Finterest d'origine :

- **Revenus** : en plus du revenu mensuel principal, autant de revenus que voulu, ponctuels (une date) ou récurrents (tous les mois).
- **Entrées et sorties** : tous les mouvements du mois à la suite, dans l'ordre des dates, avec le solde qui se construit.
- **Catégories** : entrées et sorties du mois par catégorie, les douze derniers mois, et des catégories que l'on peut créer et supprimer.
- « Achats prévus » s'appelle « Achats ».

Les données restent compatibles avec la version d'origine (tables ajoutées, rien de modifié).

## Installation (app non signée)

Ces builds ne sont ni signés ni notarisés par Apple. Au premier lancement, macOS peut dire que l'app « est endommagée » ou « ne peut pas être ouverte ». Après l'avoir copiée dans Applications :

```bash
xattr -cr "/Applications/Nebula Finterest.app"
```

ou bien clic droit → Ouvrir. Fichiers : `-arm64` pour les Mac Apple Silicon (M1 et suivants), `-x64` pour les Mac Intel.

La mise à jour automatique intégrée ne fonctionne pas sur macOS pour une app non signée : installez simplement la release Mac suivante.

## Limites connues sur macOS
- Le bouton de mise à jour indique une erreur (pas de `latest-mac.yml` dans les releases d'origine) : c'est attendu.
