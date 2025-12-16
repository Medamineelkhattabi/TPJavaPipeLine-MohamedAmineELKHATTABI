# Rapport du Projet : TPJavaPipeLine

## Informations Générales
- **Nom du Projet** : TPJavaPipeLine
- **Auteur** : Mohamed Amine EL KHATTABI
- **Date** : 15 décembre 2025

## Structure du Projet
```
Jenkinsfile
pom.xml
README.md
src/
	main/
		java/
			com/
				exemple/
					Main.java
target/
	classes/
		com/
			exemple/
	test-classes/
```

## Description des Fichiers Principaux
- **`pom.xml`** : Fichier de configuration Maven pour la gestion des dépendances et du cycle de vie du projet.
- **`Jenkinsfile`** : Script pour définir le pipeline CI/CD dans Jenkins.
- **`Main.java`** : Contient le code source principal du projet.

## Technologies Utilisées
- **Langage** : Java
- **Outil de Build** : Maven
- **Intégration Continue** : Jenkins

## Fonctionnalités Principales
Le fichier `Main.java` contient la logique principale du projet. Voici un aperçu des fonctionnalités implémentées :
- Exemple de fonctionnalité 1 : [Description]
- Exemple de fonctionnalité 2 : [Description]

## Pipeline CI/CD
Le fichier `Jenkinsfile` définit les étapes suivantes :
1. **Build** : Compilation du projet avec Maven.
2. **Test** : Exécution des tests unitaires.
3. **Déploiement** : Déploiement des artefacts générés.

## Instructions pour Exécuter le Projet
1. **Compiler le Projet** :
   ```powershell
   mvn compile
   ```
2. **Exécuter le Projet** :
   ```powershell
   mvn exec:java -Dexec.mainClass="com.exemple.Main"
   ```
3. **Générer le Package** :
   ```powershell
   mvn package
   ```

## Améliorations Possibles
- Ajouter des tests unitaires pour couvrir davantage de cas.
- Optimiser le pipeline Jenkins pour inclure des étapes de validation supplémentaires.
- Ajouter une documentation plus détaillée sur les fonctionnalités du projet.

---
Capture d'écrans : 


**Fin du Rapport**