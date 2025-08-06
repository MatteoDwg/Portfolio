---
layout: projects
title: "Fritly"
description: "Application interne pour une friterie"
---

<link rel="stylesheet" href="assets/style.css">

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
<div style="margin-bottom: 40px;">
  <p>
    Fritly regroupe tout ce dont les employés ont besoin pour simplifier leur quotidien.
    L’idée est de commencer par les fonctionnalités essentielles et d’élargir progressivement
    en fonction des retours et des besoins réels sur le terrain.
  </p>

  <!-- IMAGE : Schéma des fonctionnalités -->
  <div style="text-align: center; margin: 20px 0;">
    <img src="images/fritly_functionnalities.png" alt="Schéma des fonctionnalités de Fritly" style="max-width: 90%; border-radius: 8px;" class="zoomable">
  </div>

  <p>
    Les fonctionnalités actuellement prévues incluent :
    <ul>
      <li>Gestion des plannings (horaires, absences et remplacements)</li>
      <li>Centralisation des procédures (recettes, nettoyage, organisation des postes)</li>
      <li>Fiches quotidiennes pour le suivi des tâches</li>
      <li>Collecte des suggestions et idées (ex. “burger du mois”)</li>
    </ul>
    De nouvelles idées seront intégrées au fur et à mesure, en fonction des besoins exprimés par les utilisateurs.
  </p>
</div>
---

## 3. Stack & Tools

<div style="margin-bottom: 40px;">
  <p>
    Fritly repose sur une stack moderne, pensée pour offrir une application performante et facile à utiliser,
    tout en restant simple à déployer pour les employés.
  </p>

  <!-- IMAGE : Schéma architecture (Frontend -> Backend -> BDD) -->
  <div style="text-align: center; margin: 20px 0;">
    <img src="images/fritly_architecture.png" alt="Schéma de l'architecture de Fritly" style="max-width: 90%; border-radius: 8px;" class="zoomable">
  </div>

  <h3>Technologies principales</h3>
  <ul>
    <li><strong>Angular :</strong> pour un frontend réactif et ergonomique.</li>
    <li><strong>Spring Boot :</strong> pour un backend robuste et sécurisé.</li>
    <li><strong>PostgreSQL :</strong> pour une base de données fiable et performante.</li>
  </ul>

  <p>
    L’application est développée comme une <strong>PWA (Progressive Web App)</strong>, 
    ce qui permet :
  </p>
  <ul>
    <li>Une installation directe depuis le navigateur (pas besoin d’app store).</li>
    <li>Des mises à jour instantanées pour tous les utilisateurs.</li>
    <li>Une expérience proche du natif tout en restant légère et simple à maintenir.</li>
  </ul>

  <h3>Outils de conception et de gestion</h3>
  <p>Plusieurs outils accompagnent le développement du projet :</p>
  <ul>
    <li><strong>Figma :</strong> pour la création des maquettes UX/UI en collaboration avec le designer.</li>
    <li><strong>Jira :</strong> pour organiser les tâches et suivre la méthode Agile (Scrum simplifié).</li>
    <li><strong>GitLab :</strong> pour la gestion du dépôt et du CI/CD.</li>
    <li><strong>IntelliJ IDEA :</strong> comme IDE principal pour le développement backend.</li>
  </ul>
  
  <div id="lightbox">
    <img id="lightbox-img">
  </div>
  
  <!-- IMAGES : Screens Figma, Jira, GitLab -->
  <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; margin: 20px 0;">
    <img src="images/fritly_figma.png" alt="Maquette Figma de Fritly" style="flex: 1 1 250px; max-width: 300px; border-radius: 8px;" class="zoomable">
    <img src="images/fritly_jira.png" alt="Aperçu Jira du projet Fritly" style="flex: 1 1 250px; max-width: 300px; border-radius: 8px;" class="zoomable">
    <img src="images/fritly_gitlab.png" alt="Dépôt GitLab du projet Fritly" style="flex: 1 1 250px; max-width: 300px; border-radius: 8px;" class="zoomable"> 
  </div>
</div>

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
