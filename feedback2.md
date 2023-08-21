# Feedback 2 - Apprenant 2

L'ensemble du code est plutôt correcte mais certaines fonctionnalités manquent
- Ajout d'un professeur et d'un étudiant
- Restreindre l'accès aux utilisateurs
- Mettre en place les permissions
Il faudra revoir ces notions afin de terminer l'application.

La notion de base Model View Controller semble acquise.

### Points d'améliorations

Rque1 : Une erreur apparait lors du chargement de la liste des étudiants.
Ce bug indique un problème avec la donnée teacher_id.
Il est important de noter que cette dernière est présente dans la base de donnée mais n'existe pas dans le modèle de l'entité Student (models/student.php). Il vous faudra compléter votre code afin de corriger cette erreur.

Rque2: Le bouton "modifier" de la page "Liste des formateurs" renvoie sur le formulaire d'ajout d'un formateur. Pensez à intégrer un bouton "Ajouter" sur cette page pour accéder au formulaire d'ajout. Le bouton "modifier" étant réservé pour accéder au formulaire de modification du formateur correspondant.

Rque3: Le fichier ErrorController.php est censé gérer l'affichage d'une page 404 quand une route est inexistante. Hors, vous avez une erreur php quand votre application appelle une route qui n'existe pas (ex: après avoir cliqué sur la lien Utilisateurs dans la barre de navigation). 
Cette erreur indique que le fichier template views/error/err404.php n'existe pas. Il vous faudra compléter votre code afin de corriger cette erreur.
