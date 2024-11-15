# Documentation générale

## Présentation du projet, objectifs finaux
  - Objectif principal :
    - Depuis une machine Windows Server, on exécute un script PowerShell qui cible des ordinateurs Windows
    - Depuis une machine Debian, on exécute un script shell qui cible des ordinateurs Ubuntu

  - Objectif secondaire :
    - Depuis un serveur, cibler une machine cliente avec un type d’OS différent


## Introduction : mise en contexte
Pour ce projet nous devons réaliser un script d'actions et d'informations, sur une machine distante.

En effet ce script est partagé en deux parties actions et informations, la première partie aura pour effet d'influer directement sur l'OS ciblé, tandis que la deuxième recueillera des informations sur ce même OS.
Le choix à été fait de réaliser le script en 4 parties, une pour chacun des membres du groupe.

## Membres du groupe de projet (rôles par sprint)
  
|   | Sprint S1 | Sprint S2 |  Sprint S3 | Sprint S4 |  
| :--: | :-------: | :-------: | :-------: | :-------: |  
| SCRUM MASTER | Martin | Martin | Igor  | Nicolas |  
| PRODUCT OWNER | Igor | Nicolas | Martin | Elsa |  
| TECHNICIANS | Elsa & Nicolas | Elsa & Igor | Elsa & Nicolas | Igor & Martin |  

## Choix techniques : quel OS, quelle version, etc.

### 2 CLIENTS
      
  - **Client Windows 10** :
    - Nom : CLIWIN01
    - Compte utilisateur : wilder (dans le groupe des admins locaux)
    - Mot de passe : Azerty1*
    - Adresse IP fixe : 172.16.10.20/24

  - **Client Ubuntu 22.04/24.04 LTS** :
    - Nom : CLILIN01
    - Compte utilisateur : wilder (dans le groupe sudo)
    - Mot de passe : Azerty1*
    - Adresse IP fixe : 172.16.10.30/24

### 2 SERVEURS

  - **Serveur Windows Server 2022** :
    - Nom : SRVWIN01
    - Compte : Administrator (dans le groupe des admins locaux)
    - Mot de passe : Azerty1*
    - Adresse IP fixe : 172.16.10.5/24

  - **Serveur Debian 12** :
    - Nom : SRVLX01
    - Compte : root
    - Mot de passe : Azerty1*
    - Adresse IP fixe : 172.16.10.10/24

### Taux de réalisation des tâches
Il y avait 58 commandes à réaliser au total par langage :
36 commandes en local + 22 commandes à distance en SSH.
Taux de réalisation en pourcentage des commandes :
* BASH : 81%
* POWERSHELL : 10%


