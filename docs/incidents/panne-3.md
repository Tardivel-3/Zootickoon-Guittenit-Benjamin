| Champ | Valeur |
|---|---|
| **Numéro** | 3 |
| **Date et heure** | 13/11/2026 à 16:20 |
| **Symptôme exact** | `Test-NetConnection … -Port 80` rend `TcpTestSucceeded : False` (même signature apparente que la panne de pare-feu)[cite: 1]. |
| **Vérifications (du client au serveur)** | 1. Test TCP depuis le client (échec).<br>2. Vérification sur le serveur avec `netstat -an | findstr :80` (ne rend rien)[cite: 1]. |
| **Cause (une phrase)** | Apache était arrêté dans Laragon sur le serveur[cite: 1]. |
| **Correction (où, exactement)** | Interface de Laragon (sur le poste serveur) : cliquer sur **Start All** pour relancer Apache[cite: 1]. |
| **Preuve** | `netstat -an | findstr :80` montre une ligne `LISTENING` pour le processus httpd[cite: 1]. |
| **Durée du diagnostic** | 3 minutes |