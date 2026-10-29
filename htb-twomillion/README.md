# TwoMillion – HackTheBox (Easy)

**Plateforme** : HackTheBox (machine retirée)
**OS** : Linux (Ubuntu 22.04)
**Difficulté** : Easy
**Date** : octobre 2026

## Résumé

Chaîne d'exploitation côté web menant à un accès root :
- Contournement d'une API d'invitation faiblement protégée (ROT13 / Base64)
- Élévation de privilèges par mass assignment vers le rôle admin
- Injection de commande (aveugle) sur un endpoint d'administration
- Identifiants trouvés en clair dans un fichier `.env`
- Élévation root via CVE-2023-0386 (OverlayFS/FUSE)



## Vulnérabilités couvertes

Validation côté client, mass assignment (CWE-915), injection de commande 
(CWE-78), stockage de secrets en clair (CWE-312), réutilisation 
d'identifiants, vulnérabilité noyau (CVE-2023-0386).

Réalisé à but pédagogique sur une machine d'entraînement retirée.