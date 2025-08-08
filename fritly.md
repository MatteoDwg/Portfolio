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

- gérer facilement les horaires, absences et remplacements,
- centraliser toutes les informations utiles (procédures, fiches quotidiennes, etc.),
- et poser les bases pour ajouter d’autres fonctionnalités au fur et à mesure des besoins.

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
  <div class="tool-gallery">
    <div class="tool-item">
      <img src="images/jira.png" alt="Board Jira" class="zoomable zoomable-item">
      <p class="caption">Suivi de projet et gestion des sprints avec Jira.</p>
    </div>
    <div class="tool-item">
      <img src="images/figma.png" alt="Maquette Figma" class="zoomable zoomable-item">
      <p class="caption">Prototypage et design des interfaces avec Figma.</p>
    </div>
    <div class="tool-item">
      <img src="images/gitlab.png" alt="GitLab CI/CD" class="zoomable zoomable-item">
      <p class="caption">Gestion du code, intégration continue et déploiement via GitLab.</p>
    </div>
  </div>
</div>

---

## 4. Organisation & Méthodologie
<div style="margin-bottom: 40px;">
  <h3>Introduction à Agile et Scrum</h3>
  <p>
    Agile Scrum est une méthode de gestion de projet qui privilégie la flexibilité et l’adaptation.<br/>  
    Plutôt que de planifier un projet en entier dès le départ, Scrum découpe le travail en cycles courts, appelés <em>sprints</em>.<br/>  
    À la fin de chaque sprint, on obtient une version fonctionnelle du produit, permettant d’ajuster rapidement les priorités en fonction des retours.
  </p>

  <div style="text-align:center;display: flex;flex-direction: column;align-items: center;">
    <img src="images/scrum_agile.png" alt="Cycle scrum" class="zoomable zoomable-item" style="max-width: 80%;">
    <p class="caption">Cycle de la méthode Scrum.</p>
  </div>

  <h3>Notre adaptation de Scrum</h3>
  <p>
    Sur Fritly, nous appliquons Scrum de manière adaptée à notre contexte.<br/>  
    Nous ne réalisons pas de réunions quotidiennes (« daily scrums »), car nous travaillons à temps partiel sur le projet et chacun avance selon ses disponibilités. <br/>  
    À la place, nous faisons des points ponctuels pour faire le bilan, réaligner les objectifs et ajuster le backlog si nécessaire.
  </p>

  <h3>Gestion des versions : MVP et au-delà</h3>
  <p>
    Actuellement, nous sommes en phase de <strong>MVP</strong> (Minimum Viable Product).<br/>  
    Cela signifie que nous développons d’abord une base solide avec les fonctionnalités essentielles pour rapidement tester le produit. <br/>  
    Après cette étape, nous prévoyons un développement itératif, avec des ajouts, améliorations et corrections, toujours guidés par les retours utilisateurs.
  </p>

  <h3>Qui travaille sur Fritly ?</h3>
  <p>
    Le projet est porté par deux personnes :  
    <ul>
      <li>je m’occupe du développement, du déploiement, de la gestion du CI/CD, de l’analyse et de la planification,</li>
      <li>tandis qu’un ami graphiste est responsable du design UX/UI.</li>
    </ul>
    Cette organisation nous permet de couvrir l’ensemble des besoins du projet malgré notre petite équipe.
  </p>
</div>
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
