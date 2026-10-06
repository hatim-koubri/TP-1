# TP1 — Gestion des produits avec JPA et Hibernate

Ce TP montre comment enregistrer et consulter des produits avec **JPA**, **Hibernate** et une base de données **H2 en mémoire**.

## Fonctionnalités

- Création automatique de la table `Produit`.
- Insertion de huit produits avec leur nom et leur prix.
- Affichage de la liste des produits avec une requête JPQL.
- Recherche du produit ayant l’ID `2`.
- Démarrage de la console web H2 sur `http://localhost:8082`.

## Technologies

- Java
- Maven
- JPA 2.2
- Hibernate 5.6.5.Final
- H2 2.1.214

## Exécution

Depuis le dossier du projet, vérifiez la compilation et les tests avec :

```bash
mvn test
```

Puis lancez la classe `com.gr3.App` depuis votre IDE. La base `DBHatim` est configurée en mémoire dans `src/main/resources/META-INF/persistence.xml`.

## Captures des résultats

### 1. Consultation des produits dans la console H2

La requête `SELECT * FROM PRODUIT` affiche les huit produits enregistrés dans la base.

![Résultat de la requête SELECT dans la console H2](images/captures/01-console-h2-produits.png)

### 2. Création de la table et insertion par Hibernate

Les journaux montrent la création de la table `Produit`, puis les requêtes SQL d’insertion générées par Hibernate.

![Création de la table et requêtes d’insertion Hibernate](images/captures/02-creation-et-insertion.png)

### 3. Confirmation de l’insertion et lecture avec JPA

Le programme confirme l’insertion, puis exécute une requête pour récupérer la liste des produits.

![Confirmation de l’insertion et début de la lecture des produits](images/captures/03-insertion-et-lecture.png)

### 4. Liste complète et recherche par identifiant

La sortie affiche les huit produits et le résultat de la recherche du produit ayant l’ID `2` : **Smartphone**.

![Liste des produits et résultat de la recherche par ID](images/captures/04-liste-et-recherche.png)
