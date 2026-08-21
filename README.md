<div align="center">

<!-- Bannière avec effet de frappe — palette bleu nuit -->
<img src="assets/header.svg" alt="Clément Sauzède — BTS SIO SISR" width="100%"/>

<br/>

<!-- Badges de statut -->
[![Statut](https://img.shields.io/badge/Statut-Recherche_stage_2e_année-193B63?style=for-the-badge)](mailto:sauzede.clement@gmail.com)
[![Localisation](https://img.shields.io/badge/Localisation-Clermont--Ferrand-315B7D?style=for-the-badge)](https://www.google.com/maps/search/?api=1&query=Clermont-Ferrand)
[![Formation](https://img.shields.io/badge/BTS_SIO-Option_SISR-0B1628?style=for-the-badge)](https://c-sauzede.netlify.app/)

</div>

---

## 🎯 À propos

```yaml
identite:
  nom: "Clément Sauzède"
  statut: "Étudiant en 2e année de BTS SIO — option SISR"
  etablissement: "Lycée Sidoine Apollinaire — Clermont-Ferrand"
  objectif: "Stage de 2e année — Support, Systèmes & Réseaux"
  passions: ["Homelab & virtualisation", "Télémétrie automobile", "Automatisation", "IA locale"]
```

> 💡 **En quelques mots :** je conçois et maintiens une infrastructure virtualisée sur mon homelab (cluster Proxmox, conteneurs Docker, VPN WireGuard, supervision), et je développe des outils web autour de la donnée en temps réel et de l'automatisation.

---

<!-- Terminal simulé -->
<details open>
<summary>🖥️ <b>Terminal du homelab — <code>clement@homelab:~$ neofetch</code></b></summary>

```text
       _,met$$$$$gg.          clement@homelab
    ,g$$$$$$$$$$$$$$$P.       -------------------------------
  ,g$$P"     """Y$$.".        Hôte        : Cluster Proxmox VE — 2 nœuds
 ,$$P'              `$$$.     Avant       : VMware ESXi + vCenter
',$$P       ,ggs.     `$$b:   Conteneurs  : Docker (Heimdall, Nginx Proxy Manager,
`d$$'     ,$P"'   .    $$$                  Uptime Kuma, AdGuard, Netdata, WoL)
 $$P      d$'     ,    $$P    Réseau      : WireGuard (accès distant PC + mobile)
 $$:      $$.   -    ,d$$'                · OPNsense (déploiement prévu)
 $$;      Y$b._   _,d$P'      Supervision : Netdata · Uptime Kuma
 Y$$.    `.`"Y$$$$P"'         Poste       : ThinkPad P14s · VMware Workstation
 `$$b      "-.__              Formation   : BTS SIO SISR — Sidoine Apollinaire
  `Y$$                        Objectif    : Stage 2e année — Support / Sys / Réseaux
   `$$b.
     `Y$$b.
        `"Y$b._
            `"""
```

</details>

---

## 🛠️ Compétences techniques

<div align="center">

### Systèmes, réseaux & infrastructure
<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=debian,linux,windows,powershell,bash,docker,nginx,git,githubactions" alt="Stack systèmes et réseaux" />
</a>

### Supervision & développement
<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=prometheus,grafana,py,nodejs,js,html,css,sqlite,postman" alt="Stack supervision et développement" />
</a>

</div>

<br/>

| Domaine | Outils & technologies |
|:---|:---|
| **🖥️ Systèmes** | `Windows`, `Linux (Debian)`, `Windows Server (bases)`, `Bash`, `PowerShell` |
| **☁️ Virtualisation** | `Proxmox VE (cluster)`, `VMware ESXi`, `vCenter`, `VMware Workstation` |
| **🛡️ Réseaux & sécurité** | `TCP/IP`, `DNS`, `WireGuard`, `Nginx`, `Packet Tracer` |
| **🐳 Conteneurs** | `Docker`, `Docker Compose`, `Portainer` |
| **📈 Supervision** | `Netdata`, `Uptime Kuma`, `Prometheus`, `Grafana` |
| **⚡ Développement** | `Python`, `JavaScript`, `HTML/CSS`, `SQL`, `Node.js (bases)` |

---

## 🚀 Projets

<div align="center">

### 🏎️ Télémétrie de course en direct
*Récupération, traitement et affichage en direct de données de session automobile sur une interface web personnelle.*

`Python` `Node.js` `HTML/CSS/JS` `Temps réel`

---

### 🌐 [Portfolio personnel](https://c-sauzede.netlify.app/)
*Site vitrine responsive présentant mon parcours, mes compétences et mes projets techniques.*

`HTML5` `CSS3` `JavaScript` `Netlify`

---

### 🏠 Homelab — infrastructure & sécurité *(documentation publique en préparation)*
*Cluster Proxmox à 2 nœuds : VM et conteneurs Docker, VPN WireGuard, supervision et services auto-hébergés.*

`Proxmox VE` `Docker` `WireGuard` `Monitoring`

---

### 🤖 OpenJarvis — assistant IA local *(prototype — dépôt privé)*
*Assistant vocal local : LLM servi en local, transcription faster-whisper, synthèse vocale et actions système contrôlées.*

`Python` `LLM local` `Voice AI` `PowerShell`

</div>

---

## 🕹️ Mini-jeu : l'incident sysadmin

> **📟 Alerte :** `CRITICAL — node01 : CPU 100 % · latence > 850 ms · Nginx 502 Bad Gateway`
>
> Que faites-vous ?

<details>
<summary>👉 <b>Option A :</b> rebooter sauvagement le serveur (appui long sur l'alimentation)</summary>

> ❌ **Mauvais choix.** Redémarrage brutal, aucune donnée de diagnostic collectée, risque de corruption des VM et des conteneurs. L'incident se reproduira sans que vous sachiez pourquoi.

</details>

<details>
<summary>👉 <b>Option B :</b> ouvrir une session SSH de secours et lancer <code>htop</code> + <code>journalctl -xe</code></summary>

```bash
# Analyse
clement@homelab:~$ htop
# Constat : un conteneur Docker de test boucle des requêtes en continu

# Remédiation
clement@homelab:~$ docker stop container_rogue
clement@homelab:~$ systemctl restart nginx
clement@homelab:~$ curl -I https://homelab.local
HTTP/2 200 OK   # 🎉 Service rétabli
```

> 🏆 **Bonne analyse.** Diagnostic avant action, remédiation ciblée, production rétablie sans perte.

</details>

<details>
<summary>👉 <b>Option C :</b> « c'est un problème DNS » et aller prendre un café ☕</summary>

> ☕ **Statistiquement, c'est souvent DNS… mais pas cette fois.** Sans vérification, c'est une hypothèse, pas un diagnostic. (Et le café ne répare pas Nginx.)

</details>

---

## 📊 Activité GitHub

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Klemz-696&show_icons=true&hide_border=true&count_private=true&title_color=315B7D&icon_color=315B7D&text_color=526577&bg_color=00000000" height="165" alt="Statistiques GitHub" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Klemz-696&layout=compact&hide_border=true&title_color=315B7D&text_color=526577&bg_color=00000000" height="165" alt="Langages les plus utilisés" />

<br/>

<img src="https://streak-stats.demolab.com/?user=Klemz-696&hide_border=true&stroke=315B7D&ring=315B7D&fire=2563A3&currStreakLabel=315B7D&background=00000000" alt="Série de contributions" />

<br/><br/>

### 🐍 Contributions

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Klemz-696/Klemz-696/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Klemz-696/Klemz-696/output/github-contribution-grid-snake.svg">
  <img alt="Animation des contributions" src="https://raw.githubusercontent.com/Klemz-696/Klemz-696/output/github-contribution-grid-snake.svg">
</picture>

</div>

---

## 🤝 Contact

<div align="center">

<a href="https://c-sauzede.netlify.app/">
  <img src="https://img.shields.io/badge/Portfolio-0B1628?style=for-the-badge&logo=netlify&logoColor=white" alt="Portfolio" />
</a>
&nbsp;
<a href="https://www.linkedin.com/in/clement-sauzede/">
  <img src="https://img.shields.io/badge/LinkedIn-193B63?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
</a>
&nbsp;
<a href="mailto:sauzede.clement@gmail.com">
  <img src="https://img.shields.io/badge/Email-315B7D?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
</a>

<br/><br/>

```text
"Automatiser ce qui peut l'être, superviser tout le reste."
```

<sub>⚡ Profil maintenu par <b>Clément Sauzède</b> — BTS SIO SISR, Clermont-Ferrand</sub>

</div>
