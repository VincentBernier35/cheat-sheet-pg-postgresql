# pg / PostgreSQL

### connection au serveur PostGres
`sudo -i -u postgres psql`

### commandes basique
- `\l` liste des bases de données
- `\du` liste des utilisateurs(rôles) existants
- `\dt` liste des tables de la bdd courantes
- `\i` chemin/fichier.sql => cela permet d'importer une table
- `\conninfo` permet de voir les paramètres de connexion
 
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

