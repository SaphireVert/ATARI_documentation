## 02.05.2023
### Visite de l'expert TPI n°1
Durant cette séance, l'expert a expliqué le protocol du déroulement du TPI et fourni une copie du cahier des charges. Le cahier des charges a été signé par le candidat, l'expert et le chef de projet.
__Catégorie__ Communications avec les experts/chefs de projet
__Durée__ : 30 min

### Création planning initial
Le cahier des charges a été analysé de manière approfondie afin d'avoir une vue d'ensemble du travail à réaliser. Celui-ci a ensuite été découpé en tâches qui ont été placées dans l'ordre le plus judicieux possible. La méthodologie de gestion de projet pour ce TPI a été choisie. Il s'agit de la méthode en cascade. Le planning initial a été créé en utilisant l'outil [Instagantt](https://app.instagantt.com).
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
Une recherche a été effectuée sur le site web de la librairie [material-ui](https://mui.com/) de react car il est probable qu'il existe déjà un composant permettant de faire de l'autocomplétion sur une liste. Un des composants disponibles se nommait "[Autocomplete](https://mui.com/material-ui/react-autocomplete)", ce qui semble correspondre aux besoins du projet. Après recherche approfondir, il en ressort même qu'il est possible d'y intégrer [react-window](https://github.com/bvaughn/react-window),  une librairie permettant de virtualiser le dom de la liste, ce qui permet de grandement limiter les ressources nécessaire au rendu de celle-ci lorsqu'elle est mise à jour (à chaque fois qu'un caractère est rajouté ou enlevé). Cet aspect est d'autant plus important lorsque l'on travaille avec des grandes listes, ce qui sera le cas dans ce projet. Il permet également de réduire la quantité de mémoire utilisée en évitant d'allouer trop de noeuds du DOM. Tout cela va nous permettre d'avoir une application TRÈS réactive, et donc agréable à utiliser pour l'utilisateur final. Un exemple d'implémentation de la fonctionnalité avec une liste de 10000 entrées générées aléatoirement, est disponible [ici](https://mui.com/material-ui/react-autocomplete/#virtualization). Il a été réutilisé dans le projet. La fonctionnalité est disponible à l'essai dans un [codesandbox](https://codesandbox.io/s/r43d57?file=/demo.tsx). La principale difficulté dans cette partie était de trouver quels étaient les bons éléments de mui et où ils étaient sur le site et de trouver les bonnes props à utiliser, elles sont disponibles [ici](https://mui.com/material-ui/api/autocomplete/) notamment pour récupérer la saisie de l'utilisateur et comment intégrer tout ça dans le code du projet. Beaucoup de débogage a du être fait et il y a eu quelques problèmes de types typescript. Une difficulté supplémentaire était d'adapter le code d'exemple de la virtualisation de la liste pour le faire fonctionner avec des données du projet au lieu d'une liste générée aléatoirement. 
__Catégorie__ : Recherche de personnes
__Durée__ : 6h

### Rapport de TPI
Avancement du rapport. La partie "méthodologie de gestion de projet" a été faite et la partie "analyse" a été commencée.
__Catégorie__ : Documentation
__Durée__ : 1h

### Bilan journée
Résultats obtenus très satisfaisants pour le projet. Beaucoup de marge avait été gardée pour l'initialisation du projet en cas d'imprévu, mais qui a pour finir été terminée en avance. Le temps précieux libéré a permis de travailler plus longtemps que prévu sur la fonctionnalité "recherche de personnes".

## 04.05.2023

### Recherche de personnes
Implémentation de la fonctionnalité de "détection du type de saisie". La principale difficulté était l'utilisation des Regex pour reconnaître des patterns. L'utilisation de stackoverflow pour en chercher des exemples, comme [celui-ci](https://stackoverflow.com/a/9011554) pour détecter lorsque la chaine de caractères ne contient que des chiffres ainsi que du site web [Regex101](https://regex101.com/) pour les tester, ont été d'une grande utilié. 

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
Les résultats obtenus sont satisfaisants. Cependant, des difficultés ont été ressenties lorsqu'il a fallu utiliser des regex pour des reconnaissances de patterns.

## 09.05.2023

### Recherche de personnes
Avancement dans la fonction recherche de personnes. Le champ se rempli tout seul lorsque l'utilisateur fait des recherches dans le champ et qu'il ne reste qu'un seul résultat parmi les suggestions. Le composant déclenche automatiquement une fonction qui sera utilisée pour afficher l'utilisateur en question. Beaucoup de difficultés ont été rencontrées durant cette phase d'implémentations.
__Catégorie__ : Recherche de personnes
__Durée__ : 7h30