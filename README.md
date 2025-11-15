# Base de Données pour la Gestion d'un Blog  
Une base de données MySQL pour la gestion d'un Blog. Il contient les structures et données nécessaires pour gérer les Articles, les Commentaires et les utilisateurs par les Admins.

## Description  
Cette base de données a été conçue pour gérer un système de blog avec des fonctionnalités complètes telles que :  
- Gestion des utilisateurs  
- Publication d'articles  
- Archivage des articles  
- Ajout de commentaires  
- Système de likes  
- Gestion des tags  
- Mise en liste noire des utilisateurs  

---

## Structure de la Base de Données  

### ⚙️ Tables Principales  
1. **User** : Gère les informations des utilisateurs.  
2. **Article** : Stocke les articles publiés par les utilisateurs.  
3. **Archive** : Contient les articles archivés.  
4. **Likes** : Permet d'enregistrer les likes des utilisateurs.  
5. **Tags** : Stocke les mots-clés (tags) associés aux articles.  
6. **Article_Tage** : Table intermédiaire pour gérer la relation **articles ↔ tags**.  
7. **Commentaire** : Stocke les commentaires ajoutés par les utilisateurs.  
8. **Black_Liste** : Gère les utilisateurs bannis ou mis en liste noire.  

---

##  Relations Entre les Tables  

| **Relation**          | **Explication**                                         |  
|------------------------|---------------------------------------------------------|  
| `User ↔ Article`       | Un utilisateur peut publier plusieurs articles.         |  
| `Article ↔ Archive`    | Un article peut être archivé.                           |  
| `Article ↔ Likes`      | Un utilisateur peut aimer plusieurs articles.          |  
| `Article ↔ Tags`       | Un article peut avoir plusieurs tags (relation n..n).  |  
| `User ↔ Commentaire`   | Un utilisateur peut ajouter plusieurs commentaires.    |  
| `User ↔ Black_Liste`   | Un utilisateur peut être ajouté à la liste noire.      |  

---

