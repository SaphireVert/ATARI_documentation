## 02.05.2023
### Visite de l'expert TPI n°1
Durant cette séance, l'expert a expliqué le protocol du déroulement du TPI et fourni une copie du cahier des charges. Le cahier des carges a été signé par le candidat, l'expert et le chef de projet.
__Catégorie__ Communications avec les experts/chefs de projet
__Durée__ : 30 min

### Création planning initial. 
Le cahier des charges a été analysé de manière approfondie afin d'avoir une vue d'ensemble du travail à réaliser. Celui-ci a ensuite été découpé en tâches qui ont été placées dans l'ordre le plus judicieux possible. La méthodologie de gestion de projet pour ce TPI a été choisie. Il s'agit de la méthode en cascade.
__Catégorie__ : Documentation
__Durée__ : 5h

### Rapport de TPI
Creation des premiers éléments de structure de base du document. L'introduction a été rédigée. La rubrique "mise en contexte" a également été rajoutée.
__Catégorie__ : Documentation
__Durée__ : 2h30

### Divers
Aménagement de l'espace de travail afin de permettre un bon workflow.
Conception et réalisation d'un système de backup adapté au projet. Création d'un dépôt github qui servira pour la sauvegarde, l'archivage et la gestion de version de la documentation.
__Catégorie__ : Divers
__Durée__ : 2h

### Communications par mail
Envoi planning initial + rapport + journal de travail aux experts
__Catégorie__ : Communications avec les experts/chefs de projet
__Durée__ : 30min

__Bilan journée__ : 
La difficulté aujourd'hui était d'avoir une vision à la fois globale, détaillée et approfondie du projet car il s'agit d'un pré-requis pour concevoir un planning initial de qualité, qui sera le fil rouge à suivre pour le reste du TPI. Le respect des horaires du TPI aujourd'hui a échoué en raison d'une charge de travail plus grande qu'anticipée. Certains points mentionnés dans les critères d'évaluation (dont la gestion de version de la doc, utilisation correcte de git et de la méthodologie de gestion de projet, ergonomie de l'espace de travail) ont nécessité des dispositions et du temps d'analyse supplémentaire afin d'avoir de très bonnes bases établies dès le départ sachant qu'ils sont pour certains difficilement rattrapables, voire pas rattrapables du tout s'ils ne sont pas bien faits dès le départ du TPI.

__Total heures supplémentaires__ : 2h



## 03.05.2023

## Initialisation du dépot
Création du dépôt git du projet. Ce dernier est forké du dépot react.starterkit (dépôt sert de base de développement pour les applications react conçues à l'EPFL pour l'EPFL). Les éléments "génériques" de l'application tels que le titre et les menus du bord sont remplacés par ceux du future IDP-EXOP. 
__Catégorie__ : Initialisation projet
__Durée__ : 1h

## Recherche de personnes
L'API n'est pas encore connecté à la base de données 'CADI_HELPDESK'. Il a fallu créer un [bouchon](https://fr.wikipedia.org/wiki/Bouchon_(informatique)) pour fournir des fausses données au champ de recherche de personnes. Il s'agit d'un substitut temporaire de l'API qui n'existe pas encore. 
Le site web de la librairie [material-ui](https://mui.com/) de react. Je trouve un composant "Autocomplete" qui semble faire exactement ce que je veux faire. Je constate qu'il est même possible d'y intégrer la librairie [react-window](https://github.com/bvaughn/react-window) qui permet de virtualiser la liste, ce qui permet de grandement limiter le temps nécessaire pour faire le rendu lorsqu'on travaille sur des grandes listes. Il permet également de réduire la quantité de mémoire utilisée en évitant d'allouer trop de noeuds du DOM. Tout cela va nous permettre d'avoir une application TRES réactive, et donc agréable à utiliser pour l'utilisateur final, tout en laissant de davantage de possibilités de rajout de fonctionnalités à l'avenir sans pour autant avoir un impact sur les performances.
La principale difficulté dans cette partie était de trouver quels étaient les bons éléments de mui et où ils étaient sur le site et de trouver les bonnes props à utiliser et comment intégrer tout ça dans mon code à moi. J'ai dû faire plein de débugage et j'ai eu pas mal de problèmes de types en typescript et j'ai dû lire le code pour faire de la retroingénierie et pouvoir comprendre le comportement du composant et interférer dans le comportement du code d'exemple pour y injecter mes propres éléments de logique.

__Catégorie__ : Initialisation projet
__Durée__ : 6h

### Rapport de TPI
Avancement du rapport. J'ai eu le temps de faire la partie "methodologie de gestion de projet" et commencé la partie "analyse"
__Catégorie__ : Documentation
__Durée__ : 1h

__Bilan journée__ : Je suis content car j'ai pu bien avancer et j'ai même pris de l'avance dans la partie initialisation du projet. Avance très précieuse car elle m'a permis de prendre de l'avance sur une tâche que je devrai faire plus tard. J'avais gardé beaucoup de marge pour l'initialisation du projet en cas d'imprévu et de difficuttés d'intégration des librairies externes que j'ai utilisées mais pour finir je n'en n'ai même pas eu besoin. Côté recherche de personnes, la fonction de recherche avec virtualisation de la liste fonctionne sur des données bidon. 



Cela permet de travailler sans même avoir une API fonctionnelle. Il J'en profite même pour aller un peu plus loin (car il me reste du temps) pour préparer une collection dans mon back-end qui enverra les bonnes données au champ à terme mais qui pour le moment elle est juste remplie de quelques valeurs bidon servant juste à faire un un "proof of concept".

## 04.05.2023

### Recherche de personnes
Implémentation de la fonctionnalité de "détection du type de saisie". La principale difficulté était l'utilisation des Regex. S'en est suivi une tentative d'implémentation de l'affichage automatique dès lors qu'il ne reste plus qu'un utilisateur dans la liste des suggestions. La tentative n'a pas marché. Il ne reste plus qu'à rajouter une limite de nombre de résultats et de détecter dès que le nombre de resultats restants est égal à 1.
__Catégorie__ : Recherche de personnes
__Durée__ : 4h

### Séance avec le chef de projet
Une séance a été faite avec le chef de projet pour faire le point sur l'état d'avancement du projet ainsi que d'autres éléments. (c.f. procès verbal 04.04.2023)
__Catégorie__ : Séances
__Durée__ : 1h

### Documentation
La documentation a été avancée : 
- Chaque élément du cahier des charges a été passé en revue, réinterprété et documenté dans le rapport.
- Rédaction du procès verbal de la séance avec le chef de projet.
__Catégorie__ : Documentation
__Durée__ : 3h

### Bilan journée
Tout s'est déroulé comme prévu, sauf lorsqu'il a fallu utiliser des regex ainsi que lors de l'implémentation de la fonctionnalité de détection de la "dernière suggestion restante". Il s'agit d'un échec pour aujoud'hui, mais il reste encore des pistes à explorer pour la faire fonctionner.