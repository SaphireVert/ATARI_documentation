## 02.05.2023
### Séance avec l'expert TPI n°1
L'expert a expliqué le protocol du déroulement du TPI. Donné une copie du cahier des charges. Le candidat, l'expert et le chef de projet ont signé le cahier des carges.
__Catégorie__ Communications avec les experts/chefs de projet
__Durée__ : 30 min

### Création planning initial. 
Pour ce faire, le cahier des charges a été analysé de manière approfondie afin d'avoir une vue d'ensemble du travail à réaliser. Celui-ci a ensuite été découpé en tâches qui ont été placées dans l'ordre le plus judicieux possible. Cette tâche fait partie de l'"analyse" et de la "conception" dans la méthode de gestion de projet en cascade.
__Catégorie__ : Documentation
__Durée__ : 5h

### Communications par mail
Envoi planning initial + rapport + journal de travail
__Catégorie__ : Communications avec les experts/chefs de projet
__Durée__ : 30min

### Rapport de TPI
Creation des premiers éléments de structure de base du document + introduction + mise en contexte + objectifs
__Catégorie__ : Documentation
__Durée__ : 2h30

### Divers
Aménagement de l'espace de travail afin de permettre un bon workflow.
Conception et réalisation d'un système de backup adapté au projet.
__Catégorie__ : Divers
__Durée__ : 2h


__Bilan journée__ : 
La difficulté aujourd'hui était d'avoir une idée précise du projet dans sa globalité, afin de pouvoir rédiger correctement le planning initial, qui sera le fil rouge à suivre pour le reste du TPI. Le respect des horaires du TPI aujourd'hui a échoué en raison d'une charge de travail plus grande qu'anticipée, car certains points mentionnés dans les critères d'évaluation (dont la gestion de version de la doc, utilisation correcte de git et de la méthodologie de gestion de projet, ergonomie espace de travail) ont nécessité des dispositions et du temps d'analyse supplémentaire afin d'avoir de très bonnes bases établies dès le départ car hélas, ils sont pour certains difficilement rattrapables s'ils ne sont pas bien faits dès le départ du TPI.

__Total heures supplémentaires__ : 2h



## 03.05.2023 (À réécrire plus joliment)

## Initialisation du dépot
Création du dépôt git sur lequel je vais travailler pour mon projet. 
Pour cela je fais un fork d'un dépot "starterkit" qui sert de bundle pour les applications react de l'EPFL. Création de "boutons" https://www.wikiwand.com/fr/Bouchon_(informatique) pour mon champ de recherche dans lequel je mets le stricte nécessaire pour faire des tests et faire fonctionner ma fonctionnalité. J'en profite même pour aller un peu plus loin (car il me reste du temps) pour préparer une collection dans mon back-end qui enverra les bonnes données au champ à terme mais qui pour le moment elle est juste remplie de quelques valeurs bidon servant juste à faire un un "proof of concept".
__Catégorie__ : Initialisation projet
__Durée__ : 3h

## Recherche de personnes
Commencement de la fonctionnalité de recherche de personnes intelligente avec autocomplétion. Je me dis que ça sert à rien de réinventer la roue et que je peux utiliser des trucs déjà faits en regardant notamment dans la librairie material-ui (mui) de react. Je trouve un composant "Autocomplete" qui semble faire exactement ce que je veux faire. Je constate qu'il est même possible d'y intégrer la librairie [react-window](https://github.com/bvaughn/react-window) qui permet de virtualiser la liste, ce qui permet de grandement limiter le temps nécessaire pour faire le rendu lorsqu'on travaille sur des grandes listes. Il permet également de réduire la quantité de mémoire utilisée en évitant d'allouer trop de noeuds du DOM. Tout cela va nous permettre d'avoir une application TRES réactive, et donc agréable à utiliser pour l'utilisateur final, tout en laissant de davantage de possibilités de rajout de fonctionnalités à l'avenir sans pour autant avoir un impact sur les performances.
La principale difficulté dans cette partie était de trouver quels étaient les bons éléments de mui et où ils étaient sur le site et de trouver les bonnes props à utiliser et comment intégrer tout ça dans mon code à moi. J'ai dû faire plein de débugage et j'ai eu pas mal de problèmes de types en typescript et j'ai dû lire le code pour faire de la retroingénierie et pouvoir comprendre le comportement du composant et interférer dans le comportement du code d'exemple pour y injecter mes propres éléments de logique.

__Catégorie__ : Initialisation projet
__Durée__ : 4h

### Rapport de TPI
Avancement du rapport. J'ai eu le temps de faire la partie "methodologie de gestion de projet" et commencé la partie "analyse"
__Catégorie__ : Documentation
__Durée__ : 1h

__Bilan journée__ : Je suis content car j'ai pu bien avancer et j'ai même pris de l'avance dans la partie initialisation du projet. Avance très précieuse car elle m'a permis de prendre de l'avance sur une tâche que je devrai faire plus tard. J'avais gardé beaucoup de marge pour l'initialisation du projet en cas d'imprévu et de difficuttés d'intégration des librairies externes que j'ai utilisées mais pour finir je n'en n'ai même pas eu besoin.