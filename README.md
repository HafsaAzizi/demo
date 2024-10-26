# demo
# Projet CRUD avec Spring Boot et Thymeleaf

Ce projet est une application Web CRUD utilisant Spring Boot et Thymeleaf pour gérer des entités d'utilisateurs. Il permet l'ajout, la mise à jour, la suppression et l'affichage d'utilisateurs, en mettant en œuvre les couches de service, de référentiel et de présentation.

## Technologies utilisées

- **Java 1.8**
- **Spring Boot 2.2.6.RELEASE**
- **Thymeleaf**
- **Spring Data JPA**
- **MySQL**

## Configuration

1. **Définir les dépendances Maven**  
   Le fichier `pom.xml` inclut les dépendances pour Spring Boot, Thymeleaf, JPA, et MySQL.  
   Exemple de configuration dans `pom.xml`:

  ``` xml
   <dependency>
       <groupId>org.springframework.boot</groupId>
       <artifactId>spring-boot-starter-data-jpa</artifactId>
   </dependency>
   <dependency>
       <groupId>mysql</groupId>
       <artifactId>mysql-connector-java</artifactId>
       <scope>runtime</scope>
   </dependency>
  ``` 
   

2. **Configuration de la base de données

Le fichier application.properties doit contenir les informations de connexion MySQL :
properties
```
spring.datasource.url=jdbc:mysql://localhost:3306/thymeleaf
spring.datasource.username=root
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

##Structure du projet

Modèle (User) : Classe User annotée avec @Entity pour représenter les utilisateurs.
Référentiel (UserRepository) : Interface qui étend CrudRepository pour les opérations CRUD.
Contrôleur (UserController) : Gère les requêtes HTTP pour créer, lire, mettre à jour et supprimer les utilisateurs.
Vue (Thymeleaf) : Fichiers HTML situés dans src/main/resources/templates pour afficher et gérer les entités utilisateur.


##Exécution du projet
Pour exécuter le projet, lancez la classe principale DemothymeleafApplication :
```
@SpringBootApplication
public class DemothymeleafApplication {
    public static void main(String[] args) {
        SpringApplication.run(DemothymeleafApplication.class, args);
    }
}
```

Accédez ensuite à http://localhost:8080 dans un navigateur pour interagir avec l'application.

##Fonctionnalités

** Ajouter un utilisateur : Accédez à /signup pour remplir le formulaire d'ajout.

** Mettre à jour un utilisateur : Utilisez le lien "Edit" pour modifier un utilisateur existant.

** Supprimer un utilisateur : Utilisez le lien "Delete" pour supprimer un utilisateur.

** Lister les utilisateurs : La page d'accueil affiche tous les utilisateurs avec des options de gestion.
