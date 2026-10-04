# Nebula Finterest — builds macOS

Builds macOS de [Nebula-Finterest](https://github.com/Memel-SQT/Nebula-Finterest), téléchargeables dans les [Releases](../../releases).

- Le code de l'app vient tel quel du dépôt d'origine, à chaque nouveau commit sur `main`.
- Seuls les patchs de [`patches/`](patches) sont ajoutés. Ils ne concernent **que macOS** (chaque modification est gardée par `process.platform === 'darwin'`, une option propre à la plateforme Mac, ou une branche équivalente) : les builds Windows et Linux du dépôt d'origine ne changent pas.
- Les bugs macOS sont décrits dans [`bug-reports/macos/`](https://github.com/Memel-SQT/Nebula-Finterest/tree/main/bug-reports/macos) du dépôt d'origine.

## Installation (app non signée)

Ces builds ne sont ni signés ni notarisés par Apple. Au premier lancement, macOS peut dire que l'app « est endommagée » ou « ne peut pas être ouverte ». Après l'avoir copiée dans Applications :

```bash
xattr -cr "/Applications/Nebula Finterest.app"
```

ou bien clic droit → Ouvrir. Fichiers : `-arm64` pour les Mac Apple Silicon (M1 et suivants), `-x64` pour les Mac Intel.

La mise à jour automatique intégrée ne fonctionne pas sur macOS pour une app non signée : installez simplement la release Mac suivante.

## Limites connues sur macOS
- Le bouton de mise à jour indique une erreur (pas de `latest-mac.yml` dans les releases d'origine) : c'est attendu.
