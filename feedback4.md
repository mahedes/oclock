# Feedback 4 - Apprenant 4

De nombreuses erreurs sont à relever, ce qui explique pourquoi votre application a du mal à fonctionner

Voici quelques causes :

#### public/index.php
ligne 14 : vous appelez le controller  App\Controllers\MainController, hors celui-ci n'existe pas
ligne 42 : Etant donné que le controller  App\Controllers\MainController, cette route ne peut être fonctionnel
ligne 107,117 : Erreur de syntaxe sur l'appel du controller StudentController

#### App/Controllers/StudentController.php
La classe extend CoreController, cependant ce dernier n'existe pas
ligne 20 : vous utilisez une méthode dans une autre méthode de même nom 
ligne 42 : erreur de syntaxe sur l'instance new Students

#### App/Controllers/TeacherController.php
La classe extend CoreController, cependant ce dernier n'existe pas
ligne 20 : vous utilisez une méthode dans une autre méthode de même nom 

#### App/Controllers/UserController.php
TeacherController.php
La classe extend CoreController, cependant ce dernier n'existe pas
ligne 48, 49 : utilisation de 2 méthodes setter ( .setFirstname() et .setLastname() ) qui n'existe pas dans l'entité models/AppUser.php.

#### models/Students.php
absence de la propriété teacher_id


## Suggestions:

Je vous conseille fortement de reprendre votre travail et de faire au mieux pour le completer.
Afin de ne pas vous perdre dans votre travail, essayez d'organiser votre projet par étape.
Reprenez l'application et essayez dans un premier temps de faire fonctionner votre routeur sur l'ensemble des liens désirés. (route <-> controleur)
Ensuite, compléter vos pages avec l'intégration HTML
Puis créer vos modeles entité (student, teacher, user) afin que ces dernières correspondent bien aux données dans la base de données.
Par la suite, code vos requetes SQL.
Une quoi que tout cela fonctionne, intégrer les données dans vos pages, puis compléter les fonctionnalités des formulaires.
Pensez également à bien revoir la notion MVC
