

<!--
VIII. Le composant Jumbotron
Sur le site Bootstrap : https://getbootstrap.com/docs/4.6/components/jumbotron/
Le Jumbotron est une boite rectangulaire qui va permettre de mettre en avant un certain message. Il est très grand et donne directement un impact visuel. On ne peut pas passer à côté quand on arrive sur une page.
Pour définir un jumbotron, on va ajouter une classe .jumbotron à un élément conteneur de type div. On va ensuite pouvoir placer plus ou moins n’importe quel contenu HTML à l’intérieur.
Exemple :
<div class="jumbotron">
<h1> Hello, world!</h1>
<p class="lead">Ceci est un exemple du composant jumbotron pour capter l’attention pour son contenu, une information importante.</p>
</div>

Maintenant, vous n’êtes pas obligés de mettre le jumbotron dans un div avec une class .container mais vous pouvez avoir un div container après le jumbotron. Donnant un effet que le jumbotron prend toute la largeur de la page et que le div ayant la classe .container soit lui centré.Ça dépend de ce que l’on veut mais ce n’est pas mal non plus.
Et pour terminer vous pourriez aussi avoir un div ayant la classe container à l’intérieur de votre jumbotron. Ça n’est pas interdit. 
<div class="jumbotron text-white" style="background-color:  #563d7c">
<div class="container">
<h1> VII. Le composant Jumbotron</h1>
<p class="lead">Ceci est un exemple du composant jumbotron pour capter l’attention par son contenu, une information importante.</p>
</div>
</div>

Et pour finir, vous avez la class .jumbotron-fluid qui supprime les coins arrondis et les rends carrés. A vous de décider entre « arrondis » ou « carrés ».
Exemple : <div  class="jumbotron jumbotron-fluid">
-->
## IX. Lecteur d’écran
Sur le site Bootstrap : https://getbootstrap.com/docs/4.6/utilities/screen-readers/
J’ai découvert cette classe par hasard en me « promenant » sur le site Bootstrap. Il m’a semblé évident de vous la présenter.
La classe .sr-only, elle n’est accessible que par un lecteur d’écran.
Exemple :
<div class = "container">
<p> Votre formateur s’appelle Johnny </p>
<a class = "sr-only" href="#">Votre formateur doit absolument aller chez le coiffeur mais ça restera entre nous.</a>
<p>Votre formateur est très bien coiffé.</p>
</div>
La classe .sr-only combinée avec .sr-only-focusable n’est visible que si on utilise le clavier (TAB) pour passer d’un lien à un autre.
Exemple :
<div class = "container">
<p> Votre formateur s’appelle Johnny </p>
<a class = "sr-only" href="#">Votre formateur doit absolument aller chez le coiffeur mais ça restera entre nous.</a>
<a class = "sr-only sr-only-focusable" href ="#">Votre formateur est très bien coiffé.</a>
</div>
    X. Le Composant Carousel
Sur le site Bootstrap : https://getbootstrap.com/docs/4.6/components/carousel/
Bootstrap fournit nativement un composant visuel de diaporama très sympathique que l’on appelle le carrousel. Il est fréquent de le voir sur des pages webs. Il présente par exemple des promos qui défilent via des images, du texte avec un changement cyclique définissable.
On peut y mettre des images, du texte, etc.
    1. Construction du carousel Bootstrap
Il suit le schéma suivant basé sur l’imbrication de plusieurs div.
    1. Un div contenant notre carrousel ayant les classes .carousel et .slide 
Ce div doit avoir l’attribut suivant data-ride="carousel"
    2. Un div enfant inclus dans le premier avec la classe .carousel-inner
    3. Ensuite nous ajoutons des div pour le contenu (slide) à faire défiler. Chaque contenu est inclus dans un div ayant la classe .carousel-item. Notons qu’un des divs de slide doit impérativement avoir la classe .active. Sinon le carousel ne sera pas visible.
Exemple :
<div id="monCarousel" class="carousel slide" data-ride="carousel">
<div class="carousel-inner">
<div class="carousel-item active">
<img src="Images/la.jpg" alt="Los Angeles, arrivée d'un groupe sur scène."> Los Angeles, pour <a href="">plus de photos</a>.
</div>
<div class="carousel-item">
<img src="Images/chicago.jpg" alt="chicago, image d'un chanteur sur scène avec une guitare.">
</div>
<div class="carousel-item">
<img src="Images/ny.jpg" alt="New-York, image dans la foule en direction de la scène.">
</div>
</div>
</div>
Si vous avoir un fondu pour passer à un slide suivant. Il faut ajouter la classe carousel-fade.
On peut jouer sur la vitesse, en millisecondes, de défilement en ajoutant un attribut data-interval.
Ce qui veut dire que notre div principal contenant le carousel devrait ressembler à ceci
<div id="monCarousel" class="carousel slide carousel-fade" data-ride="carousel" data-interval="2000">
Par défaut il n’a pas de boutons de défilement mais on peut les ajouter.
    2. Ajouter des contrôles Précédent et Suivant
Lors de l’utilisation du carousel Bootstrap, il est possible de définir les boutons « suivant » et « précédent ». Mais pour cela, il faut impérativement donner un id à notre carousel, sinon il ne sera pas possible d’ajouter ces boutons de contrôle.
Bouton précédent
    1. Ajoutez un id avec comme valeur monCarousel au div ayant la classe "carousel".
    2. Positionnez-vous après la fermeture du div ayant la classe "carousel-inner".
    3. Ouvrez une balise a et définissez les attributs suivants :
        a. class=".carousel-control-prev"
        b. href="#monCarousel" (C’est l’id du carousel définit au point 1).
        c. role="button"
        d. data-slide="prev"
    4. Ajoutez <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    5. Fermez la balise a
