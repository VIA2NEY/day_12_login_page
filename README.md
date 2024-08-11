## Flutter Beautiful Login Page UI Design and Animation - Day 12

Ce projet Flutter est une interface utilisateur de connexion avec des animations de fondu pour améliorer l'expérience utilisateur. 

[Watch it on Youtube](https://youtu.be/NHAIiAmxTAU)

## Development Setup
Clone the repository and run the following commands:
```
flutter pub get
flutter run
```

## ScreenShots

<img src="assets/screenshot/one.png" height="500em" />

## Structure du Projet

**lib/**: Contient le code source de l'application.

- **main.dart**: Point d'entrée principal de l'application.
- **home_page.dart**: Contient la structure et la logique de la page de connexion.
- **animation/**:
  - **fade_animation.dart**: Définit une animation de fondu utilisée dans l'interface utilisateur.

## Description des Fichiers

<details>
<summary>1.1 main.dart</summary>

- **main.dart** : Ce fichier est le point d'entrée principal de l'application. Il initialise l'application Flutter et définit le thème de base. Il spécifie également le widget principal qui sera affiché, qui dans ce cas est `HomePage`.

</details>

<details>
<summary>1.2 home_page.dart</summary>

- **home_page.dart** : Ce fichier contient la structure de la page de connexion de l'application. Voici une explication des différentes parties :

    - **HomePage** : C'est un widget stateless qui représente la page de connexion. 
        - **Scaffold** : Le widget principal qui fournit la structure de base visuelle de la page.
        - **SingleChildScrollView** : Permet le défilement lorsque le contenu dépasse la taille de l'écran.
        - **Container** : Utilisé pour les éléments de mise en page, y compris le fond d'écran et les éléments superposés.
        - **Stack** : Permet de superposer plusieurs widgets les uns sur les autres.
            - **Positioned** : Positionne les widgets à des emplacements spécifiques dans la pile.
            - **FadeAnimation** : Applique une animation de fondu aux widgets enfants. Utilisé pour les images et le texte dans le conteneur de fond d'écran.
        - **Padding** : Ajoute un espacement autour des éléments de la colonne principale.
        - **Column** : Dispose les éléments verticalement.
        - **TextField** : Champs de saisie pour l'email et le mot de passe.
        - **Text** : Affiche le texte "Login" et "Forgot Password?" avec des styles spécifiques.
        - **FadeAnimation** : Applique des animations de fondu aux champs de texte et au bouton de connexion.

</details>

<details>
<summary>1.3 fade_animation.dart</summary>

- **fade_animation.dart** : Ce fichier définit une animation de fondu personnalisée. Voici une explication de la classe principale :

    - **FadeAnimation** : C'est un widget stateless qui applique une animation de fondu à son enfant.
        - **delay** : Délai avant le début de l'animation.
        - **child** : Widget enfant qui reçoit l'animation.
        - **tween** : Définit les propriétés animées, telles que l'opacité et le déplacement horizontal.
        - **PlayAnimationBuilder** : Utilisé pour créer une animation basée sur les valeurs définies dans le `tween`. Gère la transition de l'opacité et du décalage horizontal du widget enfant.

</details>
