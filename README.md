# Lab9_mobile – Connexion Android ↔ PHP/MySQL (XAMPP)

## Description
Application Android permettant d’ajouter un étudiant dans une base de données MySQL via un service web PHP (XAMPP).  
L’envoi des données se fait avec **Volley** (requête POST), les réponses JSON sont parsées avec **Gson**.  
Le projet illustre la communication mobile ↔ serveur local sur le même réseau Wi-Fi.

## Architecture du projet

<img width="391" height="901" alt="archiAndr" src="https://github.com/user-attachments/assets/290be8fd-1d88-4730-aeb1-af35af0736fb" />

<img width="252" height="472" alt="archiPhp" src="https://github.com/user-attachments/assets/cffeae78-1105-450a-b076-47ee6cc4ffb9" />

## Installation et configuration
Demarrez apache et PhpMyAdmin dans xampp 

<img width="996" height="646" alt="1" src="https://github.com/user-attachments/assets/fb23a659-ddff-49c5-9c64-ac66f4c51738" />

Creez une base de donnees school1 et une table etudiants avec les colonnes `id`, `nom`, `prenom`, `ville`, `sexe`.

<img width="774" height="325" alt="mysql" src="https://github.com/user-attachments/assets/96e8eb9f-7c37-48f6-8ebb-2a8259154480" />

##Test depuis Postman 

<img width="1081" height="886" alt="postman" src="https://github.com/user-attachments/assets/524c4cb3-e208-4eba-963c-6b9e8975a21b" />

##Test depuis l'application mobile 

<img width="576" height="1280" alt="tele" src="https://github.com/user-attachments/assets/5ec5916a-746d-4e32-8814-2dc3b194fdec" />

<img width="739" height="351" alt="verif" src="https://github.com/user-attachments/assets/ba4da857-c292-407c-8137-535104133c68" />

##Important 
Il faut Autoriser le trafic HTTP :
  - Dans `AndroidManifest.xml` → `android:usesCleartextTraffic="true"`.
  - Dans `httpd-xampp.conf` (XAMPP) remplacer `Require local` par `Require all granted` pour l’accès externe.

##Améliorations possibles
Afficher un Toast en cas de succès/erreur.

Affichage de la liste des étudiants dans une RecyclerView.

Utiliser HTTPS avec un certificat auto‑signé (pour éviter le “cleartext”).



