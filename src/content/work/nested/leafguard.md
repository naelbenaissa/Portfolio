---
title: LeafGuard
publishDate: 2024-03-06 00:00:00
img: /assets/aLaUne/leafguard.png
img\_alt: LeafGuard image
description: |
  LeafGuard est une application dédiée à l’analyse et à la gestion des plantes.
tags:
  - Flutter
  - Python
  - Supabase
  - Intelligence Artificielle

---

> LeafGuard - Application d'Analyse et de Gestion des Plantes

LeafGuard est une application mobile développée en Flutter qui permet d'identifier les maladies des plantes en prenant
une photo ou en sélectionnant une image depuis son smartphone ou son PC. Grâce à un modèle d'intelligence artificielle
entraîné avec des données issues de Kaggle, l'application fournit un diagnostic précis et des solutions adaptées pour
soigner la plante. L'application offre également des fonctionnalités avancées pour la gestion des soins et la
documentation des plantes.

### Fonctionnalités principales

* **Analyse des maladies** : L'utilisateur peut prendre une photo d'une plante ou choisir une image existante afin
  d'obtenir une identification de la maladie ou une confirmation que la plante est en bonne santé. L'intelligence
  artificielle traite l'image et fournit un retour détaillé sur la pathologie éventuelle ainsi que les traitements
  possibles.

* **Système de favoris** : Les utilisateurs peuvent enregistrer leurs analyses et plantes préférées pour un accès
  et un suivi rapide.

* **Gestion des tâches et soins** : L'application propose d'ajouter automatiquement des soins spécifiques en fonction du
  diagnostic obtenu. Les tâches sont intégrées à un calendrier et peuvent être modifiées ou ajoutées manuellement par
  l'utilisateur.

* **Base de données des plantes** : Une bibliothèque d'informations sur plus de 300 000 plantes est intégrée grâce à l'
  API Trefle. Chaque plante dispose d'une fiche détaillée contenant ses caractéristiques. Un système de favoris permet
  d'enregistrer les plantes.

* **Filtres de recherche** : Les utilisateurs peuvent filtrer leurs analyses et favoris en fonction de plusieurs
  critères pour un accès rapide et efficace aux informations.

* **Notifications et rappels** : Un système de notification intégré rappelle à l'utilisateur les soins à effectuer en
  fonction des tâches enregistrées dans le calendrier.

* **Thèmes personnalisables** : L'application propose un mode clair et un mode sombre pour s'adapter aux préférences des
  utilisateurs.

* **Tutoriel interactif** : Un guide est proposé lors du premier lancement de l'application afin d'aider
  l'utilisateur à comprendre toutes les fonctionnalités.

## Tester l'IA en ligne

Vous pouvez essayer l'intelligence artificielle de LeafGuard directement via une interface web :

<a href="https://leafguardai.naelbenaissa.fr/" target="_blank">Accéder à LeafGuard AI</a>

---

## Technologies utilisées

### Application Flutter

L'application est développée avec Flutter et repose sur plusieurs dépendances essentielles pour assurer son bon
fonctionnement :

```yaml
dependencies:
  flutter:
    sdk: flutter
  go_router: ^14.4.1
  supabase_flutter: ^2.7.0
  cupertino_icons: ^1.0.8
  http: ^1.3.0
  table_calendar: ^3.2.0
  sqflite: ^2.4.2
  path_provider: ^2.1.5
  path: ^1.9.1
  intl: ^0.20.2
  camera: ^0.11.1
  image_picker: ^1.1.2
  introduction_screen: ^3.1.17
  cached_network_image: ^3.4.1
  provider: ^6.1.2

  flutter_local_notifications: ^19.2.1
  timezone: ^0.10.1
  permission_handler: ^12.0.0+1

  shared_preferences: any
  flutter_svg: ^2.1.0

dev_dependencies:
  flutter_test:
    sdk: flutter
  mockito: ^5.4.6
  mocktail: ^1.0.4
  build_runner: ^2.4.15
  flutter_lints: ^4.0.0
  http: any
  flutter_launcher_icons: ^0.14.3
```

## Tests

Le projet LeafGuard intègre une suite de tests automatisés pour assurer la qualité et la robustesse de l'application.  
Les tests couvrent principalement :

- Les tests unitaires des services et des modèles métier.
- Les tests widget pour valider le rendu des interfaces utilisateur.
- Les tests d’intégration pour simuler les flux complets, notamment l’analyse d’image et la navigation.

La stratégie de tests utilise les packages `flutter_test`, `mockito` et `mocktail` pour les mocks et la simulation des dépendances.

