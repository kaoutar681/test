# tpfourniture

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).



Gestion des Fournitures
Application web interactive pour la gestion des fournitures, développée en utilisant Vue.js. Ce projet permet d'ajouter, de rechercher et de supprimer des fournitures de manière dynamique. Le projet inclut des fonctionnalités de base telles que la validation des formulaires et la manipulation du DOM.
Table des Matières
1.	Fonctionnalités
2.	Installation
3.	Utilisation
4.	Dépendances
5.	Structure du Code
6.	Captures d'écran
7.	Crédits
________________________________________
Fonctionnalités
•	Ajout de Fournitures : Ajoutez des fournitures en spécifiant le nom, la quantité et le fournisseur.
•	Suppression de Fournitures : Supprimez une fourniture de la liste.
•	Recherche en Temps Réel : Recherchez des fournitures en fonction de leur nom.
•	Validation des Formulaires : Les formulaires vérifient les saisies utilisateur pour éviter les erreurs.
•	Interface Réactive et Moderne : Utilisation de Vue.js pour une interactivité et une fluidité optimales.
•	Interface Responsive : L'interface est adaptée pour les appareils mobiles et les ordinateurs de bureau.
Installation
1.	Pré-requis : Assurez-vous que Node.js et npm sont installés sur votre machine.
node -v
npm -v
2.	Installation de Vue CLI : Si Vue CLI n'est pas installé, exécutez la npm install -g @vue/cli
git clone https://github.com/votre-repertoire/gestion-fournitures.git
cd gestion-fournitures
3.	Installez les dépendances :
npm install
4.	Lancez l'application :
npm run serve
5.	Accédez à l'application : Ouvrez votre navigateur et allez sur http://localhost:8080 pour voir l'application en action.
Utilisation
1.	Ajout de fournitures : Remplissez le formulaire avec le nom, la quantité, et le fournisseur puis cliquez sur "Ajouter Fourniture".
2.	Lister les fournitures : La liste des fournitures ajoutées est affichée avec leurs détails
3.	Suppression de fournitures : Cliquez sur le bouton "Supprimer" à côté de chaque fourniture pour la retirer de la liste.
Dépendances
•	Vue.js : Framework JavaScript progressif pour l'interface utilisateur.
•	Font Awesome : Utilisé pour ajouter des icônes dans l'application (si ajouté manuellement).
Toutes les autres dépendances sont listées dans le fichier package.json.
Structure du Code
•	App.vue : Composant principal de l'application, qui inclut le formulaire d'ajout, la liste des fournitures, et la barre de recherche.
•	data() : Définit les données utilisées par le composant, incluant la liste des fournitures et les informations pour le formulaire.
•	methods : Contient les méthodes ajouterFourniture, supprimerFourniture, et d’autres fonctions auxiliaires.
•	computed : Propriété fournituresFiltrees pour gérer la recherche en temps réel.
