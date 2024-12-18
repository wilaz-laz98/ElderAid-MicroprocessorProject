# ARCHITECTURE D'UN SYSTÈME INFORMATIQUE
Ce document met en évidence les étapes essentielles pour architecturer/concevoir un système informatique évolutif, maintenable et efficace. Il s'agit d'un guide pour les professionnels de l'informatique et les architectes système qui souhaitent concevoir un système informatique robuste et évolutif.

# Vision de Produit \-**A PREPARER?**\-
**VISION STATEMENT**:
|**Target**|**Needs**|**Product**|
|----------|---------|-----------|
| gens andicapés|-independace|-braclet:|
|gens agées|-portabilité| buzz button, microphone, capteur de mouvement, battery, localisation, moteur de vibration, GPS --- Controller: emergency alert, SIM|

------------------------------------------------------------------------------------------
## Étape 1 : Définir les exigences du système
La première étape de la conception d'un système informatique consiste à définir les exigences du système. Cela inclut l'identification de l'objectif, des fonctionnalités et des exigences de performance du système. Les exigences du système doivent être documentées de manière claire et concise, y compris les exigences fonctionnelles et non fonctionnelles du système.

### 1. Exigences Fonctionnelles
#### Fonction 01: Détection de Mouvement
- Détecter et enregistrer le mouvement de l'utilisateur.

- Notifier le soignant si l'utilisateur s'éloigne d'une distance prédéfinie.

- Alerter les services d'urgence et le soignant si l'utilisateur tombe.

#### Fonction 02: Détection de Son

- Surveiller et enregistrer en continu le son autour de l'utilisateur.

- Notifier le soignant si l'utilisateur pleure ou si une voix inconnue est détectée.

#### Fonction 03: Bouton d'Urgence

- Fournir un bouton que l'utilisateur peut presser pour appeler à l'aide.

- Annuler les autres capteurs et notifier immédiatement le soignant et les services d'urgence si le bouton est pressé plusieurs fois.

#### Fonction 04: Suivi de Localisation :

- Suivre la localisation exacte de l'utilisateur en temps réel.

- Fournir des mises à jour de localisation au soignant.

#### Fonction 05: Communication :

- Envoyer des notifications SMS au soignant.

- Passer des appels vocaux automatiques aux services d'urgence.

### 2. Exigences Non Fonctionnelles 
#### Scalabilité :
Le système doit pouvoir gérer plusieurs utilisateurs simultanément.

#### Fiabilité :
Assurer une haute disponibilité et fiabilité du système pour une surveillance continue.

#### Sécurité :
Protéger les données des utilisateurs et assurer une communication sécurisée entre les dispositifs et les services.

#### Utilisabilité :
Le système doit être facile à utiliser pour les utilisateurs âgés avec des connaissances techniques minimales.

#### Performance :
Le système doit fournir des alertes et des mises à jour en temps réel sans délais significatifs.

### 3. Cas d'Utilisation \-**A VERIFIER?**\-
#### Cas d'utilisation 1 : lire le mouvement de l'utilisateur

- **Description** : la partie portable du système enregistre constamment le mouvement de l'utilisateur.

- **Étapes** : lire le mouvement, si l'utilisateur s'éloigne de l'endroit où il est censé être, notifier le soignant, si l'utilisateur tombe par terre, contacter les services d'urgence et notifier le soignant, si l'utilisateur ne bouge pas pendant une période prolongée, notifier le soignant.

- **Critères d'acceptation** : Identification réussie du mouvement, lecture d'un comportement anormal de l'utilisateur et envoi d'une demande d'aide.

#### Cas d'utilisation 2 : lire le son de l'utilisateur

- **Description** : la partie portable du système enregistre constamment le son de l'utilisateur.

- **Étapes** : lire le son à travers le microphone, si l'utilisateur pleure de douleur ou si une voix étrangère est détectée, notifier le soignant.

- **Critères d'acceptation** : Identification réussie du son, lecture de sons anormaux de l'utilisateur et notification du soignant.