Bouton suivant
    1. Ouvrez une balise a et définissez les attributs suivants :
        a. class=".carousel-control-next"
        b. href="#monCarousel" (C’est l’id du carousel définit au point 1).
        c. role="button"
        d. data-slide="prev"
    2. Ajoutez <span class="carousel-control-next-icon" aria-hidden="true"></span>
    3. Fermez la balise a
    3. Contrôles accessibles
Alors ce carousel est très sympa. Mais il manque d’accessibilité. En effet, si un lecteur d’écran passe sur les boutons Précédent ou Suivant, nous entendrons le lecteur d’écran dire : Bouton. Ce qui est peu clair.
On peut l’améliorer en ajoutant la classe sr-only vue précédemment.
Il suffit d’ajouter dans les deux balises a des contrôles un span ayant la classe sr-only.
<span class="sr-only">Précédent</span>
<span class="sr-only">Suivant</span>
Exemple complet de contrôles accessibles
            <a class="carousel-control-prev" href="#monCarousel" role="button" data-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="sr-only">Précédent</span>
            </a>
            <a class="carousel-control-next" href="#monCarousel" role="button" data-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                <span class="sr-only">Suivant</span>
            </a>
    XI. La Grille de Bootstrap
Sur le site Bootstrap : https://getbootstrap.com/docs/4.6/layout/grid/
Bootstrap propose un système de grille très pratique et responsive. Elle permet d’agencer des contenus sous formes de colonnes. 
Cette grille est composée d’une ligne de 12 colonnes. On pourrait penser que c’est un tableau. Si on veut mais alors d’une seule ligne. Ce système de grille permet d’ajouter des éléments sous formes de colonnes.
Et comme vous le savez maintenant, utilisez Bootstrap, c’est utiliser ses classes. 
On utilise toujours un div conteneur ayant la classe .row. 
Les divs enfants seront les colonnes et auront une ou plusieurs classes.
    1. Classes pour un nombre fixe de colonnes :
    a) Les classes .col-* où * est  un nombre de 1 à 12. Quand on veut absolument un nombre défini de colonnes quel que soit la résolution. Dans ce cas, vous aurez toujours le nombre de colonnes désirés. 
Exemple où le nombre de colonnes est fixe par ligne (un .col-4 et .col-8 = 4 colonnes + 8 colonnes = 12 colonnes) :
<div class="row">
	<div class="col-4">
 	Première colonne avec un .col-4
</div>
<div class="col-8">
Deuxième colonne avec un .col-8
</div>
</div>
Ensuite, les combinaisons sont comme vous le voulez : Par exemple 3 .col-4 et vous aurez 3 colonnes. En effet, 3 x 4 colonnes = 12 colonnes , 2 .col-6 = 2 x 6 colonnes =12 colonnes,1 .col-2 et 1 .col-4+ et 1 .col-6 = 12 etc.
    b) La classe .col peut tout simplement être utilisée si vos colonnes ont exactement la même taille. Donc on pourrait avoir deux colonnes avec .col au lieu de .col-6 Ce qui veut dire que nous aurons deux colonnes quel que soit la résolution.
L’exemple :
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
On peut un peu complexifier en faisait un .col avec un .col-3. Ici notre .col sera équivalent à un .col-9
<div class="row">
	<div class="col">
 	Ceci est un texte assez répétitif. Ceci est un texte assez répétitif.
</div>
<div class="col-3">
 	Ceci est un texte assez répétitif. Ceci est un texte assez répétitif
</div>
</div>

    2. Classes pour un nombre de colonnes variables en fonction de la résolution
Nous venons de voir les classes pour un nombre fixe de colonnes. C’est top quand on veut absolument avoir ce nombre de colonnes.
Mais sachez que plus la résolution est petite et plus vos colonnes seront étroites. En effet, la lecture dans des colonnes si étroites n’est pas aisée.
Pour pallier à ce problème, Bootstrap propose de conditionner nos colonnes en fonction de la résolution.
Si cette résolution n’est pas atteinte alors au lieu de mettre les colonnes les une à côté des autres, ils les mettra les une au-dessus des autres. 
Les classes à utiliser seront : 
    • .col-sm-* où * est un nombre compris entre 1 et 12 (sm>= 576 pixels)
    • .col-md-* où * est un nombre compris entre 1 et 12 (md >= 768 pixels)
    • .col-lg-* où * est un nombre compris entre 1 et 12 (lg >= 992 pixels)
    • .col-xl-* où * est un nombre compris entre 1 et 12 (xl >= 1200 pixels)
Par exemple si on a deux colonnes ayant chacune comme classe un .col-sm-6
<div class="row">
	<div class="col-sm-4">
	Première colonne avec un .col-sm-4
	</div>
	<div class="col-sm-6">
	Ceci est la deuxième colonne avec un .col-sm-6
	</div>
</div>
Ça signifie qu’il faut afficher deux colonnes si on a une résolution d’au moins (576 pixels). Dans le cas contraire, Bootstrap affichera la première colonne et la seconde ira à la ligne. Et la lecture sera aisée sur un petit écran.
    3. Mixe entre classes à nombre de colonnes fixes et variables
Prenons un cas concret, vous souhaitez afficher 3 colonnes si la résolution le permet (md). Dans le cas contraire, vous afficher la première colonne sur une ligne et les deux autres sur la seconde.
Pour cela, vous aurez le html suivant
<h1>.col et .col-3</h1>
<div class="row text-white">
<div class="col-12 col-md-4 text-justify bg-success">
</div>
<div class="col-6 col-md-4 text-justify bg-warning"></div>
<div class="col-6 col-md-4 text-justify bg-danger"></div>
</div>


