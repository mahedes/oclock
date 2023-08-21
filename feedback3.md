# Feedback 3 - Apprenant 3

Une bonne partie du code est correcte mais certains éléments sont à revoir.
Les fonctionnalités suivantes sont manquantes:
- Restreindre l'accès aux utilisateurs
- Mettre en place les permissions
Il faudra revoir ces notions afin de terminer l'application.

La notion de base Model View Controller semble acquise, mais il faudra encore de l'entrainer pour se sentir pleinement à l'aise

Points d'améliorations
Rque1 : Présence d'erreurs dans les urls de la barre de navigation et des boutons.
Vous avez mélangé les liens vers les fichiers source (ex: "/index.html", "appuser/list.html") et le nom des routes (ex: "/home", "/teacher_list"). 
Aussi certaines routes ne correspondents pas (ex: Le bouton "Ajouter" de la page des formateurs renvoie sur le formulaire d'ajout d'un étudiant)
Votre application possède un routeur, il vous faut donc utiliser exclusivement les nom des routes.
A noter que pour la page d'accueil, il serait préférable de privilégier l'url racine "/" plutôt que la route "/home" afin de ne pas avoir une erreur 404 au lancement de l'application
Bien revoir la notion sur le router

Rque2 : Le header devrait être présent sur l'ensemble des pages de l'application. Pensez à utiliser "include" dans vos templates pour intégrer ce dernier sur toutes les pages et mais aussi pour éviter le duplicata de code dans vos fichiers.

Rque3 : Une erreur apparait lors du chargement de la liste des étudiants et l'ajout d'un étudiant.
Ce bug indique un problème avec la donnée teacher_id.
Il est important de noter que cette dernière est présente dans la base de donnée mais n'existe pas dans le modèle de l'entité Student (models/student.php). Il vous faudra compléter votre code afin de corriger cette erreur. Cela permettra de rendre votre formulaire fonctionnel

Rque4: Présence d'une méthode appelée studentAdd() dans votre TeacherController.
La méthode teacherAdd() est censée être appelé par la route '/teacher/add'. Hors elle n'existe pas
Il vous faudra corriger cette erreur et revoir le code.

