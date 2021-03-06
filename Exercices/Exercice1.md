# Exercice n°1 - Intégration des fichiers Bootstrap: css et js
L'exercice portera sur l'intégration des fichiers de base de Bootstrap pour que votre page web implémente le framework Bootstrap. A savoir le fichier css et le fichier js de Bootstrap.

Pour les prochains exercices, nous partirons sur un fichier html déjà fait. Mais il est important que vous sachiez le faire vous-même aussi.

## Partie 1 - Création du fichier Exercice1.html
Créez un fichier nommé Exercice1.html dans le répertoire EqlaExercices\Bootstrap.  
Créez ce fichier html comme vous l'avez vu avec Serge.

## Partie 2 - Ajout d'un titre
Mettez comme titre: Exercice1

## Partie 3 - Ajout du doctype
N'oubliez pas que pour Bootstrap il faut absolument de l'html5. Pour cela, vous devez mettre en toute première ligne de votre fichier html ceci: [<!doctype html>](https://developer.mozilla.org/fr/docs/Glossary/Doctype "Qu'est-ce que le doctype sur Mozilla ?")

## Partie 4 - Ajout du fichier css de Bootstrap

Dans la balise [\<head>](https://developer.mozilla.org/fr/docs/Web/HTML/Element/head "Element head sur Mozilla"), ajoutez le fichier suivant:
- [bootstrap.min.css](Files/bootstrap.min.css?raw=1) (Il faut donc le télécharger et le mettre dans le répertoire de vos exercices)

Pour rappel, utilisez la balise [\<link>](https://developer.mozilla.org/fr/docs/Web/HTML/Element/link "Element link sur Mozilla") avec les bons attributs.

## Partie 5 - Ajout du fichier js de Bootstrap

Juste avant la fermeture de la balise [\<body>](https://developer.mozilla.org/fr/docs/Web/HTML/Element/body "Element body sur Mozilla"), ajoutez le fichier suivant:
- [bootstrap.bundle.min.js](Files/bootstrap.bundle.min.js?raw=1) (Il faut donc le télécharger et le mettre dans le répertoire de vos exercices)

Pour rappel, utilisez la balise [\<script>](https://developer.mozilla.org/fr/docs/Web/HTML/Element/script#exemples "Element script sur Mozilla") avec les bons attributs.

## Partie 6 - Ajout des tag meta nécessaires
Dans la balise head, ajoutez les tags [\<meta>](https://developer.mozilla.org/fr/docs/Web/HTML/Element/meta "Element meta sur Mozilla") suivants:
```html
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
```

## Partie 7 - Ajout d'un titre 1
Mettez le texte suivant en titre1: Hello World from Exercice 1 !

## Partie 8 - Envoi sur GitHub
Si cela vous semble bon, dans un terminal envoyez vos modifications sur GitHub.
Appelez-moi pour qu'on vérifie ensemble.

Sur le site [Bootstrap](https://getbootstrap.com/docs/5.2/getting-started/introduction/ "Au point \"2. Include Bootstrap’s CSS and JS.\""), vous trouverez un exemple d'intégration. Votre exercice devrait ressembler un PEU à ça mais en travaillant sur des fichiers locaux (qui sont sur votre ordinateur). Donc ce n'est pas la solution de l'exercice mais cet exemple peut vous aider.
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Bootstrap demo</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0-beta1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-0evHe/X+R7YkIZDRvuzKMRqM+OrBnVFBL6DOitfPri4tjfHxaWutUpFmBp4vmVor" crossorigin="anonymous">
  </head>
  <body>
    <h1>Hello, world!</h1>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0-beta1/dist/js/bootstrap.bundle.min.js" integrity="sha384-pprn3073KE6tl6bjs2QrFaJGz5/SUsLqktiwsUTF55Jfv3qYSDhgCecCxMW52nD2" crossorigin="anonymous"></script>
  </body>
</html>
```