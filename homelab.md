---
layout: projects
title: Homelab
description: "Infrastructure personnelle"
---

<nav id="toc">
  <ul>
    <li><a href="#1-introduction">Introduction</a></li>
    <li><a href="#2-materiel--infrastructure-physique">Materiel & Infrastructure physique</a></li>
    <li><a href="#3-réseau">Réseau</a></li>
    <li><a href="#4-virtualisation--vms-proxmox">Virtualisation & VMs (Proxmox)</a></li>
    <li><a href="#5-services-hébergés">Services hébergés</a></li>
    <li><a href="#6-déploiement--gestion">Déploiement & gestion</a></li>
    <li><a href="#7-versions--évolution">Versions & évolution</a></li>
    <li><a href="#8-objectifs-futurs">Objectifs futurs</a></li>
  </ul>
</nav>

<div id="lightbox">
  <img id="lightbox-img">
</div>

<!-- 1. Introduction -->
## 1. Introduction
<div style="margin-bottom: 40px;">
  <p>
    Mon homelab sert à apprendre, tester des architectures, héberger des services personnels et fournir un
    environnement de développement proche de la production. Il combine matériel physique (rack / serveurs / switchs),
    virtualisation (Proxmox) et une collection de services conteneurisés.
    <br/><br/>
    Pour des raisons de sécurité, certaines informations ont été modifiées ou généralisées. Les schémas et descriptions ne reflètent donc pas exactement la configuration réelle de mon homelab.
  </p>

  <!-- schéma global -->
  <div style="text-align:center;display: flex;flex-direction: column;align-items: center;margin: 20px 0;">
    <img src="images/homepage_dashboard.png" alt="Dashboard gethomepage.dev" class="zoomable zoomable-item" style="max-width: 70%;">
    <p class="caption">Dashboard gethomepage.dev.</p>
  </div>
</div>

<!-- 2. Matériel & Infrastructure physique -->
## 2. Materiel & Infrastructure physique
<div style="margin-bottom: 40px;">
  <p>Liste synthétique du matériel principal et de l’infrastructure physique.</p>

  <ul>
    <li><strong>Serveurs :</strong> 1 serveur Proxmox (3 VMs), un laptop et 2 Raspberry pi</li>
    <li><strong>Switchs :</strong> 3 switchs manageables</li>
    <li><strong>Routeurs / Firewall :</strong> 1 Ubiquiti ER-X</li>
    <li><strong>Périphériques :</strong> imprimante classique, imprimante 3D, équipements IoT</li>
  </ul>

  <div style="text-align:center;display: flex;flex-direction: column;align-items: center;margin: 20px 0;">
    <img src="images/homelab_rack.png" alt="Photo du rack / serveurs" class="zoomable zoomable-item" style="max-width: 30%">
    <p class="caption">Photo du rack / armoire serveur (non contractuelle).</p>
  </div>
</div>

<!-- 3. Réseau -->
## 3. Réseau
<div style="margin-bottom: 40px;">
  <p>
    Mon homelab repose sur une architecture réseau segmentée afin d’isoler les usages et renforcer la sécurité.<br/>
    Plusieurs VLAN sont utilisés pour séparer les environnements (production, développement, IoT, invités, etc.), avec un pare-feu configuré pour limiter la communication entre les segments.<br/>
    L’accès distant est sécurisé via un VPN et des tunnels sécurisés, ce qui permet de gérer les services à distance tout en minimisant l’exposition directe sur Internet.<br/>
    Un DNS interne facilite la résolution des noms locaux, tandis qu’un DNS public gère les services accessibles depuis l’extérieur. Les certificats SSL sont déployés automatiquement pour garantir un chiffrement bout-à-bout.
  </p>

  <div style="text-align:center;display: flex;flex-direction: column;align-items: center;margin: 20px 0;">
    <img src="images/homelab_schema.png" alt="Vue d'ensemble du Homelab (schéma)" class="zoomable zoomable-item" style="max-width: 80%;">
    <p class="caption">Vue d’ensemble : matériel, réseau et services (non contractuelle).</p>
  </div>
