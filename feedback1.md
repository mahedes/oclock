# Feedback 1 - Apprenant 1

Ensemble très satisfaisant !

Quelques bugs sont à relever

### #7 Mettre en place les permissions

Il y a un défaut dans la compréhension de la consigne. Votre application a été crée ainsi

La fonctionnalité modification d'un professeur et d'un étudiant ne marche pas
- la liste des professeurs est caché pour les étudiants.
- l'étudiant peut ajouter, modifier et supprimer les étudiants 
Hors, les étudiants doivent avoir accès aux 2 listes (professeurs et étudiants) et il ne doit pas pouvoir ajouter, modifier ou supprimer des étudiants

### BONUS - Mise à jour d'un prof, et d'un étudiant

Il y a un bug pour cette fonctionnalité. Après validation du formulaire de modification, on a une erreur 404. Cela est du au fait que dans le fichier student_update.tpl.php, vous indiquez ligne 10, 
<form action="<?= $router->generate('student_update_post') ?>" method="POST" class="mt-5">
Il serait préférable de laisser l'attribut action vide. Ainsi la route actuellement actif sera rechargée, mais avec la méthode POST, ce qui redirigera naturellement vers la méthode teacherAddPost du controller TeacherController.

N'hésitez pas à terminer votre projet avec les fonctionnalités du bonus et superbonus (ex: CSRF) que vous n'avez pas intégré afin de perfectionner vos compétences.

### Suggestions d'amélioration
- Vous pouvez créer un fichier de configuration dédié à lister l'ensemble des routes utilisées dans l'application (ex: routes.php)
- Penser au typage des données pour la sécurité

