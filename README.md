# Borealis-Linux-Lab - Administration & Sécurisation Linux

### Alexandre KIEFER

**Administrateur Systèmes, Réseaux & Cybersécurité**  
📍 Savigny-sur-Orge, Île-de-France  
🔗 [LinkedIn](https://www.linkedin.com/in/alexandre-kiefer-847334282/) | 🐙 [GitHub](https://github.com/kieferalexandre1-creator) | ✉️ kiefer.alexandre1@gmail.com

[![Statut](https://img.shields.io/badge/Statut-En%20préparation-orange)](#)
[![Environnement](https://img.shields.io/badge/Environnement-Debian%2012-blue)](#)




> [!NOTE]
> ### 🌌 BOREALIS · LINUX LAB
>
> Projet personnel consacré à l'administration, la sécurisation et
> l'automatisation d'un environnement Linux.
>
> **Administration Linux · Hardening · Bash · Docker · Ansible**

---

## 🧭 Navigation

[🎯 Objectifs](#-objectifs) •
[🏗️ Architecture](#️-architecture) •
[🐧 Administration Linux](#-administration-linux) •
[🛡️ Hardening](#️-hardening) •
[⚙️ Automatisation](#️-automatisation) •
[🐳 Conteneurisation](#-conteneurisation) •
[🧪 Tests](#-tests) •
[📚 Documentation](#-documentation)


## Objectifs

Après Aegis Infra Lab, consacré à la mise en place d'une infrastructure d'entreprise virtualisée, Borealis Linux Lab se concentre sur l'administration et la sécurisation des systèmes Linux.
L'objectif de ce laboratoire est de construire progressivement un environnement Linux permettant de développer et de mettre en pratique mes compétences autour de plusieurs axes :

- 🐧 Administration Linux — gestion des utilisateurs, permissions, services, processus et stockage
- 🌐 Administration réseau — configuration réseau, services et accès distants
- 🛡️ Hardening — sécurisation du système et réduction de la surface d'attaque
- 💻 Bash — scripting et automatisation de tâches d'administration
- ⚙️ Ansible — automatisation et standardisation des configurations
- 🐳 Docker — déploiement et administration de services conteneurisés
- 🧪 Tests & validation — contrôle du fonctionnement et de la sécurité des configurations mises en place
  
Borealis est construit comme un laboratoire d'apprentissage pratique : chaque étape sera documentée avec les configurations réalisées, les commandes utilisées, les problèmes rencontrés et les solutions mises en œuvre.


## 🏗️ 02 — Architecture du laboratoire

Borealis est conçu comme un laboratoire Linux composé de plusieurs machines Debian ayant chacune un rôle précis.

Contrairement à **Aegis Infra Lab**, qui reproduisait l'infrastructure globale d'une petite entreprise, Borealis se concentre sur l'administration Linux. L'environnement est volontairement séparé en plusieurs serveurs afin de travailler les communications entre machines, l'administration distante, la sécurisation et l'automatisation.

### 🖥️ Infrastructure cible

| Machine | Système | Rôle principal | Statut |
|---|---|---|---|
| `SRV-BOREALIS-01` | Debian 12 | Serveur Linux principal | 🔜 Prévu |
| `SRV-BOREALIS-02` | Debian 12 | Services & conteneurs | 🔜 Prévu |
| `SRV-BOREALIS-CTL` | Debian 12 | Administration & automatisation | 🔜 Prévu |

> Les rôles et ressources pourront évoluer au cours du projet en fonction des besoins rencontrés pendant la construction du laboratoire.

---

### 🔹 SRV-BOREALIS-01

**Serveur Linux principal**

Cette machine servira de base pour travailler l'administration quotidienne d'un serveur Debian.

Objectifs prévus :

- gestion des utilisateurs et groupes
- permissions et propriété des fichiers
- administration des services avec `systemd`
- gestion des paquets
- stockage et système de fichiers
- configuration réseau
- administration distante avec SSH
- analyse des journaux système
- sécurisation progressive du serveur

---

### 🔹 SRV-BOREALIS-02

**Serveur de services & conteneurisation**

Cette machine sera utilisée pour déployer et administrer différents services Linux.

Objectifs prévus :

- installation et configuration de services
- déploiement de Docker
- création et gestion de conteneurs
- gestion des volumes
- configuration des réseaux Docker
- exposition et sécurisation des services
- tests de communication entre les différents serveurs

---

### 🔹 SRV-BOREALIS-CTL

**Serveur d'administration & automatisation**

Cette machine aura pour objectif de centraliser l'administration des autres serveurs du laboratoire.

Objectifs prévus :

- administration distante via SSH
- authentification par clés SSH
- scripts Bash d'administration
- installation d'Ansible
- inventaire des machines
- création de playbooks
- automatisation des configurations
- déploiement de configurations reproductibles

---

### 🌐 Réseau

Les différentes machines seront connectées à un réseau virtuel dédié au laboratoire.

```text
                         BOREALIS LINUX LAB

                    ┌───────────────────────┐
                    │   SRV-BOREALIS-CTL    │
                    │                       │
                    │  Admin / Ansible      │
                    │  Bash / SSH           │
                    └───────────┬───────────┘
                                │
                               SSH
                                │
                 ┌──────────────┴──────────────┐
                 │                             │
                 ▼                             ▼
       ┌───────────────────┐         ┌───────────────────┐
       │ SRV-BOREALIS-01   │         │ SRV-BOREALIS-02   │
       │                   │         │                   │
       │ Administration    │◄───────►│ Services          │
       │ Hardening         │ Réseau  │ Docker            │
       │ Debian 12         │         │ Debian 12         │
       └───────────────────┘         └───────────────────┘






