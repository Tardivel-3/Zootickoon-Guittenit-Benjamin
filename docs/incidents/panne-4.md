| Champ | Valeur |
|---|---|
| **Numéro** | 4 |
| **Date et heure** | 13/11/2026 à 16:30 |
| **Symptôme exact** | `curl.exe -I http://zootickoon.test/` rend `200 OK`, mais la page est l'accueil de Laragon (« Server is running »), servie par `00-default.conf`[cite: 1]. |
| **Vérifications (du client au serveur)** | 1. Test de la requête HTTP (réponse 200 mais contenu incorrect).<br>2. Vérification sur le serveur des fichiers de configuration (`sites-enabled`), le `.conf` porte un autre `ServerName` que `zootickoon.test`[cite: 1]. |
| **Cause (une phrase)** | L'hôte virtuel Apache était renommé ou mal configuré avec un autre `ServerName`[cite: 1]. |
| **Correction (où, exactement)** | Fichier de configuration Apache dans Laragon (`sites-enabled`) : restaurer `ServerName zootickoon.test`[cite: 1]. |
| **Preuve** | Le fichier `access_log` de Laragon enregistre la requête HTTP avec le code `200` pour le bon hôte virtuel. |
| **Durée du diagnostic** | 6 minutes |