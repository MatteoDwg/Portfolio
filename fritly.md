---
layout: default
title: "Fritly"
---

<!-- Projet 1 -->
<div style="display: flex; align-items: center;">
  <div style="flex: 1;">
    <h3>Fritly – Application interne pour une friterie</h3>
    <p>
      <strong>Contexte :</strong> Travaillant dans une friterie depuis plusieurs années, j’ai remarqué de nombreuses tâches redondantes (gestion du planning, procédures internes, recettes, etc.) qui pouvaient être centralisées dans un outil unique. J’ai décidé de créer une application interne pour centraliser ces informations et simplifier la gestion quotidienne.<br>
      <strong>Fonctionnalités principales :</strong><br>
      <ul>
        <li>Gestion et visualisation des plannings.</li>
        <li>Consultation des procédures (postes, nettoyages, recettes).</li>
        <li>Accès aux fiches d’actions quotidiennes et recettes spéciales du mois.</li>
      </ul>
      <strong>Architecture et outils :</strong><br>
      <ul>
        <li>PWA pour unifier desktop et mobile sans développement natif.</li>
        <li>Angular + Spring + PostgreSQL : un stack robuste, modulaire et maintenable pour gérer à la fois l’interface, l’API et la base de données.</li>
        <li>CI/CD avec GitLab déployé automatiquement sur mon homelab pour simuler un environnement de production réel.</li>
        <li>Organisation et suivi du projet via Jira, développement sur IntelliJ IDEA.</li>
      </ul>
      Rôle : Développement complet (analyse, conception, backend, frontend, infrastructure) en collaboration avec un designer UI/UX.
    </p>
    <p>
      Ce projet m’a permis de mettre en place une architecture complète :
      pipeline CI/CD, orchestration des services avec Docker,
      gestion de projet via Jira, et un déploiement automatisé.
    </p>
  </div>
  <div style="flex: 1; text-align: center;">
    <img src="images/fritly.png" alt="Fritly Screenshot" width="300">
  </div>
</div>
