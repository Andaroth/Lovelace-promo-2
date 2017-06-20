## Se connecter à une base de données avec PDO

### Prérequis

* connaître les manipulations de base d'une BD
  * [SELECT FROM, WHERE, HAVING, ORDER BY](https://github.com/becodeorg/BXLCentral/blob/master/Parcours/MySQL/1.select.md)
* avoir créé sa première base de données
  * [suivre ce lien pour créer sa BD](https://github.com/becodeorg/BeCode/wiki/Installer-LAMP-sur-Ubuntu)
* être familiarisé à PHPMyAdmin

### PDO: deux secondes de théorie...

PDO est une méthode **d'accès** aux base de données: **P** HP **D** ata **O** bjects
PDO est activé par défaut.
Pour le vérifier, vous pouvez vous rendre sur le fichier info.php précédement créé (à l'adresse localhost/php.info) et faire une recherche sur PDO (ctrl/pomme + F).

  > si il n'est pas activé, vous devrez le faire manuellement dans le fichier php.ini et modifier cette ligne:
  > `pdo_mysql.default_socket = /opt/lampp/var/mysql/mysql.sock`

### Se connecter à la BD avec PDO

Vous devez créer un nouveau fichier PHP dans un nouveau sous-dossier de var/html/
et utiliser ce code:

`<?php
try
{
	// On se connecte à MySQL
	$bdd = new PDO('mysql:host=localhost;dbname=becode;charset=utf8', 'root', 'MOTDEPASSE');
}
catch(Exception $e)
{
	// En cas d'erreur, on affiche un message et on arrête tout
        die('Erreur : '.$e->getMessage());
}`

Pour que ça fonctionne il vous faut ces infos:
* le nom d'hôte (localhost): généralement ceci ne change pas;
* la base de données (becode): c'est le nom de la base de données à manipuler et créée via PHPMyAdmin;
* le login (root): votre nom d'utilisateur;
* le mot de passe: sous WAMP il n'y a pas de mot de passe, sous MAMP le mot de passe est par défaut root mais il se peut que vous l'ayez changé lors de la modification des droits d'écriture.
*Qu'est-ce-que c'est que ces TRY et CATCH:* c'est pour vérifier qu'il n'y ait pas d'erreur.

### Récupérer les données
???table météo???

#### importer les données

Vous devez **importer** la table météo via PHPMyAdmin(via l'onglet 'import').
Et ajouter dans votre fichier PHP à la suite du code précédent:
`$resultat = $bd->query('SELECT * FROM meteo');`
Le contenu des parenthèses est à modifier selon les opérations/ manipulations que vous voulez faire sur la BD. Le contenu de la BD est stocké sous forme d'objet dans la variable $resultat.
#### afficher les donnée de la BD
On doit faire un `fetch()` sur la variable déclarée `$resultat`($donnees donnera un ARRAY):

`$donnees = $reponse->fetch();`

Ensuite il suffit de faire un `echo` sur la variable que vous avez déclaré, ici c'est `$donnees` et la mettre dans une **boucle**:
`while ($donnees = $reponse->fetch())
{
  echo $donnees['NOM_de_la_COLONNE'];
}
`
où ['NOM_de_la_COLONNE'] est facultatif et vous permet de récupérer le contenu d'une colonne particulière.

Enfin il faudra ajouter cette dernière ligne pour **terminer le traitement** de la requête:
 `$reponse->closeCursor();`

>ça marche?
>passez à l'étape suivante: écrire des données dans un BD

[plus d'infos sur PHP.net](http://php.net/manual/fr/book.pdo.php)
