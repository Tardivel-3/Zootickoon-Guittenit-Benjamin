| Champ | Valeur |
|---|---|
| **Numéro** | 5 |
| **Date et heure** | 13/11/2026 à 16:40 |
| **Symptôme exact** | `curl.exe -I http://zootickoon.test/` rend `200 OK`, mais la page est « Index of / », la liste des fichiers du site (Apache liste le dossier quand `index.html` manque)[cite: 1]. |
| **Vérifications (du client au serveur)** | 1. Constatation de l'affichage de l'index brut des fichiers.<br>2. Vérification du dossier du projet sur le serveur (`C:\laragon\www\zootickoon`) : le fichier `index.html` manque[cite: 1]. |
| **Cause (une phrase)** | La page d'accueil `index.html` a été supprimée de la racine du site[cite: 1]. |
| **Correction (où, exactement)** | Dossier racine du site (`C:\laragon\www\zootickoon`) : remettre en place le fichier `index.html` manquant[cite: 1]. |
| **Preuve** | Le fichier `access_log` de Laragon confirme le chargement normal de la page d'index du site web. |
| **Durée du diagnostic** | 4 minutes |