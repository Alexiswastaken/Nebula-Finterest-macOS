## Installation (app non signée)

Ces builds ne sont ni signés ni notarisés par Apple. Au premier lancement, macOS peut dire que l'app « est endommagée » ou « ne peut pas être ouverte ». Après l'avoir copiée dans Applications :

```bash
xattr -cr "/Applications/Nebula Finterest.app"
```

ou bien clic droit → Ouvrir. Fichiers : `-arm64` pour les Mac Apple Silicon (M1 et suivants), `-x64` pour les Mac Intel.

La mise à jour automatique intégrée ne fonctionne pas sur macOS pour une app non signée : installez simplement la release Mac suivante.

## Limites connues sur macOS
- Le bouton de mise à jour indique une erreur (pas de `latest-mac.yml` dans les releases d'origine) : c'est attendu.
