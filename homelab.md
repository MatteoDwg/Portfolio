---
layout: projects
title: Homelab
description: "Infrastructure personnelle"
---

<nav id="toc">
  <ul>
    <li><a href="#1-introduction">Introduction</a></li>
    <li><a href="#2-fonctionnalités-principales">Fonctionnalités principales</a></li>
    <li><a href="#3-stack--tools">Stack & Tools</a></li>
    <li><a href="#4-organisation--méthodologie">Organisation & Méthodologie</a></li>
    <li><a href="#5-cicd--environnements">CI/CD & Environnements</a></li>
    <li><a href="#6-avancement-du-projet">Avancement du projet</a></li>
  </ul>
</nav>

<!-- 1. Introduction -->
<section id="intro">
  <h2>Introduction</h2>
  <p>
    Mon homelab sert à apprendre, tester des architectures, héberger des services personnels et fournir un
    environnement de développement proche de la production. Il combine matériel physique (rack / serveurs / switchs),
    virtualisation (Proxmox) et une collection de services conteneurisés.
  </p>

  <!-- schéma global -->
  <figure>
    <img src="images/homelab_overview.png" alt="Vue d'ensemble du Homelab (schéma)" class="zoomable">
    <figcaption>Vue d’ensemble : matériel, virtualisation, réseau et services (schéma simplifié).</figcaption>
  </figure>
</section>

<!-- 2. Matériel & Infrastructure physique -->
<section id="hardware">
  <h2>Matériel & Infrastructure physique</h2>
  <p>Liste synthétique du matériel principal et de l’infrastructure physique.</p>

  <ul>
    <li><strong>Serveurs :</strong> 1-2 nœuds Proxmox (CPU, RAM, stockage)</li>
    <li><strong>Switchs :</strong> switch manageable avec support VLAN</li>
    <li><strong>Routeurs / Firewall :</strong> equipment pour routage et filtrage</li>
    <li><strong>Stockage :</strong> NAS / disques (RAID selon besoin)</li>
    <li><strong>Périphériques :</strong> imprimante 3D (pilotée via OctoPrint), équipements IoT</li>
  </ul>

  <figure>
    <img src="images/homelab_rack.jpg" alt="Photo du rack / serveurs" class="zoomable">
    <figcaption>Photo du rack / armoire serveur (exemple).</figcaption>
  </figure>
</section>

<!-- 3. Réseau -->
<section id="network">
  <h2>Réseau</h2>
  <p>
    Le réseau est segmenté par VLANs pour isoler les zones (infrastructure, services, IoT, DMZ). Un VPN assure
    l’accès distant sécurisé. Le firewall applique des règles entre les segments et filtre l’accès externe.
  </p>

  <figure>
    <img src="images/homelab_network_schema.png" alt="Schéma réseau (VLAN, VPN, firewall)" class="zoomable">
    <figcaption>Schéma réseau : VLANs, firewall, VPN et séparation des environnements.</figcaption>
  </figure>
</section>

<!-- 4. Virtualisation & VMs -->
<section id="virtualization">
  <h2>Virtualisation & VMs (Proxmox)</h2>
  <p>
    Proxmox est l’hyperviseur central. Les services sont déployés dans des VMs ou des conteneurs LXC selon le besoin.
    Quelques VMs clés sont dédiées au développement et à la production.
  </p>

  <!-- tableau VMs -->
  <figure>
    <table>
      <caption>VMs principales</caption>
      <thead>
        <tr>
          <th>Nom</th>
          <th>Rôle</th>
          <th>Services</th>
          <th>Remarques</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>vm-dev</td>
          <td>Développement / staging</td>
          <td>Traefik, Docker, GitLab, GitLab Runner</td>
          <td>Réseau interne, accès restreint</td>
        </tr>
        <tr>
          <td>vm-prod</td>
          <td>Production</td>
          <td>Traefik, Docker (services exposés)</td>
          <td>VM exposée (reverse proxy + NAT)</td>
        </tr>
        <tr>
          <td>vm-monitor</td>
          <td>Monitoring & notifications</td>
          <td>Uptime-Kuma, ntfy</td>
          <td>Alerting interne</td>
        </tr>
      </tbody>
    </table>
    <figcaption>Tableau synthétique des VMs importantes.</figcaption>
  </figure>
</section>

<!-- 5. Services hébergés -->
<section id="services">
  <h2>Services hébergés</h2>
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

  <figure>
    <img src="images/homelab_homepage.png" alt="Homepage / Dashboard" class="zoomable">
    <figcaption>Exemple : dashboard / homepage interne.</figcaption>
  </figure>
</section>

<!-- 6. Déploiement & gestion (Docker-compose) -->
<section id="deployment">
  <h2>Déploiement & gestion</h2>
  <p>
    Les services sont principalement déployés via <strong>Docker Compose</strong>. Les images sont construites localement
    ou récupérées depuis un registre, et lancées sur les VMs appropriées. Les mises à jour sont réalisées manuellement ou via
    scripts d’assistance pour orchestrer restart / backup.
  </p>

  <figure>
    <img src="images/docker-compose-example.png" alt="Extrait docker-compose" class="zoomable">
    <figcaption>Extrait simplifié d’un fichier <code>docker-compose.yml</code> utilisé.</figcaption>
  </figure>
</section>

<!-- 7. Versions (V1 / V2) -->
<section id="versions">
  <h2>Versions & évolution</h2>
  <p>
    <strong>V1</strong> : infrastructure initiale en place (Proxmox, services de base, réseau segmenté).  
    <strong>V2</strong> : en préparation — objectifs : meilleure isolation réseau, montée en performance, automatisation accrue, et rationalisation des backups.
  </p>
</section>

<!-- 8. Objectifs futurs -->
<section id="objectives">
  <h2>Objectifs futurs</h2>
  <ul>
    <li>Automatiser les déploiements et la configuration (ex. Ansible / scripts)</li>
    <li>Renforcer la sécurité réseau et le monitoring</li>
    <li>Documenter et publier certains modèles (playbooks / templates)</li>
    <li>Finaliser V2 (matériel + architecture)</li>
  </ul>
</section>