#### Cas d'utilisation 3 : bouton d'urgence

- **Description** : la partie portable du système contient un bouton poussoir qui, s'il est cliqué plus d'une fois, annule le reste des capteurs et notifie immédiatement le soignant et les services d'urgence.

- **Étapes** : le bouton est poussé 2 fois ou plus, déclarer le statut d'urgence et notifier les soignants.

- **Critères d'acceptation** : Interprétation réussie des clics pour envoyer une demande d'aide.

#### Cas d'utilisation 4 : envoyer une note SMS

- **Description** : l'unité de contrôle du système envoie des notifications par SMS.

- **Étapes** : obtenir le statut de l'utilisateur, notifier le soignant par SMS.

- **Critères d'acceptation** : Message reçu sur le téléphone du soignant.

#### Cas d'utilisation 5 : appeler les services d'urgence

- **Description** : l'unité de contrôle du système est capable de passer un appel vocal automatique aux services d'urgence.

- **Étapes** : obtenir le statut de l'utilisateur, passer un appel téléphonique aux services d'urgence.

- **Critères** d'acceptation : Appel reçu sur la ligne téléphonique d'urgence.

------------------------------------------------------------------------------------------
## Étape 2 : Étude de faisabilité
Une étude de faisabilité est une enquête préliminaire sur la praticabilité d'un système. Elle consiste à évaluer la faisabilité technique, financière et opérationnelle du système. L'étude doit identifier les risques et les défis potentiels associés au système et fournir des recommandations pour les atténuer.

1. **faisabilité technique**

2. **faisabilité financière**

3. **faisabilité opérationnelle**

4. **risques et défis** (optionnel)

5. **recommandations pour l'atténuation** (optionnel)

------------------------------------------------------------------------------------------
## Étape 3 : Conception de l'architecture du système
La conception de l'architecture du système consiste à définir la structure et l'organisation globales du système. Cela inclut l'identification des composants, des interfaces et des flux de données du système. L'architecture du système doit être conçue pour répondre aux exigences du système.

### 1. Conception de Haut Niveau
#### - Matériel
- **Microcontrôleur ESP32**: L'unité centrale de traitement du système.

- **Capteurs de Mouvement** : Pour détecter le mouvement de l'utilisateur.

- **Microphone** : Pour surveiller et enregistrer le son.

- **Bouton d'Urgence** : Pour que l'utilisateur puisse appeler à l'aide.

- **Module GPS** : Pour suivre la localisation de l'utilisateur.

#### - Logiciel
- **Firmware** : Fonctionnant sur l'ESP32 pour gérer les données des capteurs, traiter les alertes et communiquer avec les services externes.

- **Application Mobile** : Pour que les soignants reçoivent des notifications et suivent la localisation de l'utilisateur.

- **Serveur Backend** : Pour gérer le stockage des données, traiter les alertes et gérer la communication avec l'application mobile et les services d'urgence.
#### - Communication

- **Wi-Fi/Bluetooth** : Pour la communication entre l'ESP32 et l'application mobile.

- **Passerelle SMS** : Pour envoyer des notifications SMS.

- **Service VoIP** : Pour passer des appels vocaux automatiques aux services d'urgence.


#### - Flux de Données
1. Collecte des Données des Capteurs : Les capteurs de mouvement et le microphone collectent en continu des données.

2. Traitement des Données : L'ESP32 traite les données pour détecter tout comportement anormal.

3. Génération d'Alerte : Si un comportement anormal est détecté, l'ESP32 génère une alerte.

4. Notification : L'alerte est envoyée au soignant via SMS et la localisation de l'utilisateur est mise à jour dans l'application mobile.

5. Appel d'Urgence : Si nécessaire, un appel vocal automatique est passé aux services d'urgence.

------------------------------------------------------------------------------------------
## Étape 4 : Sélection de la technologie
La sélection de la technologie consiste à choisir les technologies et les outils appropriés pour le système. Cela inclut la sélection des langages de programmation, des bases de données, des systèmes d'exploitation et d'autres composants logiciels. La sélection de la technologie doit être basée sur les exigences du système et la conception de l'architecture du système.

