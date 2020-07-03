# JDBC-Questions-and-Answers-Generator
Questions and answers generator in Java with JDBC

Partie1:
Hiérarchie de l'ensemble du projet :
![image](https://user-images.githubusercontent.com/11277981/86470807-1666b400-bd34-11ea-9c2b-7c869bd51670.png)

  Pour simplifier l'enregistrement des utilisateurs dans une seule table j'ai ajouté an attribut profil (0 si c'est un professeur et 1 si c'est un étudiant) dans la table des utilisateurs.
 
![image](https://user-images.githubusercontent.com/11277981/86470822-1b2b6800-bd34-11ea-8ed4-29fa401592bc.png)



J'ai utilisé une BD Mysql et une connexion JDBC avec un singleton de connexion
 
![image](https://user-images.githubusercontent.com/11277981/86470833-2088b280-bd34-11ea-871f-6c0b67ccfb8f.png)

Voici les tables que j'ai implémenté.
![image](https://user-images.githubusercontent.com/11277981/86470847-28e0ed80-bd34-11ea-9d52-9346754d20e5.png)

  D’après le type de profil, l’utilisateur sera redirigé vers  l’interface correspondant (professeur ou étudiant).
![image](https://user-images.githubusercontent.com/11277981/86470867-31d1bf00-bd34-11ea-8deb-24b04e6e722b.png)


 Dans cette exemple, l’étudiant etudiantA se connecte et il est rediriger vers l’interface étudiant. 
![image](https://user-images.githubusercontent.com/11277981/86470887-3ac29080-bd34-11ea-9b8d-955ba9094cce.png)


Dans cette exemple, le professeur professeurA se connecte et il est rediriger vers l’interface des professeurs. 
![image](https://user-images.githubusercontent.com/11277981/86470893-401fdb00-bd34-11ea-98a0-94b72deb8c3c.png)
![image](https://user-images.githubusercontent.com/11277981/86470902-43b36200-bd34-11ea-9692-443e124b38c0.png)

  
 


  Voici l’interface des professeurs, contient 3 partie, une partie qui contient un JTable qui affiche les données de tous les utilisateurs de la base de données d la table des utilisateurs après l'avoir récupérée. Le professeur peut lister, ajouter ou supprimer un utilisateur.
Partie1:
  La deuxième partie de programme permet aux professeurs de créer des questions (QCM) et d’associer à chaque question trois réponses dans un seul est correct. Cela est fait par l’introduction des radiobox qui sont liées entre eux dans le radiobuttonsGroup, donc un seul radiobox est toujours sélectionner.
Voici un exemple d’ajout d’une question avec 3 réponses dont une est correct :
 
![image](https://user-images.githubusercontent.com/11277981/86470910-48781600-bd34-11ea-9240-bff64705785d.png)

Voici la table des questions dans notre base de donnée :
 
![image](https://user-images.githubusercontent.com/11277981/86470919-4d3cca00-bd34-11ea-94bb-e341819e2005.png)

Et voici la table des réponses :
 
![image](https://user-images.githubusercontent.com/11277981/86470931-5332ab00-bd34-11ea-8f71-36dd11c72c79.png)

On a idRep comme clé primaire et idQuest comme une clé étrangère :
 
![image](https://user-images.githubusercontent.com/11277981/86470940-57f75f00-bd34-11ea-8bd3-e5fbec3760d4.png)
![image](https://user-images.githubusercontent.com/11277981/86470953-5b8ae600-bd34-11ea-80c3-d23b8f03a114.png)


Voici un exemple d’ajout d’un étudiant Ahmed :
 
![image](https://user-images.githubusercontent.com/11277981/86470960-5fb70380-bd34-11ea-8f13-2f0c4f87810f.png)

Voici un exemple de suppression d’étudiant Ahmed :
 
![image](https://user-images.githubusercontent.com/11277981/86470968-63e32100-bd34-11ea-99f3-05aac85f60a4.png)

Le bouton List Users sert à rafraichir la JTable.
La troisième partie de programme est consacré pour la modification d’une question et ces réponses.


![image](https://user-images.githubusercontent.com/11277981/86470996-6a719880-bd34-11ea-92a2-8b06e138fd1d.png)

Partie3:

  Dans l'interface d'étudiant, on génère une épreuve de quatre questions sélectionnées d’une manière aléatoire pour chaque étudiant qui se connecte à notre application. L’application affichera à l’étudiant son score à la fin de chaque épreuve.
 
 
 
 
![image](https://user-images.githubusercontent.com/11277981/86471010-71001000-bd34-11ea-9879-a068f17cf7b1.png)
![image](https://user-images.githubusercontent.com/11277981/86471016-73626a00-bd34-11ea-9c36-fcf12e589665.png)

![image](https://user-images.githubusercontent.com/11277981/86471023-765d5a80-bd34-11ea-9bd6-70d9888a5917.png)

![image](https://user-images.githubusercontent.com/11277981/86471029-78bfb480-bd34-11ea-8ec7-b1e3eaccaea5.png)

![image](https://user-images.githubusercontent.com/11277981/86471037-7c533b80-bd34-11ea-90ff-9e972d57dad5.png)


 
À la fin, nous affichons le score à l'étudiant.
Veuillez explorer le code source pour plus d'info.