Expliquons-le petit à petit :
    • .col-12 col-md-4 : la colonne fera le 1/3 de l’écran si la résolution est supérieure ou égale à md. Dans le cas contraire, la colonne prendra toute la ligne (.col-12).
    • .col-6 col-md-4 : la seconde colonne fera le 1/3 (même raison). Dans le cas contraire, la colonne prendra la moitié de l’écran (.col-6).
    • .col-6 col-md-4 : idem que précédemment mais sera à côté de la colonne précédente si résolution inférieure à md.
Donc si la résolution est > = md, on aura 3 colonnes identiques (.col-md-4). Dans le cas contraire, on aura une colonne qui prendra toute une ligne (.col-12). Et sur une autre ligne, nous aurons deux colonnes identiques (.col-6) qui prendront toute la ligne.
    XII. Les couleurs
Sur le site Bootstrap : https://getbootstrap.com/docs/4.6/utilities/colors/
Bootstrap dispose de plusieurs classes pour les couleurs. Aux classes .bg-* (pour le background d’un élément) et aux classes .text-* on ajoute un des suffixes suivants :
- primary : bleu 
- secondary : gris 
- success : vert 
- danger : rouge 
- warning : orange 
- info : cyan 
- light : gris clair 
- dark : gris très foncé 
- body : noir 
- muted : gris 
- white : blanc

Par exemple un div avec un fond gris clair :
<div class= "container bg-light">
<p>Le fond de ce conteneur est gris clair</p>
</div>

Autre exemple, un div avec un fond rouge avec du texte blanc :
<div class= "container bg-danger text-white">
<p>Le fond de ce conteneur est rouge et le texte est blanc</p>
</div>

Pour le texte les classes suivantes peuvent aussi être utilisées :
- black-50 : texte noir semi transparent 
- white-50 : texte blanc semi transparent
Comme on peut le constater, Bootstrap fournit une cohérence dans l’utilisation des couleurs standards. Vous verrez que cette logique est suivie pour la couleur des boutons que nous allons justement voir au chapitre suivant.
    XIII. Les boutons
Sur le site Bootstrap : https://getbootstrap.com/docs/4.6/components/buttons/
Les classes Bootstrap pour les boutons sont faciles à utiliser. On utilise la balise <bouton>. Avec l’attribut type="button". Si on ne donne pas d’attribut type, il agira par défaut comme un type="submit" et essaiera d’envoyer un formulaire.
    1. Boutons avec une couleur de fond
Vous devez en premier mettre la classe .btn suivit de la couleur du bouton via la classe .btn-* : .btn-primary, .btn-success, .btn-warning, .btn-danger, etc.
Il a un léger effet lorsqu’on survole le bouton : il change légèrement de couleur (un peu plus foncé) et reprend sa couleur quand on bouge sa souris.
Exemple :
div class="container">
<h1>Boutons avec couleur de fond</h1>
<button type="button" class="btn btn-primary">Primary</button>
<button type="button" class="btn btn-secondary">Secondary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-danger">Danger</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-light">Light</button>
<button type="button" class="btn btn-dark">Dark</button>
<button type="button" class="btn btn-link">Lien</button>
</div>
    2. Boutons avec bordures
On peut avoir des boutons avec une bordure de couleur avec un fond blanc. Le texte est de la couleur de la bordure. Et quand on survole le bouton, la couleur de fond du bouton change et le texte devient blanc. Il redevient « normal » quand la souris n’est plus sur le bouton.
On utilise la classe .btn-outline-* à la place de .btn-* : .btn-outline-primary, .btn-outline-success, .btn-outline-warning, .btn-outline-danger, etc. 
Exemple :
<div class="container">
<h1>Boutons à bordures</h1>
<button type="button" class="btn btn-outline-primary">Primary</button>
<button type="button" class="btn btn-outline-secondary">Secondary</button>
<button type="button" class="btn btn-outline-success">Success</button>
<button type="button" class="btn btn-outline-danger">Danger</button>
<button type="button" class="btn btn-outline-warning">Warning</button>
<button type="button" class="btn btn-outline-info">Info</button>
<button type="button" class="btn btn-outline-light">Light</button>
<button type="button" class="btn btn-outline-dark">Dark</button>
<button type="button" class="btn btn-outline-link">Lien</button>
</div>

    3. Boutons sur la balise <a>
Rien ne nous empêche de mettre les classes des boutons sur la balise <a> pour avoir un bouton à la place d’un lien. Exemple : le bouton « Nouvelle Inscription ».
Exemple :
<a class="btn btn-primary" href="http://www.google.be">Nouvelle Inscription</a>
<a class="btn btn-warning" href="http://www.google.be">Désinscription</a>

    4. La taille des boutons
On peut modifier la taille standard des boutons en utilisant les .btn-sm (petit bouton) et .btn-lg (gros bouton). Il existe aussi la classe .btn-block qui va prendre tout l’espace de l’élément conteneur.
Exemple :
<div class="container">
<h1>Taille des Boutons</h1>
<button type="button" class="btn btn-primary btn-lg mb-2">Gros bouton</button>
<button type="button" class="btn btn-outline-primary btn-lg mb-2">Gros bouton avec bordures</button>

<button type="button" class="btn btn-success btn-sm mb-2">Petit bouton</button>
<button type="button" class="btn btn-outline-success btn-sm mb-2">Petit bouton avec bordures</button>
<br><br>
<button type="button" class="btn btn-warning btn-lg btn-block">Bouton de type block</button>
<button type="button" class="btn btn-outline-warning btn-lg btn-block">Bouton avec bordures de type block</button>
</div>

    5. Activer/Désactiver un bouton
