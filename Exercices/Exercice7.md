# Exercice n°7 - La grille Bootstrap
L'exercice portera sur l'utilisation de la [grille de Bootstrap](/Theorie/README.md#xi-la-grille-bootstrap).

Textes pour les colonnes:
- Je suis la première colonne.
- Je suis la deuxième colonne.
- Je suis la troisième colonne.
- Je suis la quatrième colonne.

## Partie 1 - Création du fichier Exercice7.html
Créez un fichier nommé Exercice7.html dans le répertoire EqlaExercices\Bootstrap.  

Copiez le contenu du fichier [template2.html](https://raw.githubusercontent.com/ZamBoyle/Eqla_Bootstrap5/master/Exercices/Templates/template2.html) dans le fichier Exercice7.html
## Partie 2 - Ajout d'un titre de page
Mettez comme titre: Exercice7

## Partie 3 - Ajout d'un titre 1
Ajoutez le titre 1 suivant: La Grille de Bootstrap

## Partie 4 - 4 colonnes
- Ajoutez un titre 2: 4 colonnes de tailles fixes
- Affichez quatre colonnes à taille fixe prenant toute la largeur.

## Partie 5 - 3 colonnes à taille fixe
- Ajoutez un titre 2: 3 colonnes à taille fixe
- Affichez trois colonnes à taille fixe ne prenant pas toute la largeur.

## Partie 6 - Taille des colonnes fonction de la taille de l'écran
- Ajoutez un titre 2: Taille des colonnes fonction de la taille de l'écran.
- Affichez deux colonnes prenant la moitié de l'écran chacune si la taille de l'écran est lg. Sinon deux lignes seront créées et la taille sera pour l'une <code>.col-md-2</code> et l'autre <code>.col-md-3</code>.

## Partie 7 - Colonnes et couleur d'arrière plan
- Ajoutez un titre 2: Colonnes et couleur d'arrière plan
- Ajoutez une colonne de taille fixe .col-4 de la ligne ayant une couleur de fond success et la couleur du texte en blanc. Le texte sera à gauche.
- Ajoutez une colonne de taille fixe prenant le 1/3 de la ligne ayant une couleur de fond warning et la couleur du texte en blanc. Le texte sera centré.
- Ajoutez une colonne prenant le reste de l'espace disponible ayant une couleur de fond danger. Le texte sera à droite.

## Partie 8 - Création d'une Galerie Photos Responsive
### 1. Objectif
Créer une galerie de photos qui s'adapte à différentes tailles d'écran en utilisant Bootstrap Grid System.

Donc, la galerie doit afficher un nombre différent de colonnes en fonction de la largeur de l'écran.

Voici 12 images pour la galerie qui devrait être responsives (il y a une classe pour cela):
1. [Cupcake à la banane](https://raw.githubusercontent.com/ZamBoyle/Eqla_HTML/master/Exercices/Site/img/products/banane.png).
2. [Cupcake au caramel](https://raw.githubusercontent.com/ZamBoyle/Eqla_HTML/master/Exercices/Site/img/products/caramel.png).
3. [Cupcake à la carotte](https://raw.githubusercontent.com/ZamBoyle/Eqla_HTML/master/Exercices/Site/img/products/carotte.png).
4. [Cupcake au chocolat](https://raw.githubusercontent.com/ZamBoyle/Eqla_HTML/master/Exercices/Site/img/products/chocolate.png).
5. [Cupcake au chocolat-menthe](https://raw.githubusercontent.com/ZamBoyle/Eqla_HTML/master/Exercices/Site/img/products/chocolat-menthe.png).
6. [Cupcake au citron](https://raw.githubusercontent.com/ZamBoyle/Eqla_HTML/master/Exercices/Site/img/products/citron.png).
7. [Cupcake à la fraise](https://raw.githubusercontent.com/ZamBoyle/Eqla_HTML/master/Exercices/Site/img/products/fraise.png).
8. [Cupcake à la framboise](https://raw.githubusercontent.com/ZamBoyle/Eqla_HTML/master/Exercices/Site/img/products/framboise.png).
9. [Cupcake au king-charles](https://raw.githubusercontent.com/ZamBoyle/Eqla_HTML/master/Exercices/Site/img/products/king-charles.png).
10. [Cupcake Marsien](https://raw.githubusercontent.com/ZamBoyle/Eqla_HTML/master/Exercices/Site/img/products/marsien.png).
11. [Cupcake à la pistache](https://raw.githubusercontent.com/ZamBoyle/Eqla_HTML/master/Exercices/Site/img/products/pistache.png).
12. [Cupcake Red-Velvet](https://raw.githubusercontent.com/ZamBoyle/Eqla_HTML/master/Exercices/Site/img/products/red-velvet%20.png).

### 2. Instructions
- Ajoutez un titre 2: Galerie Photos Responsive
- Ajoutez un <div> avec la classes row 
- Trouvez les bonnes classes à mettre à row pour que l'affichage respecte les règles suivantes:
    - 1 image par ligne sur les écrans de résolutions xs (très petite): vous mettrez ici row-cols-1.
    - 2 images par ligne sur les écrans de résolutions sm (petite).
    - 4 images par ligne sur les écrans de résolutions md (moyenne).
    - 6 images par ligne sur les écrans de résolutions lg (large).
- À l'intérieur de chaque <div> de colonne, insérez une image. Vous pouvez utiliser les images fournies ci-dessus et utiliser une classe vue en classe pour rendre les images responsives.
- Testez votre Page.
- Appelez-moi pour qu'on vérifie ensemble.
- Ajoutez sur le div row la classe: g-2
- Testez votre Page.
- Que fais la classe g-2 ?
- Appelez-moi pour qu'on vérifie ensemble.
- Essayez à la place de g-2: g-0, g-3, g-4, g-5.
- Vous pouvez voir le résultat de l'exercice [ici](https://zamboyle.github.io/Eqla_Bootstrap5/Exercices/Exercice7.html)

## Partie 9 - Envoi sur GitHub
Si cela vous semble bon, dans un terminal envoyez vos modifications sur GitHub.
