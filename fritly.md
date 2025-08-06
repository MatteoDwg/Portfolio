---
layout: projects
title: "Fritly"
description: "Application interne pour une friterie"
---


## 1. Introduction

### Pourquoi ce projet ?
Après plusieurs années à travailler dans une friterie, j’ai réalisé qu’une bonne partie du quotidien pouvait être simplifiée. Les plannings se faisaient souvent à la main, les procédures étaient éparpillées et il n’existait pas d’outil centralisé pour tout rassembler.

### L’objectif
Créer une application pensée pour les employés :

gérer facilement les horaires, absences et remplacements,

centraliser toutes les informations utiles (procédures, fiches quotidiennes, etc.),

et poser les bases pour ajouter d’autres fonctionnalités au fur et à mesure des besoins.

### Une collaboration
Je développe l’application, tandis qu’un ami graphiste/designer s’occupe de l’UX/UI. L’idée est d’allier fonctionnalité et ergonomie dès le départ.

---

## 2. Fonctionnalités principales
- Gestion des plannings par poste de travail  
- Accès aux recettes et procédures opérationnelles  
- Saisie et suivi des fiches quotidiennes  
- Vote et affichage des “burgers/sandwichs du mois”  

**Focus sur le design des plannings :**  
*(Explique brièvement les choix faits pour rendre cette fonctionnalité intuitive : code couleur, ergonomie, lisibilité, etc.)*

*(Image : schéma des fonctionnalités principales)*

---

## 3. Stack & Tools
### Stack technologique
- **Frontend** : *(préciser la techno, ex. React, Vue, etc.)*  
- **Backend** : *(préciser la techno, ex. Node.js, Laravel, etc.)*  
- **Base de données** : *(préciser, ex. PostgreSQL, MySQL, etc.)*  
- **Type d’application** : PWA (Progressive Web App) pour un accès simple et multiplateforme.

*(Si pertinent, expliquer pourquoi tu as choisi une PWA.)*

### Outils
- **GitLab** : dépôt de code et gestion des branches  
- **GitLab CI/CD** : intégration et déploiement automatisés  
- **Docker** : build et déploiement des environnements  
- **Jira** : gestion du backlog et suivi des tâches (Scrum simplifié)  
- **Figma** : conception des maquettes UX/UI  

*(Image : screenshot Jira)*  
*(Image : screenshot GitLab)*  
*(Image : capture Figma)*

---

## 4. Organisation & Méthodologie
- Méthode **Scrum simplifiée** : backlog, itérations courtes, priorisation des fonctionnalités essentielles.  
- Répartition des rôles :
  - **Moi** : développement complet, CI/CD, déploiement  
  - **Collaborateur** : UX/UI et design des interfaces (via Figma)

---

## 5. CI/CD & Environnements
- **Branches Git** : `dev` pour les développements, `main` pour la production  
- **Pipeline GitLab CI/CD** :  
  - Lancement des tests automatiques  
  - Build Docker de l’application  
  - Déploiement automatique selon la branche (dev ou prod)

*(Schéma : fonctionnement du pipeline CI/CD)*  
*(Schéma : architecture app - Frontend → Backend → Base de données)*

---

## 6. Avancement du projet
- **Déjà réalisé** : *(liste rapide, ex. maquettes Figma, base de l’API, premier prototype frontend, pipeline CI/CD configuré, etc.)*  
- **En cours / à venir** :
  - Développement complet des fonctionnalités
  - Tests utilisateurs internes
  - Déploiement en production
  - Améliorations basées sur les retours des employés
