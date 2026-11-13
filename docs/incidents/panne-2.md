| Champ | Valeur |
|---|---|
| **Numéro** | 2 |
| **Date et heure** | 13/11/2026 à 16:10 |
| **Symptôme exact** | `Test-NetConnection … -Port 80` rend `TcpTestSucceeded : False`[cite: 1]. |
| **Vérifications (du client au serveur)** | 1. Test TCP depuis le client.<br>2. Vérification sur le serveur avec `netstat -an | findstr :80` (le port écoute en `LISTENING`).<br>3. Vérification de la règle de pare-feu avec `Get-NetFirewallRule` (`Enabled : False`)[cite: 1]. |
| **Cause (une phrase)** | La règle de pare-feu était désactivée[cite: 1]. |
| **Correction (où, exactement)** | PowerShell en administrateur sur le serveur : `Set-NetFirewallRule -DisplayName "ZooTickoon HTTP salle" -Enabled True`[cite: 1]. |
| **Preuve** | `Test-NetConnection ... -Port 80` : `True`[cite: 1]. |
| **Durée du diagnostic** | 4 minutes |