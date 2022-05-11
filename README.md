# pg / PostgreSQL

### connection au serveur PostGres
`sudo -i -u postgres psql`

### commandes basique
- `\l` liste des bases de données
- `\du` liste des utilisateurs(rôles) existants
- `\dt` liste des tables de la bdd courantes

### créer un utilisateur (role)
- `CREATE ROLE nomDésiré WITH PASSWORD 'nomDésiré';`

### créer une nouvelle BDD
- `CREATE DATABASE nomDésiré OWNER 'nomDésiré';`
  
### ensuite je sors
`exit`

### maintenant pour me reconnecter
`psql -U nomDésiré -d nomDésiré;`

