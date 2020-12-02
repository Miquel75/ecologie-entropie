---
title: 'La Théorie des Jeux'
subtitle: "Un concept mathématiques utile dans de nombreux domaines dont l'écologie."
summary: "Cette théorie mathématiques à permis le développement du concept de stratégie évolutivement stable (SES). Ces notions sont ont apporté de nouveaux éclairage sur la dynamique évolutive."
authors:
- Miquel Pons

tags:
- 
categories:
- Écologie scientifique
- Concepts d'écologie
date: Sys.Date()
lastmod: "2020-11-21T00:00:00Z"
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Placement options: 1 = Full column width, 2 = Out-set, 3 = Screen-width
# Focal point options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
image:
  placement: 1
#  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []


---

### Le dilemme des prisonniers 

Deux prisonniers complices ont été arrêtés et sont dans deux cellules séparées sans aucun moyen de communiquer entre eux. On leur donne plusieurs choix : 

-	Si un seul des prisonniers dénonce l’autre, il est libéré tandis que son partenaire fera 10 ans de prison
-	Si les deux se dénoncent, ces snitchs seront condamnées à 5 ans de prison
-	Si les deux gardent le silence, ils ne feront que 6 mois de prison chacun

Que devrait faire chacun des prisonniers ? 
-	« Dans le cas où il me dénonce »
Si je me tais, je fais 10 ans de prison
Si je le dénonce, je fais 5 ans de prison
Dénoncer est plus intéressant. 
-	« Dans le cas où il se tait »
Si je me tais, je fais 6 mois de prison
Si je le dénonce, je suis libéré. 
Dénoncer est plus intéressant.

Les règles favorisant la trahison, le plus probable c’est que les prisonniers fassent 5 ans de prison chacun alors qu’ils pourraient se taire tous les deux pour un résultat optimal de 6 mois de prison. C’est là tout le dilemme du prisonnier et l’exemple couramment donné pour illustré la **théorie des jeux**.  

Ce domaine des mathématiques s’intéresse aux interactions stratégiques entre individus et est utilisé comme outil théorique dans de nombreux domaines tels que l’économie, les sciences sociales, la politique et la biologie. 

C’est un concept simple et très souvent applicable. Il est donc intéressant d’en avoir quelques notions.

### La théorie des jeux en biologie

John Maynard Smith développe en 1982 dans son livre *Evolution & the theory of games* la théorie de **stratégie évolutivement stable (SES)** en utilisant la théorie des jeux et **l’équilibre de Nash**. Dans le cas où chacun des prisonniers dénonce l’autre, on atteint l’équilibre de Nash, où chacun prévoit correctement le choix de l’autre et en tenant compte de cette prédiction, maximise son gain. Dis autrement, c’est quand aucun des « joueurs » n’a d’intérêt à changer unilatéralement de stratégie.

Dans une grande population de joueurs qui se rencontre aléatoirement, une stratégie est évolutivement stable si aucune autre stratégie n’est capable de l’envahir. 

### Stratégie Faucon vs Colombe

Il y a une ressource que l’on appellera R convoité par des individus.
Au cours de leurs interactions, les individus peuvent adopter deux comportements, deux stratégies. 
Le Faucon (F) est agressif et s’imposera jusqu’à être blessé ou que l'autre joueur batte en retraite. 
La colombe (C) bat en retraite si l’adversaire se montre agressif. 
Lorsque deux faucons se rencontrent, l’un est blessé (-B) et l’autre remporte la ressource (R) avec une probabilité de 1/2.
Lorsqu’un faucon rencontre une colombe, le faucon remporte la ressource sans être blessé et la colombe fuit également sans dommages.
Lorsque deux colombes se rencontrent,  elles partagent la ressource. 

On peut donc créer le tableau suivant :
	F	C
F	(R-B)/2	R
C	0	R/2

| Titre 1       |     Titre 2     |        Titre 3 |
| :------------ | :-------------: | -------------: |
| Colonne       |     Colonne     |        Colonne |
| Alignée à     |   Alignée au    |      Alignée à |
| Gauche        |     Centre      |         Droite |

Quelle est la meilleure stratégie ? 

Dans une population jouant Colombe, un individu jouant Faucon gagnera R au lieu de R/2 chaque fois. Son gain étant supérieur à celui des Colombes, sa **fitness** est supérieur. La **fitness** étant la capacité à survivre et à se reproduire, Faucon va donc envahir la population. 

