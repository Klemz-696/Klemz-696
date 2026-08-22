<div align="center">

<!-- Bannière animée : nom + spécialités en effet machine à écrire -->
<img src="assets/header.svg" alt="Clément Sauzède — BTS SIO SISR" width="100%"/>

<br/>

<!-- Séparateur animé subtil -->
<img src="https://capsule-render.vercel.app/api?type=rect&color=193B63&height=2&section=header" width="100%" alt=""/>

<br/>

[![Statut](https://img.shields.io/badge/Statut-Recherche_stage_2e_année-193B63?style=for-the-badge&logoColor=white)](mailto:sauzede.clement@gmail.com)
[![Localisation](https://img.shields.io/badge/Localisation-Clermont--Ferrand-315B7D?style=for-the-badge&logoColor=white)](https://www.google.com/maps/search/?api=1&query=Clermont-Ferrand)
[![Formation](https://img.shields.io/badge/BTS_SIO-SISR-0B1628?style=for-the-badge&logoColor=white)](https://c-sauzede.netlify.app/)

</div>

---

## 🎯 À propos

<table>
<tr>
<td width="55%" valign="top">

Étudiant en **2e année de BTS SIO** (option **SISR**) au lycée Sidoine Apollinaire à Clermont-Ferrand.

Je conçois et maintiens une infrastructure virtualisée sur mon homelab : cluster Proxmox à 2 nœuds, conteneurs Docker, VPN WireGuard et supervision.

Je développe aussi des outils web autour de la donnée temps réel et de l'automatisation.

</td>
<td width="45%" valign="top">

```yaml
profil:
  nom: "Clément Sauzède"
  formation: "BTS SIO SISR — 2e année"
  lieu: "Clermont-Ferrand"
  objectif: "Stage 2e année"
  domaines:
    - Support & Helpdesk
    - Systèmes & Réseaux
    - Virtualisation
    - Supervision
    - Automatisation
```

</td>
</tr>
</table>

---

## 🖥️ Mon homelab

<div align="center">

<!-- Animation serveur / réseau : SVG inline léger -->
<img src="https://capsule-render.vercel.app/api?type=venom&color=0:0B1628,100:193B63&height=180&section=header&text=clement@homelab:~$+neofetch&fontSize=24&fontColor=FFFFFF&fontAlignY=35&animation=twinkling&desc=Cluster+Proxmox+VE+%C2%B7+Docker+%C2%B7+WireGuard+%C2%B7+Monitoring&descSize=14&descAlignY=65&descColor=8FA9C2" width="90%" alt="Homelab"/>

</div>

<details open>
<summary><b>Architecture de l'infrastructure</b></summary>

<br/>

```text
                    ┌─────────────────────────────────────────┐
                    │         Cluster Proxmox VE — 2 nœuds    │
                    │                                         │
                    │  ┌─────────┐ ┌─────────┐ ┌──────────┐  │
                    │  │ VM 01   │ │ VM 02   │ │ CT Docker│  │
                    │  │ Debian  │ │ Debian  │ │ Services │  │
                    │  └────┬────┘ └────┬────┘ └────┬─────┘  │
                    │       │           │           │         │
                    │  ┌────┴───────────┴───────────┴─────┐  │
                    │  │         Réseau interne           │  │
                    │  │  Nginx Proxy Manager · AdGuard   │  │
                    │  │  Uptime Kuma · Netdata · WoL     │  │
                    │  └────────────────┬─────────────────┘  │
                    └───────────────────┼─────────────────────┘
                                        │
                    ┌───────────────────┼─────────────────────┐
                    │   VPN WireGuard   │   Accès distant     │
                    │   PC + Mobile     │   chiffré           │
                    └───────────────────┴─────────────────────┘
```

**Stack déployée :** `Heimdall` `Nginx Proxy Manager` `Uptime Kuma` `AdGuard Home` `Netdata` `Wake-on-LAN` `Docker Compose`

**Accès distant :** tunnel WireGuard depuis PC portable et smartphone — supervision et gestion à distance.

**Avant Proxmox :** environnement VMware ESXi + vCenter (machines virtuelles connectées entre elles).

</details>

---

## 🛠️ Compétences

<div align="center">

### Systèmes · Virtualisation · Réseaux
<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=debian,linux,windows,powershell,bash,docker,nginx,git,githubactions&theme=dark" alt="Stack infrastructure" />
</a>

### Supervision · Développement · Données
<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=prometheus,grafana,py,nodejs,js,html,css,sqlite,postman&theme=dark" alt="Stack supervision et développement" />
</a>

</div>

<br/>

| Domaine | Outils & technologies |
|:---|:---|
| **Systèmes** | `Windows` · `Linux (Debian)` · `Windows Server (bases)` · `Bash` · `PowerShell` |
| **Virtualisation** | `Proxmox VE (cluster)` · `VMware ESXi` · `vCenter` · `VMware Workstation` |
| **Réseaux** | `TCP/IP` · `DNS` · `WireGuard` · `Nginx` · `Packet Tracer` |
| **Conteneurs** | `Docker` · `Docker Compose` · `Portainer` |
| **Supervision** | `Netdata` · `Uptime Kuma` · `Prometheus` · `Grafana` |
| **Développement** | `Python` · `JavaScript` · `HTML/CSS` · `SQL` · `Node.js (bases)` |

---

## 🚀 Projets

<div align="center">

| | Projet | Description | Stack |
|:---:|:---|:---|:---|
| 🏎️ | **Télémétrie de course en direct** | Récupération, traitement et affichage temps réel de données de session automobile | `Python` `Node.js` `HTML/CSS/JS` `Temps réel` |
| 🌐 | **[Portfolio personnel](https://c-sauzede.netlify.app/)** | Site vitrine responsive : parcours, compétences et projets | `HTML5` `CSS3` `JavaScript` `Netlify` |
| 🏠 | **Homelab — infra & sécurité** *(doc publique en préparation)* | Cluster Proxmox 2 nœuds, Docker, VPN WireGuard, supervision | `Proxmox` `Docker` `WireGuard` `Monitoring` |
| 🤖 | **OpenJarvis — assistant IA local** *(prototype — privé)* | LLM local, reconnaissance vocale, synthèse vocale, actions système contrôlées | `Python` `LLM local` `Voice AI` `PowerShell` |

</div>

---

## 📊 Activité GitHub

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Klemz-696&show_icons=true&hide_border=true&count_private=true&title_color=4A90D9&icon_color=4A90D9&text_color=A8C5E0&bg_color=0B1628" height="165" alt="Statistiques GitHub" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Klemz-696&layout=compact&hide_border=true&title_color=4A90D9&text_color=A8C5E0&bg_color=0B1628" height="165" alt="Langages les plus utilisés" />

<br/>

<img src="https://streak-stats.demolab.com/?user=Klemz-696&hide_border=true&stroke=4A90D9&ring=4A90D9&fire=2563A3&currStreakLabel=A8C5E0&sideLabels=A8C5E0&currStreakNum=FFFFFF&sideNums=FFFFFF&dates=526577&background=0B1628" alt="Série de contributions" />

</div>

---

## 🐍 Contributions

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Klemz-696/Klemz-696/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Klemz-696/Klemz-696/output/github-contribution-grid-snake.svg">
  <img alt="Animation des contributions" src="https://raw.githubusercontent.com/Klemz-696/Klemz-696/output/github-contribution-grid-snake.svg" width="100%">
</picture>

</div>

---

## 🤝 Contact

<div align="center">

<!-- Séparateur animé -->
<img src="https://capsule-render.vercel.app/api?type=rect&color=193B63&height=2&section=header" width="60%" alt=""/>

<br/><br/>

<a href="https://c-sauzede.netlify.app/">
  <img src="https://img.shields.io/badge/Portfolio-0B1628?style=for-the-badge&logo=netlify&logoColor=4A90D9" alt="Portfolio" />
</a>
&nbsp;&nbsp;
<a href="https://www.linkedin.com/in/clement-sauzede/">
  <img src="https://img.shields.io/badge/LinkedIn-193B63?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
</a>
&nbsp;&nbsp;
<a href="mailto:sauzede.clement@gmail.com">
  <img src="https://img.shields.io/badge/Email-315B7D?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
</a>

<br/><br/>

> *"Automatiser ce qui peut l'être, superviser tout le reste."*

<sub>⚡ Profil maintenu par **Clément Sauzède** — BTS SIO SISR · Clermont-Ferrand</sub>

</div>