On le fait en utilisant la classe .active pour l’activer et .disabled pour le désactiver. Attention de ne pas penser que c’est sécurisé de mettre un bouton avec la classe .disabled. En effet, si vous pensez par exemple désactiver la vente d’un produit jusqu’à 20h00. Sur le frontend, mettre cette classe à .disabled est facilement modifiable avec des navigateurs comme Firefox/Chrome. Il faut en plus côté backend, empêcher la vente du produit tant qu’il n’est pas 20h00. 
Exemple :
<button type="button" class="btn btn-primary active">Active Primary</button>
<button type="button" class="btn btn-primary disabled">Disabled Primary</button>
    XIV. Les tableaux
Sur le site Bootstrap : https://getbootstrap.com/docs/4.6/content/tables/
Bootstrap permet de styliser nos tableaux.
    1. Simple tableau Bootstrap
La classe .table permet de donner du style à nos tableaux on l’ajoute à la balise <table>. 
Le tableau est plus grand et respire plus que le tableau par défaut qui est plus compact. Les lignes par défaut non pas de bords à gauche et à droite. L’entête du tableau définit dans <thead> ou par un <th> est en gras.
Exemple :
    <div class="container">
        <table class="table">
            <thead>
                <tr>
                    <th scope="col">Id</th>
                    <th scope="col">Nom</th>
                    <th scope="col">Prénom</th>
                    <th scope="col">Age</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <th scope="row">1</th>
                    <td>Piette</td>
                    <td>Johnny</td>
                    <td>46</td>
                </tr>
                <tr>
                    <th scope="row">2</th>
                    <td>Dupont</td>
                    <td>Patrick</td>
                    <td>35</td>
                </tr>
                <tr>
                    <th scope="row">3</th>
                    <td>Jacques</td>
                    <td>Gabriel</td>
                    <td>6</td>
                </tr>
            </tbody>
        </table>
    </div> 

    2. Description du tableau
Pour informer l’utilisateur du contenu du tableau, soit on met un titre clair ou une description à l’aide d’un titre et un paragraphe.
On peut aussi utiliser la balise caption juste après la balise table. Nous aurons en bas à gauche du tableau la description du tableau.
Exemple :
<div class="container">
        <table class="table">
            <caption>Liste des utilisateurs</caption>
            <thead>
                <tr>
                    <th scope="col">Id</th>
                    <th scope="col">Nom</th>
                    <th scope="col">Prénom</th>
                    <th scope="col">Age</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <th scope="row">1</th>
                    <td>Piette</td>
                    <td>Johnny</td>
                    <td>46</td>
                </tr>
                <tr>
                    <th scope="row">2</th>
                    <td>Dupont</td>
                    <td>Patrick</td>
                    <td>35</td>
                </tr>
                <tr>
                    <th scope="row">3</th>
                    <td>Jacques</td>
                    <td>Gabriel</td>
                    <td>6</td>
                </tr>
            </tbody>
        </table>
    </div>



    3. Entêtes clairs ou sombres
Pour avoir l’entête du tableau en noir ou en gris clair on utilise les classes .thead-dark ou .thead-light.
Exemples : <thead class="thead-dark" > ou <thead class="thead-light" >
    4. Lignes en rayures de zèbre
Pour une lecture efficace, on utilise souvent cette technique d’alterner deux couleurs, une ligne sur deux. Ça permet de plus facilement lire un tableau. Sinon on est vite « noyé » dans un tableau s’il n’applique pas cette technique.
Pour alterner une ligne sur deux, en plus de la classe .table, on utilise la classe .table-striped sur la balise <table>.
Exemple :
    <div class="container">
        <table class="table table-striped">
            <thead>
                <tr>
                    <th scope="col">Id</th>
                    <th scope="col">Nom</th>
                    <th scope="col">Prénom</th>
                    <th scope="col">Age</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <th scope="row">1</th>
                    <td>Piette</td>
                    <td>Johnny</td>
                    <td>46</td>
                </tr>
                <tr>
                    <th scope="row">2</th>
                    <td>Dupont</td>
                    <td>Patrick</td>
                    <td>35</td>
                </tr>
                <tr>
                    <th scope="row">3</th>
                    <td>Jacques</td>
                    <td>Gabriel</td>
                    <td>6</td>
                </tr>
            </tbody>
        </table>
    </div>

    5. Tableau à bordures ou sans bordure
On utilise la classe .table-bordered pour ajouter une bordure à toutes les cellules du tableau et la classe .table-borderless pour les supprimer partout.
Exemple avec bordures : <table class="table table-bordered">
Exemple sans bordure : <table class="table table-borderless">
    6. Effet lors du passage de la souris sur une ligne
Un effet de survol lorsqu’on passe la souris sur une ligne est assez sympathique. Il se caractérise par un changement de couleur de la cellule lorsqu’on la survole.
Pour ajouter cet effet, on utilise la classe .table-hover sur la balise <table>.
Exemple : Exemple avec bordures : <table class="table table-hover table-bordered">
    7. Couleurs des lignes
Nous allons pouvoir utiliser les couleurs contextuelles de Bootstrap pour changer la couleur de chaque ligne ou de chaque cellule d’un tableau. On va pouvoir utiliser les classes suivantes :
    • .table-active ;
    • .table-primary ;
    • .table-secondary ;
    • .table-success ;
    • .table-danger ;
    • .table-warning ;
    • .table-info ;
    • .table-light ;
    • .table-dark.
    8. Tableaux adaptables
