# Synchroniser les voisins avec une API 

Dans ce TP, vous allez intégrer une API permettant de synchroniser les voisins avec un serveur distant. 

## Concepts et notions 
- Retrofit
- JSON
- API

## Partie 1 : Mise en place d'un server d'application 
Pour commencer, vous allez travailler avec un serveur locale, ce qui vous permettra de l'enrichir en fonction de vos besoins. 
Pour cela, vous pouvez récupérer les sources du serveur NodeJS via le repository [https://github.com/eamosse/neighbors_api]

1. Forker le repository afin d'en créer une copie pour votre groupe
2. Suivre les étapes du README pour lancer le serveur

## Partie 2: Intégrer l'API dans votre application 
Dans cette partie, vous allez modifier votre application pour y ajouter une troisième source de données. 

1. Reprendre les sources du TP précédent et modifier le remote pour pointer vers ce repository;
2. Mettre en place un service permettant de communiquer avec votre serveur local en utilisant la librairie Retrofit
3. Configurer le repository et le menu de l'application pour prendre en compte cette 3e source
4. Mettre à jour la base de données locales avec les données de l'API

N.B: Sentez-vous libre d'adapter les sources du serveur en fonction des besoins de votre application. 

## Partie 3: Rendre votre application autonome 
Dans cette partie, vous allez modifier le comportement de l'application pour qu'elle détermine automatiquement la bonne source de données à utiliser en fonction de la configuration du téléphone. 

1. Mettre en place un mécanisme de monitoring de la connectivité du téléphone.
   a. Si aucune connexion internet n'est disponible (i.e. mode offline), utiliser les données de la base de données locales
   b. Si au contraire, le téléphone est connecté à internet, utiliser les données de l'API
2. Afficher une notification (dans la bare de statut du téléphone) indiquant à l'utilisateur qu'il n'a pas accès à internet et que l'application fonctionne uniquement avec des données locales
3. Mettre en place un mécanisme de synchronisation automatique, permettant d'envoyer les données modifiées en mode offline vers les serveur quand la connection internet est rétablie
4. Ajouter un indicateur sur la liste des voisins permettant d'identifier ceux qui ont été modifiés en mode offline

## Bonus 
- Utiliser un service d'hébergement Cloud pour déployer votre serveur Web
- Mettre en place un mécanisme d'authentification sur l'API (e.g. Oauth2)

## Rendu
- Veuiller à faire votre dernier commit avant la deadline (voir assignation)
- Ajouter dans le README le lien vers le repo de votre serveur 
