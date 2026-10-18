<h1 align="center">☁️ Private Cloud Infrastructure with Proxmox</h1>

<p align="center">
  Personal project focused on Virtualization, Linux Administration, Networking and Cloud Infrastructure.
</p>

<hr>

<h2>📖 Project Overview</h2>

<p>
This project consists of building a private cloud infrastructure using Proxmox VE.
The objective is to reproduce a small enterprise architecture by separating services across multiple virtual machines.
</p>

<h2>🏗️ Infrastructure Architecture</h2>

<pre>
                    Proxmox VE
                         │
 ┌───────────────────────┼───────────────────────┐
 │                       │                       │
 ▼                       ▼                       ▼

Web Server        Database Server      Monitoring Server
Ubuntu Server     Ubuntu Server        Ubuntu Server
Apache            MySQL                Grafana
PHP                                     Prometheus
Symfony

                         │
                         ▼

                   Backup Server
                   Ubuntu Server
                   rsync
                   Cron
</pre>

<h2>🎯 Project Objectives</h2>

<ul>
  <li>Understand virtualization concepts</li>
  <li>Deploy and manage virtual machines</li>
  <li>Build a multi-server infrastructure</li>
  <li>Separate services across dedicated servers</li>
  <li>Configure Linux environments</li>
  <li>Implement monitoring solutions</li>
  <li>Automate backups</li>
  <li>Learn enterprise network architecture</li>
</ul>

<hr>

<h2>🖥️ Virtual Machines</h2>

<h3>🌐 Web Server</h3>

<p><b>Technologies:</b></p>

<ul>
  <li>Ubuntu Server</li>
  <li>Apache2</li>
  <li>PHP</li>
  <li>Symfony</li>
</ul>

<p><b>Role:</b></p>

<ul>
  <li>Host the web application</li>
  <li>Process HTTP requests</li>
  <li>Execute PHP code</li>
  <li>Communicate with the database server</li>
</ul>

<h3>🗄️ Database Server</h3>

<p><b>Technologies:</b></p>

<ul>
  <li>Ubuntu Server</li>
  <li>MySQL Server</li>
</ul>

<p><b>Role:</b></p>

<ul>
  <li>Store application data</li>
  <li>Manage SQL queries</li>
  <li>Handle user data</li>
</ul>

<h3>📊 Monitoring Server</h3>

<p><b>Technologies:</b></p>

<ul>
  <li>Ubuntu Server</li>
  <li>Grafana</li>
  <li>Prometheus</li>
</ul>

<p><b>Role:</b></p>

<ul>
  <li>Monitor infrastructure health</li>
  <li>Collect performance metrics</li>
  <li>Display dashboards and analytics</li>
</ul>

<h3>💾 Backup Server</h3>

<p><b>Technologies:</b></p>

<ul>
  <li>Ubuntu Server</li>
  <li>rsync</li>
  <li>Cron Jobs</li>
</ul>

<p><b>Role:</b></p>

<ul>
  <li>Automated backups</li>
  <li>Data protection</li>
  <li>Disaster recovery</li>
</ul>

<hr>

<h2>🔗 Inter-VM Communication</h2>

<h3>Web ↔ MySQL</h3>

<pre>
User
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
The web application communicates with the MySQL server to store and retrieve application data.
</p>

<h3>Monitoring ↔ Infrastructure</h3>

<pre>
Prometheus
    │
    ├── Web Server
    ├── Database Server
    └── Backup Server
</pre>

<p>
Grafana uses collected metrics to generate dashboards and visualize server performance.
</p>

<h3>Backup ↔ Infrastructure</h3>

<pre>
Backup Server
      │
      ├── Web Server Files
      └── MySQL Backups
</pre>

<hr>

<h2>🛠️ Skills Demonstrated</h2>

<ul>
  <li>Proxmox VE Administration</li>
  <li>Linux Server Administration</li>
  <li>Virtualization</li>
  <li>TCP/IP Networking</li>
  <li>Apache Configuration</li>
  <li>PHP Deployment</li>
  <li>Symfony Hosting</li>
  <li>MySQL Administration</li>
  <li>Infrastructure Monitoring</li>
  <li>Backup & Recovery</li>
  <li>Cloud Infrastructure Design</li>
</ul>

<hr>

<h2>📚 Technologies Used</h2>

<p align="center">

<img src="https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColorg src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&white
<img src="https://img.shields.io/badge/Apache-D22128?style=for-theo=apache&logoColor=white
<img src="https://img.shields.io/badge/PHP-777BB4?style=for-theo=php&logoColor=white
<img src="https://img.shields.io/badge/Symfony-000000?style=for&logo=symfony&logoColor=white
<img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&white
<img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&white
<img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=&logoColor=white

</p>

<hr>

<h2>✅ Project Outcome</h2>

<p>
Design and deployment of a complete virtualized infrastructure simulating a small enterprise environment.
The project demonstrates practical experience in virtualization, systems administration, networking, monitoring and backup management using industry-standard technologies.
</p>