Si dans un tableau vous avez vraiment besoin d’afficher tous les colonnes quel que soit le média, il existe une classe .table-responsive qui va ajouter une barre une défilement horizontale. 
    XV. Classes d’espacement
Sur le site Bootstrap : https://getbootstrap.com/docs/4.6/utilities/spacing/
Dans Bootstrap, nous avons des classes qui permettent d’ajouter des paddings ou des marges
    1. Les marges
Ces classes ont deux formats :
    a. Soit une classe du type .m{côtés}-{taille}.
La taille varie de 0 à 5 (0 = 0rem, 1=0,25 rem,  2 = 0,5 rem, 3=1rem, 4 = 1,5 rem, 5 =  3 rem)
0,25 rem = 0,25 * la variable SASS $spacer qui est définie par défaut à 1rem).
« côtés » peut prendre les valeurs suivantes : rien, t (top), b(bottom), l (lef), r (right), x (gauche et droite), y (haut et bas)
m-* : ajoutera une marge aux 4 côtés.
mt-* : ajoutera une marge en haut.
mb-* : ajoutera une marge en bas.
ml-* : ajoutera une marge à gauche.
mr-* : ajoutera une marge à droite.
mx-* : ajoutera une marge à gauche et à droite.
my-* : ajoutera une marge en haut et en bas.
    b. Soit une classe du type .m{côtés}-{media}-{taille}
« media » peut prendre une des valeurs suivantes : sm, md, lg, xl. C’est donc conditionné en fonction de la taille de l’écran du périphérique. 
Exemples : m-sm-7, mx-lg-5, etc.
    2. Les paddings
Même principe que pour les marges. 
Donc on pourra avoir deux formes : .p{côtés}-{taille} et p{côtés}-{media}-{taille}.
    XVI. Les bordures
https://getbootstrap.com/docs/4.6/utilities/borders/
Il est aisé d’ajouter des bordures à des éléments avec Bootstrap. Si on ajoute la classe .border, une bordure sera ajoutée à votre élément.
    1. Les bordures additives
Les bordures additives sont en fait des 1/4 bordures. Donc juste un côté sur 4.
On a donc logiquement 4 classes pour cela. A savoir :
    • .border-top : Le côté c’est le côté haut.
    • .border-bottom : Le côté c’est le côté bas.
    • .border-left : Le côté c’est le côté gauche.
    • .border-right : Le côté c’est le côté droit.
    2. Les bordures soustractives
Ici on part d’une bordure complète que l’on retire un côté donc 1/4. Cependant avant de pouvoir ajouter ces classes il faudra auparavant ajouter la classe .border suivie de la classe de bordure à soustraire.
Les classes sont les suivantes :
    • .border-top-0 : On enlève la partie du haut de la bordure.
    • .border-bottom-0 : On enlève la partie du bas  de la bordure.
    • .border-left-0 : On enlève la partie de gauche de la bordure.
    • .border-right-0 : On enlève la partie de droite de la bordure.
Exemple on soustrait la bordure de droite d’un span : <span class="border border-right-0">Hello World</span>
    3. Les bordures colorées
Bootstrap suit la logique dans couleur pour les cadres. Il faut avant ajouter la classe .border pour ajouter une couleur de cadre.
    • .border-primary
    • .border-secondary
    • .border-success
    • .border-danger
    • .border-warning
    • .border-info
    • .border-light
    • .border-dark
    • .border-white
    4. Les bordures arrondies
Ajoutez des classes à un élément pour arrondir facilement ses coins :
    • .rounded : bordures arrondies.
    • .rounded-top : bordure arrondie en haut.
    • .rounded-right : bordures arrondies à droite.
    • .rounded-bottom : bordures arrondies en bas.
    • .rounded-left : bordures arrondies à gauche.
    • .rounded-circle : un cercle et non un cadre entoure notre élément.
    • .rounded-pill : Les côtés gauche et droit sont des demis cercles. Le haut et le bas sont des droites. Ça donne une impression d’une pilule d’où pill en anglais.
Exemple : un span avec bordures en forme de pillule avec un fond vert (bg-success), une border en rouge (border-danger), le texte en blanc et un padding de 1. J’ai en plus ajouté un style pour l’épaisseur de 5 (border-5) qui est une classe de Bootstrap 5.
<span class="border rounded-pill border-danger bg-success text-white p-1" style="border-width: 5px!important;">Hello World !</span>

Bootstrap 5 définit cette classe de la manière suivante :
.border-3 {
    border-width: 3px!important;
}
Ce qui est assez logique. 😊 Bootstrap 5 a des classes .border-1 jusqu’à .border-5. Ceci était juste une petite anecdote sur Bootstrap 5.

    XVII. Les affichages
Sur le site Bootstrap : https://getbootstrap.com/docs/4.6/utilities/display/
Vous pouvez changer la valeur du display via des classes Bootstrap.
    1. Notation
Ces classes sont nommées en utilisant le format :
    1. .d-{value} 
    2. .d-{media}-{value} pour  sm, md, lg, and xl.
Où les valeurs peuvent être :
    • None
    • Inline
    • inline-block
    • block
    • table
    • table-cell
    • table-row
    • flex
    • inline-flex
Exemple : deux div sur la même ligne
<div class="d-inline p-2 bg-primary text-white">d-inline</div>
<div class="d-inline p-2 bg-dark text-white">d-inline</div>
Exemple : deux div affichés en block
<span class="d-block p-2 bg-primary text-white">d-block</span>
<span class="d-block p-2 bg-dark text-white">d-block</span>

    2. Cacher des éléments
