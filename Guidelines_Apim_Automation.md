# 📖 Introduction  
Ce document définit les règles et bonnes pratiques pour l’automatisation de la gestion des APIs sur APIM.  

## 🎯 Objectifs  

### 1ère étape Backup & restore
1️⃣  Récupérer l’état actuel de l’APIM et permettre un backup/restore fiable.  
2️⃣  Mettre en place un repo initialisé avec l’App Registration déjà configurée.  
3️⃣  Fournir un pipeline permettant aux équipes produit de livrer leurs APIs sans intervention manuelle.  

### 2ème étape Pipeline
1️⃣  Possibilité de soumettre une demande de validation de contrat API via une PR à la Team API quand uen équipe produit modifie ou ajoute un contrat.
2️⃣  Validation de la PR déclenche le dev de l'équipe produit.
3️⃣  Le dev terminé déclenche une batterie de test(lint...) et pousse dans le repo défini dans l'étape 1.
- Le quota, la backend url doivent être fournis et poussé en même temps 
4️⃣  Du repo un merge des modification ou ajout d'opérations API doit doit être mergé dans l'API concerné. API Seller(offer, product...), API Operator(offer, product...)....
5️⃣  Le merge des contrats doivent être envoyé côté APIM, avec les policies de quota et de backend url + le fichier mergé doit être poussé côté Wordpress.

## 🔧 Prérequis Techniques
1️⃣  Créer une app registration dans Azure 
2️⃣  Avoir un environnement repo/pipeline (tfs) 
3️⃣  Paramétrer les droits dans le projet (devops, repo, pipeline ou autre)
4️⃣  Recueillir les environnement dev des équipes produits pour les connecter avec le pipeline