Voici un exemple de test unitaire asynchrone qui vérifie que la méthode predictDisease retourne bien une Map contenant la réponse de l’IA après une simulation de requête HTTP.
![Test sur la réponse de l'IA](/assets/leafguard/test_flutter.png)


### Intelligence Artificielle

L'intelligence artificielle de LeafGuard a été développée en Python 3.9.13. Le modèle repose sur des bibliothèques
spécialisées en traitement d'images et apprentissage automatique :

* **TensorFlow** : Utilisé pour la création et l'entraînement du modèle de deep learning.
* **NumPy** : Employé pour la gestion des données et des matrices utilisées dans les calculs du modèle.
* **OpenCV** : Utilisé pour le traitement et la pré-analyse des images avant leur passage dans le modèle.
* **FastAPI** : Framework permettant de transformer le modèle en API exploitable par l'application Flutter.
* **Keras** : Utilisé pour la conception et l'optimisation du réseau de neurones.

L'API est hébergée sur Google Cloud via un conteneur Docker et son code source est accessible sur [GitHub](https://github.com/naelbenaissa/IA_LeafGuard).

#### Performances du modèle

##### 1️⃣ Graphique de précision et de perte

Ce graphique illustre l'évolution des performances du modèle au fil des époques :

* **À gauche** : L'évolution de la précision en entraînement et validation. Le modèle atteint une précision optimale à l’époque 28.
* **À droite** : La diminution progressive des pertes, indiquant une amélioration de l’apprentissage sans sur-ajustement notable.

![Graphique de précision et de perte](/assets/leafguard/graphique_precision_et_perte.png)

##### 2️⃣ Matrice de confusion

Cette matrice met en évidence les performances de classification du modèle sur différentes maladies et plantes saines.

* Les valeurs diagonales montrent les bonnes prédictions.
* Les erreurs sont visibles dans les cases hors diagonale, indiquant les classes nécessitant potentiellement des améliorations.

![Matrice de confusion](/assets/leafguard/matrice_confusion.png)

Vous pouvez tester l'IA à cette adresse : [LeafGuard AI](https://leafguardai.naelbenaissa.fr/)

### Backend et gestion des données

![Image Supabase](/assets/leafguard/supabase-leafguard.png)
L'application utilise Supabase pour :

* L'authentification des utilisateurs
* Le stockage et la gestion des analyses effectuées
* La gestion des favoris et des tâches planifiées

---

## Démonstrations

<video width="100%" controls>
    <source src="/assets/leafguard/video_leafguard.mp4" type="video/mp4">
</video>

---

## Installation

### Installer l'application

L'application n'est pas destinée à être déployée sur les stores, car il s'agit d'un projet académique visant à démontrer
mes compétences.

En attendant, il est possible de la tester localement avec les commandes suivantes :

```bash
git clone https://github.com/naelbenaissa/LeafGuard.git
cd leafguard
flutter pub get
flutter run
```

### Lancer l'API d'intelligence artificielle

```bash
git clone https://github.com/naelbenaissa/IA_LeafGuard.git
cd IA_LeafGuard
pip install -r requirements.txt
uvicorn main:app --reload
```

---

## Prochaines améliorations

* Amélioration du modèle d'intelligence artificielle pour une meilleure précision des diagnostics
* Ajout de nouvelles maladies et traitements dans la base de données
* Possibilité de géolocaliser l'utilisateur et de prendre en compte les conditions climatiques locales afin d’adapter les soins en conséquence.- Intégration d'un support multilingue pour une meilleur accessibilité
* Possibilité de partager les diagnostics avec d'autres utilisateurs

---

## Contribution

Les contributions sont ouvertes à toute amélioration. Il est possible de cloner le projet, de proposer des améliorations
ou d’ouvrir une issue pour signaler un problème.

Dépôt GitHub : [LeafGuard](https://github.com/naelbenaissa/LeafGuard) Dépôt API
IA : [IA LeafGuard](https://github.com/naelbenaissa/IA_LeafGuard)

---

## Documentation technique

Vous pouvez consulter les documents réalisés dans le cadre de ce projet académique :

* [📄 Documentation technique (PDF)](/assets/leafguard/documentation_leafguard.pdf)
* [📝 Rapport de projet (PDF)](/assets/leafguard/rapport_leafguard.pdf)

---

LeafGuard est conçu pour faciliter la gestion et le soin des plantes, en offrant un outil intuitif et puissant basé sur
l'intelligence artificielle.