Dans une population de Faucon, un individu jouant Colombe gagnera 0 qu’il faut comparer (R-B)/2 que gagnent les Faucons qui rencontrent d’autres Faucons. On peut observer que (R-B)/2 est forcément inférieur à R/2. La sélection naturelle ne sélectionne donc pas la meilleure stratégie, mais aboutit à la stratégie la plus stable. 
Si R la récompense est supérieure à B l’importance des blessures, alors R>B et donc (R-B)/2 > 0. Ce qui veut dire que Colombe n’envahira jamais la population de Faucons. A ce moment-là le phénotype Faucon est une **stratégie évolutivement stable**.
Si au contraire B>R alors les Colombes pourront envahir. Ainsi aucun des deux phénotypes n’est stable car ils sont réciproquement envahissables. La stabilité se trouvera à une certaine proportion de chaque phénotype qui dépendra de la valeur de R et de B. Les gains de fitness dépendent de la fréquence des stratégies concurrentes, ce qui peut mener à la coexistence stable de différents types de comportement dans une population. 
Un mutant apparait avec une stratégie différente de Faucon et Colombe, le phénotype « Bourgeois ». 
Le Bourgeois se bat et joue Faucon lorsqu’il est le premier arrivé sur la Ressource, mais joue Colombe et évite le combat s’il arrive en second. On considère que la probabilité d’arriver le premier est de 1 chance sur 2. 

On peut montrer avec quelques calculs qu’une telle stratégie s’imposera et s’étendra progressivement à tous les individus de la population. 


Une Colombe qui rencontre Bourgeois gagnera ½ x 0 + ½ x R/2 = R/4
Un Faucon qui rencontre Bourgeois gagnera ½ x R + ½ x(R-B)/2 = R/2 + (R-B)/4
2R/4 + (R-B)/4 = (3R-B)/4

Donc un Bougeois rencontrant Faucon, se comportera une fois sur deux Faucon et l’autre fois Colombe. Son gain sera de ½ x (R-B)/2 + ½ x 0 = (R-B)/4
Un Bourgeois rencontrant Colombe aura un gain de ½ x R + ½ x R/2 = 3R/4
Un Bourgois rencontrant un Bourgeois aura un gain de :

½ x ((R-B)/2 + R) + ½ x (0 + R/2)  = (R-B)/4 + R/2 + R/4 = = (R-B)/4 + 3R/4 = R-B/4


	Faucon	Colombe 	Bourgeois
Faucon	(R-B)/2	R	(3R-B)/4
Colombe	0	R/2	R/4
Bourgeois	(R-B)/4	3R/4	R-B/4

Si par exemple on a R = 50 et B = 100

	Faucon	Colombe 	Bourgeois
Faucon	-25	50	12.5
Colombe	0	25	12.5
Bourgeois	-12.5	37.5	25

Sur une population établie de Bourgeois, un mutant Faucon ou Colombe ne pourra pas envahir, étant donné que ces deux stratégies rapportent 12.5 de gain contre 25 pour Bourgeois. Par contre un mutant Bourgeois envahira une population Colombe ou une population Faucon. La stratégie Bourgeois est une stratégie évolutivement stable car elle n’est pas envahissable.
Les gains qu’induisent un comportement permettent de déterminer quelles stratégies envahiront la population et à quelle fréquence. Bien entendu, les exemples précédemment sont extrêmement schématiques et simplifiés. 

En répétant le jeu de multiples fois, les stratégies peuvent être modifiées. En effet il devient moins intéressant dans le cas du dilemme du prisonnier de trahir si on rejoue. On s’expose à une stratégie de vengeance. Il a été observé que souvent la meilleure stratégie est de coopérer dès le début, puis de copier la stratégie adverse par la suite. S’il coopère on continue de coopérer, s’il trahit, on trahit a notre tour. 

Comme dans les exemples précédents, on peut établir la stratégie qui permettra d'obtenir le plus de gains. Ces gains donnent aux individus une meilleure **fitness** et donc une plus grande probabilité de survivre et de se reproduire.  
Les modèles basés sur ces concepts constituent des outils puissants pour comprendre l'évolution en proposant une mesure de la **valeur sélective**. 