Il est parfois utile de cacher des éléments en fonction du média, par exemple un smartphone. Pour que le site soit responsive au maximum.
Pour masquer des éléments, utilisez simplement la classe .d-none ou l'une des classes 
.d- {sm, md, lg, xl}-none pour toute variation d'écran.
Exemples de combinaisons :
Caché pour tous:.d-none
Caché seulement sur xs:.d-none .d-sm-block
Caché seulement sur sm:.d-sm-none .d-md-block
Caché seulement sur md:.d-md-none .d-lg-block
Caché seulement sur lg:.d-lg-none .d-xl-block
Caché seulement sur xl:.d-xl-none
Visible pour tous:.d-block
Visible seulement sur xs:.d-block .d-sm-none
Visible seulement sur sm:.d-none .d-sm-block .d-md-none
Visible seulement sur md:.d-none .d-md-block .d-lg-none
Visible seulement sur lg:.d-none .d-lg-block .d-xl-none
Visible seulement sur xl:.d-none .d-xl-block
Exemples html:
        <div class="d-lg-none">Je suis caché pour des écrans d’au moins lg. Mais donc visible pour des écrans plus petits que lg.</div>
        <div class="d-none d-lg-block">Je suis caché pour des écrans plus petits que lg. Mais visible pour des écrans d'au moins lg.</div>
    3. Impression
Il est possible de choisir ce qui sera affiché lors de l’impression. On peut cacher ou montrer des informations pour une impression. Pour cela on utilise les classes suivantes :
    • .d-print-none
    • .d-print-inline
    • .d-print-inline-block
    • .d-print-block
    • .d-print-table
    • .d-print-table-row
    • .d-print-table-cell
    • .d-print-flex
    • .d-print-inline-flex
Exemples
<div class="d-print-none">Affiché sur écran seulement (Caché à l’impression)</div>
<div class="d-none d-print-block">Impression seulement (Caché à l’écran)</div>
<div class="d-none d-lg-block d-print-block">Caché pour des écrans larges, mais toujours affiché pour l’impression</div>


    XVIII. Dimensionnement
Sur le site Bootstrap : https://getbootstrap.com/docs/4.6/utilities/sizing/
Il est possible de dimensionner un élément avec les classes .w-* pour la largeur et .h-* pour la hauteur.
Voici les valeurs que peuvent prendre ces classes :
    • m-25, m-50, m-75, m-100, m-auto
    • h-25, h-50, h-75, h-100, h-auto
Exemple :
<div class="w-75">Je prends 75% de la largeur.</div>
    XIX. Les formulaires
Sur le site Bootstrap : https://getbootstrap.com/docs/4.6/components/forms/
Bootstrap fournit un ensemble de classes qui permettent de rendre un formulaire beaucoup plus joli visuellement. De base, les formulaires html sont assez austères.
Pour utiliser les classes que nous allons voir, il faut bien entendu utiliser la balise « form » pour nos formulaires.
    1. Classes form-group et form-control
La classe .form-group est utilisée pour grouper le contrôle du formulaire avec sa description.
Les éléments <input>, <select> et <textarea> sont stylisés via la classe .form-control. Ce sont des contrôles dont les bords sont arrondis, grands et prennent toute la largeur du conteneur.
Avant ces contrôles, on ajoute sa description via la balise <label> avec l’attribut for= "#ControleADecrire". 
L'élément HTML <label> représente une légende pour un objet d'une interface utilisateur. Il peut être associé à un contrôle en utilisant l'attribut for ou en plaçant l'élément du contrôle à l'intérieur de l'élément <label>. Un tel contrôle est appelé contrôle étiqueté par l'élément <label>.
Exemple :
<form>
    < !-- Premier form-group -->
    <div class="form-group">
        <label for="exempleInputEmail">Adresse Email</label>
        <input type="email" class="form-control" id="exempleInputEmail" aria-describedby="emailHelp" placeholder="Entrer un email">
        <small id="emailHelp" class="form-text text-muted">Nous ne partagerons jamais votre email avec qui que ce soit.</small>
    </div>

    < !-- Deuxième form-group -->
    <div class="form-group">
        <label for="exempleInputPassword">Password</label>
        <input type="password" class="form-control" id=" exempleInputPassword " placeholder="Password">
    </div>

    < !-- Troisième form-group -->
    <div class="form-check">
        <input type="checkbox" class="form-check-input" id="exempleCheck">
        <label class="form-check-label" for="exempleCheck">Check me out</label>
    </div>
    <button type="submit" class="btn btn-primary">Soumettre</button>
</form>
Rappelons que l’attribut placeholder permet d’afficher un texte dans un champ du formulaire. Exemple : « Entrer un email ». Ce message sera affiché tant que rien n’est indiqué dans le champ du formulaire. Mais ce texte dans le placeholder ne sera pas pris comme valeur si on soumet le formulaire.
Ensuite, il est important de bien spécifier le type. En effet, ce type permettra d’être intercepté en cas de mauvais type. Exemple le type email qui testera un peu la validité d’un email. 
L’attribut required indique au formulaire que ce champ est nécessaire et ne peut valider le formulaire tant que ce champ est vide. Attention qu’il ne faut pas croire aveuglément un formulaire reçu côté back-end. Normalement les mêmes règles de validations doivent être de rigueur côté serveur. Une règle : « Ne jamais croire ce que nous recevons du front-end. On reteste les données côté back-end. »
    2. Classe .form-control-file
Pour le contrôle d’envoi de fichier on ajoute simplement cette classe au contrôle.
Exemple :
<div class="form-group">
    <label for="exempleFormControlFile">Example file input</label>
    <input type="file" class="form-control-file" id="exempleFormControlFile">
</div>

    3. Attribut readonly
