| Champ | Valeur |
|---|---|
| **Numéro** | 1 |
| **Date et heure** | 13/11/2026 à 16:00 |
| **Symptôme exact** | `ping zootickoon.test` renvoie une autre adresse IP que la vôtre, ou « hôte introuvable »[cite: 1]. |
| **Vérifications (du client au serveur)** | 1. Test du nom de domaine depuis le client (`ping zootickoon.test`).<br>2. Vérification du fichier `C:\Windows\System32\drivers\etc\hosts` sur le poste client[cite: 1]. |
| **Cause (une phrase)** | La ligne hosts du client pointait vers une adresse IP erronée ou inexistante[cite: 1]. |
| **Correction (où, exactement)** | Fichier `C:\Windows\System32\drivers\etc\hosts` du poste client (via Bloc-notes en administrateur) : remettre l'IP exacte du serveur suivie de `zootickoon.test`[cite: 1]. |
| **Preuve** | `ping zootickoon.test` -> `[192.168.2.118]`[cite: 1]. |
| **Durée du diagnostic** | 5 minutes |