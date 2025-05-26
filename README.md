Auteur

- Nom: MEBENGA OWONA
- Prenom : MICHEL STEPHANE
- Matricule: 24p767


#  TP Java – Gestion d'Événements Distribués

Projet académique en Java visant à modéliser un système de gestion d'événements (conférences, concerts) avec interface graphique.

##  Fonctionnalités

- Création et annulation d’événements
- Inscription de participants
- Notifications en temps réel (Observer)
- Interface utilisateur en Java Swing
- Sauvegarde en JSON (Jackson)
- Tests unitaires (JUnit 5)

###  Technologies utilisées

- Java 11+
- Swing
- Jackson
- JUnit 5
- Maven


#### Structure du projet (description)

- `pom.xml` : fichier de configuration Maven, avec les dépendances (JUnit, Jackson, etc.)
- `README.md` : fichier d’explication du projet
- `evenements.json` : fichier de sauvegarde des événements au format JSON
- `src/main/java/model/` : contient les classes principales comme `Evenement`, `Conference`, `Concert`, `Participant`, etc.
- `src/main/java/observer/` : contient l'interface `ParticipantObserver` et la classe `EvenementObservable` pour le pattern Observer
- `src/main/java/service/` : contient la classe `GestionEvenements` implémentée en Singleton
- `src/main/java/exception/` : contient les exceptions personnalisées comme `CapaciteMaxAtteinteException`
- `src/main/java/persistence/` : contient la classe `JsonUtil` pour sauvegarder/charger les événements en JSON
- `src/main/java/async/` : contient `AsyncNotifier` pour envoyer les notifications en différé
- `src/main/java/ui/` : contient l'interface graphique Swing (`EvenementApp`)
- `src/test/java/tests/` : contient les tests unitaires JUnit (`EvenementTest`)
- `target/` : dossier généré automatiquement par Maven lors de la compilation (à ne pas modifier)



##### Tests

- Fichier : `test/tests/EvenementTest.java`
- Objectifs : couverture ≥ 70% (inscription, erreurs, persistance)

###### Lancer le projet

1. Ouvrir dans un IDE
2. Vérifier Maven
3. Lancer `ui.EvenementApp`
4. Exécuter les tests avec `mvn test`