### 1. Matériel 

#### - Serveurs

#### - Stockage

#### - Réseautage

### 2. Logiciel 

#### - Langages de Programmation

#### - Bases de Données

#### - Systèmes d'Exploitation

------------------------------------------------------------------------------------------
## Étape 5 : Mise en œuvre du système
La mise en œuvre du système consiste à construire le système en utilisant les technologies et les outils sélectionnés. Cela inclut l'écriture du code, le test du système et le déploiement du système en production.

### 1. Contrôle de Version

### 2. Développement de Code

### 3. Tests Unitaires

------------------------------------------------------------------------------------------
## Étape 6 : Test du système et assurance qualité
Le test du système et l'assurance qualité consistent à vérifier que le système répond aux exigences du système et fonctionne comme prévu.

### 1. Test du Système

### 2. Assurance qualité

### 3. Test d'Acceptation Par Les Utilisateurs

------------------------------------------------------------------------------------------
## Étape 7 : Déploiement et maintenance du système
Le déploiement et la maintenance du système consistent à déployer le système en production et à s'assurer qu'il continue de fonctionner comme prévu.

### 1. Plan de Déploiement du Système

### 2. Installation du Système

------------------------------------------------------------------------------------------
## Étape 8 : Documentation et formation
La documentation et la formation consistent à créer la documentation pour le système et à fournir une formation aux utilisateurs et au personnel de support.

### 1. Documentation

### 2. Manuels d'Utilisation

### 3. Base de Connaissances
Cette section a de bute de donnée une description resumé de l'ensembles des approches utilisées durant l'execution de ce projet:
#### Framework Agile SCRUM \-**A LIRE?**\-

1. **Préparation et Planification** :

- **Définir la vision du produit** : Identifier les objectifs et les attentes du projet.

- **Former l'équipe Scrum** : Inclure le Product Owner, le Scrum Master et l'équipe de développement.

- **Créer le backlog produit** : Lister toutes les fonctionnalités et exigences du projet.

2. **Sprint Planning** :

- **Définir les objectifs du sprint** : Sélectionner les éléments du backlog produit à réaliser durant le sprint.

- **Planifier les tâches** : Décomposer les éléments sélectionnés en tâches plus petites et attribuer les responsabilités.

3. **Exécution du Sprint** :

- **Développement et tests** : L'équipe travaille sur les tâches planifiées, en suivant les principes de développement agile.

- **Daily Scrum** : Réunions quotidiennes pour synchroniser l'équipe, discuter des progrès et des obstacles.

4. **Revue de Sprint** :

- **Démonstration des fonctionnalités** : Présenter les fonctionnalités développées durant le sprint aux parties prenantes.

- **Collecte de feedback** : Recueillir les retours des parties prenantes pour améliorer le produit.

5. **Rétrospective de Sprint** :

- **Analyse des performances** : Discuter de ce qui a bien fonctionné et des points à améliorer.

- **Plan d'amélioration** : Identifier les actions à mettre en place pour les prochains sprints.

6. **Incrément de produit** :

- **Livraison de l'incrément** : Fournir un produit fonctionnel et potentiellement livrable à la fin de chaque sprint.

**Ces étapes sont répétées à chaque sprint jusqu'à ce que le produit soit complet et prêt à être livré. Scrum permet une gestion flexible et itérative des projets, favorisant l'adaptation aux changements et l'amélioration continue.**


-----------------------------------------------------------------------------------------
## Étape 9 : Révision et évaluation
La dernière étape du processus de conception du système informatique consiste à réviser et évaluer le système pour s'assurer qu'il répond aux exigences du système et fonctionne comme prévu. Cela implique de mener une étude sur les métriques de performance ainsi que la boucle de rétroaction continue.

### 1. Métriques de Performance

### 2. Boucle de Rétroaction Continue



