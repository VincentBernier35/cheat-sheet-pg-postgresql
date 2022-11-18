# pg / PostgreSQL

### connection au serveur PostGres
`sudo -i -u postgres psql`

### commandes basique
- `\l` liste des bases de données
- `\du` liste des utilisateurs(rôles) existants
- `\dt` liste des tables de la bdd courantes
- `\i` chemin/fichier.sql => cela permet d'importer une table
- `\conninfo` permet de voir les paramètres de connexion
- \c nomdeladb   => permet de directement me connecter à cette table

 
### créer un utilisateur (role)
- `CREATE ROLE nomDésiré WITH LOGIN PASSWORD 'nomDésiré';`

### créer une nouvelle BDD
- `CREATE DATABASE nomDésiré OWNER 'nomDésiré';`

### Modifier un utilisateur existant
- `ALTER ROLE nomUtilisateur WITH <liste des droits>;`
  
### ensuite je sors
`exit`

### maintenant pour me reconnecter     
 `psql -U nomDésiré -d nomDésiré;`

-  ou sinon sans  `-d nomDésiré` alors connexion à la BDD qui porte le même nom que l'utilisateur.

---
### supprimer une database et un role/user
- d'abord se connecter pg `sudo -i -u postgres psql`
- `DROP DATABASE nomDésiré;`
- `DROP ROLE nom désiré`;

## config authentification
- accéder au fichier pg_hba.conf
1. `psql -V` pour vérifier le n° de version de psql installé
2. `cd /etc`
3. `cd postgresql`
4. `ls` trouver le même n° de version 12 ou 14 ...
5. `cd 14` si ma version psql est 14.***
6. `cd main`
7. `ls`
8. `sudo nano pq_hba.conf`
9. dans ce fichier changer la ligne local   all    postgres        (à la place de peer mettre MD5  ou trust)
10.  MD5 signifie qu'un mot de passe sera toujours demandé  et trust = plus de mot de passe demandé pour accéder aux db
11.  `cd /etc/postgresql/14/main` puis `sudo nano pg_hba.conf`