Quand un élément comprend l’attribut readonly, le contrôle du formulaire sera désactivé et on ne saura pas le cliquer ou y écrire quelque chose. Le contrôle est juste en lecture seule.
Le contrôle sera en gris foncé avec son texte prédéfini. Exemple, dans un formulaire si on connait déjà le nom d’utilisateur et qu’il ne changera pas, on peut le préremplir et mettre l’attribut readonly. Cependant il sera envoyé par le formulaire. Si vous ne voulez pas qu’il soit envoyé, utilisez l’attribut disabled.
Exemple :
<input id="username"  class="form-control" type="text" placeholder="mcfly" readonly>

    4. Attribut readonly et la classe .form-control-plaintext
Ici le comportement sera identique : on ne saura pas interagir. Cependant la classe .form-control-plaintext supprime le bord du contrôle input. Donnant l’impression que c’est un simple texte. Mais si on clique dessus on voit apparaître les bordures du contrôle.
Exemple :
<input type="text" readonly class="form-control-plaintext" id="staticEmail" value="johnny.piette@gmail.com">

    XX. Les navbars
Sur le site Bootstrap : https://getbootstrap.com/docs/4.6/components/navbar/
Les barres de navigations s’utilisent avec la balise <nav> d’html qui permet de faire d’afficher des liens de navigation.
Tous les liens de navigations devront être à l’intérieur de la balise <nav> pir qu’ils soient bien lus pour les lecteurs d’écran. Maintenant, vous pouvez utiliser un <div> mais vous devrez ajouter l’attribut role="navigation" pour une meilleure accessibilité. Cette balise <nav> ou ce <div> auront comme classe .navbar.
A l’intérieur nous pouvons avons plusieurs types d’éléments :
    1. .navbar-brand pour une société, un produit, un nom de projet.
    2. .navbar-nav pour le menu de navigation.
    3. .navbar-toggler qui affichera le bouton « sandwich » pour afficher nos menus si l’écran est trop petit.
    4. .form-inline pour afficher des contrôles de formulaire.
    5. .navbar-text pour ajouter du texte vertical centré.
    6. .collapse navbar-collapse pour reprouper des sous-menus.
Commençons par afficher une barre de navigation simple avec le nom de notre marque :
    <div class="container">
      <h1>Navigation</h1>
      <nav class="navbar navbar-light bg-light">
        <a class="navbar-brand" href="#">Bootstrap</a>
      </nav>

Ajoutons trois liens : Accueil, Produits, A propos, Contacts
Pour cela, on commence à ajouter un <ul class="navbar-nav"> 
Chaque élément de navigation sera un <li class="nav-item"> inclus évidemment dans le précédent <ul>.
Le lien sera à l’intérieur du <li> sera de la forme <a class="nav-link" href="http://votreurl">Votre texte</a>
Cela donne donc comme code html :
<nav class="navbar navbar-light bg-light">
    <div class="nav-brand">Navigation</div>
    <ul class="navbar-nav">
        <li class="nav-item"><a class="nav-link" href="index.html">Accueil</a></li>
        <li class="nav-item"><a class="nav-link" href="produits.html">Produits</a></li>
        <li class="nav-item"><a class="nav-link" href="about.html">A propos</a></li>
        <li class="nav-item"><a class="nav-link" href="Contacts">Contacts</a></li>
    </ul>
</nav>
Alors, tout cela est très bien mais notre menu est affiché verticalement. Il est plus aisé de le voir s’afficher horizontalement. On ajoute donc à la balise <nav> la classe  navbar-expand-lg (on peut avoir -sm, -md, -lg et -xl).
Notre code devient alors :
<nav class="navbar navbar-light bg-light navbar-expand-lg">
    <a class="navbar-brand" href="#">Bootstrap</a>
    <ul class="navbar-nav">
        <li class="nav-item"><a class="nav-link" href="index.html">Accueil</a></li>
        <li class="nav-item"><a class="nav-link" href="produits.html">Produits</a></li>
        <li class="nav-item"><a class="nav-link" href="about.html">A propos</a></li>
        <li class="nav-item"><a class="nav-link" href="Contacts">Contacts</a></li>
    </ul>
</nav>
Si notre menu est trop grand, il est intéressant de le réduire dans un bouton sandwich/burger.
Pour cela après notre balise <nav> et notre marque (navbar-brand) nous ajoutons le code suivant :
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarContenu" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
            </button>
Les balises <ul> et </ul> doivent être contenues dans un div ayant les classes .collapse et .navbar-collapse ayant un id par exemple id="navbarContenu". Le code devient le suivant :
<nav class="navbar navbar-expand-lg navbar-light bg-light">
    <a class="navbar-brand" href="#">Bootstrap</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarContenu" aria-controls="navbarContenu" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
        </button>
    <div id="navbarContenu" class="collapse navbar-collapse">
        <ul class="navbar-nav">
            <li class="nav-item active"><a class="nav-link" href="index.html">Accueil</a></li>
            <li class="nav-item"><a class="nav-link" href="produits.html">Produits</a></li>
            <li class="nav-item"><a class="nav-link" href="about.html">A propos</a></li>
            <li class="nav-item"><a class="nav-link" href="Contacts">Contacts</a></li>
        </ul>
    </div>
</nav>

