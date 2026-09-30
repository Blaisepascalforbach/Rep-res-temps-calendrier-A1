# Repères A1 — version PWA

## Publier sur GitHub Pages

1. Décompresser cette archive.
2. Créer un dépôt GitHub et placer les six fichiers de ce dossier à sa racine (`index.html`, `manifest.webmanifest`, `sw.js`, les deux icônes et ce README).
3. Dans **Settings → Pages**, choisir la branche `main` et le dossier `/(root)`.
4. Envoyer aux élèves l’adresse `https://<nom-du-compte>.github.io/<nom-du-depot>/` créée par GitHub Pages.

Après la première ouverture, l’interface est mise en cache pour être consultée hors connexion. Pour l’installer, ouvrir l’adresse sur le téléphone puis choisir **Ajouter à l’écran d’accueil** ou **Installer l’application** dans le navigateur. Le micro nécessite HTTPS, l’autorisation de l’utilisateur et un navigateur compatible.

## Google Text-to-Speech

L’application appelle l’adaptateur `window.OEPRE_GOOGLE_TTS({ text, languageCode, speakingRate, speaker })` s’il est défini. Codes préparés : `fr-FR`, `ar-001`, `ps-AF`, `ka-GE`, `tr-TR`. L’adaptateur doit appeler un serveur qui contacte Google Cloud Text-to-Speech, lire l’audio reçu puis résoudre sa promesse. Ne pas inclure la clé Google dans les fichiers publiés sur GitHub.

Sans adaptateur, l’application utilise la voix du navigateur si elle est disponible. Pour l’oral, elle tente la reconnaissance vocale du navigateur ; sinon l’élève peut enregistrer, réécouter puis s’autoévaluer.
