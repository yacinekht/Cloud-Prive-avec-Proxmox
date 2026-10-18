<h1 align="center">☁️ Cloud Privé avec Proxmox</h1>

<p align="center">
Projet de virtualisation simulant une infrastructure d'entreprise basée sur Proxmox VE.
</p>

<hr>

<h2>📖 Présentation</h2>

<p>
L'objectif de ce projet est de mettre en place une infrastructure virtualisée reproduisant l'architecture d'une petite entreprise.

Plutôt que d'utiliser un seul serveur pour tous les services, chaque rôle est isolé dans une machine virtuelle dédiée afin d'améliorer la sécurité, la maintenance et l'évolutivité de l'infrastructure.
</p>

<h2>🏗️ Architecture</h2>

<pre>
                    Proxmox VE
                         │
 ┌───────────────────────┼───────────────────────┐
 │                       │                       │
 ▼                       ▼                       ▼

Serveur Web      Serveur Base de Données   Serveur Monitoring
Ubuntu Server       Ubuntu Server          Ubuntu Server
Apache              MySQL                  Grafana
PHP                                         Prometheus
Symfony

                         │
                         ▼

                 Serveur de Sauvegarde
                    Ubuntu Server
                    rsync / Cron
</pre>

<hr>

<h2>🎯 Objectifs du projet</h2>

<ul>
<li>Découvrir la virtualisation avec Proxmox</li>
<li>Administrer plusieurs serveurs Linux</li>
<li>Déployer une application web Symfony</li>
<li>Séparer les services sur plusieurs machines</li>
<li>Mettre en place une base de données distante</li>
<li>Superviser l'infrastructure</li>
<li>Automatiser les sauvegardes</li>
<li>Comprendre l'architecture d'un mini datacenter</li>
</ul>

<hr>

<h2>🖥️ Machines Virtuelles</h2>

<h3>🌐 Serveur Web</h3>

<p><b>Technologies :</b></p>

<ul>
<li>Ubuntu Server</li>
<li>Apache2</li>
<li>PHP</li>
<li>Symfony</li>
</ul>

<p><b>Rôle :</b></p>

<ul>
<li>Hébergement du site web</li>
<li>Traitement des requêtes HTTP</li>
<li>Exécution de l'application Symfony</li>
<li>Communication avec le serveur MySQL</li>
</ul>

<h3>🗄️ Serveur Base de Données</h3>

<p><b>Technologies :</b></p>

<ul>
<li>Ubuntu Server</li>
<li>MySQL Server</li>
</ul>

<p><b>Rôle :</b></p>

<ul>
<li>Stockage des données applicatives</li>
<li>Gestion des requêtes SQL</li>
<li>Administration des utilisateurs et permissions</li>
</ul>

<h3>📊 Serveur Monitoring</h3>

<p><b>Technologies :</b></p>

<ul>
<li>Ubuntu Server</li>
<li>Prometheus</li>
<li>Grafana</li>
</ul>

<p><b>Rôle :</b></p>

<ul>
<li>Collecte des métriques système</li>
<li>Surveillance CPU, RAM et stockage</li>
<li>Création de tableaux de bord</li>
<li>Visualisation de l'état de l'infrastructure</li>
</ul>

<h3>💾 Serveur Backup</h3>

<p><b>Technologies :</b></p>

<ul>
<li>Ubuntu Server</li>
<li>rsync</li>
<li>Cron</li>
</ul>

<p><b>Rôle :</b></p>

<ul>
<li>Sauvegardes automatisées</li>
<li>Archivage des données</li>
<li>Restauration après incident</li>
</ul>

<hr>

<h2>🔗 Communication entre les serveurs</h2>

<h3>Serveur Web ↔ Base de Données</h3>

<pre>
Utilisateur
      │
      ▼
 Apache
      │
      ▼
 Symfony
      │
      ▼
  MySQL
</pre>

<p>
L'application Symfony communique avec MySQL afin de stocker et récupérer les données de l'application.
</p>

<h3>Monitoring ↔ Infrastructure</h3>

<pre>
Prometheus
     │
     ├── Serveur Web
     ├── Serveur MySQL
     └── Serveur Backup
</pre>

<p>
Grafana exploite les métriques collectées afin d'afficher des tableaux de bord de supervision.
</p>

<h3>Sauvegarde ↔ Infrastructure</h3>

<pre>
Serveur Backup
       │
       ├── Fichiers Symfony
       └── Bases MySQL
</pre>

<hr>

<h2>🛠️ Compétences développées</h2>

<ul>
<li>Virtualisation avec Proxmox VE</li>
<li>Administration Linux</li>
<li>Gestion réseau TCP/IP</li>
<li>Configuration Apache</li>
<li>Déploiement Symfony</li>
<li>Administration MySQL</li>
<li>Monitoring avec Grafana et Prometheus</li>
<li>Mise en place de sauvegardes automatisées</li>
<li>Architecture Cloud et Datacenter</li>
<li>Communication inter-serveurs</li>
</ul>

<hr>

<h2>🚀 Évolutions possibles</h2>

<ul>
<li>Mise en place du HTTPS avec Let's Encrypt</li>
<li>Déploiement Docker</li>
<li>Mise en place d'un VPN</li>
<li>Cluster Proxmox</li>
<li>Reverse Proxy</li>
<li>Centralisation des logs</li>
<li>Haute disponibilité (HA)</li>
</ul>

<hr>

<h2>✅ Résultat</h2>

<p>
Ce projet permet de reproduire une infrastructure professionnelle complète basée sur la virtualisation.

Il met en œuvre les notions de Cloud, Réseau, Linux, Virtualisation, Monitoring, Sauvegarde et Administration Système à travers une architecture multi-serveurs gérée par Proxmox VE.
</p>