Alors j’ai ajouté au point de menu « Accueil » la classe .active. Ça met un peu en évidence notre lien en cours.
Admettons que vous voudriez avoir une zone de recherche avec un bouton rechercher dans votre menu au bout à droite (en ajoutant la classe .mr-auto à la balise <ul> sinon elle sera collée aux autres éléments du menu.
Il suffit d’ajouter le code suivant après la balise </ul> :
<form class="form-inline my-2 my-lg-0">
    <input class="form-control mr-sm-2" type="search" placeholder="Produit à rechercher" aria-label="Produit à rechercher">
    <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Rechercher</button>
</form>
Notre code final deviendra :
        <nav class="navbar navbar-expand-lg navbar-light bg-light">
            <a class="navbar-brand" href="#">Bootstrap</a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarContenu" aria-controls="navbarContenu" aria-expanded="false" aria-label="Toggle navigation">                <span class="navbar-toggler-icon"></span>            </button>
            <div id="navbarContenu" class="collapse navbar-collapse">
                <ul class="navbar-nav mr-auto">
                    <li class="nav-item active"><a class="nav-link" href="index.html">Accueil</a></li>
                    <li class="nav-item"><a class="nav-link" href="produits.html">Produits</a></li>
                    <li class="nav-item"><a class="nav-link" href="about.html">A propos</a></li>
                    <li class="nav-item"><a class="nav-link" href="Contacts">Contacts</a></li>
                </ul>
                <form class="form-inline my-2 my-lg-0">
                    <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
                    <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
                </form>
            </div>
        </nav>
Votre menu soit vous mettez dans un div="container". De cette manière, il sera centré sur votre page.
Ou bien, vous avez besoin d’utiliser toute la largeur de la page, dans ce cas on utilisera la classe .container-fluid. Notons que vous pouvez avoir pour le menu un div avec la classe container-fluid et un div pour le contenu avec la classe .container.


    XXI. Les alertes
Sur le site Bootstrap : https://getbootstrap.com/docs/4.6/components/alerts/
    1. Les classes
Bootstrap fournit un système d’alerte. On entend par alerte un message encadré avec un background. Les classes pour ces alertes sont :
    • alert-primary
    • alert-secondary
    • alert-success
    • alert-danger
    • alert-warning
    • alert-info
    • alert-light
    • alert-dark
Exemples : 3 alertes
<div class="alert alert-success" role="alert">
	L’utilisateur a été créé avec succès !
</div>
<div class="alert alert-warning" role="alert">
	Certains champs n’ont pas été remplis !
</div>
<div class="alert alert-danger" role="alert">
	Erreur : Impossible de se connecter à la base de données. Veuillez patienter.
</div>

    2. Les liens
Si vous mettez un lien hypertexte dans une alerte, on utilise la classe .alert-link. Cette classe adaptera la couleur en fonction de la couleur de l’alerte.
Exemple :
<div class="alert alert-primary" role="alert">
  Une simple alerte primary <a href="#" class="alert-link">an example link</a>. Cliquez si vous avez envie.
</div>

    3. Bouton Close
On peut faire apparaître un bouton permettant de faire disparaître notre alerte. C’est utile quand on veut en haut du page afficher une information qu’on peut éventuellement fermer à l’aide d’un bouton.
Pour cela on ajouter la classe . alert-dismissible.

Exemple : Alerte avec un bouton de fermeture
    <div class="alert alert-warning alert-dismissible fade show" role="alert">
        <strong>Hey !</strong> Tu devrais vérifier quelques champs du formulaire.
        <button type="button" class="close" data-dismiss="alert" aria-label="Close">
          <span aria-hidden="true">x</span>
        </button>
    </div>
On utilise un span avec x comme texte pour indiquer la fermeture. Vous pouvez aussi rencontrer comme texte  &times; (signe de multiplication). Ça ressemble aussi à un x . Choisissez ! 😊
L’exemple précédent montre que si l’on veut avoir un effet de fondu quand on ferme l’alerte, il faut ajouter deux classes : fade show.
Alerte avec contenu
On peut structurer le contenu de notre alerte et en ajoutant par exemple des titres 1, 2, 3, etc. Mais il faut alors ajouter à la balise de titre (h1, h2, etc) la classe alert-heading Ca mettra une couleur de titre proche de la couleur du contenu de l’alerte. Si vous avez une alert-success, le titre sera d’un vert foncé.
    XXII. Les icones Bootstrap
Sur le site Bootstrap : https://icons.getbootstrap.com/
Bootstrap fournit un ensemble d’icônes prêtes à l’emploi. Il y a un moteur de recherches pour trouver une icône. Vous n’êtes pas obligés de l’utiliser qu’avec Bootstrap. Ces icônes peuvent être utilisées sans Bootstrap.
Ces icônes dépannent dans pas mal de situations mais si vous avez vraiment besoin d’icônes non listées allez voir sur le site Font Awesome : https://fontawesome.com/ Vous avez les icônes gratuites et payantes. Site à retenir !
Il y a deux techniques pour ajouter les icônes de Bootstrap dans notre page :
    • Il faut pour cela ajouter dans notre page web le lien vers le fichier css : <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.4.1/font/bootstrap-icons.css">
    • Ou directement dans un fichier css de notre site : @import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@1.4.1/font/bootstrap-icons.css");
Exemples d’utilisation : une icône d’un panier, une icône de Facebook, une icône d’une poubelle
<i class="bi bi-cart" role="img" aria-label="Panier"></i>
<i class="bi bi-facebook" role="img" aria-label="Facebook"></i>
<i class="bi bi-trash" role="img" aria-label="Poubelle"></i>

Exemple d’un bouton avec une icône d’une lettre et « Contacter Eqla » 
<a href="https://eqla.be/contact/" class="btn btn-default btn-primary"><i class="bi bi-envelope"></i> Contacter Eqla </a>
Exemple d’un bouton de suppression d’un utilisateur :
<a href="http://UrlPourSupprimer" class="btn btn-default btn-danger  align-middle"><i class="bi bi-person-dash-fill align-middle"></i><span class="align-middle"> Supprimer</span> </a>