</div>

<!-- 4. Virtualisation & VMs -->
## 4. Virtualisation & VMs (Proxmox)
<div style="margin-bottom: 40px;">
  <p>
    Mon homelab repose sur une infrastructure virtualisée avec Proxmox.
    J’y héberge plusieurs machines virtuelles, chacune ayant un rôle bien défini :
  </p>

  <ul>
    <li>VM Développement : environnement dédié à la gestion et au déploiement d’applications en phase de test.</li>
    <li>VM Production : héberge les applications stables et opérationnels.</li>
    <li>VM Multi-services : regroupe certains outils et applications utilitaires.</li>
  </ul>

  Cette séparation permet d’isoler les environnements, de limiter les risques en cas d’incident, et de segmenter l’utilisation des ressources matérielles dans le réseau.

<!-- 5. Services hébergés -->
## 5. Services hébergés
<div style="margin-bottom: 40px;">
  <p>Principaux services organisés par catégorie.</p>

  <h4>Administration & Dev</h4>
  <ul>
    <li>GitLab (dépôt & CI), GitLab Runner</li>
    <li>Portainer (gestion Docker)</li>
    <li>Traefik (reverse proxy)</li>
    <li>homepage.dev (page d’accueil interne)</li>
  </ul>

  <h4>Sécurité & Auth</h4>
  <ul>
    <li>Bitwarden (vault)</li>
    <li>Authentik (SSO / gestion identités)</li>
    <li>Pi-hole (filtrage DNS)</li>
  </ul>

  <h4>Surveillance & Notifications</h4>
  <ul>
    <li>Uptime-Kuma (monitoring temps réel)</li>
    <li>ntfy (notifications)</li>
  </ul>

  <h4>Perso / Divers</h4>
  <ul>
    <li>OctoPrint (imprimante 3D)</li>
    <li>Serveur Minecraft</li>
    <li>Slash (outil perso)</li>
    <li>Cloudflared (tunnel / DNS) et autres outils d’accès</li>
  </ul>

  <div style="text-align:center;display: flex;flex-direction: column;align-items: center;margin: 20px 0;">
    <img src="images/homelab_homepage.png" alt="Homepage / Dashboard" class="zoomable zoomable-item">
    <p class="caption">Exemple : dashboard / homepage interne.</p>
  </div>
</div>

<!-- 6. Déploiement & gestion (Docker-compose) -->
## 6. Déploiement & gestion
<div style="margin-bottom: 40px;">
  <p>
    Les services sont principalement déployés via <strong>Docker Compose</strong>. Les images sont construites localement
    ou récupérées depuis un registre, et lancées sur les VMs appropriées. Les mises à jour sont réalisées manuellement ou via
    scripts d’assistance pour orchestrer restart / backup.
  </p>

  <div style="text-align:center;display: flex;flex-direction: column;align-items: center;margin: 20px 0;">
    <img src="images/docker-compose-example" alt="Extrait docker-compose" class="zoomable zoomable-item">
    <p class="caption">Extrait simplifié d’un fichier <code>docker-compose.yml</code> utilisé.</p>
  </div>
</div>

<!-- 7. Versions (V1 / V2) -->
## 7. Versions & évolution
<div style="margin-bottom: 40px;">
  <p>
    <strong>V1</strong> : infrastructure initiale en place (Proxmox, services de base, réseau segmenté).  
    <strong>V2</strong> : en préparation — objectifs : meilleure isolation réseau, montée en performance, automatisation accrue, et rationalisation des backups.
  </p>
</div>

<!-- 8. Objectifs futurs -->
## 8. Objectifs futurs
<div style="margin-bottom: 40px;">
  <ul>
    <li>Automatiser les déploiements et la configuration (ex. Ansible / scripts)</li>
    <li>Renforcer la sécurité réseau et le monitoring</li>
    <li>Documenter et publier certains modèles (playbooks / templates)</li>
    <li>Finaliser V2 (matériel + architecture)</li>
  </ul>
</div>
