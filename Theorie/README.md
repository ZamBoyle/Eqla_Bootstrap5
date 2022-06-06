# Bootstrap 5
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
- Compatible à la majorité des navigateurs : tous les navigateurs. Sauf IE pour Bootstrap 5.
- Responsive.
- Open Source.
### 4. Bootstrap 4.x et Bootstrap 5

En ce moment, février 2021, nous sommes au moment où Bootstrap 5 va bientôt pointer le bout de son nez. Il est toujours en phase béta. Comme la version 4.x est la plus déployée, je pense qu’il est plus intéressant pour vous de voir la version 4.x qui est la plus installée et utilisée.

La version 4.x dépend de la librairie JavaScript jQuery qui doit impérativement être chargée avant le fichier JavaScript de Bootstrap.

Mais le passage à Bootstrap 5 ne devrait pas être trop difficile normalement. De plus Bootstrap 5 va se libérer de sa dépendance à jQuery et fera du pur JavaScript (appelé parfois Vanilla JS).

En mai 2022, la version 5.2 est la dernière version de Bootstrap. Et comme dit précédemment, elle se libère de sa dépendance avec jQuery. Cependant, il ne vous est pas interdit d'utiliser jQuery.

Si vous devez continuer de supporter Internet Explorer alors vous devrez vous tourner vers Bootstrap 4. Car Internet Explorer n'est plus supporté depuis la version 5. Sachez que maintenant, Microsoft Edge (basé sur Chromium) est le nouveau navigateur de Microsoft. Et c'est une bénédiction pour les développeurs. :-) 

### 5. Comment Utiliser Bootstrap ?

Bootstrap est un Framework qui est composé d’un ensemble de fichiers. Pour utiliser Bootstrap, il nous faut donc utiliser des fichiers que vous pourrez trouver à cette adresse : https://getbootstrap.com/docs/5.2/getting-started/download/

Il y a deux manières d’utiliser ces fichiers :