|Type|Cible|Tâche|Bash|PowerShell|
|:-:|:-:|:-:|:-:|:-:|
|Action|Utilisateur|Création de compte utilisateur local|:white_check_mark:||
|Action|Utilisateur|Changement de mot de passe|:white_check_mark:||
|Action|Utilisateur|Suppression de compte utilisateur local|:white_check_mark:||
|Action|Utilisateur|Désactivation de compte utilisateur local|:white_check_mark:||
|Action|Utilisateur|Ajout à un groupe d'administration|:white_check_mark:||
|Action|Utilisateur|Ajout à un groupe local|:white_check_mark:||
|Action|Utilisateur|Sortie d’un groupe local|:white_check_mark:||
|Action|Ordinateur client|Arrêt (local)|:white_check_mark:||
|Action|Ordinateur client |Arrêt (SSH)||:white_check_mark:|
|Action|Ordinateur client|Redémarrage (local)|:white_check_mark:||
|Action|Ordinateur client|Redémarrage (SSH)||:white_check_mark:|
|Action|Ordinateur client|Verrouillage (local)|:white_check_mark:||
|Action|Ordinateur client|Verrouillage (SSH)||:white_check_mark:|
|Action|Ordinateur client|Mise-à-jour du système (local)|:white_check_mark:||
|Action|Ordinateur client|Mise-à-jour du système (SSH)||:white_check_mark:|
|Action|Ordinateur client|Création de répertoire (local)|:white_check_mark:||
|Action|Ordinateur client|Création de répertoire (SSH)||:white_check_mark:|
|Action|Ordinateur client|Modification de répertoire (local)|:white_check_mark:||
|Action|Ordinateur client|Modification de répertoire (SSH)|||
|Action|Ordinateur client|Suppression de répertoire (local)|:white_check_mark:||
|Action|Ordinateur client|Suppression de répertoire (SSH)|||
|Action|Ordinateur client|Activation du pare-feu (local)|:white_check_mark:||
|Action|Ordinateur client|Activation du pare-feu (SSH)|||
|Action|Ordinateur client|Désactivation du pare-feu (local)|:white_check_mark:||
|Action|Ordinateur client|Désactivation du pare-feu (SSH)|||
|Action|Ordinateur client|Installation de logiciel (local)|:white_check_mark:||
|Action|Ordinateur client|Installation de logiciel (SSH)|||
|Action|Ordinateur client|Désinstallation de logiciel (local)|:white_check_mark:||
|Action|Ordinateur client|Désinstallation de logiciel (SSH)|||
|Information|Utilisateur|Date de dernière connexion d’un utilisateur|:white_check_mark:||
|Information|Utilisateur|Date de dernière modification du mot de passe|:white_check_mark:||
|Information|Utilisateur|Liste des sessions ouvertes par l'utilisateur|:white_check_mark:||
|Information|Utilisateur|Groupe d’appartenance d’un utilisateur|:white_check_mark:||
|Information|Utilisateur|Historique des commandes exécutées par l'utilisateur|:white_check_mark:||
|Information|Utilisateur|Droits/permissions de l’utilisateur sur un dossier|:white_check_mark:||
|Information|Utilisateur|Droits/permissions de l’utilisateur sur un fichier|:white_check_mark:||
|Information|Ordinateur client|Version de l'OS (local)|:white_check_mark:||
|Information|Ordinateur client|Version de l'OS (SSH)|:white_check_mark:|:white_check_mark:|
|Information|Ordinateur client|Nombre de disque (local)|:white_check_mark:||
|Information|Ordinateur client|Nombre de disque (SSH)|:white_check_mark:||
|Information|Ordinateur client|Partition (nombre, nom, FS, taille) par disque (local)|:white_check_mark:||
|Information|Ordinateur client|Partition (nombre, nom, FS, taille) par disque (SSH)|:white_check_mark:||
|Information|Ordinateur client|Espace disque restant par partition/volume (local)|:white_check_mark:||
|Information|Ordinateur client|Espace disque restant par partition/volume (SSH)|:white_check_mark:||
|Information|Ordinateur client|Nom et espace disque d'un dossier (nom de dossier demandé) (local)|:white_check_mark:||
|Information|Ordinateur client|Nom et espace disque d'un dossier (nom de dossier demandé) (SSH)|:white_check_mark:||
|Information|Ordinateur client|Liste des lecteurs monté (disque, CD, etc.) (local)|:white_check_mark:||
|Information|Ordinateur client|Liste des lecteurs monté (disque, CD, etc.) (SSH)|:white_check_mark:||
|Information|Ordinateur client|Liste des applications/paquets installées (local)|:white_check_mark:||
|Information|Ordinateur client|Liste des applications/paquets installées (SSH)|:white_check_mark:||
|Information|Ordinateur client|Liste des services en cours d'execution|:white_check_mark:||
|Information|Ordinateur client|Liste des utilisateurs locaux|:white_check_mark:||
|Information|Ordinateur client|Mémoire RAM totale|:white_check_mark:||
|Information|Ordinateur client|Utilisation de la RAM|:white_check_mark:||
|Information|Script|Recherche des evenements dans le fichier log_evt.log pour un utilisateur|:white_check_mark:||
|Information|Script|Recherche des evenements dans le fichier log_evt.log pour un ordinateur|:white_check_mark:||





**- Difficultés rencontrées : problèmes techniques rencontrés**

1) Notre première difficulté à été de comprendre les besoins de ce script, et donc les solutions que nous allions devoir trouver.
2) La recherche et la compréhention des commandes pour les actions demandées.
3) La compréhention de ce que représente, ainsi que la création de la partie information.
4) La dernière partie du script sur les fichiers log_evt.log
5) Organisation dans le groupe, notament un agenda commun des tache type Myro

**- Solutions trouvées : Solutions et alternatives trouvées**
 1)  Beaucoup de temps passé à se documenter
 

**- Améliorations possibles : suggestions d’améliorations futures**
1) Passer les commandes en ssh sans copier le/les script(s)
2) 
