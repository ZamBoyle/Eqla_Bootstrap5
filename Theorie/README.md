# Bootstrap 5


<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Bootstrap 5](#bootstrap-5)
  - [I. A propos](#i-a-propos)
  - [II. Prérequis](#ii-prérequis)
  - [III. Présentation de Bootstrap](#iii-présentation-de-bootstrap)
    - [1. Brainstorming : Qu’est-ce que Bootstrap pour vous ?](#1-brainstorming--quest-ce-que-bootstrap-pour-vous-)
    - [2. Brève présentation de Bootstrap](#2-brève-présentation-de-bootstrap)
    - [3. Pourquoi utiliser Bootstrap ?](#3-pourquoi-utiliser-bootstrap-)
    - [4. Bootstrap 4.x et Bootstrap 5](#4-bootstrap-4x-et-bootstrap-5)
    - [5. Comment Utiliser Bootstrap ?](#5-comment-utiliser-bootstrap-)
  - [IV. Intégration des Fichiers Bootstrap](#iv-intégration-des-fichiers-bootstrap)
  - [V. Fonctionnement de Bootstrap](#v-fonctionnement-de-bootstrap)
    - [La classe .container](#la-classe-container)
    - [La classe .container-fluid](#la-classe-container-fluid)
  - [VI. Manipulation du texte](#vi-manipulation-du-texte)
    - [1. Alignement du texte](#1-alignement-du-texte)
    - [2. Alignement du texte fonction de l’écran](#2-alignement-du-texte-fonction-de-lécran)
    - [3. Les classes de mise en forme](#3-les-classes-de-mise-en-forme)
    - [4. Transformation du texte](#4-transformation-du-texte)
  - [VII. Les images](#vii-les-images)
    - [1. Responsive](#1-responsive)
    - [2. Thumbnail](#2-thumbnail)
    - [3. Alignement](#3-alignement)
    - [4. Images aux bords arrondis](#4-images-aux-bords-arrondis)
  - [VIII. L'Accessibilité](#viii-laccessibilité)
    - [1. Lecteur d'écran](#1-lecteur-décran)
    - [2. Animation réduite](#2-animation-réduite)
  - [IX. Les breakpoints](#ix-les-breakpoints)
  - [X. Les couleurs & Couleurs d'Arrière Plan.](#x-les-couleurs--couleurs-darrière-plan)
  - [XI. La Grille Bootstrap](#xi-la-grille-bootstrap)
    - [1. Classes pour un nombre fixe de colonnes](#1-classes-pour-un-nombre-fixe-de-colonnes)
    - [2. Classes pour un nombre de colonnes variables en fonction de la résolution](#2-classes-pour-un-nombre-de-colonnes-variables-en-fonction-de-la-résolution)
    - [3.	Mixe entre classes à nombre de colonnes fixes et variables](#3-mixe-entre-classes-à-nombre-de-colonnes-fixes-et-variables)
    - [4. Définir le nombre de colonnes sur la row](#4-définir-le-nombre-de-colonnes-sur-la-row)
    - [5. Gutters / les gouttières](#5-gutters--les-gouttières)
  - [XII. Les classes d'affichages](#xii-les-classes-daffichages)
    - [1. Notation](#1-notation)
    - [2. Cacher/Montrer des éléments en fonction de l'écran](#2-cachermontrer-des-éléments-en-fonction-de-lécran)
      - [2.1 Cacher des éléments](#21-cacher-des-éléments)
      - [2.1 Montrer des éléments](#21-montrer-des-éléments)
    - [3. Affichage lors de l'impression](#3-affichage-lors-de-limpression)
  - [XIII. Les espacements](#xiii-les-espacements)
    - [1. Les marges](#1-les-marges)
      - [a. Soit une classe du type .m{côtés}-{taille}.](#a-soit-une-classe-du-type-mcôtés-taille)
      - [b. Soit une classe du type .m{côtés}-{media}-](#b-soit-une-classe-du-type-mcôtés-media-)
    - [2. Les paddings](#2-les-paddings)
  - [XIV. Les navbars](#xiv-les-navbars)
    - [1. Introduction](#1-introduction)
    - [2. navbar dans un container ou container-fluid](#2-navbar-dans-un-container-ou-container-fluid)
    - [3. Structure](#3-structure)
    - [4. container-fluid](#4-container-fluid)
    - [5. nav](#5-nav)
      - [a. navbar-expand-lg](#a-navbar-expand-lg)
      - [b. navbar-light](#b-navbar-light)
      - [c. bg-light](#c-bg-light)
    - [6. navbar-brand](#6-navbar-brand)
      - [a. Exemple sans logo:](#a-exemple-sans-logo)
      - [b. Exemple avec logo:](#b-exemple-avec-logo)
    - [Exemple complet](#exemple-complet)
    - [4. navbar-light ou navbar-dark](#4-navbar-light-ou-navbar-dark)
  - [XIV Les formulaires](#xiv-les-formulaires)
    - [1. classe form-label](#1-classe-form-label)
    - [2. classe form-control](#2-classe-form-control)
    - [3. form-select](#3-form-select)
    - [4. required](#4-required)
    - [5. disabled](#5-disabled)
    - [6. form-floating](#6-form-floating)
    - [7. Marges](#7-marges)
    - [8. Classes btn et btn-primary](#8-classes-btn-et-btn-primary)
    - [9. Layout avec le système de grille](#9-layout-avec-le-système-de-grille)

<!-- /code_chunk_output -->



## I. A propos

Ce document contient les notes de cours sur Bootstrap. Il est difficile de voir tout Bootstrap. En effet, généralement Bootstrap consiste dans l'application d'une multitude de classes. On consulte la documentation concernant l'aspect que l'on veut avoir des informations. C'est pourquoi, ici je verrai Bootstrap dans les grandes lignes. Mais pas dans les détails car nous n'avons pas le temps.

<!-- De plus, il est complémentaire au site http://eqla.ddns.net que je vous invite à visiter.-->

## II. Prérequis

Pour aborder Bootstrap les prérequis suivants sont nécessaires :
- HTML
- CSS
- Un peu de JS pour certains composants.

En effet, Bootstrap étant un Framework basé sur la présentation, les notions de class et id sur des balises sont nécessaires.

Petit rappel : Quelle est la différence entre les attributs id et class ?

Tous les deux se trouvent sur des balises HTML.
- id : cet attribut doit être unique. Il peut être utilisé pour appliquer un style très précis à une balise.
- class : n’a pas la prétention d’être unique mais peut l’être. Il est utilisé pour appliquer un même style à différentes balises.

L’utilisation des class dans Bootstrap est omniprésente donc il est important de bien comprendre ce qu’est un attribut.

De plus, il est très courant de savoir qu’un élément puisse avoir plusieurs classes. Et dans Bootstrap c’est monnaie courante d’ajouter plusieurs classes à un élément.

## III. Présentation de Bootstrap

### 1. Brainstorming : Qu’est-ce que Bootstrap pour vous ?

On commence par demander aux stagiaires ce qu’est Bootstrap ? Quels sont ses intérêts ?

### 2. Brève présentation de Bootstrap

Bootstrap est le Framework CSS le plus célèbre au monde. Il fournit une liste d’outils qui permet de simplifier le design de sites internet. L’adresse officielle est https://getbootstrap.com/

C’est un ensemble qui contient des boutons, des formulaires, des outils de navigations, une typographie et divers composants. 

Il est dit « Responsive » ou « Responsive Web Design » : permet la consultation confortable sur des écrans de différentes tailles. Ça peut allez du desktop, smartphone, tablette, télévision, etc.

En avril 2020, il est le 7ème projet le plus populaire sur GitHub.

### 3. Pourquoi utiliser Bootstrap ?

Il n’est pas obligatoire de l’utiliser mais il peut vous faire gagner pas mal de temps dans certaines situations. Il permet d’avoir une certaine cohérence graphique pour les sites.  Il est possible de trouver des thèmes gratuits et payants.

Les avantages d’utiliser Bootstrap sont les suivants :
- Gain de temps en développement.
- Cohérence dans le design de votre site.
- Pensé Mobile First : Android, IOS, Windows 10 mobile.
- Compatible à la majorité des navigateurs : tous les navigateurs. Sauf IE pour Bootstrap 5.x
- Responsive.
- Open Source.
### 4. Bootstrap 4.x et Bootstrap 5

En ce moment, février 2021, nous sommes au moment où Bootstrap 5 va bientôt pointer le bout de son nez. Il est toujours en phase béta. Comme la version 4.x est la plus déployée, je pense qu’il est plus intéressant pour vous de voir la version 4.x qui est la plus installée et utilisée.

La version 4.x dépend de la librairie JavaScript jQuery qui doit impérativement être chargée avant le fichier JavaScript de Bootstrap.

Mais le passage à Bootstrap 5 ne devrait pas être trop difficile normalement. De plus Bootstrap 5 va se libérer de sa dépendance à jQuery et fera du pur JavaScript (appelé parfois Vanilla JS).

En octobre 2023, la version 5.3 est la dernière version de Bootstrap. Et comme dit précédemment, elle se libère de sa dépendance avec jQuery. Cependant, il ne vous est pas interdit d'utiliser jQuery.

Si vous devez continuer de supporter Internet Explorer alors vous devrez vous tourner vers Bootstrap 4. Car Internet Explorer n'est plus supporté depuis la version 5. Sachez que maintenant, Microsoft Edge (basé sur Chromium) est le nouveau navigateur de Microsoft. Et c'est une bénédiction pour les développeurs. :-) 

### 5. Comment Utiliser Bootstrap ?

Bootstrap est un Framework qui est composé d’un ensemble de fichiers. Pour utiliser Bootstrap, il nous faut donc utiliser des fichiers que vous pourrez trouver à cette adresse : https://getbootstrap.com/docs/5.3/getting-started/download/#cdn-via-jsdelivr

Il y a deux manières d’utiliser ces fichiers :

- Soit vous les téléchargez (1 fichier CSS et 1 ou 2 fichiers JS) sur le site Bootstrap. Et vous ajoutez le lien dans votre HTML. Vous voyez que j’ai mis 1 ou 2 fichiers JS :
    - 2 fichiers JavaScript :
        - L’un pour Popper.js qui permet d’avoir des Tooltips (info-bulles) sur des éléments de votre page. Donnant un bel effet.
        - L’autre pour le JavaScript de Bootstrap.
    - 1 fichier JavaScript : c’est un bundle (un paquet) qui contient Popper et Bootstrap. (C'est celui que je prends personnellement)
- Soit vous utilisez des adresses qui pointent sur ce qu’on appelle des CDN(Content Delivery Network). L’avantage des CDN c’est qu’ils sont super rapides mais si vous voulez les utiliser, vous devez ajouter l’attribut integrity pour vérifier que c’est le code javascript que vous voulez et qu’il n’a pas été remplacé par un hacker. Les navigateurs modernes vérifieront grâce à la valeur mise pour l’attribut integrity qu’il s’agit bien du fichier que vous voulez.
    
Cependant, avec Bootstrap 4.x et versions antérieures, il est impératif d’ajouter la librairie JavaScript jQuery. Elle doit être chargée avant les fichiers JavaScript Popperet Bootstrap. C’est-à-dire que dans votre page HTML vous mettrez la balise \<javascript\> de jQuery avant celles de Popper et de Bootstrap. Le cas échéant, Bootstrap ne fonctionnera pas. 

C’est pourquoi Bootstrap 5 n’utilise plus jQuery. Le JavaScript moderne permet de s’en affranchir.

Vous aurez des exemples d’intégration à la page suivante : https://getbootstrap.com/docs/5.3/getting-started/introduction/

Pour vous simplifier la tâche, j’ai créé dans le répertoire [Exercices/Templates](/Exercices/Templates/) deux fichiers html modèles pour commencer vos exercices. Ils se nomment [template1.html](/Exercices/Templates/template1.html) et [template2.html](/Exercices/Templates/template2.html). Ils comprennent les ressources nécessaires qui pointent sur des CDN. Maintenant, libre à vous de l’utiliser ou non. Mais ça vous fera gagner du temps.

Dans ces fichiers, j’ai fait pointer vers la dernière version 5.3 de Bootstrap. De plus, j’ai ajouté un fichier CSS supplémentaire (Icônes Bootstrap) que nous discuterons plus tard mais comme ça nous avons notre page web modèle Bootstrap déjà prête pour cela.

La différence entre [template1.html](/Exercices/Templates/template1.html) et [template2.html](/Exercices/Templates/template2.html).html, c'est que [template2.html](/Exercices/Templates/template2.html) comprend le \<div class="container"> juste après la balise \<body>.

## IV. Intégration des Fichiers Bootstrap
Sur le site Bootstrap : https://getbootstrap.com/docs/5.3/getting-started/introduction/

Nous allons le faire depuis l'[exercice n°1](/Exercices/Exercice1.md "Exercice sur l'intégration des fichiers Bootstrap: css et js").

## V. Fonctionnement de Bootstrap

Sur le site Bootstrap : https://getbootstrap.com/docs/5.3/getting-started/introduction/
Bootstrap fonctionne principalement avec l’utilisation de [classes css](https://developer.mozilla.org/fr/docs/Web/CSS/Class_selectors "Sélecteurs de classe sur Mozilla"). Il faut savoir que le fichier CSS de Bootstrap quand il n’est pas minifié (ramené sur une ligne pour qu’il prenne moins de place) fait 10400 lignes… Il n’est pas nécessaire de connaître par cœur toutes les classes. Personnellement j’utilise le site principal et Google.

### La classe .container
La première classe que l’on va utiliser est la classe [.container](https://getbootstrap.com/docs/5.3/layout/containers/ "Les classes containers sur Bootstrap") que l’on applique à un div. Elle permettra d’adapter la largeur du div en fonction de la résolution de l’écran du périphérique utilisé. Elle effectue aussi un léger padding gauche et droit.

J'utilise la notation .container (point container) que c'est une classe définie dans le fichier css de Bootstrap. Mais son utilisation avec l'attribut class d'une balise se fera sans ce point.

Exemple :
```html
<body>
    <div class= "container">
        <h1>Hello, World !</h1>
        <p>
            <span class="fw-bold">Le Lorem Ipsum</span> est simplement du faux
                texte employé dans la composition et la mise en page avant impression. Le
                Lorem Ipsum est le faux texte standard de l'imprimerie depuis les années
                1500, quand un imprimeur anonyme assembla ensemble des morceaux de texte 
                pour réaliser un livre spécimen de polices de texte. Il n'a pas fait que 
                survivre cinq siècles, mais s'est aussi adapté à la bureautique 
                informatique, sans que son contenu n'en soit modifié. Il a été popularisé 
                dans les années 1960 grâce à la vente de feuilles Letraset contenant des 
                passages du Lorem Ipsum, et, plus récemment, par son inclusion dans des 
                applications de mise en page de texte, comme AldusPageMaker.
        </p>
    </div>
</body>
```
Si l’on regarde le CSS de Bootstrap, on voit que dès que l’on utilise la classe .container, que tout va s’adapter.

Regardons rapidement ce CSS pour la classe .container On voit que tout changera automatiquement en fonction du média utilisé. Vous pouvez en même temps voir qu’il y a d’autres classes .container, .container-fluid, etc

```css
.container,
.container-fluid,
.container-lg,
.container-md,
.container-sm,
.container-xl,
.container-xxl {
  --bs-gutter-x: 1.5rem;
  --bs-gutter-y: 0;
  width: 100%;
  padding-right: calc(var(--bs-gutter-x) * 0.5);
  padding-left: calc(var(--bs-gutter-x) * 0.5);
  margin-right: auto;
  margin-left: auto;
}

@media (min-width: 576px) {
  .container,
  .container-sm {
    max-width: 540px;
  }
}
@media (min-width: 768px) {
  .container,
  .container-md,
  .container-sm {
    max-width: 720px;
  }
}
@media (min-width: 992px) {
  .container,
  .container-lg,
  .container-md,
  .container-sm {
    max-width: 960px;
  }
}
@media (min-width: 1200px) {
  .container,
  .container-lg,
  .container-md,
  .container-sm,
  .container-xl {
    max-width: 1140px;
  }
}
@media (min-width: 1400px) {
  .container,
  .container-lg,
  .container-md,
  .container-sm,
  .container-xl,
  .container-xxl {
    max-width: 1320px;
  }
}
```
.container agit différemment en fonction des résolutions des périphériques (d’après l’analyse du morceau de CSS mis plus haut) :  
- Cas n°1 : résolution inférieure à 576 pixels => 100% de l’écran
- Cas n°2 : résolution supérieure ou égale à 576 pixels et inférieure à 768 pixels, l’élément s’affichera au centre de l’écran et sa largeur sera de 540 pixels.
- Cas n°3 : résolution supérieure ou égale à 768 pixels et inférieure à 992 pixels, l’élément s’affichera au centre de l’écran et sa largeur sera de 720 pixels.
- Cas n°4 : résolution supérieure ou égale à 992 pixels et inférieure à 1200 pixels, l’élément s’affichera au centre de l’écran et sa largeur sera de 960 pixels.
- Cas n°5 : résolution supérieure ou égale à 1200 pixels et inférieure à 1140 pixels, l’élément s’affichera au centre de l’écran et sa largeur sera de 1320 pixels.
- Cas n°6 (nouveau Bootstrap 5) : résolution supérieure ou égale à 1400 pixels et inférieure à 1320 pixels, l'élément s'affichera au centre de l'écran et sa largeur sera de 1320 pixels.

### La classe .container-fluid
.container-fluid permet d’utiliser 100% de la taille de votre écran et n’est pas fixée comme l’est .container.

Cependant, avec la classe .container, comme nous l’avons vu plus haut au cas n°1, si l’écran est inférieur à 576 pixels alors 100% sera utilisé comme .container-fluid.

Reprenons l’exemple précédent avec .container-fluid
```html
<body>
    <div class= "container-fluid">
        <h1>Hello, World !</h1>
        <p>
            <span class="fw-bold">Le Lorem Ipsum</span> est simplement du faux
             texte employé dans la composition et la mise en page avant impression. Le
             Lorem Ipsum est le faux texte standard de l'imprimerie depuis les années
             1500, quand un imprimeur anonyme assembla ensemble des morceaux de texte 
             pour réaliser un livre spécimen de polices de texte. Il n'a pas fait que 
             survivre cinq siècles, mais s'est aussi adapté à la bureautique 
             informatique, sans que son contenu n'en soit modifié. Il a été popularisé 
             dans les années 1960 grâce à la vente de feuilles Letraset contenant des 
             passages du Lorem Ipsum, et, plus récemment, par son inclusion dans des 
             applications de mise en page de texte, comme AldusPageMaker.
        </p>
    </div>
</body>
```
Si vous en avez la possibilité, comparez le résultat de la page sur un smartphone et un ordinateur de bureau. Ou encore, jouez sur la largeur du navigateur sur votre desktop, la largeur s’auto adapte.

Passons à la pratique avec l'[exercice n°2](/Exercices/Exercice2.md "Exercice sur l'utilisation de la classe container").
    
## VI. Manipulation du texte

Sur le site Bootstrap : https://getbootstrap.com/docs/5.3/utilities/text/
### 1. Alignement du texte

- La classe .text-start (en bs4 .text-left)
Elle permet d’aligner à gauche votre texte.

- La classe .text-center
Elle permet de centrer le texte.

- La classe .text-end (en bs4 .text-right)
Elle permet d’aligner à droite votre texte.

Exemples:
```html
<p class="text-start">Le texte est aligné à gauche sur tout type d'écran.</p>
<p class="text-center">Le texte est centré sur tout type d'écran.</p>
<p class="text-end">Le texte est aligné à droite sur tout type d'écran.</p>
```

- La classe .text-justify
Elle n'existe plus dans Bootstrap 5. Elle permettait de justifier le texte. La raison de Bootstrap d'après la documentation:
> Notez que nous ne fournissons pas de classes utilitaires pour le texte justifié. Bien que, d'un point de vue esthétique, un texte justifié puisse sembler plus attrayant, il rend l'espacement des mots plus aléatoire et donc plus difficile à lire.

Si maintenant, vous voudriez avoir à nouveau la classe text-justify, ajoutez soit dans le head de votre page ou mieux dans un fichier css, le code suivant:
```css
.text-justify {
    text-align: justify!important
}
```
Pour info, j'ai simplement copié le code du fichier css de Bootstrap 4. ;)

### 2. Alignement du texte fonction de l’écran

Des abréviations peuvent s’ajouter à certaines classes pour conditionner l’action en fonction de l’écran.
- sm (small) :résolution supérieure ou égale à 576 pixels et inférieure à 768 pixels.
- md (medium): résolution supérieure ou égale à 768 pixels et inférieure à 992 pixels. 
- lg (large): résolution supérieure ou égale à 992 pixels et inférieure à 1200 pixels
- xl (extra large): résolution supérieure ou égale à 1200 pixels.
- xxl (extra extra large): résolution supérieure ou égale à 1400 pixels.


Dans la littérature Bootstrap on voit souvent l’utilisation du caractère * pour certaines classes. Ça veut dire qu’il le faut remplacer par une valeur numérique ou du texte.

Exemples :
    .text-\*-start : .text-xl-start (mets à gauche pour une résolution à partir de xl)
    .text-\*-center : .text-md-center (centre pour résolution à partir de md)
    .text-\*-end : .text-sm-end (mets à droite pour une résolution à partir de sm)

### 3. Les classes de mise en forme

Dans les exemples suivants on va souvent utiliser le préfixe fw-* pour font weight.
En fait, il correspond en css à la propriété [font-weight](https://developer.mozilla.org/fr/docs/Web/CSS/font-weight "font-weight sur Mozilla"). Font-weight définit la finesse ou l'épaisseur d'une police.

La classe .fw-bold: met en gras.
La classe .fw-bolder: met en plus gras.
La classe .fw-normal: met le texte normal.
La classe .fw-light: met dans une font claire (en fait la police est plus fine)
La classe .fw-lighter: met dans une font encore plus claire (encore plus fine).

Exemples:
```html
<p class="fw-bold">Je suis en gras</p>
<p class="fw-bolder">Je suis plus gras que le paragraphe précédent</p>
<p class="fw-light">Je suis en light</p>
<p class="fw-lighter">Je suis en lighter</p>
```

Pour mettre en italic on va utiliser le préfixe fst-* pour font style. Il correspond en css à la propriété [font-style](https://developer.mozilla.org/fr/docs/Web/CSS/font-style "font-style sur Mozilla").

La classe .fst-italic: met le texte en italic.
La classe .fst-normal: met le texte en normal. 

### 4. Transformation du texte
La classe .text-lowercase: texte converti en minuscules.
La classe .text-uppercase: TEXTE CONVERTI EN MAJUSCULES.
La classe .text-capitalize: Première Lettre De Chaque Mot Est En Majuscule.

Exemples :
```html
<p>.text-lowercase: <span class="text-lowercase">TEXTE CONVERTI EN MINUSCULES </span>.</p>
<p>.text-uppercase: <span class="text-uppercase">texte converti en majuscules</span>.</p>
<p>.text-capitalize: <span class="text-capitalize">première lettre de chaque mot est en majuscule.</span></p>
```
Résultat:
```
texte converti en minuscules.
TEXTE CONVERTI EN MAJUSCULES.
Première Lettre De Chaque Mot Est En Majuscule.
```
Passons à la pratique avec l'[exercice n°3](/Exercices/Exercice3.md "Exercice sur la manipulation du texte").


## VII. Les images
Sur le site Bootstrap : https://getbootstrap.com/docs/5.3/content/images/
Nous allons voir que Bootstrap permet de facilement rendre une image responsive, en faire une jolie vignette, aligner celle-ci.

Évidemment toutes ces classes peuvent être combinées entre elles.

### 1. Responsive
Bootstrap permet de rapidement permettre à une image d’être responsive. Ajouter la classe .img-fluid et votre image va s’auto-adapter en fonction de l’écran. 
```html
<img src="https://zamboyle.github.io/Cours/2022/Bootstrap/Exercices/Images/Logo_Eqla.png" class="img-fluid" alt="logo d'Eqla" width="10000px"  />
```
Ici on a ajouté l’attribut width="10000px". L’image ne fera bien sûr jamais 10000 pixels. Bootstrap veille au grain. 😊 
### 2. Thumbnail
La classe .img-thumbnail ajoute à l’image un bord blanc arrondi. Si vous utilisez cette classe, vous n'avez pas besoin d'utilisez la classe .img-fluid. En effet, .img-thumbnail rend l'image responsive.
```html
<img src="https://zamboyle.github.io/Cours/2022/Bootstrap/Exercices/Images/Paris.jpg" class="img-thumbnail" alt="Image de paris" />
```
### 3. Alignement
Permet de mettre des images à gauche .float-start ou à droite .float-end quel que soit la taille de l’écran.
```html
<img src="https://zamboyle.github.io/assets/img/Logo_Eqla.png" class="img-fluid float-start" alt="logo d'Eqla" />
<img src="https://zamboyle.github.io/assets/img/Paris.jpg" class="img-fluid img-thumbnail float-end" alt="Image de paris" />
```
On peut aussi définir ces alignements en fonction du périphérique :.float-\*-start ou .float-\*-end où * peut avoir différentes valeurs.
- sm : small
- md : medium
- lg : large
- xl : extra-large
- xxl: extra extra-large

### 4. Images aux bords arrondis
Il suffit d'utiliser la classe .rounded

```html
<img class="img-fluid rounded" src="https://zamboyle.github.io/assets/img/Logo_Eqla.png" alt="logo d'Eqla" />
```

## VIII. L'Accessibilité
Sur le site Bootstrap : https://getbootstrap.com/docs/5.3/getting-started/accessibility/
Bootstrap fournit différentes classes permettant à des messages d'être lues seulement pour les utilisateurs de lecteurs d'écran.

Bootstrap fournit aussi des classes permettant de réduire certaines de ses animations: transition, ouverture, d'une fenêtre modale, etc.

### 1. Lecteur d'écran
La classe <code>.visually-hidden</code> permet d'afficher des messages lisibles uniquement par un lecteur d'écran.  

Dans l'exemple suivant, le texte ne sera jamais affiché mais lu par les lecteurs d'écran:
``` html
<p class="text-danger">
    <span class="visually-hidden">Danger: </span>
    Cette action est irréversible !
</p>
```
La classe <code>.visually-hidden-focusable</code>, à utiliser avec la balise a, permet de mettre le focus et d'afficher le texte du lien même s'il est caché: via les tabulations.

Exemple:
```html
<a class="visually-hidden-focusable" href="#content">Je suis un lien d'évitement</a>
```

### 2. Animation réduite
Bootstrap permet de diminuer un maximum ses animations si <code>prefers-reduced-motion</code> est activé. Cela s'active de différentes manières.

Voici comment faire (en anglais):
> - In GTK/GNOME: GNOME Tweaks > General tab (or Appearance, depending on version) > Animations is turned off.
> Alternatively, add gtk-enable-animations = false to the [Settings] block of the GTK 3 configuration file.
> - In Plasma/KDE: System Settings > Workspace Behavior -> General Behavior > “Animation speed” is set all the way to right to “Instant”.
> - In Windows 10: Settings > Ease of Access > Display > Show animations in Windows.
> - In Windows 11: Settings > Accessibility > Visual Effects > Animation Effects
> - In Windows 7: Control Panel > Ease of Access > Make the computer easier to see > Turn off all unnecessary animations (when possible).
> - In macOS: System Preferences > Accessibility > Display > Reduce motion.
> - In iOS: Settings > General > Accessibility > Reduce Motion.
> - In Android 9+: Settings > Accessibility > Remove animations.
> - In Firefox about:config: Add a number preference called ui.prefersReducedMotion and set its value to either 0 for full animation or to 1 to indicate a preference for reduced motion. Changes to this preference take effect immediately.

En effet, en termes d'accessibilité, il vaut mieux éviter les animations.

## IX. Les breakpoints
Sur Bootstrap: https://getbootstrap.com/docs/5.3/layout/breakpoints/

Comme nous l'avons déjà vu il existe différents breakpoints (points d'arrêt) que nous avons déjà utilisés et vu dans le fichier css de Bootstrap.

En voici le résumé car vous me l'avez souvent demandé.;-)

|Breakpoint|	Class infixe |	Dimensions|
|---|---|---|
|Extra small	|xs|	<576px
|Small|	sm|	≥576px
|Medium|	md|	≥768px
|Large|	lg|	≥992px
|Extra large|	xl|	≥1200px
|Extra extra large|	xxl|	≥1400px

## X. Les couleurs & Couleurs d'Arrière Plan.

Ce chapitre est une synthèse des deux pages Bootstrap 5:
- [Colors](https://getbootstrap.com/docs/5.3/utilities/colors/)
- [Background](https://getbootstrap.com/docs/5.3/utilities/background/)

Comme GitHub ne va pas interprêter nos couleurs, j'ai fait une page web qui vous montrera visuellement les couleurs que Bootstrap gère.  

Pour avoir un visuel de cette partie, allez à la page [suivante](http://zamboyle.github.io/htmlpreview?https://github.com/ZamBoyle/Eqla_Bootstrap5/blob/master/Theorie/Exemples/couleurs.html).

## XI. La Grille Bootstrap

Sur le site Bootstrap : https://getbootstrap.com/docs/5.3/layout/grid/

Et voici des exemples: [ici](http://zamboyle.github.io/htmlpreview?https://github.com/ZamBoyle/Eqla_Bootstrap5/blob/master/Theorie/Exemples/grid.html)

Visualisation des exemples de la théorie: [ici](http://zamboyle.github.io/htmlpreview?https://github.com/ZamBoyle/Eqla_Bootstrap5/blob/master/Theorie/Exemples/grid2.html)

Bootstrap propose un système de grille très pratique et responsive. Elle permet d’agencer des contenus sous formes de colonnes. 

Cette grille est composée d’une ligne de 12 colonnes. On pourrait penser que c’est un tableau. Si on veut mais alors d’une seule ligne. Ce système de grille permet d’ajouter des éléments sous formes de colonnes.

Et comme vous le savez maintenant, utilisez Bootstrap, c’est utiliser ses classes. 

On utilise toujours un div conteneur ayant la classe .row. 

Les divs enfants seront les colonnes et auront une ou plusieurs classes.

###	1. Classes pour un nombre fixe de colonnes

- Les classes .col-* où * est  un nombre de 1 à 12. Quand on veut absolument un nombre défini de colonnes quel que soit la résolution. Dans ce cas, vous aurez toujours le nombre de colonnes désirés.
  Exemple où le nombre de colonnes est fixe par ligne (un .col-4et .col-8 = 4 colonnes + 8 colonnes = 12 colonnes) :
```html
<div class="row">
	<div class="col-4">
 	Première colonne avec un .col-4
  </div>
  <div class="col-8">
  Deuxième colonne avec un .col-8
  </div>
</div>
```
Ensuite, les combinaisons sont comme vous le voulez : Par exemple 3 .col-4 et vous aurez 3 colonnes. En effet, 3 x 4 colonnes = 12colonnes , 2 .col-6 = 2 x 6 colonnes =12 colonnes,1 .col-2 et 1 .col-4+ et 1 .col-6 = 12 etc.

- La classe .colpeut tout simplement être utilisée si vos colonnes ont exactement la même taille. Donc on pourrait avoir deux colonnes avec .col au lieu de .col-6 Ce qui veut dire que nous aurons deux colonnes quel que soit la résolution.
Exemple :
```html
<div class="row">
  <div class="col">
 	Première colonne avec un .col
  </div>
  <div class="col">
    Deuxième colonne avec un .col
  </div>
  </div>
  Est identique à 
  <div class="row">
    <div class="col-6">
    Première colonne avec un .col-6
  </div>
  <div class="col-6">
    Deuxième colonne avec un .col-6
  </div>
  </div>
  On peut un peu complexifier en faisant un .col avec un .col-3. Ici notre .col sera équivalent à un .col-9
  <div class="row">
    <div class="col">
    Ceci est un texte assez répétitif. Ceci est un texte assez répétitif.
  </div>
  <div class="col-3">
    Ceci est un texte assez répétitif. Ceci est un texte assez répétitif
  </div>
</div>
```
### 2. Classes pour un nombre de colonnes variables en fonction de la résolution
Nous venons de voir les classes pour un nombre fixe de colonnes. C’est top quand on veut absolument avoir ce nombre de colonnes.

Mais sachez que plus la résolution est petite et plus vos colonnes seront étroites. En effet, la lecture dans des colonnes si étroites n’est pas aisé.

Pour pallier à ce problème, Bootstrap propose de conditionner nos colonnes en fonction de la résolution.

Si cette résolution n’est pas atteinte alors au lieu de mettre les colonnes les une à côté des autres, ils les mettra les une au-dessus des autres.

Les classes à utiliser seront : 
- .col-*  où * est un nombre compris entre 1 et 12 (< 576 pixels) prendra automatiquement toute la largeur.
-	.col-sm-* où * est un nombre compris entre 1 et 12 (sm>= 576 pixels)
-	.col-md-* où * est un nombre compris entre 1 et 12 (md >= 768 pixels)
-	.col-lg-* où * est un nombre compris entre 1 et 12 (lg >= 992 pixels)
-	.col-xl-* où * est un nombre compris entre 1 et 12 (xl >= 1200 pixels)
- .col-xxl-* où * est un nombre compris entre 1 et 12 (xl >= 1400px pixels)

Par exemple si on a deux colonnes ayant chacune comme classe un .col-sm-6
```html
<div class="row">
	<div class="col-sm-4">
	Première colonne avec un .col-sm-4
	</div>
	<div class="col-sm-6">
	Ceci est la deuxième colonne avec un .col-sm-6
	</div>
</div>
```
Ça signifie qu’il faut afficher deux colonnes si on a une résolution d’au moins (576 pixels). Dans le cas contraire, Bootstrap affichera la première colonne et la seconde ira à la ligne. Et la lecture sera aisée sur un petit écran.

### 3.	Mixe entre classes à nombre de colonnes fixes et variables
Prenons un cas concret, vous souhaitez afficher 3 colonnes si la résolution le permet (md). Dans le cas contraire, vous afficher la première colonne sur une ligne et les deux autres sur la seconde.
Pour cela, vous aurez le html suivant
```html
<h1>.col et .col-3</h1>
<div class="row text-white">
  <div class="col-12 col-md-4 bg-success">Je suis votre prof !</div>
  <div class="col-6 col-md-4 bg-warning">Bientôt, je ne serai plus votre prof !</div>
  <div class="col-6 col-md-4 bg-danger">Je ne suis plus votre prof !</div>
</div>
```
Expliquons-le petit à petit :
-	.col-12 col-md-4 : la colonne fera le 1/3 de l’écran si la résolution est supérieure ou égale à md. Dans le cas contraire, la colonne prendra toute la ligne (.col-12).
-	.col-6 col-md-4 : la seconde colonne fera le 1/3 (même raison). Dans le cas contraire, la colonne prendra la moitié de l’écran (.col-6).
-	.col-6 col-md-4 : idem que précédemment mais sera à côté de la colonne précédente si résolution inférieure à md.
Donc si la résolution est > = md, on aura 3 colonnes identiques (.col-md-4). Dans le cas contraire, on aura une colonne qui prendra toute une ligne (.col-12)>. Et sur une autre ligne, nous aurons deux colonnes identiques (.col-6) qui prendront toute la ligne.

### 4. Définir le nombre de colonnes sur la row
Il est possible de définir le nombre de colonnes sur une ligne. Pour cela, il faut utiliser la classe .row-cols-* où * est un nombre compris entre 1 et 12.

On peut aussi jouer sur la résolution avec les classes .row-cols-sm-*, .row-cols-md-*, .row-cols-lg-*, .row-cols-xl-*, .row-cols-xxl-*.

Exemple:
```html
<div class="row row-cols-2 row-cols-lg-5 g-2 g-lg-3">
    <div class="col">
        <div class="border border-primary p-3">🚀 Fusée rapide</div>
    </div>
    <div class="col">
        <div class="border border-primary p-3">🍕 Pizza délicieuse</div>
    </div>
    <div class="col">
        <div class="border border-primary p-3">🐱 Chat curieux</div>
    </div>
    <div class="col">
        <div class="border border-primary p-3">🎸 Guitare rock</div>
    </div>
    <div class="col">
        <div class="border border-primary p-3">☕ Café chaud</div>
    </div>
    <div class="col">
        <div class="border border-primary p-3">🌍 Globe terrestre</div>
    </div>
    <div class="col">
        <div class="border border-primary p-3">🎨 Palette artistique</div>
    </div>
    <div class="col">
        <div class="border border-primary p-3">🎮 Manette de jeu</div>
    </div>
    <div class="col">
        <div class="border border-primary p-3">🌵 Cactus solitaire</div>
    </div>
    <div class="col">
        <div class="border border-primary p-3">📘 Livre passionnant</div>
    </div>
</div>
```
Dans cet exemple, on a 5 colonnes par ligne pour une résolution supérieure ou égale à lg. Dans le cas contraire, on aura 2 colonnes par ligne.

### 5. Gutters / les gouttières
Les gouttières sont les espaces entre les colonnes. Par défaut, Bootstrap met un espace de 1.5rem (24px) entre les colonnes. Cet espace est géré par la classe .gutter-* où * est un nombre compris entre 0 et 5.


## XII. Les classes d'affichages
Sur Bootstrap: https://getbootstrap.com/docs/5.3/utilities/display
Reprenons le synopsis de la page de Bootstrap traduite avec Google Translate bien entendu ;-)
> Basculez rapidement et de manière réactive la valeur d'affichage des composants et plus encore avec nos utilitaires d'affichage. Inclut la prise en charge de certaines des valeurs les plus courantes, ainsi que des extras pour contrôler l'affichage lors de l'impression.

On voit donc qu'il est possible de gérer de manière responsive l'affichage au sens large comprenant aussi l'impression sur une imprimante.

Nous allons voir avec quelles classes car évidemment tout se passe dans des classes avec Bootstrap. ;-)

### 1. Notation
Les classes s'écrivent de la manière suivante:
- <code>.d-{value}</code>
- <code>.d-{breakpoint}-{value}</code> for sm, md, lg, xl, xxl

Les valeurs peuvent être les suivantes:
- none
- inline
- inline-block
- block
- grid
- table
- table-cell
- table-row
- flex
- inline-flex

Nous allons nous attarder uniquement sur les valeurs: none, inline, block et inline-block.

En css, cela correspond à respectivement:

|css| Explication|
|---|---|
|display: none; | - N'affiche pas l'élément. <br/> - Il est invisible mais présent dans le code html.|
|display: inline; |- S'affiche à la suite sur une ligne.<br/> - La hauteur et la largeur ne sont pas variables.<br/>- Ne pousse pas l'élément suivant à la ligne suivante.|
|display: block;|- S'affiche sur une ligne.<br/>- Pousse les élèments sur la ligne suivante.<br/> - La hauteur et la largeur sont variables/définissables.|
|display: inline-block.| - Peut pas être seul sur la ligne. <br/> - Ne pousse pas les éléments à la ligne suivante. <br/> - La hauteur et la largeur sont variables/définissables.|


Le résultat d'affichage des exemples précédents peut être vu à cette [page](http://zamboyle.github.io/htmlpreview?https://raw.githubusercontent.com/ZamBoyle/Eqla_Bootstrap5/master/Theorie/Exemples/display.html)

### 2. Cacher/Montrer des éléments en fonction de l'écran
En fonction du type d'écran, il est possible de cacher/montrer du contenu.

Exemple:
```html
<div class="d-lg-none">Caché pour les écrans lg et plus</div>
<div class="d-none d-lg-block">Caché pour les écrans plus petit que lg</div>
```

#### 2.1 Cacher des éléments
| Taille d'écran      | Class                           |
|---------------------|---------------------------------|
| Caché pour tout     | .d-none                         |
| Caché seulement sur xs   | .d-none .d-sm-block             |
| Caché seulement sur sm   | .d-sm-none .d-md-block          |
| Caché seulement sur md   | .d-md-none .d-lg-block          |
| Caché seulement sur lg   | .d-lg-none .d-xl-block          |
| Caché seulement sur xl   | .d-xl-none .d-xxl-block         |
| Caché seulement sur xxl  | .d-xxl-none                     |

#### 2.1 Montrer des éléments
| Taille d'écran      | Class                           |
|---------------------|---------------------------------|
| Visible pour tout      | .d-block                        |
| Visible seulement pour xs  | .d-block .d-sm-none             |
| Visible seulement pour sm  | .d-none .d-sm-block .d-md-none  |
| Visible seulement pour md  | .d-none .d-md-block .d-lg-none  |
| Visible seulement pour lg  | .d-none .d-lg-block .d-xl-none  |
| Visible seulement pour xl  | .d-none .d-xl-block .d-xxl-none |
| Visible seulement pour xxl | .d-none .d-xxl-block            |

### 3. Affichage lors de l'impression
Il est possible de conditionner l'affichage lors de l'impression d'une page.

- .d-print-none
- .d-print-inline
- .d-print-inline-block
- .d-print-block
- .d-print-grid
- .d-print-table
- .d-print-table-row
- .d-print-table-cell
- .d-print-flex
- .d-print-inline-flex

Ces différentes classes peuvent être combinées.

Exemple:
```html
<div class="d-print-none">S'affichera uniquement sur écran et sera caché lors de l'impression.</div>
<div class="d-none d-print-block">S'affichera uniquement lors de l'impression et sera caché à l'écran.</div>
<div class="d-none d-lg-block d-print-block">Caché jusqu'à un écran large mais sera toujours affiché lors de l'impression.</div>
```
## XIII. Les espacements
Sur le site Bootstrap : https://getbootstrap.com/docs/5.3/utilities/spacing/

Dans Bootstrap, nous avons des classes qui permettent d’ajouter des paddings ou des marges

### 1. Les marges
Ces classes ont deux formats :
#### a. Soit une classe du type .m{côtés}-{taille}.
<!-- La taille varie de 0 à 5 (0 = 0rem, 1=0,25 rem,  2 = 0,5 rem, 3=1rem, 4 = 1,5 rem, 5 =  3 rem)
0,25 rem = 0,25 * la variable SASS $spacer qui est définie par défaut à 1rem).-->
« côtés » peut prendre les valeurs suivantes : rien, t (top), b(bottom), s (start), e (end), x (gauche et droite), y (haut et bas)
m-* : ajoutera une marge aux 4 côtés.
mt-* : ajoutera une marge en haut.
mb-* : ajoutera une marge en bas.
ms-* : ajoutera une marge à gauche.
me-* : ajoutera une marge à droite.
mx-* : ajoutera une marge à gauche et à droite.
my-* : ajoutera une marge en haut et en bas.
#### b. Soit une classe du type .m{côtés}-{media}-{taille}
« media » peut prendre une des valeurs suivantes : sm, md, lg, xl, xxl. C’est donc conditionné en fonction de la taille de l’écran du périphérique. 
Exemples : m-sm-7, mx-lg-5, etc.
### 2. Les paddings
Même principe que pour les marges. 
Donc on pourra avoir deux formes : .p{côtés}-{taille} et p{côtés}-{media}-{taille}.

Des exemples peuvent être vus à cette [page](http://zamboyle.github.io/htmlpreview?https://raw.githubusercontent.com/ZamBoyle/Eqla_Bootstrap5/master/Theorie/Exemples/spacing.html)

## XIV. Les navbars

### 1. Introduction
Sur le site Bootstrap: https://getbootstrap.com/docs/5.3/components/navbar/

Une `navbar` (barre de navigation) dans Bootstrap est typiquement utilisée pour organiser et présenter les options de navigation principales d'un site web. Elle agit comme un menu car elle permet aux utilisateurs de naviguer facilement à travers différentes sections ou pages du site.

Elle est généralement placée en haut de la page web. Elle est responsive et s'adapte à la taille de l'écran. En effet, sur un smartphone, elle sera réduite et les options de navigation seront cachées dans un menu hamburger.

En résumé, bien que la navbar puisse inclure d'autres éléments comme des logos ou des formulaires de recherche, sa fonction principale est de servir de menu de navigation et est responsive.

### 2. navbar dans un container ou container-fluid

Une navbar peut être placée dans un container ou un container-fluid. Cela dépend de l'effet que vous voulez obtenir. Si vous optez pour un container, la navbar sera centrée. Si vous optez pour un container-fluid, la navbar sera étendue sur toute la largeur de l'écran.

J'entends déjà des questions dans vos têtes:
- _On a toujours utilisé un container pour centrer notre page. Pourquoi ne pas utiliser un container pour centrer notre navbar ?_
  > En effet, nous avons toujours utilisé un container pour centrer notre page. Mais la navbar est un élément à part. Elle est généralement placée en haut de la page. Donc, il est logique de l'étendre sur toute la largeur de l'écran. C'est pour cela que nous utiliserons un container-fluid pour la navbar. Mais ce n'est pas une obligation. Vous pouvez utiliser un div avec la classe container pour la navbar et le contenu. C'est à vous de voir. 
- _On peut avoir un div avec la classe container-fluid pour la navbar et un div avec une classe container pour le contenu ?_
  > Oui, c'est possible. C'est généralement ce que je fais. 
- _On peut avoir un div avec la classe container pour la navbar et un div avec une classe container-fluid pour le contenu ?_
  > Oui, c'est possible. Mais cela dépend de l'effet que vous voulez obtenir. Si vous voulez que votre navbar soit centrée et que votre contenu soit étendu, vous pouvez utiliser une div avec la classe container pour la navbar et un container-fluid pour le contenu. Mais je trouve que ça ferait un effet un peu bizarre.  
  Je préfère utiliser un container-fluid pour la navbar et un container pour le contenu.
- _On peut avoir un div avec la classe container-fluid pour la navbar et un div avec une classe container-fluid pour le contenu ?_
  > Oui mais alors on ne fera qu'un seul container-fluid pour la navbar et le contenu.


### 3. Structure
Comme vous le savez en html, on peut avoir des balises qui en contiennent d'autres comme les poupées russes. C'est le cas de la balise `<nav>` qui peut contenir d'autres balises comme `<div>`, `<ul>`, `<li>`, etc.

L'exemple de la documentation de Bootstrap met un div avec une classe container-fluid dans un nav. Je vais le mettre avant le nav. C'est juste pour que ça soit plus facile de comprendre la structure.

Comme dit précédemment, nous pourrions avoir un div avec une classe container. Mais alors nous serions limités dans la longueur de notre menu. C'est pourquoi, on utilise la classe container-fluid.

Je vais maintenant dans les points suivants vous expliquer la structure d'une navbar. Après, nous aurons un exemple complet.

### 4. container-fluid

Le div aura la classe `.container-fluid`. Ce div contiendra la balise `nav`. Cela permettra d'étendre la navbar sur toute la largeur de l'écran. 

### 5. nav

La balise `nav` contient les éléments de la navbar. C'est elle qui va permettre de mettre en forme notre navbar. 

```html
<div class="container-fluid">
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <!-- Contenu de la navbar que nous allons voir -->
    </nav>
</div>
```


```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
    <!-- Contenu de la navbar que nous allons voir -->
</nav>
```
On constate que notre balise contient plusieurs classes. Nous allons voir à quoi elles servent.

#### a. navbar-expand-lg
La classe `navbar-expand-lg` permet de rendre la navbar responsive. En effet, sur un smartphone, la navbar sera réduite et les options de navigation seront cachées dans un menu hamburger. Dans cet exemple, lorsque la résolution est inférieure à 992 pixels, la navbar sera réduite.

#### b. navbar-light
La classe `navbar-light` permet de rendre la navbar claire. En effet, la navbar est par défaut foncée.

#### c. bg-light
La classe `bg-light` permet de rendre le fond de la navbar clair. En effet, le fond de la navbar est par défaut foncé.

### 6. navbar-brand
La classe `navbar-brand` permet de mettre un logo ou un texte dans la navbar. C'est généralement le nom du site ou le logo du site.

On applique cette classe à une balise `<a>` et comme lien, on met le lien vers la page d'accueil du site.

#### a. Exemple sans logo:
```html
<a class="navbar-brand" href="#">Navbar</a>
```

#### b. Exemple avec logo:
```html
<a class="navbar-brand" href="#">
    <img src="https://zamboyle.github.io/assets/img/Logo_Eqla.png" alt="logo d'Eqla" width="30" height="24">
</a>
```



### Exemple complet



Je vais présenter le code qui va suivre que vous pourrez consulter à cette page: [Démo navbar](http://zamboyle.github.io/htmlpreview?https://raw.githubusercontent.com/ZamBoyle/Eqla_Bootstrap5/master/Theorie/Exemples/navbar.html)

```html
<div class="container-fluid">
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <a class="navbar-brand" href="#">Navbar</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
            aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a class="nav-link active" aria-current="page" href="#">Accueil</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Fonctionalité</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Prix</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Contact</a>
                </li>
            </ul>
        </div>
    </nav>
</div>
```

### 4. navbar-light ou navbar-dark



## XIV Les formulaires
Sur le site Bootstrap: [Les formulaires](https://getbootstrap.com/docs/5.3/forms/overview/)

Pour le Hackathon, nous allons en profiter pour voir les class Bootstrap en rapport avec les formulaires.

Nous allons reprendre un formulaire que nous avons fait lors d'un exercice préparatoire au Hackathon.

```html
<form action="http://zamboyle.synology.me" method="get">
    <input id="repo" name="repo" type="hidden" value="ZamBoyle/Eqla_Hackathon">
    <input id="program" name="program" type="hidden" value="Demo.java">
    Fonction:<input id="function" name="function" type="text"><br/>
    Paramètre p1:<input id="p1" name="p1" type="text"><br/>
    Paramètre p2:<input id="p2" name="p2" type="text"><br/>
    <input type="submit" value="Envoyer">
</form>
```
Notre formulaire sera légèrement plus joli grâce à Bootstrap: champ texte et bouton plus grands.

Mais Bootstrap peut faire nettement mieux :-)  

Je vais Bootstraper ce formulaire et vous l'expliquer.

```html
<form action="http://zamboyle.synology.me" method="get">
    <input id="repo" name="repo" type="hidden" value="ZamBoyle/Eqla_Hackathon">
    <input id="program" name="program" type="hidden" value="Demo.java">
        <label for="function" class="form-label">Fonction</label>
        <select id="function" name="function" class="form-select mb-3" required>
            <option selected value="">Cliquez pour sélectionner une fonction</option>
            <option value="helloworld">helloworld ()</option>
            <option value="hi">hi (p1)</option>                    
            <option value="hola" disabled>hola (p1)</option>
            <option value="add">add (int p1, int p2)</option>
            <option value="tablemultiplication">tablemultiplication (int table, int max)</option>
            <option value="help">help ()</option>
        </select>

        <label for="p1" class="form-label">Paramètre p1</label>
        <input id="p1" name="p1" class="form-control" type="text">

        <div class="form-floating my-3">
            <input id="p2" name="p2" class="form-control" type="text" placeholder="Paramètre p2">
            <label for="p2" class="form-label">Paramètre p2</label>                    
        </div>
    <input type="submit" class="btn btn-primary" value="Envoyer">
</form>
```

Lorsque vous lancez ce formulaire avec le Framework Bootstrap, directement vous constatez que celui-ci est beaucoup plus esthétique.

Le champ text a les bords arrondis, la zone est plus grande et celle-ci devient bleue si la zone est activée.

Résultat visible à cette [adresse](http://zamboyle.github.io/htmlpreview?https://raw.githubusercontent.com/ZamBoyle/Eqla_Bootstrap5/master/Theorie/Exemples/form1.html).

### 1. classe form-label
La classe form-label est utilisée avec la balise html label avec l’attribut for= "#ControleADecrire". La valeur #ControleADecrire est l'id du contrôle sur lequel on veut mettre le label.

### 2. classe form-control
Les champs de type texte, mot de passe doivent avoir cette classe.

### 3. form-select
Elle s'utilise sur la balise html select

### 4. required
Comme nous l'avons déjà vu, l'attribut required indique que le champ est obligatoire. Le formulaire ne saura pas être transmis si le champ n'a pas de valeur.

### 5. disabled
On voit que l'attribut disabled peut être utilisé sur un des choix d'un select. Le texte apparaîtra mais ne sera pas sélectionnable. Il sera aussi légèrement grisé.


### 6. form-floating
C'est une forme de présentation du champ qui est intéressante: le label est dans le champ et quand on commence à écrire dans le champ, le label reste dans le champ et devient tout petit une fois que le champ aura le focus.

Pour cela, on va créer un div avec la classe form-floating. On va ensuite mettre le champ avec un placeholder. Et pour finir un ajoutera un label. L'ordre est important: div, input et enfin label.

### 7. Marges
Pour éviter de coller les champs on peut ajouter des marges:
- à gauche (ms-valeur): exemple ms-3  
- à droite (me-valeur): exemple me-2  
- en haut (mt-valeur): exemple mt-1  
- en bas (mb-valeur): exemple mb-2  
- en haut et en bas (my-valeur): exemple my-3  
- à gauche et à droite (mx-valeur): exemple mx-2  
- partout: m-3  
 
### 8. Classes btn et btn-primary
La classe btn transformera le bouton submit en un joli bouton Bootstrap.
Enfin, la classe btn-primary utilisera la couleur primary pour le bouton (revoir le chapitre sur les couleurs).

### 9. Layout avec le système de grille
Pour présenter autrement notre formulaire, nous pouvons aussi utiliser la [grille Bootstrap](#xi-la-grille-bootstrap) que nous avons vue précédemment.

On crée un div avec la classe .row et ensuite on avec des div ayant une des classes sur les colonnes: col, col-auto, col-2, etc.

N'oubliez pas que la grille Bootstrap est composée de 12 colonnes par ligne. Si vous dépassez les 12 colonnes, une nouvelle ligne se crée.

Exemple 1:
```html
<form action="http://zamboyle.synology.me" method="get">
    <input id="repo" name="repo" type="hidden" value="ZamBoyle/Eqla_Hackathon">
    <input id="program" name="program" type="hidden" value="Demo.java">
    <div class="row">
        <div class="col-6">
            <label for="function" class="form-label">Fonction</label>
            <select id="function" name="function" class="form-select mb-3" required>
                <option selected value="">Cliquez pour sélectionner une fonction</option>
                <option value="helloworld">helloworld ()</option>
                <option value="hi">hi (p1)</option>
                <option value="hola" disabled>hola (p1)</option>
                <option value="add">add (int p1, int p2)</option>
                <option value="tablemultiplication">tablemultiplication (int table, int max)</option>
                <option value="help">help ()</option>
            </select>
        </div>
    </div>
    <div class="row">
        <div class="col-6 mb-3">
            <input id="p1" name="p1" class="form-control col" type="text" aria-label="Paramètre p1"
                placeholder="Paramètre p1">
        </div>
        <div class="col-6">
            <input id="p2" name="p2" class="form-control col" type="text" aria-label="Paramètre p2"
                placeholder="Paramètre p2">
        </div>

        <div class="col-12 text-end">
            <input type="submit" class="btn btn-primary mt-2" value="Envoyer">
        </div>
    </div>
</form>
```
Exemple 2:

```html
<form action="http://zamboyle.synology.me" method="get">
    <input id="repo" name="repo" type="hidden" value="ZamBoyle/Eqla_Hackathon">
    <input id="program" name="program" type="hidden" value="Demo.java">
    <div class="row mb-3">
        <div class="col-sm-3">
            <label for="functionbis" class="col-form-label">Fonction</label>
        </div>
        <div class="col-sm-9">
            <select id="functionbis" name="function" class="form-select" required>
                <option selected value="">Cliquez pour sélectionner une fonction</option>
                <option value="helloworld">helloworld ()</option>
                <option value="hi">hi (p1)</option>
                <option value="hola" disabled>hola (p1)</option>
                <option value="add">add (int p1, int p2)</option>
                <option value="tablemultiplication">tablemultiplication (int table, int max)</option>
                <option value="help">help ()</option>
            </select>
        </div>
    </div>
    <div class="row mb-3">
        <div class="col-sm-3">
            <label for="p1bis" class="col-form-label">Paramètre p1</label>
        </div>
        <div class="col-sm-9">
            <input id="p1bis" name="p1" class="form-control" type="text" placeholder="Paramètre p1">
        </div>
    </div>
    <div class="row mb-3">
        <div class="col-sm-3">
            <label class="form-label" for="p2bis">Paramètre p2</label>
        </div>
        <div class="col-sm-9">
            <input id="p2bis" name="p2" class="form-control" type="text" aria-label="Paramètre p2"
                placeholder="Paramètre p2">
        </div>
    </div>
    <div class="row mb-3">
        <div class="col-12 text-end">
            <input type="submit" class="btn btn-primary mt-2" value="Envoyer">
        </div>
    </div>
</form>
```
Résultat visible à cette [adresse](http://zamboyle.github.io/htmlpreview?https://raw.githubusercontent.com/ZamBoyle/Eqla_Bootstrap5/master/Theorie/Exemples/form2.html).