- Soit vous les téléchargez (1 fichier CSS et 1 ou 2 fichiers JS) sur le site Bootstrap. Et vous ajoutez le lien dans votre HTML. Vous voyez que j’ai mis 1 ou 2 fichiers JS :
    - 2 fichiers JavaScript :
        - L’un pour Popper.js qui permet d’avoir des Tooltips (info-bulles) sur des éléments de votre page. Donnant un bel effet.
        - L’autre pour le JavaScript de Bootstrap.
    - 1 fichier JavaScript : c’est un bundle (un paquet) qui contient Popper et Bootstrap. (C'est celui que je prends personnellement)
- Soit vous utilisez des adresses qui pointent sur ce qu’on appelle des CDN(Content Delivery Network). L’avantage des CDN c’est qu’ils sont super rapides mais si vous voulez les utiliser, vous devez ajouter l’attribut integrity pour vérifier que c’est le code javascript que vous voulez et qu’il n’a pas été remplacé par un hacker. Les navigateurs modernes vérifieront grâce à la valeur mise pour l’attribut integrity qu’il s’agit bien du fichier que vous voulez.
    
Cependant, avec Bootstrap 4.x et versions antérieures, il est impératif d’ajouter la librairie JavaScript jQuery. Elle doit être chargée avant les fichiers JavaScript Popperet Bootstrap. C’est-à-dire que dans votre page HTML vous mettrez la balise \<javascript> de jQuery avant celles de Popper et de Bootstrap. Le cas échéant, Bootstrap ne fonctionnera pas. 

C’est pourquoi Bootstrap 5 n’utilise plus jQuery. Le JavaScript moderne permet de s’en affranchir.

Vous aurez des exemples d’intégration à la page suivante : https://getbootstrap.com/docs/5.2/getting-started/introduction/

Pour vous simplifier la tâche, j’ai créé dans le répertoire [Exercices/Templates](/Exercices/Templates/) deux fichiers html modèles pour commencer vos exercices. Ils se nomment [template1.html](/Exercices/Templates/template1.html) et [template2.html](/Exercices/Templates/template2.html). Ils comprennent les ressources nécessaires qui pointent sur des CDN. Maintenant, libre à vous de l’utiliser ou non. Mais ça vous fera gagner du temps.

Dans ces fichiers, j’ai fait pointer vers la dernière version 5.2 de Bootstrap. De plus, j’ai ajouté un fichier CSS supplémentaire (Icônes Bootstrap) que nous discuterons plus tard mais comme ça nous avons notre page web modèle Bootstrap déjà prête pour cela.

La différence entre [template1.html](/Exercices/Templates/template1.html) et [template2.html](/Exercices/Templates/template2.html).html, c'est que [template2.html](/Exercices/Templates/template2.html) comprend le \<div class="container"> juste après la balise \<body>.

## IV. Intégration des Fichiers Bootstrap
Sur le site Bootstrap : https://getbootstrap.com/docs/5.2/getting-started/introduction/

Nous allons le faire depuis l'[exercice n°1](/Exercices/Exercice1.md "Exercice sur l'intégration des fichiers Bootstrap: css et js").

## V. Fonctionnement de Bootstrap

Sur le site Bootstrap : https://getbootstrap.com/docs/5.2/getting-started/introduction/
Bootstrap fonctionne principalement avec l’utilisation de [classes css](https://developer.mozilla.org/fr/docs/Web/CSS/Class_selectors "Sélecteurs de classe sur Mozilla"). Il faut savoir que le fichier CSS de Bootstrap quand il n’est pas minifié (ramené sur une ligne pour qu’il prenne moins de place) fait 10400 lignes… Il n’est pas nécessaire de connaître par cœur toutes les classes. Personnellement j’utilise le site principal et Google.

### La classe .container
La première classe que l’on va utiliser est la classe [.container](https://getbootstrap.com/docs/5.2/layout/containers/ "Les classes containers sur Bootstrap") que l’on applique à un div. Elle permettra d’adapter la largeur du div en fonction de la résolution de l’écran du périphérique utilisé. Elle effectue aussi un léger padding gauche et droit.

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
- Cas n°5 : résolution supérieure ou égale à 1200 pixels et inférieure à 1140 pixels, l’élément s’affichera au centre de l’écran et sa largeur sera de 1140 pixels.
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

Sur le site Bootstrap : https://getbootstrap.com/docs/5.2/utilities/text/
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
Sur le site Bootstrap : https://getbootstrap.com/docs/5.2/content/images/
Nous allons voir que Bootstrap permet de facilement rendre une image responsive, en faire une jolie vignette, aligner celle-ci.
Évidemment toutes ces classes peuvent être combinées entre elles comme dans le précédent exemple.

### 1. Responsive
Bootstrap permet de rapidement permettre à une image d’être responsive. Ajouter la classe .img-fluid et votre image va s’auto-adapter en fonction de l’écran. 
```html
<img src="https://zamboyle.github.io/Cours/2022/Bootstrap/Exercices/Images/Logo_Eqla.png" class="img-fluid" alt="logo d'Eqla" width="10000px"  />
```
Ici on a ajouté l’attribut width="10000px". L’image ne fera bien sûr jamais 10000 pixels. Bootstrap veille au grain. 😊 
### 2. Thumbnail
La classe .img-thumbnail ajoute à l’image un bord blanc arrondi.
```html
<img src="https://zamboyle.github.io/Cours/2022/Bootstrap/Exercices/Images/Paris.jpg" class="img-thumbnail" alt="Image de paris" />
```
### 3. Alignement
Permet de mettre des images à gauche .float-start ou à droite .float-end quel que soit la taille de l’écran.
```html
<img src="/Images/logo_eqla.png" class="img-fluid float-start" alt="logo d'Eqla" />
<img src="/Images/paris.jpg" class="img-fluid img-thumbnail float-end" alt="Image de paris" />
```
On peut aussi définir ces alignements en fonction du périphérique :.float-\*-start ou .float-\*-end où * peut avoir différentes valeurs.
- sm : small
- md : medium
- lg : large
- xl : extra-large
- xxl: extra extra-large
