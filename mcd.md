# Livrable n°4 : retour sur un MCD d’un.e apprenant.e

Bon travail !
Attention à bien respecter la syntaxe merisienne. (Exemple: Les association doivent être dans des ellipses)

Des erreurs sont à noter sur la cardinalité de l'association LIKE. Ce dernier signifie :
- User peut liker entre 1 et 1 produit
- Un produit est liké entre 1 et 1 user
Hors
- User peut liker entre 0 et plusieurs produits
- Un produit est liké entre 0 et plusieurs users
Il faut mettre la cardinalité "0,n" pour les 2

Il pourrait aussi être intéressant d'ajouter plus d'attributs dans l'entité User comme le nom, le prénom ou encore la date de naissance.