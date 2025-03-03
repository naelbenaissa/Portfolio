---
title: GSB
publishDate: 2025-05-07 00:00:00
img: /assets/aLaUne/gsb.jpg
img_alt: Image de la page d'accueil de GSB Frais.
description: |
  GSB est une plateforme web complète qui facilite la gestion centralisée et efficace des données médicales numériques, répondant aux besoins spécifiques des professionnels de la santé.
tags:
  - Angular
  - Laravel
  - Santé
---

## GSB, plus qu'un service

> GSB est une application Full-Stack conçue pour optimiser la gestion des données médicales numériques, offrant une
> solution centralisée et efficace adaptée aux besoins des professionnels de la santé.

#### [Testez l'application !](https://gsb.naelbenaissa.fr/)

Identifiant de test : "Villechalane", mot de passe : "secret"

identifiant en mode admin : "Andre", mot de passe : "secret"

### Une interface intuitive

L'interface utilisateur de la page GSB est conçue avec une approche moderne et esthétique, intégrant les principes de
conception de Bootstrap pour assurer une expérience utilisateur optimale.

Chaque élément visuel est soigneusement
positionné pour garantir une navigation fluide et intuitive. Les boutons et les éléments interactifs sont disposés de
manière réfléchie, facilitant ainsi l'accès aux fonctionnalités principales de l'application.

En combinant l'esthétique visuelle avec la convivialité de Bootstrap, la page GSB offre aux utilisateurs une expérience
moderne et agréable,
favorisant ainsi une utilisation de toutes les fonctionnalités proposées.

![Image de la page de connexion](/assets/gsb/gsb-home-connect.png)

#### Backend Laravel :

> ##### Le backend Laravel offre une architecture robuste pour gérer les données et fournir une API sécurisée aux clients frontaux. Il se compose de modèles de données bien structurés et d'endpoints définis pour des fonctionnalités telles que la gestion des visites médicales et des régions géographiques.

- Laravel MVC pour une gestion efficace des modèles, des vues et des contrôleurs.
- Utilisation de Web Services pour fournir une API RESTful sécurisée.
- Utilisation de Bootstrap pour le style et la mise en forme.

#### [Testez l'application Backend !](https://gsbcore.naelbenaissa.fr/)

Identifiant de test : "Villechalane", mot de passe : "secret"

#### Frontend Angular :

> ##### Le frontend Angular fournit une interface utilisateur moderne et réactive pour interagir avec l'API Laravel. Il comprend des composants Angular pour afficher les données des visiteurs médicaux et des régions géographiques, ainsi que des fonctionnalités avancées telles que la recherche et l'édition.

- Utilisation de TypeScript pour un développement plus sécurisé et plus productif.
- Intégration de HttpClient pour les requêtes HTTP vers le backend.
- Utilisation de Bootstrap et d'une feuille de style personnalisée pour la mise en page et le style.

#### [Testez l'application Frontend !](https://gsb.naelbenaissa.fr/)

### Une application web sécurisée

La sécurité est une priorité absolue dans le projet GSB, notamment lors des échanges de données sensibles. Pour garantir
un niveau de sécurité élevé, nous utilisons des tokens d'authentification pour vérifier l'identité des utilisateurs. Ces
tokens sont générés de manière aléatoire et sont requis pour accéder aux ressources protégées de l'API Laravel.

De plus, toutes les informations échangées entre le frontend Angular et le backend Laravel sont au format JSON, un
format structuré qui facilite la sécurisation des données. Le JSON offre une meilleure lisibilité et une manipulation
simplifiée des données, tout en permettant une validation plus rigoureuse.

En ce qui concerne la gestion des mots de passe, ceux-ci sont stockés de manière sécurisée en utilisant le hachage.
Lorsqu'un utilisateur se connecte, le mot de passe fourni est comparé avec sa version hachée enregistrée dans la base de
données. Cela garantit que même en cas de compromission de la base de données, les mots de passe des utilisateurs
restent confidentiels et ne peuvent pas être récupérés en clair.

![Image du code API](/assets/gsb/gsb-token-code.png)

### Intégration d'Angular Material

Dans le contexte de GSB, Angular Material a été largement utilisé pour améliorer l'expérience utilisateur en fournissant
une gamme d'éléments prêts à l'emploi, notamment des champs de saisie intuitifs, des popups interactifs et des icônes
visuellement attrayantes. L'intégration d'Angular Material a permis d'optimiser la convivialité de l'interface
utilisateur tout en offrant une esthétique moderne et uniforme à travers l'ensemble de l'application.

![Image de la page de recherche](/assets/gsb/research.png)

### Fonctionnalités Avancées

Les fonctionnalités avancées de la page GSB comprennent la possibilité de gérer les frais et les frais hors forfait,
d'effectuer des modifications sur les activités, de rechercher des données avec des filtres spécifiques, et de mettre à
jour les informations de l'utilisateur.

Cette gamme de fonctionnalités offre aux utilisateurs une expérience complète en
leur permettant de saisir, modifier et supprimer les données relatives aux frais, d'effectuer des
recherches ciblées pour obtenir des résultats précis, et de mettre à jour leurs informations personnelles en toute
simplicité.

![Image de la page d'inscription](/assets/gsb/inscription.png)

### Maîtrise de Laravel et Angular

Ce projet démontre ma compétence dans le développement web avec les frameworks Laravel et Angular. Acquises durant mes
cours en 2ème année de BTS et en autodidacte, ces compétences illustrent ma capacité à apprendre et à appliquer des
technologies avancées
pour créer des applications web fonctionnelles et esthétiques.

D'autres projets réalisés avec Angular et Laravel ont été développés, tels que <a href="/work/pokedex">Pokedex</a>
et <a href="/work/nested/estimify">Estimify</a>.

En résumé, le projet GSB que j'ai développé témoigne de ma capacité à concevoir et développer des applications web
modernes en utilisant les frameworks Laravel et Angular, tout en créant une expérience utilisateur conviviale. Pour plus
de détails, vous pouvez consulter <a href="https://github.com/naelbenaissa/GSBCore" target="blank">le code source
Laravel </a>et
<a href="https://github.com/naelbenaissa/GSB" target="blank">le code source Angular.</a>